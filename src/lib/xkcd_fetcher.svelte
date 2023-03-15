<script>
    let comicImage;
    let comicTitle;
    let comicAlt;
    let comicDate;
  
    fetch("https://fwd.innopolis.app/api/hw2?email=y.kim@innopolis.university")
      .then(response => response.json())
      .then(data => {
        fetch(`https://getxkcd.vercel.app/api/comic?num=${data}`)
          .then(response => response.json())
          .then(data => {
            comicImage = data.img;
            comicTitle = data.title;
            comicAlt = data.alt;
            comicDate = new Date(data.year, data.month - 1, data.day).toLocaleDateString();
          });
      });
  </script>
  
  <div id="xkcd">
    <h3>{comicTitle}</h3>
    <p>{comicDate}</p>
    <img src={comicImage} alt={comicAlt} />
  </div>