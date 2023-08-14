<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Advanced Movies Website</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>PORN4HUB</h1>
        <input type="text" id="searchInput" placeholder="Search videos...">
    </header>
    <main id="movieList">
        <!-- Movie cards will be dynamically added here -->
    </main>
    <script src="script.js"></script>
</body>
</html>
<style>body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

header {
    background-color: #333;
    color: #fff;
    padding: 20px;
    text-align: center;
}

h1 {
    margin: 0;
}

main {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    padding: 20px;
}

.movie-card {
    width: 300px;
    border: 1px solid #ccc;
    margin: 10px;
    padding: 10px;
}

.movie-card img {
    width: 100%;
}

.movie-card h2 {
    margin: 10px 0;
}

.movie-card p {
    font-size: 14px;
}
.extra-title{display:none}
</style>
<script>// Sample data for movies (you can replace this with actual movie data)
const movies = [
    {       
      title: ' Not Posing As Innocent',       
  extraTitle: '1080p brunette cum shot fetish pov shaved pussy small tits Venice Rose ',       
  image: 'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj4_yaZPC8cxwlU4yzPnFYp2hob1RVSTd7MoE_c5MKfrb2_Hb-N62clkt_jXzat_jgrP9ZgtNAQt8YCzP3QLGcnJ7FlFQU1HKSaQQRa60zOarV8w8KCW_v5rwoMhQoVyQeX9utD310jyREfFNKJaVhF3dM3NzX8v33l5Xd6ZORFXPFuzcJ0AVjFIisV_OI/s16000/f29da7a10dee78f_main.jpg ',      
   description: ' 1h 59m 26s',       
  link: 'https://mydaddy.cc/video/8e7e22dad3557b81ca/'
},

{
        title: 'In Or Around Her Mouth',
        extraTitle: '1080p amateur big dickbig tits blondeblowjob cum shot fetish milf pov redhead threesome Roxy Cox Lenina Crowne',
        image: 'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhnOa71IADK1tLtJ223VHq5-QElY21OyBiMsoXchGhS9tldhlwktigXOgsG6Fg69sZXhe-dL7xtgtqbDgzqGIQaMyHD755BAV-obm0qpfKccJ1roYJaGtzw33ypMy4nhdQrztfuV4xAHXg-yVj4SBptqolGA9GgNIj6S5aUERT0sD37kT2iTQCGsHaHZwA/s16000/3c92a4309b7bd10_main.jpg',
        description: '27m 55s',
        link: 'https://mydaddy.cc/video/13d29e6e8cf1bcf4ca/'
    },
{
title: 'For Another Kind Of Ride, Honey',
extraTitle: '1080p babe big tits brunette out door pickup pov public shaved pussy small tits Vanessa Alessia',
image: 'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgGezx0FhyyvMWQfPnzdUGOe_ylPq2ZzbhdRI9i_m4RAJgnOV80coz6PvAZkURwYbVuzfnWan1xfdx3bkD7nPpZXFP8P_ZUvUY-AYcKOuvUwyih-VZrbQr093mKHXsAhjWVA9v6aY6Ye6syKa8akkD5s_BeDfdoqFM5LsKI3PRakvjejr7IchJ20BKIJqs/s16000/4abfdcae322e1e9_main.jpg',
description: '20m 0s',
link: 'https://mydaddy.cc/video/6a46fc9cf2e83b10ca/'
},


{       title: 'The Easy Access Mood Today',        
extraTitle: ' 1080p blonde cum shot hairy pov teen Khloe Kapri',       
  image: 'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjZH6RgsocS3sW1XU7N0VOEXW-1Q7DONaSwIBx4I4XoMXQsBJVbZV9MBTpx6T2G6mGgP_mRKx_A42E5hkVmujsZAqEC47DYjOSbY47gB3lDW9z8WZTcTpQj7vHQddRjxApyKHPn8Pk64fFqxg3tfg3cagOJivVXH-0V9mbjFe_IOHsnGOo5qOXtr1Tcqf8/s16000/2a37c59d982f37c_main.jpg',      
   description: '23m 47s',       
  link: 'https://mydaddy.cc/video/7acf9a6623c2769fca/'

},

    // Add more movie objects here...
];

const movieListElement = document.getElementById('movieList');

function displayMovies(movies) {
    movieListElement.innerHTML = '';
    movies.forEach(movie => {
        const movieCard = document.createElement('div');
        movieCard.classList.add('movie-card');

        const movieLink = document.createElement('a');
        movieLink.href = movie.link;
        movieLink.target = '_blank';

        const movieImage = document.createElement('img');
        movieImage.src = movie.image;
        movieImage.alt = movie.title;

        const movieTitle = document.createElement('h2');
        movieTitle.textContent = movie.title;

        const movieDescription = document.createElement('p');
        movieDescription.textContent = movie.description;

        // Check if there's an extra title and create a paragraph for it
        if (movie.extraTitle) {
            const extraTitleParagraph = document.createElement('p');
            extraTitleParagraph.textContent = movie.extraTitle;
            extraTitleParagraph.classList.add('extra-title');
            movieCard.appendChild(extraTitleParagraph);
        }

        movieLink.appendChild(movieImage);
        movieCard.appendChild(movieLink);
        movieCard.appendChild(movieTitle);
        movieCard.appendChild(movieDescription);

        movieListElement.appendChild(movieCard);
    });
}

// Call displayMovies with the initial movies data
displayMovies(movies);

// Search movies based on the input
document.getElementById('searchInput').addEventListener('input', (event) => {
    const searchTerm = event.target.value.toLowerCase();
    const filteredMovies = movies.filter(movie => 
        movie.title.toLowerCase().includes(searchTerm) || 
        (movie.extraTitle && movie.extraTitle.toLowerCase().includes(searchTerm))
    );
    displayMovies(filteredMovies);
});
</script>
