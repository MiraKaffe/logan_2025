<script type="module">
    import GameControl from '{{site.baseurl}}/assets/js/rpg/GameControl.js';

    const path = "{{site.baseurl}}";  // Path for game assets

    // Background image and sprite data
    const image_src = "{{site.baseurl}}/images/rpg/water.png";
    const image_data = { pixels: { height: 580, width: 1038 } };
    const image = { src: image_src, data: image_data };

    const sprite_src_turtle = "{{site.baseurl}}/images/rpg/turtle.png";
    const sprite_data_turtle = {
        SCALE_FACTOR: 10,
        STEP_FACTOR: 1000,
        ANIMATION_RATE: 50,
        pixels: { height: 280, width: 256 },
        orientation: { rows: 4, columns: 3 },
        down: { row: 0, start: 0, columns: 3 },
        left: { row: 1, start: 0, columns: 3 },
        right: { row: 2, start: 0, columns: 3 },
        up: { row: 3, start: 0, columns: 3 }
    };
    const turtle = { src: sprite_src_turtle, data: sprite_data_turtle };

    const sprite_src_fish = "{{site.baseurl}}/images/rpg/fishies.png";
    const sprite_data_fish = {
        SCALE_FACTOR: 16,  // Adjust this based on your scaling needs
        STEP_FACTOR: 400,
        ANIMATION_RATE: 50,
        pixels: { height: 256, width: 384 },
        orientation: { rows: 8, columns: 12 },
        down: { row: 0, start: 0, columns: 3 },
        left: { row: 1, start: 0, columns: 3 },
        right: { row: 2, start: 0, columns: 3 },
        up: { row: 3, start: 0, columns: 3 }
    };
    const fish = { src: sprite_src_fish, data: sprite_data_fish };

    const assets = { image: image, turtle: turtle, fish: fish };

    // Resize canvas and adjust game scale
    function resizeCanvas() {
        const canvas = document.getElementById('gameCanvas');
        const width = window.innerWidth;
        const height = window.innerHeight;
        
        // Set the canvas size to match the window size
        canvas.width = width;
        canvas.height = height;

        // Adjust the scaling factor based on the window size
        const scale = Math.min(width / 1920, height / 1080);  // Assuming 1920x1080 as the base resolution

        // Optionally, pass the scale factor to the game control to adjust the game assets
        GameControl.setScale(scale);
    }

    // Listen for window resize events
    window.addEventListener('resize', resizeCanvas);

    // Initial call to set canvas size and scale
    resizeCanvas();

    // Start the game engine
    GameControl.start(assets);
</script>
