<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>A-Frame Example</title>
    <script src="https://aframe.io/releases/1.7.0/aframe.min.js"></script>
    <script>
        function box_enter (event) {
            document.querySelector("a-box").setAttribute("color", "black")
        }
        function box_exit (event) {
            document.querySelector("a-box").setAttribute("color", "#d10808")
        }
        function cylinder_enter (event) {
            document.querySelector("a-cylinder").setAttribute("color", "#d108cf")
        }
        function cylinder_exit (event) {
            document.querySelector("a-cylinder").setAttribute("color", "red")
        }
    </script>
</head>
<body>
    <a-scene>
        <a-sound src="src: url(sad-meow-song.mp3)" autoplay="true" position="-3 3 5"></a-sound>
        <a-torus animation="property: radius; to: 1; dur: 1000; easing: linear; loop: true" color="cyan" arc="270" radius="5" radius-tubular="0.1"></a-torus>
        <a-cone animation="property: position; to: 0 10 10; dur: 1000; easing: linear; loop: true" color="yellow" radius-bottom="2" radius-top="0.5" position="0 3 0"></a-cone>
        <a-box onmouseenter="box_enter()" onmouseleave="box_exit()" animation="property: rotation; to: 360 360 360; dur: 1000; easing: linear; loop: true" position="0 3 -3" rotation="0 45 45" color="#d10808"></a-box>
        <a-cylinder onmouseenter="cylinder_enter()" onmouseleave="cylinder_exit()" animation="property: rotation; to: 360 360 360; dur: 1000; easing: linear; loop: true" position="0 0 3" rotation="0 0 0" color="#d108cf" height="10" radius="1.5"></a-cylinder>
        <a-sphere animation="property: position; to: 1 0 -32; dur: 1000; easing: linear; loop: true" position="0 -3 0" rotation="0 32 0" color="#08d141" radius="5"></a-sphere>
        <a-light animation="property: position; to: 1 0 -32; dur: 1000; easing: linear; loop: true"  color="white" position="-1 2 -2"></a-light>
        <a-text animation="property: rotation; to: 0 120 360; dur: 1000; easing: linear; loop: true" value="OwO" rotation="0 120 0" position="-3 3 0" color="blue" height="50" width="50"></a-text>
    
        <a-camera>
            <a-cursor></a-cursor>
        </a-camera>
    </a-scene>
</body>
</html>
