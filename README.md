<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Less Whiny More Fixy</title>
  <meta name="description" content="Doe gewoon je werk">
  <meta itemprop="name" content="Less Whiny More Fixy">
  <meta itemprop="description" content="Doe gewoon je werk">
  <meta name="twitter:card" content="summary">
  <meta name="twitter:title" content="Less Whiny More Fixy">
  <meta name="twitter:description" content="Doe gewoon je werk">
  <meta name="og:title" content="Less Whiny More Fixy">
  <meta name="og:description" content="Doe gewoon je werk">
  <meta name="og:type" content="website">

  <style>
    * {
      margin: 0;
      padding: 0;
    }

    #ticker {
      text-transform: uppercase;
      font-family: sans-serif;
      font-size: 20vh;
      line-height: 50vh;
      width: 100vw;
      height: 100vh;
      overflow: hidden;
      display: flex;
      flex-direction: column;
      color: white;
      background-image: linear-gradient(to bottom, #FB923C, #FB923C 50%, #BEF264 50%);
    }

    #ticker > * {
      white-space: nowrap;
      overflow: visible;
      animation-duration: 1500ms;
    }

    @keyframes slidefromright {
      from {
        transform: translateX(100vw);
      }

      to {
        transform: translateX(0);
      }
    }
    @keyframes slidefromleft {
      from {
        transform: translateX(-100vw);
      }

      to {
        transform: translateX(0);
      }
    }

    @media (orientation: landscape) {
      #top {
        animation-name: slidefromright;
      }

      #bottom {
        align-self: flex-end;
        animation-name: slidefromleft;
      }
    }
    @media (orientation: portrait) {
      #top {
        animation-name: slidefromleft;
      }

      #bottom {
        align-self: flex-end;
        animation-name: slidefromright;
      }
    }

    #whiny, #fixy {
      font-weight: bold;
    }

    #whiny {
      color: #7C3AED;
    }
    #fixy {
      color: #E879F9;
    }
  </style>
</head>
<body>
  <h1 id="ticker">
    <div id="top">
      <span id="less">Less</span> <span id="whiny">whiny</span>
    </div>
    <div id="bottom">
      <span id="more">more</span> <span id="fixy">fixy</span>
    </div>
  </h1>
</body>
</html>
