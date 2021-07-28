# Welcome to Travelp!

[Travelp](https://travelp-review.herokuapp.com/) is a hotel finder application that displays hotels nearby.

# Overall Structure
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" /> <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" />
<img src="https://img.shields.io/badge/Redux-593D88?style=for-the-badge&logo=redux&logoColor=white%22%3E" /> <img src="https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white%22/%3E" />
<img src="https://img.shields.io/badge/CSS-239120?&style=for-the-badge&logo=css3&logoColor=white%22%3E" />
<img alt="TypeScript" src="https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white"/>
<img alt="Python" src="https://img.shields.io/badge/python-%2314354C.svg?style=for-the-badge&logo=python&logoColor=white"/>
<img alt="Material UI" src="https://img.shields.io/badge/materialui-%230081CB.svg?style=for-the-badge&logo=material-ui&logoColor=white"/>
<img alt="Flask" src="https://img.shields.io/badge/flask-%23000.svg?style=for-the-badge&logo=flask&logoColor=white"/>
<img alt="Heroku" src="https://img.shields.io/badge/heroku-%23430098.svg?style=for-the-badge&logo=heroku&logoColor=white"/>

## Technologies/Languauges

- React/Redux
-  [Google Places API](https://developers.google.com/maps/documentation/places/web-service/overview?hl=en_US)
-  [Geolocation API](https://developers.google.com/maps/documentation/geolocation/overview?hl=en_US)
-  [Geocoding API](https://developers.google.com/maps/documentation/geocoding/overview?hl=en_US)
-  TypeScript
-  Flask

## How to Use Travelp

1.  Go to  [https://travelp-review.herokuapp.com/](https://travelp-review.herokuapp.com/)
2.  Turn your browser location on.

## Main Technical Features

Users can browse hotels nearby if browser location is turn on or type their destination in a search box.

<a href="https://ibb.co/PwhHzKh"><img src="https://i.ibb.co/9sT536T/Screen-Shot-2021-07-28-at-16-19-15.png" alt="Screen-Shot-2021-07-28-at-16-19-15" border="0"></a>
<a href="https://imgbb.com/"><img src="https://i.ibb.co/Jpw0tWR/Screen-Shot-2021-07-28-at-17-50-31.png" alt="Screen-Shot-2021-07-28-at-17-50-31" border="0"></a>
<a href="https://ibb.co/vzkYQy3"><img src="https://i.ibb.co/Lp15Jjx/Screen-Shot-2021-07-28-at-17-51-43.png" alt="Screen-Shot-2021-07-28-at-17-51-43" border="0"></a>
<a href="https://ibb.co/BN87WDH"><img src="https://i.ibb.co/dgn3C9s/Screen-Shot-2021-07-28-at-17-53-13.png" alt="Screen-Shot-2021-07-28-at-17-53-13" border="0"></a>

## Instructions
1. Clone repo `git clone https://github.com/mimike/mapstest.git .`
2. Install dependencies

      ```bash
      pipenv install --dev -r dev-requirements.txt && pipenv install -r requirements.txt
      ```

3. Create a **.env** file based on the example with proper settings for your
   development environment

4. Create a **.env** file based on the example with proper settings for your
   development environment
    - Install packages `npm install`
    - Start dev server `npm start`
    - Note: The [Google API](https://console.cloud.google.com/apis/library?project=genuine-tuner-154003&rif_reserved) was used to collect this data. Create a `.env` file in root dir and add your Google API key as `REACT_APP_API_KEY`

## To Do

- [ ] Implement light mode & dark mode
- [ ] Add aria
- [ ] Add loading spinner to the Enter by Destination option
- [ ] Allow users to press enter to search Enter by Destination


##Deploy to Heroku

To run the React App in development, checkout the [README](./react-app/README.md) inside the `react-app` directory.

***
*IMPORTANT!*
   If you add any python dependencies to your pipfiles, you'll need to regenerate your requirements.txt before deployment.
   You can do this by running:

   ```bash
   pipenv lock -r > requirements.txt
   ```

*ALSO IMPORTANT!*
   psycopg2-binary MUST remain a dev dependency because you can't install it on apline-linux.
   There is a layer in the Dockerfile that will install psycopg2 (not binary) for us.
***


## Deploy to Heroku

1. Create a new project on Heroku

2. Install the [Heroku CLI](https://devcenter.heroku.com/articles/heroku-command-line)
3. Run

   ```bash
   heroku login
   ```

4. Login to the heroku container registry

   ```bash
   heroku container:login
   ```

5. Update the `REACT_APP_BASE_URL` variable in the Dockerfile.
   This should be the full URL of your Heroku app: i.e. "https://flask-react-aa.herokuapp.com"
6. Push your docker container to heroku from the root directory of your project.
   This will build the dockerfile and push the image to your heroku container registry

   ```bash
   heroku container:push web -a {NAME_OF_HEROKU_APP}
   ```

8. Release your docker container to heroku

   ```bash
   heroku container:release web -a {NAME_OF_HEROKU_APP}
   ```

9. Under Settings find "Config Vars" and add any additional/secret .env variables.

