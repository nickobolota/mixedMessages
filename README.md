# MIXED MESSAGES PROJECT
## Generating random fortune cookies 
* using an obect to contain my compoonents.
```javascript
const source = {
    tense: ['You will','be patient soon you will', 'soon you will', 'if you wait long enough you will'],
    what:  ['recieve','come across', 'find', 'discover'],
    gift: ['a brand new', 'an old', 'a devine', 'a sneeky', 'a cheap', 'a dirty'],
    typeGift: ['car', 'set of clothes', 'friend', 'stack of money', 'set of skills you never knew you had']
};
```
* generating a random number set to the length of each array to reference a string within the array
```javascript
const randomNum = (a) => Math.floor(Math.random() * a.length );
```
* then using a arrow function that takes in 4 arguments which iterate through the source object.
```javascript
const randomWord = (arrTense, arrWhat, arrGift, arrType) => {

    const tenseOne = arrTense[randomNum(arrTense)];
    const whatOne = arrWhat[randomNum(arrWhat)];
    const giftOne = arrGift[randomNum(arrGift)];
    const typeOne = arrType[randomNum(arrType)];
```
* then assigning the now random strings to a new const using string interpolation
```javascript
    const sentence = `${tenseOne} ${whatOne} ${giftOne} ${typeOne}`;
    return sentence;
```
* and finally reasiging the value of the randomWord funtion and its arguments and logging the result to the console.
```javascript
const finalSentence = randomWord(source.tense, source.what, source.gift, source.typeGift);

console.log(finalSentence);
```
