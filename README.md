## Parcel Test

Setup directory, cd into it and setup initial web files:

~~~~
mkdir simple-site
cd simple-site
touch index.html && touch style.scss && touch index.js
~~~~

Add boilerplate HTML to index file:

'nano index.html'

~~~~
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <link href="https://fonts.googleapis.com/css?family=Lato&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="style.scss">
  <title>Parcel Tutorial</title>
</head>
<body>
  <div class="container">
    <h1>Today is:</h1>
    <span class="today"></span>
    <h2>and the image of the day:</h2>
    <img src="https://source.unsplash.com/random/600x400" alt="unsplash random image">
</div>
<script src="index.js"></script>
</body>
</html>
~~~~

Install Parcel:

~~~~
npm install -g parcel-bundler
~~~~

Add the package.json file:

~~~~
npm init -y
~~~~

Tell Parcel which file to watch as the entrypoint:

~~~~
parcel index.html
~~~~

Server should start running so you can copy and paste the server address into the browser (should be similar to below):

~~~~
http://localhost:1234
~~~~

Now start adding styles to the scss file:

~~~~
$container-size: 768px;
$bg: #000;
$text: #fff;
$primary-yellow: #f9f929;

*, *::after, *::before {
  box-sizing: border-box;
}

body {
  background: $bg;
  color: $text;
  font-family: 'Lato', sans-serif;
  margin: 0;
  padding: 0;
}

.container {
  margin: 0 auto;
  max-width: $container-size;
  text-align: center;

  h1 {
    display: inline-block;
    font-size: 36px;
  }

  span {
    color: $primary-yellow;
    font-size: 36px;
    margin-left: 10px;
  }
}
~~~~
