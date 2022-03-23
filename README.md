# life-line
<html>
  <head>
     <meta chareset ='utf-8">
     <title>My first three.js app</title>
     <style>
         body { margin: 0; }
         canvas { display: block;}
     </style>
  </head>  
  <body>                    
      <script src= "js/three.js"></script>
      <script>
          const scene = new THREE.Scene();
          const camera = new THREE.PerspectiveCamera( 75, window.innerWidth / window.innerHeight, 0.1, 1000 );         
          const renderer = new THREE.WebGLRenderer();
          renderer.setSize( window.innerWidth, window.innerHeight );
          document.body.appendChild( renderer.domElement );
          const geometry = new THREE.BoxGeometry();
          const material = new THREE.MeshBasicMaterial( {color:  0x00ff00 } );
          const cube = new THREE.Mesh( geometry, material );
          scene.add( cube );
                      
          camera.position.z = 5;
                      
          function animate() {
              requestAnimationFrame( animate );
                      
              cube.rotation.x += 0.01;
              cube.rotation.y += 0.01;
                      
              renderer.render( scene, camera );
          };
                      
          animate();            
      </script>
   </body>
</html>                      
