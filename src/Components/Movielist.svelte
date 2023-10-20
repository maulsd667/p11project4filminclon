<script>
    const url='https://api.themoviedb.org/3/discover/movie?include_adult=false&include_video=false&language=en-US&page=1&sort_by=popularity.desc'
    const options = {
  method: 'GET',
  headers: {
    accept: 'application/json',
    Authorization: 'Bearer eyJhbGciOiJIUzI1NiJ9.eyJhdWQiOiI3NmEyMmNmOWZhMTFiNDM3NzUyNjFmODg5YTY1MDJjMiIsInN1YiI6IjY1MzBkZjI2YzQzOWMwMDEzODM2MTJlOSIsInNjb3BlcyI6WyJhcGlfcmVhZCJdLCJ2ZXJzaW9uIjoxfQ.frw5Fv-T4ehEuNiqzKFJkvFxB0VQgrPiUizW8VlCwdU'
  }
};
   
let movies =[]
 
fetch(url,options )  
  .then((response )=> response.json())
  .then(data => movies = data.results)
  .catch((err) => console.error(err));
</script>

{#each movies as movie}
     <p>{movie.tittle}</p>
{/each}

    
