# Swiper Card

A Lovelace card that uses [swiper](http://idangero.us/swiper/) to create a touch slider that lets you flick through multiple cards.
You can use (almost?) all options of swiper, these can be found [here](http://idangero.us/swiper/api/).


## Configuration:

And add a card with type `custom:swiper-card`:

```yaml
- type: custom:swiper-card
  cards: []
```

## Parameters

| Name              | Type           | Default | Supported options                                                                                                                                                                                                                                                                                                                  | Description                                                                                                         |
|-------------------|----------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| `card_width`      | string         |         | Any css option that fits in the `width` css value                                                                                                                                                                                                                                                                                  | Will force the width of the swiper container                                                                        |
| `start_card`      | number         | 0       | Any number                                                                                                                                                                                                                                                                                                                         | The card being displayed at the beginning - indexing starts at 0, negative values index from the end starting at -1 |
| `reverse`         | boolean        | false   | true/false                                                                                                                                                                                                                                                                                                                         | Will reverse the slider direction rtl <-> ltr                                                                       |
| `background_html` | string         |         | Any HTML in string form, currently no template support                                                                                                                                                                                                                                                                             | Will render the given HTML as the first child of the slider element, for use as a slider background or similar      |
| `style`           | string         |         | Any css - it will be injected in the same node as the swiper DOM elements                                                                                                                                                                                                                                                          |                                                                                                                     |
| `script`          | string         |         | Any JS code to be prepended to the card before the swiper container                                                                                                                                                                                                                                                                |                                                                                                                     |
| `parameters`      | object         |         | Any parameter from [here](https://swiperjs.com/swiper-api#parameters)                                                                                                                                                                                                                                                              | Configuration of the swiper                                                                                         |
| `reset_after`     | number         |         | Any number                                                                                                                                                                                                                                                                                                                         | Will reset the swiper to the `start_card` if defined or the first card after `reset_after` seconds                  |
| `cards`           | Array / string |         | Any Lovelace Card config OR type: 'swiper-image' with 'src' and optional html attribute to simply render an image, or type: swiper-html with html attribute to directly render HTML content<br/>   If given an Array, this will render immediately, if a string it will be rendered as a template and the result rendered as cards |

# Swiper Modules

The following Swiper Modules are currently supported:
 - Scrollbar
 - Navigation
 - Pagination
 - Zoom
 - EffectFade
 - EffectCards
 - EffectCube
 - EffectCoverflow
 - EffectFlip
 - Parallax
