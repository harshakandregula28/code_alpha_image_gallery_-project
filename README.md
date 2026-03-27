<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Image Gallery</title>

    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            background: #111;
            color: white;
            text-align: center;
        }

        h1 {
            margin: 20px 0;
        }

        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            padding: 20px;
        }

        .gallery img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            border-radius: 10px;
            cursor: pointer;
            transition: transform 0.3s;
        }

        .gallery img:hover {
            transform: scale(1.05);
        }

        /* Lightbox */
        .lightbox {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.9);
            display: none;
            justify-content: center;
            align-items: center;
            flex-direction: column;
        }

        .lightbox img {
            max-width: 95%;
            max-height: 90vh;
            width: auto;
            height: auto;
            border-radius: 100px;
        }

        .lightbox button {
            margin-top: 20px;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
        }
    </style>
</head>

<body>

    <h1>Image Gallery</h1>

    <div class="gallery">
        <img src="https://picsum.photos/id/100/400/300" onclick="openLightbox(this.src)">
        <img src="https://picsum.photos/id/101/400/300" onclick="openLightbox(this.src)">
        <img src="https://picsum.photos/id/102/400/300" onclick="openLightbox(this.src)">
        <img src="https://picsum.photos/id/103/400/300" onclick="openLightbox(this.src)">
        <img src="https://picsum.photos/id/104/400/300" onclick="openLightbox(this.src)">

        <img src="https://picsum.photos/id/106/400/300" onclick="openLightbox(this.src)">
        <img src="https://picsum.photos/id/107/400/300" onclick="openLightbox(this.src)">
        <img src="https://picsum.photos/id/108/400/300" onclick="openLightbox(this.src)">
        <img src="https://picsum.photos/id/109/400/300" onclick="openLightbox(this.src)">
        <img src="https://picsum.photos/id/110/400/300" onclick="openLightbox(this.src)">
        <img src="https://picsum.photos/id/111/400/300" onclick="openLightbox(this.src)">
        <img src="https://picsum.photos/id/112/400/300" onclick="openLightbox(this.src)">
        <img src="https://picsum.photos/id/113/400/300" onclick="openLightbox(this.src)">
        <img src="https://picsum.photos/id/114/400/300" onclick="openLightbox(this.src)">
        <img src="https://picsum.photos/id/115/400/300" onclick="openLightbox(this.src)">
        <img src="https://picsum.photos/id/116/400/300" onclick="openLightbox(this.src)">
        <img src="https://picsum.photos/id/117/400/300" onclick="openLightbox(this.src)">
        <img src="https://picsum.photos/id/118/400/300" onclick="openLightbox(this.src)">
        <img src="https://picsum.photos/id/119/400/300" onclick="openLightbox(this.src)">
        <img src="https://picsum.photos/id/120/400/300" onclick="openLightbox(this.src)">
        <img src="https://picsum.photos/id/121/400/300" onclick="openLightbox(this.src)">
        <img src="https://picsum.photos/id/122/400/300" onclick="openLightbox(this.src)">
        <img src="https://picsum.photos/id/123/400/300" onclick="openLightbox(this.src)">
        <img src="https://picsum.photos/id/124/400/300" onclick="openLightbox(this.src)">
        <img src="https://picsum.photos/id/125/400/300" onclick="openLightbox(this.src)">
        <img src="https://picsum.photos/id/126/400/300" onclick="openLightbox(this.src)">
        <img src="https://picsum.photos/id/127/400/300" onclick="openLightbox(this.src)">
        <img src="https://picsum.photos/id/128/400/300" onclick="openLightbox(this.src)">
        <img src="https://picsum.photos/id/129/400/300" onclick="openLightbox(this.src)">
        <img src="https://picsum.photos/id/130/400/300" onclick="openLightbox(this.src)">
        <img src="https://picsum.photos/id/131/400/300" onclick="openLightbox(this.src)">
        <img src="https://picsum.photos/id/132/400/300" onclick="openLightbox(this.src)">
        <img src="https://picsum.photos/id/133/400/300" onclick="openLightbox(this.src)">
        <img src="https://picsum.photos/id/134/400/300" onclick="openLightbox(this.src)">

    </div>

    <div class="lightbox" id="lightbox">
        <img id="lightboxImg">
        <button onclick="closeLightbox()">Close</button>
    </div>

    <script>
        const lightbox = document.getElementById("lightbox");
        const lightboxImg = document.getElementById("lightboxImg");

        function openLightbox(src) {
            lightbox.style.display = "flex";
            lightboxImg.src = src;
        }

        function closeLightbox() {
            lightbox.style.display = "none";
        }

        // Close when clicking outside image
        lightbox.addEventListener("click", (e) => {
            if (e.target === lightbox) {
                closeLightbox();
            }
        });
    </script>

</body>

</html>
