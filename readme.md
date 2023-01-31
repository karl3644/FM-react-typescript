# Typescript and React

- checks data types even down to reactElements, HTMLDivElement etc
- add https://typescript-eslint.io/ for extra layer of checking
- `"plugin:@typescript-eslint/recommended-requiring-type-checking"` added to eslintrc is very strict
- typed API response & context component
- interface like variable of types. can also be written inline
- `npm run lint` or `npx tsc --noEmit` to check for any errors
- in non-react projects typescript will compile and output TS files with which ever target script. for older browser support use es2015/2017 etc, or es22022 and then use babel to recompile

## Checking

- format. prettier formats app
- format:check. checks if all files have had prettier run on them
- lint
- typecheck

## variable declaration

let age = 6; shows as type number. 6 can be reassigned but keeps type. TS infer
const age = 6; type shows as 6. this cannot be reassigned, and because number is immutable then it means 6 will always be 6. literal type

## function arguments and return values

can declare both argument types and the return type.

`function add(a: number, b: number): number {}`

by declaring the return type this is effective way to cover all ground of null/undefined outputs etc.

## objects

`{`
`make: "Toyota",`
`model: "Corolla",`
`year: 2002`
`}`

would be defined as

`{`
` make: string`
` model: string`
` year: number`
`}`

### objects within functions

`function doSomething(car: {`
` make: string`
` model: string`
` year: number`
` chargeVoltage? : number`
`}) {}`

## optional properties

use ? chaining operator. means will either be number or undefined. it can also be left out completely

`{`
`make: "Toyota",`
`model: "Corolla",`
`year: 2002`
`chargeVoltage?: number`
`}`

## excess property checking

if passing in another type when running a function e.g not already defined, TS will throw error
