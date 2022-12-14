# vue3-avataaars

Simple random avatar generation for Vue3.

![Random Example 1](https://vue3-avataaars.com/svg?isCircle=false&skinColor=D08B5B&hairColor=F59797&topColor=5199E4&clothesColor=3C4F5C&facialHairColor=724133&eyes=Dizzy&eyebrows=UpDown&mouth=Eating&top=ShortHairDreads01&clothes=Hoodie&graphicShirt=Skull&facialHair=BeardMedium&accessories=Wayfarers)
![Random Example 2](https://vue3-avataaars.com/svg?isCircle=true&skinColor=F8D25C&hairColor=2C1B18&topColor=B1E2FF&clothesColor=929598&facialHairColor=D6B370&eyes=Squint&eyebrows=RaisedExcited&mouth=Twinkle&top=LongHairStraight&clothes=BlazerShirt&graphicShirt=Resist&facialHair=Blank&accessories=Prescription01)
![Random Example 3](https://vue3-avataaars.com/svg?isCircle=false&skinColor=F8D25C&hairColor=B58143&topColor=FF5C5C&clothesColor=E6E6E6&facialHairColor=D6B370&eyes=Close&eyebrows=Angry&mouth=ScreamOpen&top=Hijab&clothes=GraphicShirt&graphicShirt=Deer&facialHair=Blank&accessories=Prescription02)

Implemented with [avataaars](https://avataaars.com/) designed by [Pablo Stanley](https://twitter.com/pablostanley) and inspired by 
Or Gordin's [vuejs-avataaars](https://github.com/orgordin/vuejs-avataaars).

## Installation

```sh
npm install vue3-avataaars
```

## Usage

While the library enables random avatars, the component itself requires a full set of parameters. The assumption here is that it is useful to know what parameters went into creating an avatar. For example, so that those parameters can be persisted.

```ts
import { Avatar, Factory } from 'vue3-avataaars';
const props = Factory()
```

```vue
<Avatar v-bind="props" />
```

## Parameters

The list of available parameters can be viewed in [Types.ts](https://github.com/n1c/vue3-avataaars/blob/a2736148cfb8fb5701a778ac0941fe8bcefbeced/src/Types.ts#L17).

```ts
{
  isCircle: boolean, // Place avatar in a background-circle

  circleColor?: Hex,
  hairColor: Hex,
  skinColor: Hex,
  clothesColor: Hex,
  topColor: Hex,
  facialHairColor: Hex,

  clothes: keyof typeof Clothes,
  graphicShirt: keyof typeof GraphicShirt,
  top: keyof typeof Tops,
  accessories: keyof typeof Accessories,
  facialHair: keyof typeof FacialHair,
  eyes: keyof typeof Eyes,
  eyebrows: keyof typeof Eyebrows,
  mouth: keyof typeof Mouths,
}
```

A very simple implementation can be seen in action at [vue3-avataaars.com](https://vue3-avataaars.com/)
