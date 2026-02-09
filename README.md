# swishstation-app<!DOCTYPE html>
<html lang="zh">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Swish Station</title>

  <link rel="manifest" href="manifest.json">
  <meta name="theme-color" content="#000000">
</head>

<body style="margin:0">
  <iframe
    src="https://sites.google.com/view/swishstation/home"
    style="border:0;width:100vw;height:100vh"
    allowfullscreen>
  </iframe>

  <script>
    if ('serviceWorker' in navigator) {
      navigator.serviceWorker.register('sw.js');
    }
  </script>
</body>
</html>
{
  "name": "Swish Station",
  "short_name": "Swish",
  "start_url": ".",
  "display": "standalone",
  "background_color": "#ffffff",
  "theme_color": "#000000",
  "icons": [
    {
      "src": "icon-192.png",
      "sizes": "192x192",
      "type": "image/png"
    },
    {
      "src": "icon-512.png",
      "sizes": "512x512",
      "type": "image/png"
    }
  ]
}
self.addEventListener('install', () => {
  self.skipWaiting();
});
