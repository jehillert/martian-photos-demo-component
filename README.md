# martian-photos-coding-exercise-jeh-2021

## About my solution
If I had some time, there is a lot of things I would fix, or do differently. I will briefly point a few of them out so you are aware that I am aware, if that makes any sense.
- tsconfig is in there mostly for the aliases, to get vscode to control-click.
- For simplicity, this only queries Curiosity rover photos
- The calendar component I used seems to work ok, but you will find it is generating a lot of errors in the console.  I decided to try and add tests with the rest of my time rather than troubleshoot.
- There are a lot of unnecessary dependencies because I tried a new webpack project generator I had not seen before.  It would take a while to chop down the webpack configuration and remove dependencies I do not think are necessary, so I am foregoing in favor of other priorities.
- The image shifts whenever a photo fills the entire height of the screen.  Probably one line of CSS would fix that, but I would need to experiment.  I do not work with images with variable dimensions too often.
- The Calendar looks nice, but one flaw is that it does not have an onClick event it seems, only an onChange.  If I had more time, I would either add a button with an indicator that it refreshes the currently selected date.
- It was somewhat silly to add theming capability and aliases, but the former is something that gets harder to add the longer a person waits (in a bigger project), and the latter, well, who doesn't love aliases?
- Folder structure for components is probably not ideal.  In a larger project, there would be one folder called MartianPicPicker or something like that, and the folders would be nested according to a parent child relationship.
- It would be good to have intro text, and to account for when the selected day has no pictures.  Currently it either repeats the last picture or it is blank if no picture has previously been selected.
- There's more to this list, but going to use the rest of my time for testing...


This project was generated using [React Webpack Starter](https://github.com/Create-Node-App/create-react-webpack-app).

## Development

### Running the Project

Start development environment running

```sh
$ yarn start
# or with npm
$ npm run start
```

Start development environment with docker running

```sh
$ yarn docker:dev
# or with npm
$ npm run docker:dev
```

`docker:dev` generate a docker image named martian-photos-coding-exercise-jeh-2021 and run it in a container. Run `docker:dev:start` for only start a container without build a new docker image

While developing, you will probably rely mostly on `yarn start`; however, there are additional scripts at your disposal:

| `yarn <script>`       | Description                                                                                                             |
| --------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| `start`               | Serves your app at `localhost:8091`                                                                                     |
| `build:dev`           | Builds the application to ./build (_the build output dir could be configured in `./config/common-paths.js`_)            |
| `build:dev:watch`     | Builds the application and watch for changes                                                                            |
| `build:dev:analyze`   | Builds the application with Bundle Analyzer and Visualizer Plugins instaled                                             |
| `build:dev:dashboard` | Builds the application with Dashboard                                                                                   |
| `serve:dev:dashboard` | Builds the application with Dashboard                                                                                   |
| `test`                | Runs unit tests with Jest. See [testing](#testing)                                                                      |
| `test:watch`          | Runs `test` in watch mode to re-run tests when changed                                                                  |
| `lint`                | [Lints](http://stackoverflow.com/questions/8503559/what-is-linting) the project for potential errors                    |
| `lint:fix`            | Lints the project and [fixes all correctable errors](http://eslint.org/docs/user-guide/command-line-interface.html#fix) |

### Hot Reloading

Hot reloading is enabled by default when the application is running in development mode (`yarn start`). This feature is implemented with webpack's [Hot Module Replacement](https://webpack.github.io/docs/hot-module-replacement.html) capabilities, where code updates can be injected to the application while it's running, no full reload required. Here's how it works:

For **JavaScript** modules, a code change will trigger the application to re-render from the top of the tree. **Global state is preserved (i.e. redux), but any local component state is reset**. This differs from React Hot Loader, but we've found that performing a full re-render helps avoid subtle bugs caused by RHL patching.

## Production

Generate production files running

```sh
$ yarn build
# or with npm
$ npm run build
```

Generate and serve production files running

```sh
$ yarn serve
# or with npm
$ npm run serve
```

## Testing

To add a unit test, create a `.test.js` file anywhere inside of `./test`. Jest and webpack will automatically find these files.

## More info

You can learn more about the operation of this starter kit in the official [github repository](https://github.com/Create-Node-App/create-react-webpack-app).
