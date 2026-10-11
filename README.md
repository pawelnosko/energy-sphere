<h1>⚡ Interactive Energy Sphere – Three.js, WebGL &amp; GLSL</h1>
<p><strong> A fully interactive 3D energy sphere featuring procedural plasma, branching lightning bolts, glowing particles, and advanced lighting effects — built entirely with JavaScript, Three.js, WebGL, and GLSL shaders. </strong></p>
<p>No 3D models, pre-rendered animations, or external texture files required. Everything is generated procedurally in real time.</p>
<p>The entire project is contained in a single HTML file.</p>
<h2>✨ Features</h2>
<h3>Procedural Plasma Core</h3>
<ul>
<li>
<p>Custom GLSL vertex and fragment shaders.</p>
</li>
<li>
<p>Animated fractal noise using Fractional Brownian Motion (FBM).</p>
</li>
<li>
<p>Dynamic blue, purple, and green plasma patterns.</p>
</li>
<li>
<p>Glowing energy veins and illuminated sphere edges.</p>
</li>
<li>
<p>Continuous color transitions and surface animation.</p>
</li>
</ul>
<h3>Fractal Lightning System</h3>
<ul>
<li>
<p>30 independently generated lightning bolts.</p>
</li>
<li>
<p>Recursive branching algorithm.</p>
</li>
<li>
<p>Randomized directions, lengths, and colors.</p>
</li>
<li>
<p>Animated lightning growth and fading.</p>
</li>
<li>
<p>Additional electrical sparks at branching points.</p>
</li>
</ul>
<h3>Interactive Lightning</h3>
<ul>
<li>
<p>10 additional lightning bolts targeting the mouse cursor.</p>
</li>
<li>
<p>3D cursor position calculated using ray-sphere intersection.</p>
</li>
<li>
<p>Dynamic lightning regeneration.</p>
</li>
<li>
<p>Glowing effects around the target position.</p>
</li>
</ul>
<h3>Particle System</h3>
<ul>
<li>
<p>1,400 animated particles.</p>
</li>
<li>
<p>Randomized velocity, direction, color, and lifetime.</p>
</li>
<li>
<p>Efficient rendering with Three.js BufferGeometry.</p>
</li>
<li>
<p>Continuous emission from the sphere's surface.</p>
</li>
</ul>
<h3>Visual Effects</h3>
<ul>
<li>
<p>Procedural animated nebula background.</p>
</li>
<li>
<p>Soft radial glow textures generated using Canvas.</p>
</li>
<li>
<p>Additive blending.</p>
</li>
<li>
<p>UnrealBloomPass postprocessing.</p>
</li>
<li>
<p>Pulsating halo with dynamic color transitions.</p>
</li>
</ul>
<h3>User Interaction</h3>
<ul>
<li>
<p>Mouse and touch rotation.</p>
</li>
<li>
<p>Automatic sphere rotation.</p>
</li>
<li>
<p>Lightning reactions to cursor movement.</p>
</li>
<li>
<p>Responsive rendering.</p>
</li>
</ul>
<h2>🛠 Technologies</h2>
<ul>
<li>
<p><strong> JavaScript </strong> – animation logic, lightning generation, particles, and interactions.</p>
</li>
<li>
<p><strong> Three.js r128 </strong> – 3D rendering, geometry, camera, and scene management.</p>
</li>
<li>
<p><strong> WebGL </strong> – GPU-accelerated graphics.</p>
</li>
<li>
<p><strong> GLSL </strong> – procedural plasma and background shaders.</p>
</li>
<li>
<p><strong> HTML5 Canvas </strong> – dynamically generated glow textures.</p>
</li>
<li>
<p><strong> EffectComposer / UnrealBloomPass </strong> – postprocessing and lighting effects.</p>
</li>
</ul>
<h2>🚀 Getting Started</h2>
<ol>
<li>
<p>Download or clone this repository.</p>
</li>
<li>
<p>Open <code>
    energy_sphere.html
  </code> in a modern WebGL-compatible browser.</p>
</li>
<li>
<p>Move your mouse to interact with the lightning.</p>
</li>
<li>
<p>Click and drag to rotate the sphere.</p>
</li>
</ol>
<p>No npm, Node.js, build tools, or installation required.</p>
<p><strong> Note: </strong> An internet connection is required because Three.js and its postprocessing scripts are loaded from CDN.</p>
<h2>🎮 Controls</h2>
<table>
<tbody>
<tr>
<th>Action</th>
<th>Result</th>
</tr>
<tr>
<td>Move mouse</td>
<td>Lightning targets the cursor</td>
</tr>
<tr>
<td>Click and drag</td>
<td>Rotate the energy sphere</td>
</tr>
<tr>
<td>Touch and drag</td>
<td>Rotate on touch devices</td>
</tr>
<tr>
<td>No interaction</td>
<td>Automatic rotation and continuous animation</td>
</tr>
</tbody>
</table>
<h2>⚙️ Customization</h2>
<p>You can modify the animation directly in the JavaScript source.</p>
<pre>  <code>
    const R = 2.2;                 // Sphere radius
const CURSOR_ACTION = true;    // Enable cursor interaction
const NC = CURSOR_ACTION ? 10 : 0;

// Lightning settings
const MAXSEG = 1200;
const MAXNODE = 120;
const NB = 30;

// Particle count
const NPART = 1400;
  </code>
</pre>
<p>Additional customization options include:</p>
<ul>
<li>
<p>Plasma colors and shader animation speed.</p>
</li>
<li>
<p>Lightning length, branching depth, and lifetime.</p>
</li>
<li>
<p>Particle velocity and emission behavior.</p>
</li>
<li>
<p>Bloom intensity and radius.</p>
</li>
<li>
<p>Sphere rotation speed.</p>
</li>
<li>
<p>Background nebula colors.</p>
</li>
</ul>
<p>For better performance on lower-powered devices, consider reducing the particle count, lightning count, or renderer pixel ratio.</p>
<h2>🧠 How It Works</h2>
<p>The effect combines GPU-based procedural rendering with dynamically generated geometry.</p>
<p><strong> Plasma generation: </strong> Custom GLSL shaders use layered fractal noise to create animated energy patterns directly on the sphere.</p>
<p><strong> Lightning generation: </strong> A recursive JavaScript algorithm creates irregular electrical paths with randomized branches. Geometry buffers are updated dynamically without recreating every visual object.</p>
<p><strong> Particle simulation: </strong> Thousands of small particles move outward from the sphere, gradually fade, and respawn.</p>
<p><strong> Cursor interaction: </strong> Mouse coordinates are converted into 3D positions, allowing lightning bolts to target points in the scene.</p>
<p><strong> Rendering: </strong> Three.js combines these systems into a single animation loop, while Bloom and additive blending produce the final glowing appearance.</p>
<h2>💡 Possible Applications</h2>
<p>This project can serve as a foundation for:</p>
<ul>
<li>
<p>Futuristic website hero sections.</p>
</li>
<li>
<p>AI and technology landing pages.</p>
</li>
<li>
<p>Interactive developer portfolios.</p>
</li>
<li>
<p>Science-fiction interfaces and game effects.</p>
</li>
<li>
<p>Energy reactors and magical artifacts.</p>
</li>
<li>
<p>Interactive audio visualizers with additional Web Audio API integration.</p>
</li>
<li>
<p>Creative WebGL experiments.</p>
</li>
</ul>
<h2>👨‍💻 Author</h2>
<p><strong> Paweł Nosko – Design Cart </strong></p>
<p>Web developer specializing in e-commerce solutions, JavaScript, PHP, custom extensions, and interactive web experiences.</p>
<ul>
<li>
<p><a href="https://pawelnosko.com/"> Author – Paweł Nosko </a></p>
</li>
<li>
<p><a href="https://pawelnosko.com/js-frontend-tools/sandslider-building-a-webgl-image-slider-with-sand-blow-transitions-in-three-js"> Design Cart – Official Website </a></p>
</li>
</ul>
<h2>⭐ Support the Project</h2>
<p>If you find this project useful, consider giving the repository a star.</p>
<p>Feel free to explore the code, experiment with the shaders, and build your own variations of the energy sphere.</p>
<p><strong> Built with JavaScript, mathematics, and a little electricity. ⚡ </strong></p>
