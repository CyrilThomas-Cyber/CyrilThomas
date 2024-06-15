<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Typewriter Effect</title>
  <style>
    
    @keyframes typing {
      0%, 10% { width: 0 }
      90% { width: 21em }
    }

    @keyframes blink-caret {
      0% { border-color: transparent }
      50% { border-color: orange }
    }

    @keyframes gradient {
      0% { background-position: 0 50% }
      50% { background-position: 100% 50% }
    }

    @keyframes hi {
      0%, 60% { transform: rotate(0deg) }
      10%, 30% { transform: rotate(14deg) }
      20% { transform: rotate(-8deg) }
      40% { transform: rotate(-4deg) }
      50% { transform: rotate(10deg) }
    }

    .typewriter {
      width: 100%;
      height: 150px;
      display: flex;
      justify-content: center;
      align-items: center;
      font-family: Inter, Roboto, Helvetica, 'Segoe UI', Montserrat, Arial, sans-serif;
      font-size: 13px;
      line-height: 1.5;
      color: white;
      background: linear-gradient(135deg, #FF6B6B, #FFD166, #06D6A0, #118AB2);
      background-size: 400% 400%;
      animation: gradient 16s ease infinite;
    }

    @media (prefers-color-scheme: light) {
      .typewriter {
        color: white;
      }
    }

    .typewriter h1 {
      margin: 0 auto;
      white-space: nowrap;
      overflow: hidden;
      border-right: .15em solid orange;
      letter-spacing: .15em;
      animation: typing 4s steps(40, end) infinite alternate forwards, blink-caret .75s infinite step-end forwards;
    }

    .hi {
      display: inline-block;
      transform-origin: 70% 70%;
      animation: hi 1.5s linear -.5s infinite;
    }

    @media (prefers-reduced-motion) {
      .hi, h1 {
        animation: none;
      }
    }
  </style>
</head>
<body>
  <div class="typewriter">
    <h1>Hi There<div class="hi">!</div>, My Name is Cyril Thomas</h1>
  </div>
</body>
</html>
