## How to download a file with fetch and send it with fetch (without fs) ? 🤔

Hello 👋,

I wrote this article because I struggle a lot to do a simple thing in Node.JS and I want to share it with you 🙂.

On a personal scrapping projects, I'm caching images to render it on a PDF. To do this, I save scrapped images on a dedicated server 📁. 

But my problem is on my Electron App, If I'm on macOS, I can't save my temp image on App Installation folder. Fs access is forbidden ❌.

So with node-fetch, I try to simulate File API with some libraries, send Stream, Buffer, etc. None of these solutions have been working. 

Except this one ✅ :


```js
import FormData from 'form-data';
import fetch from 'node-fetch';

// Download original Image
const res = await fetch(imageUrl);

// Convert response to buffer
const arrayBuffer = await res.arrayBuffer();
const buffer = Buffer.from(
  arrayBuffer,
  undefined,
  arrayBuffer.byteLength,
);

const formData = new FormData();

formData.append('file', buffer, {
  contentType: 'text/plain',
  name: 'file',
  filename: 'test.png',
});

try {
  //Send it to new server
  await fetch(
    `https://my-server.com/image`,
    {
      method: 'POST',
      body: formData,
      headers: formData.getHeaders(),
    },
  );
} catch (error) {
  console.log(error);
}


``` 

I hope this solution will help you too. Because I have lost nearly 4 hours with this problem 😅