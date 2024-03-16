# Document Object Model (DOM)
[DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model)  is the data representation of the objects that comprise the structure and content of a document on the web. This guide will introduce the DOM, look at how the DOM represents an HTML document in memory and how to use APIs to create web content and applications.

### 1. currentTarget
penggunaan   ```currentTarget``` haruslah menggunakan argument ```event``` pada function, contohnya : 
```js
belajar(event) {
    console.log(event.currentTarget.getAttribute('data-nama'))
}
```