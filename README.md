this NODE JS Script will run multiple rearches on various APIS, you can run the following commands to run LIRI: 
- concert-this
- spotify-this-song
- movie-this
- do-what-it-says

  EXAMPLES:
  "liri.js concert-this daddy yankee"
  "liri.js spotify-this-song thotiana"
  "liri.js movie-this the avengers"
  "liri.js do-what-it-says"
  
# EXAMPLE VIDEO -> link to the video here <https://drive.google.com/file/d/1okAk9QhAaTF9zHUp3BR7UrsdrzABdk3r/view>

# I created a shell script to store all my env vars and ran:
# I posted a copy of the script LIRI_Script_Example.sh just put your own keys and run it by :

`$ chmod u+x LIRI_Script_Example.sh`
then
`./LIRI_Script_Example.sh`

# Breakdown of what each Script executes : 

1. `node liri.js concert-this <artist/band name here>`

   - This will search the Bands in Town Artist Events API (`"https://rest.bandsintown.com/artists/" + artist + "/events?app_id=codingbootcamp"`) for an artist and render the following information about each event to the terminal:

     - Name of the venue

     - Venue location

     - Date of the Event (use moment to format this as "MM/DD/YYYY")

2. `node liri.js spotify-this-song '<song name here>'`

   - This will show the following information about the song in your terminal/bash window

     - Artist(s)

     - The song's name

     - A preview link of the song from Spotify

     - The album that the song is from -->

- If no song is provided then your program will default to "The Sign" by Ace of Base.

   <!-- - You will utilize the [node-spotify-api](https://www.npmjs.com/package/node-spotify-api) package in order to retrieve song information from the Spotify API.
   - The Spotify API requires you sign up as a developer to generate the necessary credentials. You can follow these steps in order to generate a **client id** and **client secret**:
  
   - Step One: Visit <https://developer.spotify.com/my-applications/#!/>
  
   - Step Two: Either login to your existing Spotify account or create a new one (a free account is fine) and log in.
  
   - Step Three: Once logged in, navigate to <https://developer.spotify.com/my-applications/#!/applications/create> to register a new application to be used with the Spotify API. You can fill in whatever you'd like for these fields. When finished, click the "complete" button.
  
   - Step Four: On the next screen, scroll down to where you see your client id and client secret. Copy these values down somewhere, you'll need them to use the Spotify API and the [node-spotify-api package](https://www.npmjs.com/package/node-spotify-api).-->

3. `node liri.js movie-this '<movie name here>'`

   - This will output the following information to your terminal/bash window:

     ```
       * Title of the movie.
       * Year the movie came out.
       * IMDB Rating of the movie.
       * Rotten Tomatoes Rating of the movie.
       * Country where the movie was produced.
       * Language of the movie.
       * Plot of the movie.
       * Actors in the movie.
     ```

   - If the user doesn't type a movie in, the program will output data for the movie 'Mr. Nobody.'

     - If you haven't watched "Mr. Nobody," then you should: <http://www.imdb.com/title/tt0485947/>

     - It's on Netflix!

   - You'll use the `axios` package to retrieve data from the OMDB API. Like all of the in-class activities, the OMDB API requires an API key. You may use `trilogy`.

4. `node liri.js do-what-it-says`

   - Using the `fs` Node package, LIRI will take the text inside of random.txt and then use it to call one of LIRI's commands.

     - It should run `spotify-this-song` for "I Want it That Way," as follows the text in `random.txt`.

     - Edit the text in random.txt to test out the feature for movie-this and concert-this.
