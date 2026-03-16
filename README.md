<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>React Three Fiber Camera Switcher</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      line-height: 1.6;
      margin: 0;
      padding: 0;
      background: #f9f9f9;
      color: #333;
    }
    header {
      background: #24292e;
      color: #fff;
      padding: 20px;
      text-align: center;
    }
    header h1 {
      margin: 0;
      font-size: 2em;
    }
    main {
      max-width: 900px;
      margin: 20px auto;
      padding: 20px;
      background: #fff;
      border-radius: 8px;
      box-shadow: 0 2px 6px rgba(0,0,0,0.1);
    }
    h2 {
      border-bottom: 2px solid #eee;
      padding-bottom: 5px;
      margin-top: 30px;
    }
    pre {
      background: #f4f4f4;
      padding: 10px;
      border-radius: 5px;
      overflow-x: auto;
    }
    code {
      font-family: Consolas, monospace;
      color: #c7254e;
    }
    ul {
      margin: 10px 0;
      padding-left: 20px;
    }
    .license {
      margin-top: 40px;
      font-size: 0.9em;
      color: #666;
    }
  </style>
</head>
<body>
  <header>
    <h1>React Three Fiber Camera Switcher 🎥</h1>
    <p>Toggle between Perspective and Orthographic cameras with interactive controls</p>
  </header>
  <main>
    <h2>🚀 Features</h2>
    <ul>
      <li>Switch between Perspective and Orthographic cameras</li>
      <li>Adjust FOV (field of view) for perspective camera</li>
      <li>Adjust Zoom for orthographic camera</li>
      <li>OrbitControls for smooth navigation</li>
      <li>Colorful 3D scene with sphere and cubes</li>
    </ul>

    <h2>📦 Installation</h2>
    <pre><code>git clone https://github.com/your-username/react-three-camera-switcher.git
cd react-three-camera-switcher
npm install</code></pre>

    <h2>▶️ Usage</h2>
    <pre><code>npm run dev</code></pre>
    <p>Open <a href="http://localhost:5173">http://localhost:5173</a> in your browser.</p>

    <h2>🛠 Dependencies</h2>
    <ul>
      <li>React</li>
      <li>@react-three/fiber</li>
      <li>@react-three/drei</li>
      <li>three</li>
    </ul>

    <h2>📂 Code Example</h2>
    <pre><code>import { useState } from 'react'
import { Canvas } from '@react-three/fiber'
import { PerspectiveCamera, OrthographicCamera, OrbitControls } from '@react-three/drei'

function App() {
  const [cameraType, setCameraType] = useState("perspective")
  const [zoom, setZoom] = useState(50)
  const [fov, setFov] = useState(50)

  return (
    &lt;div style={{ height: "100vh", width:"100vw"}}&gt;
      &lt;Canvas&gt;
        {cameraType === "orthographic" &amp;&amp; (
          &lt;OrthographicCamera makeDefault zoom={zoom} /&gt;
        )}
        {cameraType === "perspective" &amp;&amp; (
          &lt;PerspectiveCamera makeDefault fov={fov} /&gt;
        )}
        &lt;OrbitControls /&gt;
        {/* Meshes here */}
      &lt;/Canvas&gt;
    &lt;/div&gt;
  )
}

export default App</code></pre>

    <div class="license">
      <h2>📖 License</h2>
      <p>MIT License – feel free to use and modify.</p>
    </div>
  </main>
</body>
</html>
