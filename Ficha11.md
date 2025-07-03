<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>StackEdit Styled Page</title>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.css">
  <script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.js"></script>
  <script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/contrib/auto-render.min.js"></script>
  <script>
    document.addEventListener("DOMContentLoaded", function() {
      renderMathInElement(document.body, {
        delimiters: [
          {left: "$$", right: "$$", display: true},
          {left: "$", right: "$", display: false}
        ]
      });
    });
  </script>
  <style>
    body {
      font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
      line-height: 1.6;
      max-width: 800px;
      margin: 40px auto;
      padding: 0 20px;
      color: #333;
      background-color: #f8f8f8;
    }

    h1, h2, h3, h4, h5, h6 {
      font-weight: bold;
      margin-top: 1.2em;
      margin-bottom: 0.5em;
    }

    p {
      margin-bottom: 1em;
    }

    code {
      background: #eee;
      padding: 2px 4px;
      font-size: 90%;
      border-radius: 4px;
    }

    pre {
      background: #eee;
      padding: 1em;
      overflow-x: auto;
      border-radius: 6px;
    }

    blockquote {
      border-left: 4px solid #ccc;
      padding-left: 1em;
      color: #555;
      margin: 1em 0;
    }

    ul, ol {
      padding-left: 2em;
      margin-bottom: 1em;
    }

    a {
      color: #0366d6;
      text-decoration: none;
    }

    a:hover {
      text-decoration: underline;
    }
  </style>
</head>
<body>

  <h1>Example StackEdit Styled Template</h1>
  <p>This is a sample paragraph styled like StackEdit. It's clean, legible, and comfortable to read.</p>

  <blockquote>This is a blockquote—used to highlight key ideas or quotes.</blockquote>

  <pre><code>// Sample code block
function greet(name) {
  return 'Hello ' + name;
}
</code></pre>

  <ul>
    <li>Styled list item one</li>
    <li>Styled list item two</li>
  </ul>

  <p>Visit <a href="https://stackedit.io">StackEdit</a> for the real deal!</p>

</body>
</html>
