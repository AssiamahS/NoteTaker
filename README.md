# Note Taker Application
## Author: Sylvester Assiamah - Module 11

## Description

This Note Taker application allows users to write, save, and delete notes. The application uses an Express.js back end to handle API requests and store note data in a JSON file. The front end was provided, and the focus was on creating and connecting the back end to ensure efficient note management. The code has been meticulously developed and optimized to meet user requirements, with clear and consistent elements and tags. Comments have been added strategically to elucidate key sections of the code, enhancing understanding and maintainability. The overall functionality and appearance of the application have been thoughtfully preserved, facilitating seamless note-taking.

## Visuals

![Landing Page](public/assets/images/LandingPage.png)

![Notes Page](public/assets/images/NotesPage.png)

## Deployment

Access the deployed application via this link: [Note Taker Application](https://your-deployment-url-on-render.com)

## Usage

1. Start the server:
    ```bash
    npm start
    ```

2. Open your browser and navigate to:
    ```
    http://localhost:3000
    ```

3. You will be presented with a landing page with a link to a notes page. On the notes page, you can view existing notes, create new notes, and delete notes.

## API Endpoints

### HTML Routes

- `GET /notes`
  - Returns the `notes.html` file.

- `GET *`
  - Returns the `index.html` file for all other routes.

### API Routes

- `GET /api/notes`
  - Reads the `db.json` file and returns all saved notes as JSON.

- `POST /api/notes`
  - Receives a new note to save on the request body, adds it to the `db.json` file, and returns the new note to the client. Each note is given a unique ID using the `uuid` package.

- `DELETE /api/notes/:id`
  - Receives a query parameter containing the ID of a note to delete, removes the note with the given ID property, and rewrites the notes to the `db.json` file.

## Deployment

This application can be easily deployed using Render.

1. Create a `render.yaml` file in the root directory with the following content:

    ```yaml
    services:
      - type: web
        name: note-taker
        env: node
        region: oregon
        buildCommand: npm install
        startCommand: node server.js
    ```

2. Push all changes to your GitHub repository.

3. Go to [Render](https://render.com/) and create a new account if you don't have one.

4. Click on "New +" and choose "Web Service".

5. Connect your GitHub account and select the repository you created.

6. Render will automatically detect the `render.yaml` file and configure the deployment settings.

7. Click "Create Web Service" to deploy your application.

## Credits

- ASKBCS - Assisted in setting up the API routes and deployment configurations.

## License

Please refer to the LICENSE file in the repository.
