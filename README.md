# Make Hello World Starter Template (Vue)

This project was bootstrapped with [Vue CLI](https://cli.vuejs.org/guide/installation.html).

## Looking for a different language?
- [React](https://github.com/Outfitio/make-hello-world-react-template)
- Vue
- [Angular](https://github.com/Outfitio/make-hello-world-angular-template)

<img src="https://files.outfit.io/media_library_items/236742/Screen%2520Shot%25202020-11-03%2520at%252010.35.52%2520am.png" style="width: 60%; margin: 0 auto; display: block;" alt="make starter template" />

## Development server

Install all necessary dependencies `yarn install`

Run `yarn serve` for a dev server. Navigate to `http://localhost:8080/`.

## Building for Make

Run `yarn build` to build the project with correct resource pathing for the sake of deploying to make.

The build artifacts will be stored in the `/dist` directory.

## Importing into Make

When importing into Make be sure to import from the `/dist` folder.

The following `data` inputs are available as well.

- `headline`: string
- `backgroundImage`: string (public URL)
- `showLogos`: boolean

## Support

Here are some helpful links to get you started
- [Docs](https://docs.make.cm): First point of call
- [Twitter](https://twitter.com/home): Drop us a message on twitter if you find a bug or have any feedback
- [Vue CLI documentation](https://cli.vuejs.org/guide/)
