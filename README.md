<!DOCTYPE html>
<html>
<head>
<title>Cat API Example</title>
</head>
<body>
<img id="cat-image" src="" alt="Random cat image">
<script>
const request = new XMLHttpRequest();
request.open('GET', 'https://api.thecatapi.com/v1/images/search');
request.onload = function () {
const data = JSON.parse(request.responseText);
const catImage = document.getElementById('cat-image');
catImage.src = data[0].url;
};
request.send();
</script>
</body>
</html>
