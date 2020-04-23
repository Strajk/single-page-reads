Generated from https://github.com/wallabyjs/interactive-examples for easier reading.

## array/array-concat

```js
const array1 = ['a', 'b', 'c'];
const array2 = ['d', 'e', 'f'];

console.log(array1.concat(array2));
// expected output: Array ["a", "b", "c", "d", "e", "f"]
```

## array/array-copywithin

```js
const array1 = ['a', 'b', 'c', 'd', 'e'];

// copy to index 0 the element at index 3
console.log(array1.copyWithin(0, 3, 4));
// expected output: Array ["d", "b", "c", "d", "e"]

// copy to index 1 all elements from index 3 to the end
console.log(array1.copyWithin(1, 3));
// expected output: Array ["d", "d", "e", "d", "e"]
```

## array/array-entries

```js
const array1 = ['a', 'b', 'c'];

const iterator1 = array1.entries();

console.log(iterator1.next().value);
// expected output: Array [0, "a"]

console.log(iterator1.next().value);
// expected output: Array [1, "b"]
```

## array/array-every

```js
const isBelowThreshold = (currentValue) => currentValue < 40;

const array1 = [1, 30, 39, 29, 10, 13];

console.log(array1.every(isBelowThreshold));
// expected output: true
```

## array/array-fill

```js
const array1 = [1, 2, 3, 4];

// fill with 0 from position 2 until position 4
console.log(array1.fill(0, 2, 4));
// expected output: [1, 2, 0, 0]

// fill with 5 from position 1
console.log(array1.fill(5, 1));
// expected output: [1, 5, 5, 5]

console.log(array1.fill(6));
// expected output: [6, 6, 6, 6]
```

## array/array-filter

```js
const words = ['spray', 'limit', 'elite', 'exuberant', 'destruction', 'present'];

const result = words.filter(word => word.length > 6);

console.log(result);
// expected output: Array ["exuberant", "destruction", "present"]
```

## array/array-find

```js
const array1 = [5, 12, 8, 130, 44];

const found = array1.find(element => element > 10);

console.log(found);
// expected output: 12
```

## array/array-findindex

```js
const array1 = [5, 12, 8, 130, 44];

const isLargeNumber = (element) => element > 13;

console.log(array1.findIndex(isLargeNumber));
// expected output: 3
```

## array/array-foreach

```js
const array1 = ['a', 'b', 'c'];

array1.forEach(element => console.log(element));

// expected output: "a"
// expected output: "b"
// expected output: "c"
```

## array/array-from

```js
console.log(Array.from('foo'));
// expected output: Array ["f", "o", "o"]

console.log(Array.from([1, 2, 3], x => x + x));
// expected output: Array [2, 4, 6]
```

## array/array-includes

```js
const array1 = [1, 2, 3];

console.log(array1.includes(2));
// expected output: true

const pets = ['cat', 'dog', 'bat'];

console.log(pets.includes('cat'));
// expected output: true

console.log(pets.includes('at'));
// expected output: false
```

## array/array-indexof

```js
const beasts = ['ant', 'bison', 'camel', 'duck', 'bison'];

console.log(beasts.indexOf('bison'));
// expected output: 1

// start from index 2
console.log(beasts.indexOf('bison', 2));
// expected output: 4

console.log(beasts.indexOf('giraffe'));
// expected output: -1
```

## array/array-join

```js
const elements = ['Fire', 'Air', 'Water'];

console.log(elements.join());
// expected output: "Fire,Air,Water"

console.log(elements.join(''));
// expected output: "FireAirWater"

console.log(elements.join('-'));
// expected output: "Fire-Air-Water"
```

## array/array-keys

```js
const array1 = ['a', 'b', 'c'];
const iterator = array1.keys();

for (const key of iterator) {
  console.log(key);
}

// expected output: 0
// expected output: 1
// expected output: 2
```

## array/array-lastindexof

```js
const animals = ['Dodo', 'Tiger', 'Penguin', 'Dodo'];

console.log(animals.lastIndexOf('Dodo'));
// expected output: 3

console.log(animals.lastIndexOf('Tiger'));
// expected output: 1
```

## array/array-length

```js
const clothing = ['shoes', 'shirts', 'socks', 'sweaters'];

console.log(clothing.length);
// expected output: 4
```

## array/array-map

```js
const array1 = [1, 4, 9, 16];

// pass a function to map
const map1 = array1.map(x => x * 2);

console.log(map1);
// expected output: Array [2, 8, 18, 32]
```

## array/array-pop

```js
const plants = ['broccoli', 'cauliflower', 'cabbage', 'kale', 'tomato'];

console.log(plants.pop());
// expected output: "tomato"

console.log(plants);
// expected output: Array ["broccoli", "cauliflower", "cabbage", "kale"]

plants.pop();

console.log(plants);
// expected output: Array ["broccoli", "cauliflower", "cabbage"]
```

## array/array-push

```js
const animals = ['pigs', 'goats', 'sheep'];

const count = animals.push('cows');
console.log(count);
// expected output: 4
console.log(animals);
// expected output: Array ["pigs", "goats", "sheep", "cows"]

animals.push('chickens', 'cats', 'dogs');
console.log(animals);
// expected output: Array ["pigs", "goats", "sheep", "cows", "chickens", "cats", "dogs"]
```

## array/array-reduce-right

```js
const array1 = [[0, 1], [2, 3], [4, 5]].reduceRight(
  (accumulator, currentValue) => accumulator.concat(currentValue)
);

console.log(array1);
// expected output: Array [4, 5, 2, 3, 0, 1]
```

## array/array-reduce

```js
const array1 = [1, 2, 3, 4];
const reducer = (accumulator, currentValue) => accumulator + currentValue;

// 1 + 2 + 3 + 4
console.log(array1.reduce(reducer));
// expected output: 10

// 5 + 1 + 2 + 3 + 4
console.log(array1.reduce(reducer, 5));
// expected output: 15
```

## array/array-reverse

```js
const array1 = ['one', 'two', 'three'];
console.log('array1:', array1);
// expected output: "array1:" Array ["one", "two", "three"]

const reversed = array1.reverse();
console.log('reversed:', reversed);
// expected output: "reversed:" Array ["three", "two", "one"]

/* Careful: reverse is destructive. It also changes
the original array */
console.log('array1:', array1);
// expected output: "array1:" Array ["three", "two", "one"]
```

## array/array-shift

```js
const array1 = [1, 2, 3];

const firstElement = array1.shift();

console.log(array1);
// expected output: Array [2, 3]

console.log(firstElement);
// expected output: 1
```

## array/array-slice

```js
const animals = ['ant', 'bison', 'camel', 'duck', 'elephant'];

console.log(animals.slice(2));
// expected output: Array ["camel", "duck", "elephant"]

console.log(animals.slice(2, 4));
// expected output: Array ["camel", "duck"]

console.log(animals.slice(1, 5));
// expected output: Array ["bison", "camel", "duck", "elephant"]
```

## array/array-some

```js
const array = [1, 2, 3, 4, 5];

// checks whether an element is even
const even = (element) => element % 2 === 0;

console.log(array.some(even));
// expected output: true
```

## array/array-sort

```js
const months = ['March', 'Jan', 'Feb', 'Dec']; 
months.sort();
console.log(months);
// expected output: Array ["Dec", "Feb", "Jan", "March"]

const array1 = [1, 30, 4, 21, 100000];
array1.sort();
console.log(array1);
// expected output: Array [1, 100000, 21, 30, 4]
```

## array/array-splice

```js
const months = ['Jan', 'March', 'April', 'June'];
months.splice(1, 0, 'Feb');
// inserts at index 1
console.log(months);
// expected output: Array ["Jan", "Feb", "March", "April", "June"]

months.splice(4, 1, 'May');
// replaces 1 element at index 4
console.log(months);
// expected output: Array ["Jan", "Feb", "March", "April", "May"]
```

## array/array-tolocalestring

```js
const array1 = [1, 'a', new Date('21 Dec 1997 14:12:00 UTC')];
const localeString = array1.toLocaleString('en', {timeZone: "UTC"});

console.log(localeString);
// expected output: "1,a,12/21/1997, 2:12:00 PM",
// This assumes "en" locale and UTC timezone - your results may vary
```

## array/array-tostring

```js
const array1 = [1, 2, 'a', '1a'];

console.log(array1.toString());
// expected output: "1,2,a,1a"
```

## array/array-unshift

```js
    const array1 = [1, 2, 3];

console.log(array1.unshift(4, 5));
// expected output: 5

console.log(array1);
// expected output: Array [4, 5, 1, 2, 3]
```

## array/array-values

```js
const array1 = ['a', 'b', 'c'];
const iterator = array1.values();

for (const value of iterator) {
  console.log(value);
}

// expected output: "a"
// expected output: "b"
// expected output: "c"
```

## arraybuffer/arraybuffer-bytelength

```js
// create an ArrayBuffer with a size in bytes
const buffer = new ArrayBuffer(8);

// use byteLength to check the size
const bytes = buffer.byteLength;

console.log(bytes);
// expected output: 8
```

## arraybuffer/arraybuffer-constructor

```js
// create an ArrayBuffer with a size in bytes
const buffer = new ArrayBuffer(8);

console.log(buffer.byteLength);
// expected output: 8
```

## arraybuffer/arraybuffer-isview

```js
// create an ArrayBuffer with a size in bytes
const buffer = new ArrayBuffer(16);

console.log(ArrayBuffer.isView(new Int32Array()));
// expected output: true
```

## arraybuffer/arraybuffer-slice

```js
// create an ArrayBuffer with a size in bytes
const buffer = new ArrayBuffer(16);
const int32View = new Int32Array(buffer);
// produces Int32Array [0, 0, 0, 0]

int32View[1] = 42;
const sliced = new Int32Array(buffer.slice(4,12));
// produces Int32Array [42, 0]

console.log(sliced[0]);
// expected output: 42
```

## atomics/atomics-add

```js
// create a SharedArrayBuffer with a size in bytes
const buffer = new SharedArrayBuffer(16);
const uint8 = new Uint8Array(buffer);
uint8[0] = 7;

// 7 + 2 = 9
console.log(Atomics.add(uint8, 0, 2));
// expected output: 7

console.log(Atomics.load(uint8, 0));
// expected output: 9
```

## atomics/atomics-and

```js
// create a SharedArrayBuffer with a size in bytes
const buffer = new SharedArrayBuffer(16);
const uint8 = new Uint8Array(buffer);
uint8[0] = 7;

// 7 (0111) AND 2 (0010) = 2 (0010)
console.log(Atomics.and(uint8, 0, 2));
// expected output: 7

console.log(Atomics.load(uint8, 0));
// expected output: 2
```

## atomics/atomics-compareexchange

```js
// create a SharedArrayBuffer with a size in bytes
const buffer = new SharedArrayBuffer(16);
const uint8 = new Uint8Array(buffer);
uint8[0] = 5;

Atomics.compareExchange(uint8, 0, 5, 2); // returns 5
console.log(Atomics.load(uint8, 0));
// expected output: 2

Atomics.compareExchange(uint8, 0, 5, 4); // returns 2
console.log(Atomics.load(uint8, 0));
// expected output: 2
```

## atomics/atomics-exchange

```js
// create a SharedArrayBuffer with a size in bytes
const buffer = new SharedArrayBuffer(16);
const uint8 = new Uint8Array(buffer);
uint8[0] = 5;

console.log(Atomics.load(uint8, 0));
// expected output: 5

Atomics.exchange(uint8, 0, 2); // returns 5
console.log(Atomics.load(uint8, 0));
// expected output: 2
```

## atomics/atomics-islockfree

```js
console.log(Atomics.isLockFree(3));
// 3 is not one of the BYTES_PER_ELEMENT values
// expected output: false

console.log(Atomics.isLockFree(4));
// 4 is one of the BYTES_PER_ELEMENT values
// expected output: true
```

## atomics/atomics-load

```js
// create a SharedArrayBuffer with a size in bytes
const buffer = new SharedArrayBuffer(16);
const uint8 = new Uint8Array(buffer);
uint8[0] = 5;

// 5 + 2 = 7
console.log(Atomics.add(uint8, 0, 2));
// expected output: 5

console.log(Atomics.load(uint8, 0));
// expected output: 7
```

## atomics/atomics-or

```js
// create a SharedArrayBuffer with a size in bytes
const buffer = new SharedArrayBuffer(16);
const uint8 = new Uint8Array(buffer);
uint8[0] = 5;

// 5 (0101) OR 2 (0010) = 7 (0111)
console.log(Atomics.or(uint8, 0, 2));
// expected output: 5

console.log(Atomics.load(uint8, 0));
// expected output: 7
```

## atomics/atomics-store

```js
// create a SharedArrayBuffer with a size in bytes
const buffer = new SharedArrayBuffer(16);
const uint8 = new Uint8Array(buffer);
uint8[0] = 5;

console.log(Atomics.store(uint8, 0, 2));
// expected output: 2

console.log(Atomics.load(uint8, 0));
// expected output: 2
```

## atomics/atomics-sub

```js
// create a SharedArrayBuffer with a size in bytes
const buffer = new SharedArrayBuffer(16);
const uint8 = new Uint8Array(buffer);
uint8[0] = 7;

// 7 - 2 = 5
console.log(Atomics.sub(uint8, 0, 2));
// expected output: 7

console.log(Atomics.load(uint8, 0));
// expected output: 5
```

## atomics/atomics-xor

```js
// create a SharedArrayBuffer with a size in bytes
const buffer = new SharedArrayBuffer(16);
const uint8 = new Uint8Array(buffer);
uint8[0] = 7;

// 7 (0111) XOR 2 (0010) = 5 (0101)
console.log(Atomics.xor(uint8, 0, 2));
// expected output: 7

console.log(Atomics.load(uint8, 0));
// expected output: 5
```

## bigint/bigint-asintn

```js
const max = 2n ** (64n - 1n) - 1n;

function check64bit(number) {
  (number > max) ?
    console.log("Number doesn't fit in signed 64-bit integer!") :
    console.log(BigInt.asIntN(64, number));
}

check64bit(2n ** 64n);
// expected output: "Number doesn't fit in signed 64-bit integer!"

check64bit(2n ** 32n);
// expected output: 4294967296
```

## bigint/bigint-asuintn

```js
const max = 2n ** 64n - 1n;

function check64bit(number) {
  (number > max) ?
    console.log("Number doesn't fit in unsigned 64-bit integer!") :
    console.log(BigInt.asUintN(64, number));
}

check64bit(2n ** 64n);
// expected output: "Number doesn't fit in unsigned 64-bit integer!"

check64bit(2n ** 32n);
// expected output: 4294967296
```

## bigint/bigint-tolocalestring

```js
const bigint = 123456789123456789n;

// German uses period for thousands
console.log(bigint.toLocaleString('de-DE'));
// expected output: "123.456.789.123.456.789"

// request a currency format
console.log(bigint.toLocaleString('de-DE', { style: 'currency', currency: 'EUR' }));
// expected output: "€123.456.789.123.456.789,00"
```

## bigint/bigint-tostring

```js
console.log(1024n.toString());
// expected output: "1024"

console.log(1024n.toString(2));
// expected output: "10000000000"

console.log(1024n.toString(16));
// expected output: "400"
```

## bigint/bigint-valueof

```js
console.log(typeof Object(1n));
// expected output: "object"

console.log(typeof Object(1n).valueOf());
// expected output: "bigint"
```

## boolean/boolean-constructor

```js
const flag = new Boolean();

console.log(flag);
// expected output: Boolean: false
```

## boolean/boolean-tostring

```js
const flag1 = new Boolean(true);

console.log(flag1.toString());
// expected output: "true"

const flag2 = new Boolean(1);

console.log(flag2.toString());
// expected output: "true"
```

## boolean/boolean-valueof

```js
const x = new Boolean();

console.log(x.valueOf());
// expected output: false

const y = new Boolean("Mozilla");

console.log(y.valueOf());
// expected output: true
```

## classes/classes-constructor

```js
class Polygon {
  constructor() {
    this.name = "Polygon";
  }
}

const poly1 = new Polygon();

console.log(poly1.name);
// expected output: "Polygon"
```

## classes/classes-extends

```js
class formatDate extends Date {
  constructor(dateStr) {
    super(dateStr);
  }

  getFormattedDate() {
    const months = ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun',
                  'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec'];

    return `${this.getDate()}-${months[this.getMonth()]}-${this.getFullYear()}`;
  }
}

console.log(new formatDate('August 19, 1975 23:15:30').getFormattedDate());
// expected output: "19-Aug-1975"
```

## classes/classes-static

```js
class ClassWithStaticMethod {
  static staticMethod() {
    return 'static method has been called.';
  }
}

console.log(ClassWithStaticMethod.staticMethod());
// expected output: "static method has been called."
```

## dataview/dataview-buffer

```js
//create an ArrayBuffer
const buffer = new ArrayBuffer(123);

// Create a view
const view = new DataView(buffer);

console.log(view.buffer.byteLength);
// expected output: 123
```

## dataview/dataview-bytelength

```js
// create an ArrayBuffer with a size in bytes
const buffer = new ArrayBuffer(16);

const view1 = new DataView(buffer);
const view2 = new DataView(buffer,12,4); //from byte 12 for the next 4 bytes

console.log(view1.byteLength + view2.byteLength); // 16 + 4
// expected output: 20
```

## dataview/dataview-byteoffset

```js
// create an ArrayBuffer with a size in bytes
const buffer = new ArrayBuffer(16);

const view = new DataView(buffer,12,4); //from byte 12 for the next 4 bytes

console.log(view.byteOffset);
// expected output: 12
```

## dataview/dataview-constructor

```js
// create an ArrayBuffer with a size in bytes
const buffer = new ArrayBuffer(16);

// Create a couple of views
const view1 = new DataView(buffer);
const view2 = new DataView(buffer,12,4); //from byte 12 for the next 4 bytes
view1.setInt8(12, 42); // put 42 in slot 12

console.log(view2.getInt8(0));
// expected output: 42
```

## dataview/dataview-getbigint64

```js
// create an ArrayBuffer with a size in bytes
const buffer = new ArrayBuffer(16);

// Highest possible BigInt value that fits in a signed 64-bit integer
const max = 2n ** (64n -1n) - 1n;

const view = new DataView(buffer);
view.setBigInt64(1, max);

console.log(view.getBigInt64(1));
// expected output: 9223372036854775807
```

## dataview/dataview-getbiguint64

```js
// create an ArrayBuffer with a size in bytes
const buffer = new ArrayBuffer(16);

// Highest possible BigInt value that fits in an unsigned 64-bit integer
const max = 2n ** 64n - 1n;

const view = new DataView(buffer);
view.setBigUint64(1, max);

console.log(view.getBigUint64(1));
// expected output: 18446744073709551615
```

## dataview/dataview-getfloat32

```js
// create an ArrayBuffer with a size in bytes
const buffer = new ArrayBuffer(16);

const view = new DataView(buffer);
view.setFloat32(1, Math.PI);

console.log(view.getFloat32(1));
// expected output: 3.1415927410125732
```

## dataview/dataview-getfloat64

```js
// create an ArrayBuffer with a size in bytes
const buffer = new ArrayBuffer(16);

const view = new DataView(buffer);
view.setFloat64(1, Math.PI);

console.log(view.getFloat64(1));
// expected output: 3.141592653589793
```

## dataview/dataview-getint16

```js
// create an ArrayBuffer with a size in bytes
const buffer = new ArrayBuffer(16);

const view = new DataView(buffer);
view.setInt16(1, 32767); // (max signed 16-bit integer)

console.log(view.getInt16(1));
// expected output: 32767
```

## dataview/dataview-getint32

```js
// create an ArrayBuffer with a size in bytes
const buffer = new ArrayBuffer(16);

const view = new DataView(buffer);
view.setInt32(1, 2147483647); // (max signed 32-bit integer)

console.log(view.getInt32(1));
// expected output: 2147483647
```

## dataview/dataview-getint8

```js
// create an ArrayBuffer with a size in bytes
const buffer = new ArrayBuffer(16);

const view = new DataView(buffer);
view.setInt8(1, 127); // (max signed 8-bit integer)

console.log(view.getInt8(1));
// expected output: 127
```

## dataview/dataview-getuint16

```js
// create an ArrayBuffer with a size in bytes
const buffer = new ArrayBuffer(16);

const view = new DataView(buffer);
view.setUint16(1, 65535); // (max unsigned 16-bit integer)

console.log(view.getUint16(1));
// expected output: 65535
```

## dataview/dataview-getuint32

```js
// create an ArrayBuffer with a size in bytes
const buffer = new ArrayBuffer(16);

const view = new DataView(buffer);
view.setUint32(1, 4294967295); // (max unsigned 32-bit integer)

console.log(view.getUint32(1));
// expected output: 4294967295
```

## dataview/dataview-getuint8

```js
// create an ArrayBuffer with a size in bytes
const buffer = new ArrayBuffer(16);

const view = new DataView(buffer);
view.setUint8(1, 255); // (max unsigned 8-bit integer)

console.log(view.getUint8(1));
// expected output: 255
```

## dataview/dataview-setbigint64

```js
// create an ArrayBuffer with a size in bytes
const buffer = new ArrayBuffer(16);

// Highest possible BigInt value that fits in a signed 64-bit integer
const max = 2n ** (64n -1n) - 1n;

const view = new DataView(buffer);
view.setBigInt64(1, max);

console.log(view.getBigInt64(1));
// expected output: 9223372036854775807
```

## dataview/dataview-setbiguint64

```js
// create an ArrayBuffer with a size in bytes
const buffer = new ArrayBuffer(16);

// Highest possible BigInt value that fits in an unsigned 64-bit integer
const max = 2n ** 64n - 1n;

const view = new DataView(buffer);
view.setBigUint64(1, max);

console.log(view.getBigUint64(1));
// expected output: 18446744073709551615
```

## dataview/dataview-setfloat32

```js
// create an ArrayBuffer with a size in bytes
const buffer = new ArrayBuffer(16);

const view = new DataView(buffer);
view.setFloat32(1, Math.PI);

console.log(view.getFloat32(1));
// expected output: 3.1415927410125732
```

## dataview/dataview-setfloat64

```js
// create an ArrayBuffer with a size in bytes
const buffer = new ArrayBuffer(16);

const view = new DataView(buffer);
view.setFloat64(1, Math.PI);

console.log(view.getFloat64(1));
// expected output: 3.141592653589793
```

## dataview/dataview-setint16

```js
// create an ArrayBuffer with a size in bytes
const buffer = new ArrayBuffer(16);

const view = new DataView(buffer);
view.setInt16(1, 32767); // (max signed 16-bit integer)

console.log(view.getInt16(1));
// expected output: 32767
```

## dataview/dataview-setint32

```js
// create an ArrayBuffer with a size in bytes
const buffer = new ArrayBuffer(16);

const view = new DataView(buffer);
view.setInt32(1, 2147483647); // (max signed 32-bit integer)

console.log(view.getInt32(1));
// expected output: 2147483647
```

## dataview/dataview-setint8

```js
// create an ArrayBuffer with a size in bytes
const buffer = new ArrayBuffer(16);

const view = new DataView(buffer);
view.setInt8(1, 127); // (max signed 8-bit integer)

console.log(view.getInt8(1));
// expected output: 127
```

## dataview/dataview-setuint16

```js
// create an ArrayBuffer with a size in bytes
const buffer = new ArrayBuffer(16);

const view = new DataView(buffer);
view.setUint16(1, 65535); // (max unsigned 16-bit integer)

console.log(view.getUint16(1));
// expected output: 65535
```

## dataview/dataview-setuint32

```js
// create an ArrayBuffer with a size in bytes
const buffer = new ArrayBuffer(16);

const view = new DataView(buffer);
view.setUint32(1, 4294967295); // (max unsigned 32-bit integer)

console.log(view.getUint32(1));
// expected output: 4294967295
```

## dataview/dataview-setuint8

```js
// create an ArrayBuffer with a size in bytes
const buffer = new ArrayBuffer(16);

const view = new DataView(buffer);
view.setUint8(1, 255); // (max unsigned 8-bit integer)

console.log(view.getUint8(1));
// expected output: 255
```

## date/date-constructor

```js
const date1 = new Date('December 17, 1995 03:24:00');
// Sun Dec 17 1995 03:24:00 GMT...

const date2 = new Date('1995-12-17T03:24:00');
// Sun Dec 17 1995 03:24:00 GMT...

console.log(date1 === date2);
// expected output: false;

console.log(date1 - date2);
// expected output: 0
```

## date/date-getdate

```js
const birthday = new Date('August 19, 1975 23:15:30');
const date1 = birthday.getDate();

console.log(date1);
// expected output: 19
```

## date/date-getday

```js
const birthday = new Date('August 19, 1975 23:15:30');
const day1 = birthday.getDay();
// Sunday - Saturday : 0 - 6

console.log(day1);
// expected output: 2
```

## date/date-getfullyear

```js
const moonLanding = new Date('July 20, 69 00:20:18');

console.log(moonLanding.getFullYear());
// expected output: 1969
```

## date/date-gethours

```js
const birthday = new Date('March 13, 08 04:20');

console.log(birthday.getHours());
// expected output: 4
```

## date/date-getmilliseconds

```js
const moonLanding = new Date('July 20, 69 00:20:18');
moonLanding.setMilliseconds(123);

console.log(moonLanding.getMilliseconds());
// expected output: 123
```

## date/date-getminutes

```js
const birthday = new Date('March 13, 08 04:20');

console.log(birthday.getMinutes());
// expected output: 20
```

## date/date-getmonth

```js
const moonLanding = new Date('July 20, 69 00:20:18');

console.log(moonLanding.getMonth()); // (January gives 0)
// expected output: 6
```

## date/date-getseconds

```js
const moonLanding = new Date('July 20, 69 00:20:18');

console.log(moonLanding.getSeconds());
// expected output: 18
```

## date/date-gettime

```js
const moonLanding = new Date('July 20, 69 00:20:18 GMT+00:00');

// milliseconds since Jan 1, 1970, 00:00:00.000 GMT
console.log(moonLanding.getTime());
// expected output: -14254782000
```

## date/date-gettimezoneoffset

```js
const date1 = new Date('August 19, 1975 23:15:30 GMT+07:00');
const date2 = new Date('August 19, 1975 23:15:30 GMT-02:00');

console.log(date1.getTimezoneOffset());
// expected output: your local timezone offset in minutes
// (eg -120). NOT the timezone offset of the date object.

console.log(date1.getTimezoneOffset() === date2.getTimezoneOffset());
// expected output: true
```

## date/date-getutcdate

```js
const date1 = new Date('August 19, 1975 23:15:30 GMT+11:00');
const date2 = new Date('August 19, 1975 23:15:30 GMT-11:00');

console.log(date1.getUTCDate());
// expected output: 19

console.log(date2.getUTCDate());
// expected output: 20
```

## date/date-getutcday

```js
const date1 = new Date('August 19, 1975 23:15:30 GMT+11:00');
const date2 = new Date('August 19, 1975 23:15:30 GMT-11:00');

// Tuesday
console.log(date1.getUTCDay());
// expected output: 2

// Wednesday
console.log(date2.getUTCDay());
// expected output: 3
```

## date/date-getutcfullyear

```js
const date1 = new Date('December 31, 1975, 23:15:30 GMT+11:00');
const date2 = new Date('December 31, 1975, 23:15:30 GMT-11:00');

console.log(date1.getUTCFullYear());
// expected output: 1975

console.log(date2.getUTCFullYear());
// expected output: 1976
```

## date/date-getutchours

```js
const date1 = new Date('December 31, 1975, 23:15:30 GMT+11:00');
const date2 = new Date('December 31, 1975, 23:15:30 GMT-11:00');

console.log(date1.getUTCHours());
// expected output: 12

console.log(date2.getUTCHours());
// expected output: 10
```

## date/date-getutcmilliseconds

```js
const exampleDate = new Date('2018-01-02T03:04:05.678Z'); // 2 January 2018, 03:04:05.678 (UTC)

console.log(exampleDate.getUTCMilliseconds());
// expected output: 678
```

## date/date-getutcminutes

```js
const date1 = new Date('1 January 2000 03:15:30 GMT+07:00');
const date2 = new Date('1 January 2000 03:15:30 GMT+03:30');

console.log(date1.getUTCMinutes()); // 31 Dec 1999 20:15:30 GMT
// expected output: 15

console.log(date2.getUTCMinutes()); // 31 Dec 1999 23:45:30 GMT
// expected output: 45
```

## date/date-getutcmonth

```js
const date1 = new Date('December 31, 1975, 23:15:30 GMT+11:00');
const date2 = new Date('December 31, 1975, 23:15:30 GMT-11:00');

// December
console.log(date1.getUTCMonth());
// expected output: 11

// January
console.log(date2.getUTCMonth());
// expected output: 0
```

## date/date-getutcseconds

```js
const moonLanding = new Date('July 20, 1969, 20:18:04 UTC');

console.log(moonLanding.getUTCSeconds());
// expected output: 4
```

## date/date-now

```js
// this example takes 2 seconds to run
const start = Date.now();

console.log('starting timer...');
// expected output: starting timer...

setTimeout(() => {
  const millis = Date.now() - start;

  console.log(`seconds elapsed = ${Math.floor(millis/1000)}`);
  // expected output : seconds elapsed = 2
}, 2000);
```

## date/date-parse

```js
const unixTimeZero = Date.parse('01 Jan 1970 00:00:00 GMT');
const javaScriptRelease = Date.parse('04 Dec 1995 00:12:00 GMT');

console.log(unixTimeZero);
// expected output: 0

console.log(javaScriptRelease);
// expected output: 818035920000
```

## date/date-setdate

```js
const event = new Date('August 19, 1975 23:15:30');

event.setDate(24);

console.log(event.getDate());
// expected output: 24

event.setDate(32);
// Only 31 days in August!

console.log(event.getDate());
// expected output: 1
```

## date/date-setfullyear

```js
const event = new Date('August 19, 1975 23:15:30');

event.setFullYear(1969);

console.log(event.getFullYear());
// expected output: 1969

event.setFullYear(0);

console.log(event.getFullYear());
// expected output: 0
```

## date/date-sethours

```js
const event = new Date('August 19, 1975 23:15:30');
event.setHours(20);

console.log(event);
// expected output: Tue Aug 19 1975 20:15:30 GMT+0200 (CEST)
// (note: your timezone may vary)

event.setHours(20,21,22);

console.log(event);
// expected output: Tue Aug 19 1975 20:21:22 GMT+0200 (CEST)
```

## date/date-setmilliseconds

```js
const event = new Date('August 19, 1975 23:15:30');

console.log(event.getMilliseconds());
// expected output: 0

event.setMilliseconds(456);

console.log(event.getMilliseconds());
// expected output: 456
```

## date/date-setminutes

```js
const event = new Date('August 19, 1975 23:15:30');

event.setMinutes(45);

console.log(event.getMinutes());
// expected output: 45

console.log(event);
// expected output: Tue Aug 19 1975 23:45:30 GMT+0200 (CEST)
// (note: your timezone may vary)
```

## date/date-setmonth

```js
const event = new Date('August 19, 1975 23:15:30');

event.setMonth(3);

console.log(event.getMonth());
// expected output: 3

console.log(event);
// Sat Apr 19 1975 23:15:30 GMT+0100 (CET)
// (note: your timezone may vary)
```

## date/date-setseconds

```js
const event = new Date('August 19, 1975 23:15:30');

event.setSeconds(42);

console.log(event.getSeconds());
// expected output: 42

console.log(event);
// Sat Aug 19 1975 23:15:42 GMT+0100 (CET)
// (note: your timezone may vary)
```

## date/date-settime

```js
const event1 = new Date('July 1, 1999');
const event2 = new Date();
event2.setTime(event1.getTime());

console.log(event1);
// expected output: Thu Jul 01 1999 00:00:00 GMT+0200 (CEST)

console.log(event2);
// expected output: Thu Jul 01 1999 00:00:00 GMT+0200 (CEST)
// (note: your timezone may vary)
```

## date/date-setutcdate

```js
const event = new Date('August 19, 1975 23:15:30 GMT-3:00');

console.log(event.getUTCDate());
// expected output: 20

event.setUTCDate(19);

console.log(event.getUTCDate());
// expected output: 19
```

## date/date-setutcfullyear

```js
const event = new Date('December 31, 1975 23:15:30 GMT-3:00');

console.log(event.getUTCFullYear());
// expected output: 1976

console.log(event.toUTCString());
// expected output: Thu, 01 Jan 1976 02:15:30 GMT

event.setUTCFullYear(1975);

console.log(event.toUTCString());
// expected output: Wed, 01 Jan 1975 02:15:30 GMT
```

## date/date-setutchours

```js
const event = new Date('August 19, 1975 23:15:30 GMT-3:00');

console.log(event.toUTCString());
// expected output: Wed, 20 Aug 1975 02:15:30 GMT

console.log(event.getUTCHours());
// expected output: 2

event.setUTCHours(23);

console.log(event.toUTCString());
// expected output: Wed, 20 Aug 1975 23:15:30 GMT
```

## date/date-setutcmilliseconds

```js
const date1 = new Date('2018-01-24T12:38:29.069Z');

console.log(date1.getUTCMilliseconds());
// expected output: 69

date1.setUTCMilliseconds(420);

console.log(date1.getUTCMilliseconds());
// expected output: 420
```

## date/date-setutcminutes

```js
const date1 = new Date('December 31, 1975, 23:15:30 GMT+11:00');

console.log(date1.getUTCMinutes());
// expected output: 15

date1.setUTCMinutes(25);

console.log(date1.getUTCMinutes());
// expected output: 25
```

## date/date-setutcmonth

```js
const event = new Date('December 31, 1975 23:15:30 GMT-3:00');

console.log(event.toUTCString());
// Thu, 01 Jan 1976 02:15:30 GMT

console.log(event.getUTCMonth());
// expected output: 0

event.setUTCMonth(11);

console.log(event.toUTCString());
// expected output: Wed, 01 Dec 1976 02:15:30 GMT
```

## date/date-setutcseconds

```js
const date1 = new Date('December 31, 1975, 23:15:30 GMT+11:00');

console.log(date1.getUTCSeconds());
// expected output: 30

date1.setUTCSeconds(39);

console.log(date1.getUTCSeconds());
// expected output: 39
```

## date/date-todatestring

```js
const event = new Date(1993, 6, 28, 14, 39, 7);

console.log(event.toString());
// expected output: Wed Jul 28 1993 14:39:07 GMT+0200 (CEST)
// (note: your timezone may vary)

console.log(event.toDateString());
// expected output: Wed Jul 28 1993
```

## date/date-toisostring

```js
const event = new Date('05 October 2011 14:48 UTC');
console.log(event.toString());
// expected output: Wed Oct 05 2011 16:48:00 GMT+0200 (CEST)
// (note: your timezone may vary)

console.log(event.toISOString());
// expected output: 2011-10-05T14:48:00.000Z
```

## date/date-tojson

```js
const event = new Date('August 19, 1975 23:15:30 UTC');

const jsonDate = event.toJSON();

console.log(jsonDate);
// expected output: 1975-08-19T23:15:30.000Z

console.log(new Date(jsonDate).toUTCString());
// expected output: Tue, 19 Aug 1975 23:15:30 GMT
```

## date/date-tolocaledatestring

```js
// Note: this snippet only works in the browser

const event = new Date(Date.UTC(2012, 11, 20, 3, 0, 0));

const options = { weekday: 'long', year: 'numeric', month: 'long', day: 'numeric' };

console.log(event.toLocaleDateString('de-DE', options));
// expected output: Donnerstag, 20. Dezember 2012

console.log(event.toLocaleDateString('ar-EG', options));
// expected output: الخميس، ٢٠ ديسمبر، ٢٠١٢

console.log(event.toLocaleDateString('ko-KR', options));
// expected output: 2012년 12월 20일 목요일
```

## date/date-tolocalestring

```js
const event = new Date(Date.UTC(2012, 11, 20, 3, 0, 0));

// British English uses day-month-year order and 24-hour time without AM/PM
console.log(event.toLocaleString('en-GB', { timeZone: 'UTC' }));
// expected output: 20/12/2012, 03:00:00

// Korean uses year-month-day order and 12-hour time with AM/PM
console.log(event.toLocaleString('ko-KR', { timeZone: 'UTC' }));
// expected output: 2012. 12. 20. 오전 3:00:00
```

## date/date-tolocaletimestring

```js
// Depending on timezone, your results will vary
const event = new Date('August 19, 1975 23:15:30 GMT+00:00');

console.log(event.toLocaleTimeString('en-US'));
// expected output: 1:15:30 AM

console.log(event.toLocaleTimeString('it-IT'));
// expected output: 01:15:30

console.log(event.toLocaleTimeString('ar-EG'));
// expected output: ١٢:١٥:٣٠ ص
```

## date/date-tostring

```js
const event = new Date('August 19, 1975 23:15:30');

console.log(event.toString());
// expected output: Tue Aug 19 1975 23:15:30 GMT+0200 (CEST)
// (note: your timezone may vary)
```

## date/date-totimestring

```js
const event = new Date('August 19, 1975 23:15:30');

console.log(event.toTimeString());
// expected output: 23:15:30 GMT+0200 (CEST)
// (note: your timezone may vary)
```

## date/date-toutcstring

```js
const event = new Date('14 Jun 2017 00:00:00 PDT');

console.log(event.toUTCString());
// expected output: Wed, 14 Jun 2017 07:00:00 GMT
```

## date/date-utc

```js
const utcDate1 = new Date(Date.UTC(96, 1, 2, 3, 4, 5));
const utcDate2 = new Date(Date.UTC(0, 0, 0, 0, 0, 0));

console.log(utcDate1.toUTCString());
// expected output: Fri, 02 Feb 1996 03:04:05 GMT

console.log(utcDate2.toUTCString());
// expected output: Sun, 31 Dec 1899 00:00:00 GMT
```

## date/date-valueof

```js
const date1 = new Date(Date.UTC(96, 1, 2, 3, 4, 5));

console.log(date1.valueOf());
// expected output: 823230245000

const date2 = new Date('02 Feb 1996 03:04:05 GMT');

console.log(date2.valueOf());
// expected output: 823230245000
```

## expressions/expressions-arithmetic

```js
// Number addition and subtraction
console.log(2 + 3 - 1);
// expected output: 4

// Number multiplication and division
console.log(4 * 3 / 2); // 12 / 2
// expected output: 6

// Number remainder and exponential
console.log(11 % 3 ** 2); // 11 % 9
// expected output: 2
```

## expressions/expressions-assignment

```js
var x = 2;
var y = 3;

console.log(x);
// expected output: 2

console.log(x = y + 1); // 3 + 1
// expected output: 4

console.log(x = x * y); // 4 * 3
// expected output: 12
```

## expressions/expressions-bitwiseoperators

```js
console.log(5 & 13); // 0101 & 1101 = 0101
// expected output: 5;

console.log(parseInt("0101",2) & parseInt("1101",2));
// expected output: 5;

console.log(5 & 13 & 3); // 0101 & 1101 & 0011 = 0001
// expected output: 1;

console.log(5 | 13); // 0101 | 1101 = 1101
// expected output: 13
```

## expressions/expressions-classexpression

```js
var Rectangle = class {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
  area() {
    return this.height * this.width;
  }
}

console.log(new Rectangle(5,8).area());
// expected output: 40
```

## expressions/expressions-commaoperators

```js
var x = 1;

x = (x++, x);

console.log(x);
// expected output: 2

x = (2, 3);

console.log(x);
// expected output: 3
```

## expressions/expressions-comparisonoperators

```js
console.log(1 == 1);
// expected output: true

console.log("1" == 1);
// expected output: true

console.log(1 === 1);
// expected output: true

console.log("1" === 1);
// expected output: false
```

## expressions/expressions-conditionaloperators

```js
function getFee(isMember) {
  return (isMember ? "$2.00" : "$10.00");
}

console.log(getFee(true));
// expected output: "$2.00"

console.log(getFee(false));
// expected output: "$10.00"

console.log(getFee(1));
// expected output: "$2.00"
```

## expressions/expressions-deleteoperator

```js
var Employee = {
  firstname: "John",
  lastname: "Doe"
}

console.log(Employee.firstname);
// expected output: "John"

delete Employee.firstname;

console.log(Employee.firstname);
// expected output: undefined
```

## expressions/expressions-destructuringassignment

```js
var a, b, rest;
[a, b] = [10, 20];

console.log(a);
// expected output: 10

console.log(b);
// expected output: 20

[a, b, ...rest] = [10, 20, 30, 40, 50];

console.log(rest);
// expected output: [30,40,50]
```

## expressions/expressions-functionasteriskexpression

```js
function* foo() {
  yield 'a';
  yield 'b';
  yield 'c';
}

var str = "";
for (let val of foo()) {
  str = str + val;
}

console.log(str);
// expected output: "abc"
```

## expressions/expressions-functionexpression

```js
var getRectArea = function(width, height) {
    return width * height;
}

console.log(getRectArea(3,4));
// expected output: 12
```

## expressions/expressions-groupingoperator

```js
console.log(1 + 2 * 3); // 1 + 6
// expected output: 7

console.log(1 + (2 * 3)); // 1 + 6
// expected output: 7

console.log((1 + 2) * 3); // 3 * 3
// expected output: 9

console.log(1 * 3 + 2 * 3); // 3 + 6
// expected output: 9
```

## expressions/expressions-inoperator

```js
var car = {make: 'Honda', model: 'Accord', year: 1998};

console.log('make' in car);
// expected output: true

delete car.make;
if ('make' in car === false) {
  car.make = 'Suzuki';
}

console.log(car.make);
// expected output: "Suzuki"
```

## expressions/expressions-instanceof

```js
function Car(make, model, year) {
  this.make = make;
  this.model = model;
  this.year = year;
}
var auto = new Car('Honda', 'Accord', 1998);

console.log(auto instanceof Car);
// expected output: true

console.log(auto instanceof Object);
// expected output: true
```

## expressions/expressions-logicaloperator

```js
var a = 3;
var b = -2;

console.log(a > 0 && b > 0);
// expected output: false

console.log(a > 0 || b > 0);
// expected output: true

console.log(!(a > 0 || b > 0));
// expected output: false
```

## expressions/expressions-newoperator

```js
function Car(make, model, year) {
  this.make = make;
  this.model = model;
  this.year = year;
}

var car1 = new Car('Eagle', 'Talon TSi', 1993);

console.log(car1.make);
// expected output: "Eagle"
```

## expressions/expressions-newtarget

```js
function Foo() {
  if (!new.target) throw 'Foo() must be called with new';
}

try {
  Foo();
}
catch(e) {
  console.log(e);
  // expected output: "Foo() must be called with new"
}
```

## expressions/expressions-objectinitializer

```js
var object1 = {a: 'foo', b: 42, c: {}};

console.log(object1.a);
// expected output: "foo"

var a = 'foo';
var b = 42;
var c = {};
var object2 = {a: a, b: b, c: c};

console.log(object2.b);
// expected output: 42
```

## expressions/expressions-operatorprecedence

```js
console.log(3 + 4 * 5); // 3 + 20
// expected output: 23

console.log(4 * 3 ** 2); // 4 * 9
// expected output: 36

var a;
var b;

console.log(a = b = 5);
// expected output: 5;
```

## expressions/expressions-propertyaccessors

```js
var person = {};
person['firstname'] = 'Mario';
person['lastname'] = 'Rossi';

console.log(person.firstname);
// expected output: "Mario"

person = {'firstname': 'John', 'lastname': 'Doe'}

console.log(person['lastname']);
// expected output: "Doe"
```

## expressions/expressions-spreadsyntax

```js
function sum(x, y, z) {
  return x + y + z;
}

const numbers = [1, 2, 3];

console.log(sum(...numbers));
// expected output: 6

console.log(sum.apply(null, numbers));
// expected output: 6
```

## expressions/expressions-this

```js
var test = {
  prop: 42,
  func: function() {
    return this.prop;
  },
};

console.log(test.func());
// expected output: 42
```

## expressions/expressions-typeof

```js
console.log(typeof 42);
// expected output: "number"

console.log(typeof 'blubber');
// expected output: "string"

console.log(typeof true);
// expected output: "boolean"

console.log(typeof declaredButUndefinedVariable);
// expected output: "undefined";
```

## expressions/expressions-voidoperator

```js
void function test() {
  console.log('boo!');
  // expected output: "boo!"
}();

try {
  test();
}
catch(e) {
  console.log(e);
  // expected output: ReferenceError: test is not defined
}
```

## expressions/expressions-yield

```js
function* foo(index) {
  while (index < 2) {
    yield index++;
  }
}

const iterator = foo(0);

console.log(iterator.next().value);
// expected output: 0

console.log(iterator.next().value);
// expected output: 1
```

## expressions/expressions-yieldasterisk

```js
function* func1() {
  yield 42;
}

function* func2() {
  yield* func1();
}

const iterator = func2();

console.log(iterator.next().value);
// expected output: 42
```

## function/function-apply

```js
const numbers = [5, 6, 2, 3, 7];

const max = Math.max.apply(null, numbers);

console.log(max);
// expected output: 7

const min = Math.min.apply(null, numbers);

console.log(min);
// expected output: 2
```

## function/function-bind

```js
const module = {
  x: 42,
  getX: function() {
    return this.x;
  }
}

const unboundGetX = module.getX;
console.log(unboundGetX()); // The function gets invoked at the global scope
// expected output: undefined

const boundGetX = unboundGetX.bind(module);
console.log(boundGetX());
// expected output: 42
```

## function/function-call

```js
function Product(name, price) {
  this.name = name;
  this.price = price;
}

function Food(name, price) {
  Product.call(this, name, price);
  this.category = 'food';
}

console.log(new Food('cheese', 5).name);
// expected output: "cheese"
```

## function/function-constructor

```js
const sum = new Function('a', 'b', 'return a + b');

console.log(sum(2, 6));
// expected output: 8
```

## function/function-length

```js
function func1() {}

function func2(a, b) {}

console.log(func1.length);
// expected output: 0

console.log(func2.length);
// expected output: 2
```

## function/function-name

```js
const func1 = function() {}
  
const object = {
  func2: function() {}
}

console.log(func1.name);
// expected output: "func1"

console.log(object.func2.name);
// expected output: "func2"
```

## function/function-tostring

```js
function sum(a, b) {
  return a + b;
}

console.log(sum.toString());
// expected output: "function sum(a, b) {
//                     return a + b;
//                   }"

console.log(Math.abs.toString());
// expected output: "function abs() { [native code] }"
```

## functions/functions-arguments

```js
function func1(a, b, c) {
  console.log(arguments[0]);
  // expected output: 1

  console.log(arguments[1]);
  // expected output: 2

  console.log(arguments[2]);
  // expected output: 3
}

func1(1, 2, 3);
```

## functions/functions-arrow

```js
var materials = [
  'Hydrogen',
  'Helium',
  'Lithium',
  'Beryllium'
];

console.log(materials.map(material => material.length));
// expected output: Array [8, 6, 7, 9]
```

## functions/functions-default

```js
function multiply(a, b = 1) {
  return a * b;
}

console.log(multiply(5, 2));
// expected output: 10

console.log(multiply(5));
// expected output: 5
```

## functions/functions-definitions

```js
var obj = {
  foo() {
    return 'bar';
  }
}

console.log(obj.foo());
// expected output: "bar"
```

## functions/functions-getter

```js
var obj = {
  log: ['a', 'b', 'c'],
  get latest() {
    if (this.log.length == 0) {
      return undefined;
    }
    return this.log[this.log.length - 1];
  }
}

console.log(obj.latest);
// expected output: "c"
```

## functions/functions-restparameters

```js
function sum(...theArgs) {
  return theArgs.reduce((previous, current) => {
    return previous + current;
  });
}

console.log(sum(1, 2, 3));
// expected output: 6

console.log(sum(1, 2, 3, 4));
// expected output: 10
```

## functions/functions-setter

```js
var language = {
  set current(name) {
    this.log.push(name);
  },
  log: []
}

language.current = 'EN';
language.current = 'FA';

console.log(language.log);
// expected output: Array ["EN", "FA"]
```

## globalprops/globalprops-decodeuri

```js
const uri = 'https://mozilla.org/?x=шеллы';
const encoded = encodeURI(uri);
console.log(encoded);
// expected output: "https://mozilla.org/?x=%D1%88%D0%B5%D0%BB%D0%BB%D1%8B"

try {
  console.log(decodeURI(encoded));
  // expected output: "https://mozilla.org/?x=шеллы"
} catch(e) { // catches a malformed URI
  console.error(e);
}
```

## globalprops/globalprops-decodeuricomponent

```js
function containsEncodedComponents(x) {
  // ie ?,=,&,/ etc
  return (decodeURI(x) !== decodeURIComponent(x));
}

console.log(containsEncodedComponents('%3Fx%3Dtest')); // ?x=test
// expected output: true

console.log(containsEncodedComponents('%D1%88%D0%B5%D0%BB%D0%BB%D1%8B')); // шеллы
// expected output: false
```

## globalprops/globalprops-encodeuri

```js
const uri = 'https://mozilla.org/?x=шеллы';
const encoded = encodeURI(uri);
console.log(encoded);
// expected output: "https://mozilla.org/?x=%D1%88%D0%B5%D0%BB%D0%BB%D1%8B"

try {
  console.log(decodeURI(encoded));
  // expected output: "https://mozilla.org/?x=шеллы"
} catch(e) { // catches a malformed URI
  console.error(e);
}
```

## globalprops/globalprops-encodeuricomponent

```js
// encodes characters such as ?,=,/,&,:
console.log(encodeURIComponent('?x=шеллы'));
// expected output: "%3Fx%3D%D1%88%D0%B5%D0%BB%D0%BB%D1%8B"

console.log(encodeURIComponent('?x=test'));
// expected output: "%3Fx%3Dtest"
```

## globalprops/globalprops-eval

```js
console.log(eval('2 + 2'));
// expected output: 4

console.log(eval(new String('2 + 2')));
// expected output: 2 + 2

console.log(eval('2 + 2') === eval('4'));
// expected output: true

console.log(eval('2 + 2') === eval(new String('2 + 2')));
// expected output: false
```

## globalprops/globalprops-globalthis

```js
function canMakeHTTPRequest() {
    return typeof globalThis.XMLHttpRequest === 'function';
}

console.log(canMakeHTTPRequest());
// expected output: false
```

## globalprops/globalprops-infinity

```js
const maxNumber = Math.pow(10, 1000); // max positive number

if (maxNumber === Infinity) {
  console.log("Let's call it Infinity!");
  // expected output: "Let's call it Infinity!"
}

console.log(1 / maxNumber);
// expected output: 0
```

## globalprops/globalprops-isfinite

```js
function div(x) {
  if (isFinite(1000 / x)) {
    return 'Number is NOT Infinity.';
  }
  return "Number is Infinity!";
}

console.log(div(0));
// expected output: "Number is Infinity!""

console.log(div(1));
// expected output: "Number is NOT Infinity."
```

## globalprops/globalprops-isnan

```js
function milliseconds(x) {
  if (isNaN(x)) {
    return 'Not a Number!';
  }
  return x * 1000;
}

console.log(milliseconds('100F'));
// expected output: "Not a Number!"

console.log(milliseconds('0.0314E+2'));
// expected output: 3140
```

## globalprops/globalprops-nan

```js
function sanitise(x) {
  if (isNaN(x)) {
    return NaN;
  }
  return x;
}

console.log(sanitise('1'));
// expected output: "1"

console.log(sanitise('NotANumber'));
// expected output: NaN
```

## globalprops/globalprops-null

```js
function getVowels(str) {
  const m = str.match(/[aeiou]/gi);
  if (m === null) {
    return 0;
  }
  return m.length;
}

console.log(getVowels('sky'));
// expected output: 0
```

## globalprops/globalprops-parsefloat

```js
function circumference(r) {
  return parseFloat(r) * 2.0 * Math.PI;
}

console.log(circumference(4.567));
// expected output: 28.695307297889173

console.log(circumference('4.567abcdefgh'));
// expected output: 28.695307297889173

console.log(circumference('abcdefgh'));
// expected output: NaN
```

## globalprops/globalprops-parseint

```js
function roughScale(x, base) {
  const parsed = parseInt(x, base);
  if (isNaN(parsed)) { return 0 }
  return parsed * 100;
}

console.log(roughScale(' 0xF', 16));
// expected output: 1500

console.log(roughScale('321', 2));
// expected output: 0
```

## globalprops/globalprops-undefined

```js
function test(t) {
  if (t === undefined) {
     return 'Undefined value!';
  }
  return t;
}

let x;

console.log(test(x));
// expected output: "Undefined value!"
```

## intl/intl-collator-prototype-compare

```js
const enCollator = new Intl.Collator('en');
const deCollator = new Intl.Collator('de');
const svCollator = new Intl.Collator('sv');

console.log(enCollator.compare('z', 'a') > 0);
// expected output: true

console.log(deCollator.compare('z', 'ä') > 0);
// expected output: true

console.log(svCollator.compare('z', 'ä') > 0);
// expected output: true
```

## intl/intl-collator-supportedlocalesof

```js
// Note: this snippet only works in the browser

var locales1 = ['ban', 'id-u-co-pinyin', 'de-ID'];
var options1 = { localeMatcher: 'lookup' };

console.log(Intl.Collator.supportedLocalesOf(locales1, options1));
// expected output: Array ["id-u-co-pinyin", "de-ID"]
// (Note: the exact output may be browser-dependent)
```

## intl/intl-collator

```js
// Note: this snippet only works in the browser

function letterSort(lang, letters) {
  letters.sort(new Intl.Collator(lang).compare);
  return letters;
}

console.log(letterSort('de', ['a','z','ä']));
// expected output: Array ["a", "ä", "z"]

console.log(letterSort('sv', ['a','z','ä']));
// expected output: Array ["a", "z", "ä"]
```

## intl/intl-datetimeformat-prototype-format

```js
// Note: this snippet only works in the browser

var options1 = { weekday: 'long', year: 'numeric', month: 'long', day: 'numeric' };
var date1 = new Date(2012, 05);

var dateTimeFormat1 = new Intl.DateTimeFormat('sr-RS', options1);
console.log(dateTimeFormat1.format(date1));
// expected output: "петак, 1. јун 2012."

var dateTimeFormat2 = new Intl.DateTimeFormat('en-GB', options1);
console.log(dateTimeFormat2.format(date1));

var dateTimeFormat3 = new Intl.DateTimeFormat('en-US', options1);
console.log(dateTimeFormat3.format(date1));
```

## intl/intl-datetimeformat-prototype-formatrange

```js
var options1 = { weekday: 'long', year: 'numeric', month: 'long', day: 'numeric' };
var options2 = { year: '2-digit', month: 'numeric', day: 'numeric' };

var startDate = new Date(Date.UTC(2007, 0, 10, 10, 0, 0));
var endDate = new Date(Date.UTC(2008, 0, 10, 11, 0, 0));

var dateTimeFormat = new Intl.DateTimeFormat('en', options1);
console.log(dateTimeFormat.formatRange(startDate, endDate));
// expected output: Wednesday, January 10, 2007 – Thursday, January 10, 2008

var dateTimeFormat2 = new Intl.DateTimeFormat("en", options2);
console.log(dateTimeFormat2.formatRange(startDate, endDate));
// expected output: 1/10/07 – 1/10/08
```

## intl/intl-datetimeformat-prototype-resolvedoptions

```js
var region1 = new Intl.DateTimeFormat('zh-CN', { timeZone: 'UTC' });
var options1 = region1.resolvedOptions();

console.log(options1.locale);
// expected output: "zh-CN"

console.log(options1.calendar);
// expected output: "gregory"

console.log(options1.numberingSystem);
// expected output: "latn"
```

## intl/intl-datetimeformat-supportedlocalesof

```js
// Note: this snippet only works in the browser

var locales1 = ['ban', 'id-u-co-pinyin', 'de-ID'];
var options1 = { localeMatcher: 'lookup' };

console.log(Intl.DateTimeFormat.supportedLocalesOf(locales1, options1));
// expected output: Array ["id-u-co-pinyin", "de-ID"]
// (Note: the exact output may be browser-dependent)
```

## intl/intl-datetimeformat

```js
// Note: this snippet only works in the browser

var date = new Date(Date.UTC(2012, 11, 20, 3, 0, 0));
// Results below assume UTC timezone - your results may vary

console.log(new Intl.DateTimeFormat('en-US').format(date));
// expected output: "12/20/2012"

console.log(new Intl.DateTimeFormat('en-GB').format(date));
// expected output: "20/12/2012"

// Include a fallback language, in this case Indonesian
console.log(new Intl.DateTimeFormat(['ban', 'id']).format(date));
// expected output: "20/12/2012"
```

## intl/intl-getcanonicallocales

```js
console.log(Intl.getCanonicalLocales('EN-US'));
// expected output: Array ["en-US"]

console.log(Intl.getCanonicalLocales(['EN-US', 'Fr']));
// expected output: Array ["en-US", "fr"]

try {
  Intl.getCanonicalLocales('EN_US');
} catch (err) {
  console.log(err);
  // expected output: RangeError: invalid language tag: EN_US
}
```

## intl/intl-listformat

```js
const vehicles = ['Motorcycle', 'Bus', 'Car'];

const formatter = new Intl.ListFormat('en', { style: 'long', type: 'conjunction' });
console.log(formatter.format(vehicles));
// expected output: "Motorcycle, Bus, and Car"

const formatter2 = new Intl.ListFormat('de', { style: 'short', type: 'disjunction' });
console.log(formatter2.format(vehicles));
// expected output: "Motorcycle, Bus or Car"

const formatter3 = new Intl.ListFormat('en', { style: 'narrow', type: 'unit' });
console.log(formatter3.format(vehicles));
// expected output: "Motorcycle Bus Car"
```

## intl/intl-locale-prototype-maximize

```js
const english = new Intl.Locale("en");
const korean = new Intl.Locale("ko");
const arabic = new Intl.Locale("ar");

console.log(english.maximize().baseName);
// expected output: "en-Latn-US"

console.log(korean.maximize().baseName);
// expected output: "ko-Kore-KR"

console.log(arabic.maximize().baseName);
// expected output: "ar-Arab-EG"
```

## intl/intl-locale-prototype-minimize

```js
const english = new Intl.Locale("en-Latn-US");
const korean = new Intl.Locale("ko-Kore-KR");
const arabic = new Intl.Locale("ar-Arab-EG");

console.log(english.minimize().baseName);
// expected output: "en"

console.log(korean.minimize().baseName);
// expected output: "ko"

console.log(arabic.minimize().baseName);
// expected output: "ar"
```

## intl/intl-locale-prototype-tostring

```js
const french = new Intl.Locale("fr-Latn-FR", {calendar: "gregory", hourCycle: "h24"});
const korean = new Intl.Locale("ko-Kore-KR", {numeric: true, caseFirst: "upper"});

console.log(french.toString());
// expected output: "fr-Latn-FR-u-ca-gregory-hc-h24"

console.log(korean.toString())
//expected output: "ko-Kore-KR-u-kf-upper-kn"
```

## intl/intl-locale

```js
const korean = new Intl.Locale('ko', {
  script: 'Kore', region: 'KR', hourCycle: 'h24', calendar: 'gregory'
});

const japanese = new Intl.Locale('ja-Jpan-JP-u-ca-japanese-hc-h12');

console.log(korean.baseName, japanese.baseName);
// expected output: "ko-Kore-KR" "ja-Jpan-JP"

console.log(korean.hourCycle, japanese.hourCycle);
// expected output: "h24" "h12"
```

## intl/intl-numberformat-prototype-format

```js
var amount = 654321.987;

var options1 = { style: 'currency', currency: 'RUB' };
var numberFormat1 = new Intl.NumberFormat('ru-RU', options1);

console.log(numberFormat1.format(amount));
// expected output: "654 321,99 ₽"

var options2 = { style: 'currency', currency: 'USD' };
var numberFormat2 = new Intl.NumberFormat('en-US', options2);

console.log(numberFormat2.format(amount));
// expected output: "$654,321.99"
```

## intl/intl-numberformat-prototype-resolvedoptions

```js
var numberFormat1 = new Intl.NumberFormat('de-DE');
var options1 = numberFormat1.resolvedOptions();

console.log(options1.locale);
// expected output (Firefox / Safari): "de-DE"
// expected output (Chrome): "de"

console.log(options1.numberingSystem);
// expected output: "latn"

console.log(options1.style);
// "decimal"
```

## intl/intl-numberformat-supportedlocalesof

```js
// Note: this snippet only works in the browser

var locales1 = ['ban', 'id-u-co-pinyin', 'de-ID'];
var options1 = { localeMatcher: 'lookup' };

console.log(Intl.NumberFormat.supportedLocalesOf(locales1, options1));
// expected output: Array ["id-u-co-pinyin", "de-ID"]
// (Note: the exact output may be browser-dependent)
```

## intl/intl-numberformat

```js
var number = 123456.789;

console.log(new Intl.NumberFormat('de-DE', { style: 'currency', currency: 'EUR' }).format(number));
// expected output: "123.456,79 €"

// the Japanese yen doesn't use a minor unit
console.log(new Intl.NumberFormat('ja-JP', { style: 'currency', currency: 'JPY' }).format(number));
// expected output: "￥123,457"

// limit to three significant digits
console.log(new Intl.NumberFormat('en-IN', { maximumSignificantDigits: 3 }).format(number));
// expected output: "1,23,000"
```

## intl/intl-relativetimeformat-prototype-format

```js
var rtf1 = new Intl.RelativeTimeFormat('en', { style: 'narrow' });

console.log(rtf1.format(3, 'quarter'));
// expected output: "in 3 qtrs."

console.log(rtf1.format(-1, 'day'));
// expected output: "1 day ago"

console.log(rtf1.format(10, 'seconds'));
// expected output: "in 10 sec."
```

## intl/intl-relativetimeformat-prototype-formattoparts

```js
var rtf1 = new Intl.RelativeTimeFormat('en', { numeric: 'auto' });
var parts = rtf1.formatToParts(10, 'seconds');

console.log(parts[0].value);
// expected output: "in "

console.log(parts[1].value);
// expected output: "10"

console.log(parts[2].value);
// expected output: " seconds"
```

## intl/intl-relativetimeformat-prototype-resolvedoptions

```js
var rtf1 = new Intl.RelativeTimeFormat('en', { style: 'narrow' });
var options1 = rtf1.resolvedOptions();

var rtf2 = new Intl.RelativeTimeFormat('es', { numeric: 'auto' });
var options2 = rtf2.resolvedOptions();

console.log(`${options1.locale}, ${options1.style}, ${options1.numeric}`);
// expected output: "en, narrow, always"

console.log(`${options2.locale}, ${options2.style}, ${options2.numeric}`);
// expected output: "es, long, auto"
```

## intl/intl-relativetimeformat-supportedlocalesof

```js
// Note: this snippet only works in the browser

var locales1 = ['ban', 'id-u-co-pinyin', 'de-ID'];
var options1 = { localeMatcher: 'lookup' };

console.log(Intl.RelativeTimeFormat.supportedLocalesOf(locales1, options1));
// expected output: Array ["id-u-co-pinyin", "de-ID"]
// (Note: the exact output may be browser-dependent)
```

## intl/intl-relativetimeformat

```js
var rtf1 = new Intl.RelativeTimeFormat('en', { style: 'narrow' });

console.log(rtf1.format(3, 'quarter'));
//expected output: "in 3 qtrs."

console.log(rtf1.format(-1, 'day'));
//expected output: "1 day ago"

var rtf2 = new Intl.RelativeTimeFormat('es', { numeric: 'auto' });

console.log(rtf2.format(2, 'day'));
//expected output: "pasado mañana"
```

## json/json-parse

```js
var json = '{"result":true, "count":42}';
obj = JSON.parse(json);

console.log(obj.count);
// expected output: 42

console.log(obj.result);
// expected output: true
```

## json/json-stringify

```js
console.log(JSON.stringify({ x: 5, y: 6 }));
// expected output: "{"x":5,"y":6}"

console.log(JSON.stringify([new Number(3), new String('false'), new Boolean(false)]));
// expected output: "[3,"false",false]"

console.log(JSON.stringify({ x: [10, undefined, function(){}, Symbol('')] }));
// expected output: "{"x":[10,null,null,null]}"

console.log(JSON.stringify(new Date(2006, 0, 2, 15, 4, 5)));
// expected output: ""2006-01-02T15:04:05.000Z""
```

## map/map-prototype-@@iterator

```js
var map1 = new Map();

map1.set('0', 'foo');
map1.set(1, 'bar');

var iterator1 = map1[Symbol.iterator]();

for (let item of iterator1) {
  console.log(item);
  // expected output: Array ["0", "foo"]
  // expected output: Array [1, "bar"]
}
```

## map/map-prototype-@@tostringtag

```js
var map1 = Object.prototype.toString.call(new Map());

console.log(map1);
// expected output: "[object Map]"
```

## map/map-prototype-clear

```js
var map1 = new Map();

map1.set('bar', 'baz');
map1.set(1, 'foo');

console.log(map1.size);
// expected output: 2

map1.clear();

console.log(map1.size);
// expected output: 0
```

## map/map-prototype-delete

```js
var map1 = new Map();
map1.set('bar', 'foo');

console.log(map1.delete('bar'));
// expected result: true
// (true indicates successful removal)

console.log(map1.has('bar'));
// expected result: false
```

## map/map-prototype-entries

```js
var map1 = new Map();

map1.set('0', 'foo');
map1.set(1, 'bar');

var iterator1 = map1.entries();

console.log(iterator1.next().value);
// expected output: ["0", "foo"]

console.log(iterator1.next().value);
// expected output: [1, "bar"]
```

## map/map-prototype-foreach

```js
function logMapElements(value, key, map) {
  console.log(`m[${key}] = ${value}`);
}

new Map([['foo', 3], ['bar', {}], ['baz', undefined]])
  .forEach(logMapElements);

// expected output: "m[foo] = 3"
// expected output: "m[bar] = [object Object]"
// expected output: "m[baz] = undefined"
```

## map/map-prototype-get

```js
var map1 = new Map();
map1.set('bar', 'foo');

console.log(map1.get('bar'));
// expected output: "foo"

console.log(map1.get('baz'));
// expected output: undefined
```

## map/map-prototype-has

```js
var map1 = new Map();
map1.set('bar', 'foo');

console.log(map1.has('bar'));
// expected output: true

console.log(map1.has('baz'));
// expected output: false
```

## map/map-prototype-keys

```js
var map1 = new Map();

map1.set('0', 'foo');
map1.set(1, 'bar');

var iterator1 = map1.keys();

console.log(iterator1.next().value);
// expected output: "0"

console.log(iterator1.next().value);
// expected output: 1
```

## map/map-prototype-set

```js
var map1 = new Map();
map1.set('bar', 'foo');

console.log(map1.get('bar'));
// expected output: "foo"

console.log(map1.get('baz'));
// expected output: undefined
```

## map/map-prototype-size

```js
var map1 = new Map();

map1.set('a', 'alpha');
map1.set('b', 'beta');
map1.set('g', 'gamma');

console.log(map1.size);
// expected output: 3
```

## map/map-prototype-values

```js
var map1 = new Map();

map1.set('0', 'foo');
map1.set(1, 'bar');

var iterator1 = map1.values();

console.log(iterator1.next().value);
// expected output: "foo"

console.log(iterator1.next().value);
// expected output: "bar"
```

## math/math-abs

```js
function difference(a, b) {
  return Math.abs(a - b);
}

console.log(difference(3, 5));
// expected output: 2

console.log(difference(5, 3));
// expected output: 2

console.log(difference(1.23456, 7.89012));
// expected output: 6.6555599999999995
```

## math/math-acos

```js
// Calculates angle of a right-angle triangle in radians
function calcAngle(adjacent, hypotenuse) {
  return Math.acos(adjacent / hypotenuse);
}

console.log(calcAngle(8, 10));
// expected output: 0.6435011087932843

console.log(calcAngle(5, 3));
// expected output: NaN
```

## math/math-acosh

```js
console.log(Math.acosh(0.999999999999));
// expected output: NaN

console.log(Math.acosh(1));
// expected output: 0

console.log(Math.acosh(2));
// expected output: 1.3169578969248166

console.log(Math.acosh(2.5));
// expected output: 1.566799236972411
```

## math/math-asin

```js
// Calculates angle of a right-angle triangle in radians
function calcAngle(opposite, hypotenuse) {
  return Math.asin(opposite / hypotenuse);
}

console.log(calcAngle(6, 10));
// expected output: 0.6435011087932844

console.log(calcAngle(5, 3));
// expected output: NaN
```

## math/math-asinh

```js
console.log(Math.asinh(1));
// expected output: 0.881373587019543

console.log(Math.asinh(0));
// expected output: 0

console.log(Math.asinh(-1));
// expected output: -0.881373587019543

console.log(Math.asinh(2));
// expected output: 1.4436354751788103
```

## math/math-atan

```js
// Calculates angle of a right-angle triangle in radians
function calcAngle(opposite, adjacent) {
  return Math.atan(opposite / adjacent);
}

console.log(calcAngle(8, 10));
// expected output: 0.6747409422235527

console.log(calcAngle(5, 3));
// expected output: 1.0303768265243125
```

## math/math-atan2

```js
function calcAngleDegrees(x, y) {
  return Math.atan2(y, x) * 180 / Math.PI;
}

console.log(calcAngleDegrees(5, 5));
//expected output: 45

console.log(calcAngleDegrees(10, 10));
//expected output: 45

console.log(calcAngleDegrees(0, 10));
//expected output: 90
```

## math/math-atanh

```js
console.log(Math.atanh(-1));
// expected output: -Infinity

console.log(Math.atanh(0));
// expected output: 0

console.log(Math.atanh(0.5));
// expected output: 0.549306144334055 (approximately)

console.log(Math.atanh(1));
// expected output: Infinity
```

## math/math-cbrt

```js
console.log(Math.cbrt(-1));
// expected output: -1

console.log(Math.cbrt(1));
// expected output: 1

console.log(Math.cbrt(Infinity));
// expected output: Infinity

console.log(Math.cbrt(64));
// expected output: 4
```

## math/math-ceil

```js
console.log(Math.ceil(.95));
// expected output: 1

console.log(Math.ceil(4));
// expected output: 4

console.log(Math.ceil(7.004));
// expected output: 8

console.log(Math.ceil(-7.004));
// expected output: -7
```

## math/math-clz32

```js
// 00000000000000000000000000000001
console.log(Math.clz32(1));
// expected output: 31

// 00000000000000000000000000000100
console.log(Math.clz32(4));
// expected output: 29

// 00000000000000000000001111101000
console.log(Math.clz32(1000));
// expected output: 22
```

## math/math-cos

```js
function getCircleX(radians, radius) {
  return Math.cos(radians) * radius;
}

console.log(getCircleX(1, 10));
// expected output: 5.403023058681398

console.log(getCircleX(2, 10));
// expected output: -4.161468365471424

console.log(getCircleX(Math.PI, 10));
// expected output: -10
```

## math/math-cosh

```js
console.log(Math.cosh(0));
// expected output: 1

console.log(Math.cosh(1));
// expected output: 1.543080634815244 (approximately)

console.log(Math.cosh(-1));
// expected output: 1.543080634815244 (approximately)

console.log(Math.cosh(2));
// expected output: 3.7621956910836314
```

## math/math-e

```js
function compoundOneYear(interestRate, currentVal) {
  return currentVal * (Math.E ** interestRate);
}

console.log(Math.E);
// expected output: 2.718281828459045

console.log((1 + (1/1000000)) ** 1000000);
// expected output: 2.718280469 (approximately)

console.log(compoundOneYear(0.05, 100));
// expected output: 105.12710963760242
```

## math/math-exp

```js
console.log(Math.exp(0));
// expected output: 1

console.log(Math.exp(1));
// expected output: 2.718281828459 (approximately)

console.log(Math.exp(-1));
// expected output: 0.36787944117144233

console.log(Math.exp(2));
// expected output: 7.38905609893065
```

## math/math-expm1

```js
console.log(Math.expm1(0));
// expected output: 0

console.log(Math.expm1(1));
// expected output: 1.718281828459045

console.log(Math.expm1(-1));
// expected output: -0.6321205588285577

console.log(Math.expm1(2));
// expected output: 6.38905609893065
```

## math/math-floor

```js
console.log(Math.floor(5.95));
// expected output: 5

console.log(Math.floor(5.05));
// expected output: 5

console.log(Math.floor(5));
// expected output: 5

console.log(Math.floor(-5.05));
// expected output: -6
```

## math/math-fround

```js
console.log(Math.fround(5.5));
// expected output: 5.5

console.log(Math.fround(5.05));
// expected output: 5.050000190734863

console.log(Math.fround(5));
// expected output: 5

console.log(Math.fround(-5.05));
// expected output: -5.050000190734863
```

## math/math-hypot

```js
console.log(Math.hypot(3, 4));
// expected output: 5

console.log(Math.hypot(5, 12));
// expected output: 13

console.log(Math.hypot(3, 4, 5));
// expected output: 7.0710678118654755

console.log(Math.hypot(-5));
// expected output: 5
```

## math/math-imul

```js
console.log(Math.imul(3, 4));
// expected output: 12

console.log(Math.imul(-5, 12));
// expected output: -60

console.log(Math.imul(0xffffffff, 5));
// expected output: -5

console.log(Math.imul(0xfffffffe, 5));
// expected output: -10
```

## math/math-ln10

```js
function getNatLog10() {
  return Math.LN10;
}

console.log(getNatLog10());
// expected output: 2.302585092994046
```

## math/math-ln2

```js
function getNatLog2() {
  return Math.LN2;
}

console.log(getNatLog2());
// expected output: 0.6931471805599453
```

## math/math-log

```js
function getBaseLog(x, y) {
  return Math.log(y) / Math.log(x);
}

// 2 x 2 x 2 = 8
console.log(getBaseLog(2, 8));
// expected output: 3

// 5 x 5 x 5 x 5 = 625
console.log(getBaseLog(5, 625));
// expected output: 4
```

## math/math-log10

```js
console.log(Math.log10(100000));
// expected output: 5

console.log(Math.log10(2));
// expected output: 0.3010299956639812

console.log(Math.log10(1));
// expected output: 0

console.log(Math.log10(0));
// expected output: -Infinity
```

## math/math-log10e

```js
function getLog10e() {
  return Math.LOG10E;
}

console.log(getLog10e());
// expected output: 0.4342944819032518
```

## math/math-log1p

```js
console.log(Math.log1p(1));
// expected output: 0.6931471805599453

console.log(Math.log1p(0));
// expected output: 0

console.log(Math.log1p(-1));
// expected output: -Infinity

console.log(Math.log1p(-2));
// expected output: NaN
```

## math/math-log2

```js
console.log(Math.log2(3));
// expected output: 1.584962500721156

console.log(Math.log2(2));
// expected output: 1

console.log(Math.log2(1));
// expected output: 0

console.log(Math.log2(0));
// expected output: -Infinity
```

## math/math-log2e

```js
function getLog2e() {
  return Math.LOG2E;
}

console.log(getLog2e());
// expected output: 1.4426950408889634
```

## math/math-max

```js
console.log(Math.max(1, 3, 2));
// expected output: 3

console.log(Math.max(-1, -3, -2));
// expected output: -1

var array1 = [1, 3, 2];

console.log(Math.max(...array1));
// expected output: 3
```

## math/math-min

```js
console.log(Math.min(2, 3, 1));
// expected output: 1

console.log(Math.min(-2, -3, -1));
// expected output: -3

var array1 = [2, 3, 1];

console.log(Math.min(...array1));
// expected output: 1
```

## math/math-pi

```js
function calculateCircumference(radius) {
  return 2 * Math.PI * radius;
}

console.log(Math.PI);
// expected output: 3.141592653589793

console.log(calculateCircumference(10));
// expected output: 62.83185307179586
```

## math/math-pow

```js
console.log(Math.pow(7, 3));
// expected output: 343

console.log(Math.pow(4, 0.5));
// expected output: 2

console.log(Math.pow(7, -2));
// expected output: 0.02040816326530612
//                  (1/49)

console.log(Math.pow(-7, 0.5));
// expected output: NaN
```

## math/math-random

```js
function getRandomInt(max) {
  return Math.floor(Math.random() * Math.floor(max));
}

console.log(getRandomInt(3));
// expected output: 0, 1 or 2

console.log(getRandomInt(1));
// expected output: 0

console.log(Math.random());
// expected output: a number between 0 and 1
```

## math/math-round

```js
console.log(Math.round(0.9));
// expected output: 1

console.log(Math.round(5.95), Math.round(5.5), Math.round(5.05));
// expected output: 6 6 5

console.log(Math.round(-5.05), Math.round(-5.5), Math.round(-5.95));
// expected output: -5 -5 -6
```

## math/math-sign

```js
console.log(Math.sign(3));
// expected output: 1

console.log(Math.sign(-3));
// expected output: -1

console.log(Math.sign(0));
// expected output: 0

console.log(Math.sign('-3'));
// expected output: -1
```

## math/math-sin

```js
function getCircleY(radians, radius) {
  return Math.sin(radians) * radius;
}

console.log(getCircleY(1, 10));
// expected output: 8.414709848078965

console.log(getCircleY(2, 10));
// expected output: 9.092974268256818

console.log(getCircleY(Math.PI, 10));
// expected output: 1.2246467991473533e-15
```

## math/math-sinh

```js
console.log(Math.sinh(0));
// expected output: 0

console.log(Math.sinh(1));
// expected output: 1.1752011936438014

console.log(Math.sinh(-1));
// expected output: -1.1752011936438014

console.log(Math.sinh(2));
// expected output: 3.626860407847019
```

## math/math-sqrt

```js
function calcHypotenuse(a, b) {
  return(Math.sqrt((a * a) + (b * b)));
}

console.log(calcHypotenuse(3, 4));
// expected output: 5

console.log(calcHypotenuse(5, 12));
// expected output: 13

console.log(calcHypotenuse(0, 0));
// expected output: 0
```

## math/math-sqrt1_2

```js
function getRoot1Over2() {
  return Math.SQRT1_2;
}

console.log(getRoot1Over2());
// expected output: 0.7071067811865476
```

## math/math-sqrt2

```js
function getRoot2() {
  return Math.SQRT2;
}

console.log(getRoot2());
// expected output: 1.4142135623730951
```

## math/math-tan

```js
function getTanFromDegrees(degrees) {
  return Math.tan(degrees * Math.PI/180);
}

console.log(getTanFromDegrees(0));
// expected output: 0

console.log(getTanFromDegrees(45));
// expected output: 0.9999999999999999

console.log(getTanFromDegrees(90));
// expected output: 16331239353195370
```

## math/math-tanh

```js
console.log(Math.tanh(-1));
// expected output: -0.7615941559557649

console.log(Math.tanh(0));
// expected output: 0

console.log(Math.tanh(Infinity));
// expected output: 1

console.log(Math.tanh(1));
// expected output: 0.7615941559557649
```

## math/math-trunc

```js
console.log(Math.trunc(13.37));
// expected output: 13

console.log(Math.trunc(42.84));
// expected output: 42

console.log(Math.trunc(0.123));
// expected output: 0

console.log(Math.trunc(-0.123));
// expected output: -0
```

## number/number-epsilon

```js
var result = Math.abs(0.2 - 0.3 + 0.1);

console.log(result);
// expected output: 2.7755575615628914e-17

console.log(result < Number.EPSILON);
// expected output: true
```

## number/number-isfinite

```js
console.log(Number.isFinite(1/0));
// expected output: false

console.log(Number.isFinite(10/5));
// expected output: true

console.log(Number.isFinite(0/0));
// expected output: false
```

## number/number-isinteger

```js
function fits(x, y) {
  if (Number.isInteger(y / x)) {
    return 'Fits!';
  }
  return 'Does NOT fit!';
}

console.log(fits(5, 10));
// expected output: "Fits!"

console.log(fits(5, 11));
// expected output: "Does NOT fit!"
```

## number/number-isnan

```js
function typeOfNaN(x) {
  if (Number.isNaN(x)) {
    return 'Number NaN';
  }
  if (isNaN(x)) {
    return 'NaN';
  }
}

console.log(typeOfNaN('100F'));
// expected output: "NaN"

console.log(typeOfNaN(NaN));
// expected output: "Number NaN"
```

## number/number-issafeinteger

```js
function warn(x) {
  if (Number.isSafeInteger(x)) {
    return 'Precision safe.';
  }
  return 'Precision may be lost!';
}

console.log(warn(Math.pow(2, 53)));
// expected output: "Precision may be lost!"

console.log(warn(Math.pow(2, 53) - 1));
// expected output: "Precision safe."
```

## number/number-max-safe-integer

```js
var x = Number.MAX_SAFE_INTEGER + 1;
var y = Number.MAX_SAFE_INTEGER + 2;

console.log(Number.MAX_SAFE_INTEGER);
// expected output: 9007199254740991

console.log(x);
// expected output: 9007199254740992

console.log(x === y);
// expected output: true
```

## number/number-max-value

```js
function multiply(x, y) {
  if (x * y > Number.MAX_VALUE) {
    return ("Process as Infinity");
  }
  return (x * y);
}

console.log(multiply(1.7976931348623157e+308, 1));
// expected output: 1.7976931348623157e+308

console.log(multiply(1.7976931348623157e+308, 2));
// expected output: "Process as Infinity"
```

## number/number-min-safe-integer

```js
var x = Number.MIN_SAFE_INTEGER - 1;
var y = Number.MIN_SAFE_INTEGER - 2;

console.log(Number.MIN_SAFE_INTEGER);
// expected output: -9007199254740991

console.log(x);
// expected output: -9007199254740992

console.log(x === y);
// expected output: true
```

## number/number-min-value

```js
function multiply(x, y) {
  if (x * y < Number.MIN_VALUE) {
    return "Process as -Infinity";
  }
  return (x * y);
}

console.log(multiply(5e-324, 1));
// expected output: 5e-324

console.log(multiply(-1.7976931348623157e+308, 2));
// expected output: Process as -Infinity
```

## number/number-nan

```js
function clean(x) {
  if (x === Number.NaN) {
    // can never be true
    return null;
  }
  if (isNaN(x)) {
    return 0;
  }
}

console.log(clean(Number.NaN));
// expected output: 0
```

## number/number-negative-infinity

```js
function checkNumber(smallNumber) {
  if (smallNumber === Number.NEGATIVE_INFINITY) {
    return 'Process number as -Infinity';
  }
  return smallNumber;
}

console.log(checkNumber(-Number.MAX_VALUE));
// expected output: -1.7976931348623157e+308

console.log(checkNumber(-Number.MAX_VALUE * 2));
// expected output: "Process number as -Infinity"
```

## number/number-parsefloat

```js
function circumference(r) {
  if (Number.isNaN(Number.parseFloat(r))) {
    return 0;
  }
  return parseFloat(r) * 2.0 * Math.PI ;
}

console.log(circumference('4.567abcdefgh'));
// expected output: 28.695307297889173

console.log(circumference('abcdefgh'));
// expected output: 0
```

## number/number-parseint

```js
function roughScale(x, base) {
  var parsed = Number.parseInt(x, base);
  if (Number.isNaN(parsed)) {
    return 0;
  }
  return parsed * 100;
}

console.log(roughScale(' 0xF', 16));
// expected output: 1500

console.log(roughScale('321', 2));
// expected output: 0
```

## number/number-positive-infinity

```js
function checkNumber(bigNumber) {
  if (bigNumber === Number.POSITIVE_INFINITY) {
    return 'Process number as Infinity';
  }
  return bigNumber;
}

console.log(checkNumber(Number.MAX_VALUE));
// expected output: 1.7976931348623157e+308

console.log(checkNumber(Number.MAX_VALUE * 2));
// expected output: Process number as Infinity
```

## number/number-toexponential

```js
function expo(x, f) {
  return Number.parseFloat(x).toExponential(f);
}

console.log(expo(123456, 2));
// expected output: "1.23e+5"

console.log(expo('123456'));
// expected output: "1.23456e+5"

console.log(expo('oink'));
// expected output: "NaN"
```

## number/number-tofixed

```js
function financial(x) {
  return Number.parseFloat(x).toFixed(2);
}

console.log(financial(123.456));
// expected output: "123.46"

console.log(financial(0.004));
// expected output: "0.00"

console.log(financial('1.23e+5'));
// expected output: "123000.00"
```

## number/number-tolocalestring

```js
function eArabic(x){
  return x.toLocaleString('ar-EG');
}

console.log(eArabic(123456.789));
// expected output: "١٢٣٬٤٥٦٫٧٨٩"

console.log(eArabic("123456.789"));
// expected output: "123456.789"

console.log(eArabic(NaN));
// expected output: "ليس رقم"
```

## number/number-toprecision

```js
function precise(x) {
  return Number.parseFloat(x).toPrecision(4);
}

console.log(precise(123.456));
// expected output: "123.5"

console.log(precise(0.004));
// expected output: "0.004000"

console.log(precise('1.23e+5'));
// expected output: "1.230e+5"
```

## number/number-tostring

```js
function hexColour(c) {
  if (c < 256) {
    return Math.abs(c).toString(16);
  }
  return 0;
}

console.log(hexColour(233));
// expected output: "e9"

console.log(hexColour('11'));
// expected output: "b"
```

## number/number-valueof

```js
var numObj = new Number(42);
console.log(typeof numObj);
// expected output: "object"

var num = numObj.valueOf();
console.log(num);
// expected output: 42

console.log(typeof num);
// expected output: "number"
```

## object/object-assign

```js
const target = { a: 1, b: 2 };
const source = { b: 4, c: 5 };

const returnedTarget = Object.assign(target, source);

console.log(target);
// expected output: Object { a: 1, b: 4, c: 5 }

console.log(returnedTarget);
// expected output: Object { a: 1, b: 4, c: 5 }
```

## object/object-create

```js
const person = {
  isHuman: false,
  printIntroduction: function () {
    console.log(`My name is ${this.name}. Am I human? ${this.isHuman}`);
  }
};

const me = Object.create(person);

me.name = "Matthew"; // "name" is a property set on "me", but not on "person"
me.isHuman = true; // inherited properties can be overwritten

me.printIntroduction();
// expected output: "My name is Matthew. Am I human? true"
```

## object/object-defineproperties

```js
const object1 = {};

Object.defineProperties(object1, {
  property1: {
    value: 42,
    writable: true
  },
  property2: {}
});

console.log(object1.property1);
// expected output: 42
```

## object/object-defineproperty

```js
const object1 = {};

Object.defineProperty(object1, 'property1', {
  value: 42,
  writable: false
});

object1.property1 = 77;
// throws an error in strict mode

console.log(object1.property1);
// expected output: 42
```

## object/object-entries

```js
const object1 = {
  a: 'somestring',
  b: 42
};

for (let [key, value] of Object.entries(object1)) {
  console.log(`${key}: ${value}`);
}

// expected output:
// "a: somestring"
// "b: 42"
// order is not guaranteed
```

## object/object-freeze

```js
const obj = {
  prop: 42
};

Object.freeze(obj);

obj.prop = 33;
// Throws an error in strict mode

console.log(obj.prop);
// expected output: 42
```

## object/object-fromentries

```js
const entries = new Map([
  ['foo', 'bar'],
  ['baz', 42]
]);

const obj = Object.fromEntries(entries);

console.log(obj);
// expected output: Object { foo: "bar", baz: 42 }
```

## object/object-getownpropertydescriptor

```js
const object1 = {
  property1: 42
}

const descriptor1 = Object.getOwnPropertyDescriptor(object1, 'property1');

console.log(descriptor1.configurable);
// expected output: true

console.log(descriptor1.value);
// expected output: 42
```

## object/object-getownpropertydescriptors

```js
const object1 = {
  property1: 42
};

const descriptors1 = Object.getOwnPropertyDescriptors(object1);

console.log(descriptors1.property1.writable);
// expected output: true

console.log(descriptors1.property1.value);
// expected output: 42
```

## object/object-getownpropertynames

```js
const object1 = {
  a: 1,
  b: 2,
  c: 3
};

console.log(Object.getOwnPropertyNames(object1));
// expected output: Array ["a", "b", "c"]
```

## object/object-getownpropertysymbols

```js
const object1 = {};
const a = Symbol('a');
const b = Symbol.for('b');

object1[a] = 'localSymbol';
object1[b] = 'globalSymbol';

const objectSymbols = Object.getOwnPropertySymbols(object1);

console.log(objectSymbols.length);
// expected output: 2
```

## object/object-getprototypeof

```js
const prototype1 = {};
const object1 = Object.create(prototype1);

console.log(Object.getPrototypeOf(object1) === prototype1);
// expected output: true
```

## object/object-isextensible

```js
const object1 = {};

console.log(Object.isExtensible(object1));
// expected output: true

Object.preventExtensions(object1);

console.log(Object.isExtensible(object1));
// expected output: false
```

## object/object-isfrozen

```js
const object1 = {
  property1: 42
};

console.log(Object.isFrozen(object1));
// expected output: false

Object.freeze(object1);

console.log(Object.isFrozen(object1));
// expected output: true
```

## object/object-issealed

```js
const object1 = {
  property1: 42
};

console.log(Object.isSealed(object1));
// expected output: false

Object.seal(object1);

console.log(Object.isSealed(object1));
// expected output: true
```

## object/object-keys

```js
const object1 = {
  a: 'somestring',
  b: 42,
  c: false
};

console.log(Object.keys(object1));
// expected output: Array ["a", "b", "c"]
```

## object/object-preventextensions

```js
const object1 = {};

Object.preventExtensions(object1);

try {
  Object.defineProperty(object1, 'property1', {
    value: 42
  });
} catch (e) {
  console.log(e);
  // Expected output: TypeError: Cannot define property property1, object is not extensible
}
```

## object/object-prototype-hasownproperty

```js
const object1 = new Object();
object1.property1 = 42;

console.log(object1.hasOwnProperty('property1'));
// expected output: true

console.log(object1.hasOwnProperty('toString'));
// expected output: false

console.log(object1.hasOwnProperty('hasOwnProperty'));
// expected output: false
```

## object/object-prototype-isprototypeof

```js
function object1() {}
function object2() {}

object1.prototype = Object.create(object2.prototype);

const object3 = new object1();

console.log(object1.prototype.isPrototypeOf(object3));
// expected output: true

console.log(object2.prototype.isPrototypeOf(object3));
// expected output: true
```

## object/object-prototype-propertyisenumerable

```js
    const object1 = {};
const array1 = [];
object1.property1 = 42;
array1[0] = 42;

console.log(object1.propertyIsEnumerable('property1'));
// expected output: true

console.log(array1.propertyIsEnumerable(0));
// expected output: true

console.log(array1.propertyIsEnumerable('length'));
// expected output: false
```

## object/object-prototype-seal

```js
const object1 = {
  property1: 42
};

Object.seal(object1);
object1.property1 = 33;
console.log(object1.property1);
// expected output: 33

delete object1.property1; // cannot delete when sealed
console.log(object1.property1);
// expected output: 33
```

## object/object-prototype-tolocalestring

```js
const date1 = new Date(Date.UTC(2012, 11, 20, 3, 0, 0));

console.log(date1.toLocaleString('ar-EG'));
// expected output: "٢٠‏/١٢‏/٢٠١٢ ٤:٠٠:٠٠ ص"

const number1 = 123456.789;

console.log(number1.toLocaleString('de-DE'));
// expected output: "123.456,789"
```

## object/object-prototype-tostring

```js
function Dog(name) {
  this.name = name;
}

var dog1 = new Dog('Gabby');

Dog.prototype.toString = function dogToString() {
  return '' + this.name;
}

console.log(dog1.toString());
// expected output: "Gabby"
```

## object/object-prototype-valueof

```js
function MyNumberType(n) {
  this.number = n;
}

MyNumberType.prototype.valueOf = function() {
  return this.number;
};

const object1 = new MyNumberType(4);

console.log(object1 + 3);
// expected output: 7
```

## object/object-values

```js
const object1 = {
  a: 'somestring',
  b: 42,
  c: false
};

console.log(Object.values(object1));
// expected output: Array ["somestring", 42, false]
```

## promise/promise-all

```js
var promise1 = Promise.resolve(3);
var promise2 = 42;
var promise3 = new Promise(function(resolve, reject) {
  setTimeout(resolve, 100, 'foo');
});

Promise.all([promise1, promise2, promise3]).then(function(values) {
  console.log(values);
});
// expected output: Array [3, 42, "foo"]
```

## promise/promise-allsettled

```js
const promise1 = Promise.resolve(3);
const promise2 = new Promise((resolve, reject) => setTimeout(reject, 100, 'foo'));
const promises = [promise1, promise2];

Promise.allSettled(promises).
  then((results) => results.forEach((result) => console.log(result.status)));

// expected output:
// "fulfilled"
// "rejected"
```

## promise/promise-catch

```js
var promise1 = new Promise(function(resolve, reject) {
  throw 'Uh-oh!';
});

promise1.catch(function(error) {
  console.error(error);
});
// expected output: Uh-oh!
```

## promise/promise-constructor

```js
var promise1 = new Promise(function(resolve, reject) {
  setTimeout(function() {
    resolve('foo');
  }, 300);
});

promise1.then(function(value) {
  console.log(value);
  // expected output: "foo"
});

console.log(promise1);
// expected output: [object Promise]
```

## promise/promise-race

```js
var promise1 = new Promise(function(resolve, reject) {
    setTimeout(resolve, 500, 'one');
});

var promise2 = new Promise(function(resolve, reject) {
    setTimeout(resolve, 100, 'two');
});

Promise.race([promise1, promise2]).then(function(value) {
  console.log(value);
  // Both resolve, but promise2 is faster
});
// expected output: "two"
```

## promise/promise-reject

```js
function resolved(result) {
  console.log('Resolved');
}

function rejected(result) {
  console.error(result);
}

Promise.reject(new Error('fail')).then(resolved, rejected);
// expected output: Error: fail
```

## promise/promise-resolve

```js
var promise1 = Promise.resolve(123);

promise1.then(function(value) {
  console.log(value);
  // expected output: 123
});
```

## promise/promise-then

```js
var promise1 = new Promise(function(resolve, reject) {
  resolve('Success!');
});

promise1.then(function(value) {
  console.log(value);
  // expected output: "Success!"
});
```

## proxyhandler/proxyhandler-apply

```js
  function sum(a, b) {
  return a + b;
}

const handler = {
  apply: function(target, thisArg, argumentsList) {
    console.log(`Calculate sum: ${argumentsList}`);
    // expected output: "Calculate sum: 1,2"

    return target(argumentsList[0], argumentsList[1]) * 10;
  }
};

var proxy1 = new Proxy(sum, handler);

console.log(sum(1, 2)); 
// expected output: 3
console.log(proxy1(1, 2));
// expected output: 30
```

## proxyhandler/proxyhandler-construct

```js
function monster1(disposition) {
  this.disposition = disposition;
}

const handler1 = {
  construct(target, args) {
    console.log('monster1 constructor called');
    // expected output: "monster1 constructor called"

    return new target(...args);
  }
};

const proxy1 = new Proxy(monster1, handler1);

console.log(new proxy1('fierce').disposition);
// expected output: "fierce"
```

## proxyhandler/proxyhandler-defineproperty

```js
const handler1 = {
  defineProperty(target, key, descriptor) {
    invariant(key, 'define');
    return true;
  }
};

function invariant(key, action) {
  if (key[0] === '_') {
    throw new Error(`Invalid attempt to ${action} private "${key}" property`);
  }
}

const monster1 = {};
const proxy1 = new Proxy(monster1, handler1);

console.log(proxy1._secret = 'easily scared');
// expected output: Error: Invalid attempt to define private "_secret" property
```

## proxyhandler/proxyhandler-deleteproperty

```js
const monster1 = {
  texture: 'scaly'
};

const handler1 = {
  deleteProperty(target, prop) {
    if (prop in target) {
      delete target[prop];
      console.log(`property removed: ${prop}`);
      // expected output: "property removed: texture"
    }
  }
};

console.log(monster1.texture);
// expected output: "scaly"

const proxy1 = new Proxy(monster1, handler1);
delete proxy1.texture;

console.log(monster1.texture);
// expected output: undefined
```

## proxyhandler/proxyhandler-get

```js
const monster1 = {
  secret: 'easily scared',
  eyeCount: 4
};

const handler1 = {
  get: function(target, prop, receiver) {
    if (prop === 'secret') {
      return `${target.secret.substr(0, 4)} ... shhhh!`;
    } else {
      return Reflect.get(...arguments);
    }
  }
};

const proxy1 = new Proxy(monster1, handler1);

console.log(proxy1.eyeCount);
// expected output: 4

console.log(proxy1.secret);
// expected output: "easi ... shhhh!"
```

## proxyhandler/proxyhandler-getownpropertydescriptor

```js
const monster1 = {
  eyeCount: 4
};

const handler1 = {
  getOwnPropertyDescriptor(target, prop) {
    console.log(`called: ${prop}`);
    // expected output: "called: eyeCount"

    return { configurable: true, enumerable: true, value: 5 };
  }
};

const proxy1 = new Proxy(monster1, handler1);

console.log(Object.getOwnPropertyDescriptor(proxy1, 'eyeCount').value);
// expected output: 5
```

## proxyhandler/proxyhandler-getprototypeof

```js
const monster1 = {
  eyeCount: 4
};

const monsterPrototype = {
  eyeCount : 2
};

const handler = {
  getPrototypeOf(target) {
    return monsterPrototype;
  }
};

const proxy1 = new Proxy(monster1, handler);

console.log(Object.getPrototypeOf(proxy1) === monsterPrototype);
// expected output: true

console.log(Object.getPrototypeOf(proxy1).eyeCount);
// expected output: 2
```

## proxyhandler/proxyhandler-has

```js
const handler1 = {
  has (target, key) {
    if (key[0] === '_') {
      return false;
    }
    return key in target;
  }
};

const monster1 = {
  _secret: 'easily scared',
  eyeCount: 4
};

const proxy1 = new Proxy(monster1, handler1);
console.log('eyeCount' in proxy1);
// expected output: true

console.log('_secret' in proxy1);
// expected output: false

console.log('_secret' in monster1);
// expected output: true
```

## proxyhandler/proxyhandler-isextensible

```js
const monster1 = {
  canEvolve: true
};

const handler1 = {
  isExtensible(target) {
    return Reflect.isExtensible(target);
  },
  preventExtensions(target) {
    target.canEvolve = false;
    return Reflect.preventExtensions(target);
  }
};

const proxy1 = new Proxy(monster1, handler1);

console.log(Object.isExtensible(proxy1));
// expected output: true

console.log(monster1.canEvolve);
// expected output: true

Object.preventExtensions(proxy1);

console.log(Object.isExtensible(proxy1));
// expected output: false

console.log(monster1.canEvolve);
// expected output: false
```

## proxyhandler/proxyhandler-ownkeys

```js
const monster1 = {
  _age: 111,
  [Symbol('secret')]: 'I am scared!',
  eyeCount: 4
}

const handler1 = {
  ownKeys (target) {
    return Reflect.ownKeys(target)
  }
}

const proxy1 = new Proxy(monster1, handler1);

for (let key of Object.keys(proxy1)) {
  console.log(key);
  // expected output: "_age"
  // expected output: "eyeCount"
}
```

## proxyhandler/proxyhandler-preventextensions

```js
const monster1 = {
  canEvolve: true
};

const handler1 = {
  preventExtensions(target) {
    target.canEvolve = false;
    Object.preventExtensions(target);
    return true;
  }
};

const proxy1 = new Proxy(monster1, handler1);

console.log(monster1.canEvolve);
// expected output: true

Object.preventExtensions(proxy1);

console.log(monster1.canEvolve);
// expected output: false
```

## proxyhandler/proxyhandler-set

```js
function Monster() {
  this.eyeCount = 4;
}

const handler1 = {
  set(obj, prop, value) {
    if ((prop === 'eyeCount') && ((value % 2) !== 0)) {
      console.log('Monsters must have an even number of eyes');
    } else {
      return Reflect.set(...arguments);
    }
  }
};

const monster1 = new Monster();
const proxy1 = new Proxy(monster1, handler1);
proxy1.eyeCount = 1;
// expected output: "Monsters must have an even number of eyes"

console.log(proxy1.eyeCount);
// expected output: 4
```

## proxyhandler/proxyhandler-setprototypeof

```js
  const handler1 = {
  setPrototypeOf(monster1, monsterProto) {
    monster1.geneticallyModified = true;
    return false;
  }
};

const monsterProto = {};
const monster1 = {
  geneticallyModified : false
};

const proxy1 = new Proxy(monster1, handler1);
// Object.setPrototypeOf(proxy1, monsterProto); // throws a TypeError

console.log(Reflect.setPrototypeOf(proxy1, monsterProto));
// expected output: false

console.log(monster1.geneticallyModified);
// expected output: true
```

## reflect/reflect-apply

```js
console.log(Reflect.apply(Math.floor, undefined, [1.75]));
// expected output: 1

console.log(Reflect.apply(String.fromCharCode, undefined, [104, 101, 108, 108, 111]));
// expected output: "hello"

console.log(Reflect.apply(RegExp.prototype.exec, /ab/, ['confabulation']).index);
// expected output: 4

console.log(Reflect.apply(''.charAt, 'ponies', [3]));
// expected output: "i"
```

## reflect/reflect-construct

```js
function func1(a, b, c) {
  this.sum = a + b + c;
}

const args = [1, 2, 3];
const object1 = new func1(...args);
const object2 = Reflect.construct(func1, args);

console.log(object2.sum);
// expected output: 6

console.log(object1.sum);
// expected output: 6
```

## reflect/reflect-defineproperty

```js
const object1 = {};

if (Reflect.defineProperty(object1, 'property1', {value: 42})) {
  console.log('property1 created!');
  // expected output: "property1 created!"
} else {
  console.log('problem creating property1');
}

console.log(object1.property1);
// expected output: 42
```

## reflect/reflect-deleteproperty

```js
const object1 = {
  property1: 42
};

Reflect.deleteProperty(object1, 'property1');

console.log(object1.property1);
// expected output: undefined

var array1 = [1, 2, 3, 4, 5];
Reflect.deleteProperty(array1, '3');

console.log(array1);
// expected output: Array [1, 2, 3, , 5]
```

## reflect/reflect-get

```js
const object1 = {
  x: 1,
  y: 2
};

console.log(Reflect.get(object1, 'x'));
// expected output: 1

var array1 = ['zero', 'one'];

console.log(Reflect.get(array1, 1));
// expected output: "one"
```

## reflect/reflect-getownpropertydescriptor

```js
  const object1 = {
  property1: 42
};

console.log(Reflect.getOwnPropertyDescriptor(object1, 'property1').value);
// expected output: 42

console.log(Reflect.getOwnPropertyDescriptor(object1, 'property2'));
// expected output: undefined

console.log(Reflect.getOwnPropertyDescriptor(object1, 'property1').writable);
// expected output: true
```

## reflect/reflect-getprototypeof

```js
const object1 = {
  property1: 42
};

const proto1 = Reflect.getPrototypeOf(object1);

console.log(proto1);
// expected output: [object Object]

console.log(Reflect.getPrototypeOf(proto1));
// expected output: null
```

## reflect/reflect-has

```js
const object1 = {
  property1: 42
};

console.log(Reflect.has(object1, 'property1'));
// expected output: true

console.log(Reflect.has(object1, 'property2'));
// expected output: false

console.log(Reflect.has(object1, 'toString'));
// expected output: true
```

## reflect/reflect-isextensible

```js
const object1 = {};

console.log(Reflect.isExtensible(object1));
// expected output: true

Reflect.preventExtensions(object1);

console.log(Reflect.isExtensible(object1));
// expected output: false

const object2 = Object.seal({});

console.log(Reflect.isExtensible(object2));
// expected output: false
```

## reflect/reflect-ownkeys

```js
const object1 = {
  property1: 42,
  property2: 13
};

var array1 = [];

console.log(Reflect.ownKeys(object1));
// expected output: Array ["property1", "property2"]

console.log(Reflect.ownKeys(array1));
// expected output: Array ["length"]
```

## reflect/reflect-preventextensions

```js
var object1 = {};

console.log(Reflect.isExtensible(object1));
// expected output: true

Reflect.preventExtensions(object1);

console.log(Reflect.isExtensible(object1));
// expected output: false
```

## reflect/reflect-set

```js
const object1 = {};
Reflect.set(object1, 'property1', 42);

console.log(object1.property1);
// expected output: 42

const array1 = ['duck', 'duck', 'duck'];
Reflect.set(array1, 2, 'goose');

console.log(array1[2]);
// expected output: "goose"
```

## reflect/reflect-setprototypeof

```js
const object1 = {};

console.log(Reflect.setPrototypeOf(object1, Object.prototype));
// expected output: true

console.log(Reflect.setPrototypeOf(object1, null));
// expected output: true

const object2 = {};

console.log(Reflect.setPrototypeOf(Object.freeze(object2), null));
// expected output: false
```

## regexp/regexp-constructor

```js
var regex1 = /\w+/;
var regex2 = new RegExp('\\w+');

console.log(regex1);
// expected output: /\w+/

console.log(regex2);
// expected output: /\w+/

console.log(regex1 === regex2);
// expected output: false
```

## regexp/regexp-getregexp-@@species

```js
class MyRegExp extends RegExp {
  // Overwrite MyRegExp species to the parent RegExp constructor
  static get [Symbol.species]() {
    return RegExp;
  }
}

const regex1 = new MyRegExp('foo','g');

console.log(regex1.test('football'));
// expected output: true
```

## regexp/regexp-lastindex

```js
var regex1 = new RegExp( "foo", "g" );
var str1 = 'table football, foosball';

regex1.test(str1);

console.log(regex1.lastIndex);
// expected output: 9

regex1.test(str1);

console.log(regex1.lastIndex);
// expected output: 19
```

## regexp/regexp-prototype-@@match

```js
class RegExp1 extends RegExp {
  [Symbol.match](str) {
    var result = RegExp.prototype[Symbol.match].call(this, str);
    if (result) {
      return 'VALID';
    }
    return 'INVALID';
  }
}

console.log('2012-07-02'.match(new RegExp1('([0-9]+)-([0-9]+)-([0-9]+)')));
// expected output: "VALID"
```

## regexp/regexp-prototype-@@matchall

```js
class MyRegExp extends RegExp {
    [Symbol.matchAll](str) {
        let result = RegExp.prototype[Symbol.matchAll].call(this, str);
        if (!result) {
            return null;
        }
        return Array.from(result);
    }
}

let re = new MyRegExp('-[0-9]+', 'g');
console.log('2016-01-02|2019-03-07'.matchAll(re));
// expected output: Array [Array ["-01"], Array ["-02"], Array ["-03"], Array ["-07"]]
```

## regexp/regexp-prototype-@@replace

```js
class RegExp1 extends RegExp {
  [Symbol.replace](str) {
    return RegExp.prototype[Symbol.replace].call(this, str, '#!@?');
  }
}

console.log('football'.replace(new RegExp1('foo')));
// expected output: "#!@?tball"
```

## regexp/regexp-prototype-@@search

```js
class RegExp1 extends RegExp {
  constructor(str) {
    super(str)
    this.pattern = str;
  }
  [Symbol.search](str) {
    return str.indexOf(this.pattern);
  }
}

console.log('table football'.search(new RegExp1('foo')));
// expected output: 6
```

## regexp/regexp-prototype-@@split

```js
class RegExp1 extends RegExp {
  [Symbol.split](str, limit) {
    var result = RegExp.prototype[Symbol.split].call(this, str, limit);
    return result.map(x => "(" + x + ")");
  }
}

console.log('2016-01-02'.split(new RegExp1('-')));
// expected output: Array ["(2016)", "(01)", "(02)"]

console.log('2016-01-02'.split(new RegExp('-')));
// expected output: Array ["2016", "01", "02"]
```

## regexp/regexp-prototype-exec

```js
var regex1 = RegExp('foo*','g');
var str1 = 'table football, foosball';
var array1;

while ((array1 = regex1.exec(str1)) !== null) {
  console.log(`Found ${array1[0]}. Next starts at ${regex1.lastIndex}.`);
  // expected output: "Found foo. Next starts at 9."
  // expected output: "Found foo. Next starts at 19."
}
```

## regexp/regexp-prototype-flags

```js
// outputs RegExp flags in alphabetical order

console.log(/foo/ig.flags);
// expected output: "gi"

console.log(/bar/myu.flags);
// expected output: "muy"
```

## regexp/regexp-prototype-global

```js
var regex1 = new RegExp('foo', 'g');

console.log(regex1.global);
// expected output: true

var regex2 = new RegExp('bar', 'i');

console.log(regex2.global);
// expected output: false
```

## regexp/regexp-prototype-ignorecase

```js
var regex1 = new RegExp('foo');
var regex2 = new RegExp('foo', 'i');

console.log(regex1.test('Football'));
// expected output: false

console.log(regex2.ignoreCase);
// expected output: true

console.log(regex2.test('Football'));
// expected output: true
```

## regexp/regexp-prototype-multiline

```js
var regex1 = new RegExp('^football');
var regex2 = new RegExp('^football', 'm');

console.log(regex1.multiline);
// expected output: false

console.log(regex2.multiline);
// expected output: true

console.log(regex1.test('rugby\nfootball'));
// expected output: false

console.log(regex2.test('rugby\nfootball'));
// expected output: true
```

## regexp/regexp-prototype-source

```js
var regex1 = /fooBar/ig;

console.log(regex1.source);
// expected output: "fooBar"

console.log(new RegExp().source);
// expected output: "(?:)"

console.log(new RegExp('\n').source === '\\n');
// expected output: true (starting with ES5)
// (due to escaping)
```

## regexp/regexp-prototype-sticky

```js
var str1 = 'table football';
var regex1 = new RegExp('foo','y');

regex1.lastIndex = 6;

console.log(regex1.sticky);
// expected output: true

console.log(regex1.test(str1));
// expected output: true

console.log(regex1.test(str1));
// expected output: false
```

## regexp/regexp-prototype-test

```js
var str = 'table football';

var regex = RegExp('foo*');
var globalRegex = RegExp('foo*','g');

console.log(regex.test(str));
// expected output: true

console.log(regex.test(str));
// expected output: true

console.log(globalRegex.lastIndex);
// expected output: 0

console.log(globalRegex.test(str));
// expected output: true

console.log(globalRegex.lastIndex);
// expected output: 9

console.log(globalRegex.test(str));
// expected output: false
```

## regexp/regexp-prototype-tostring

```js
console.log(new RegExp('a+b+c'));
// expected output: /a+b+c/

console.log(new RegExp('a+b+c').toString());
// expected output: "/a+b+c/"

console.log(new RegExp('bar', 'g').toString());
// expected output: "/bar/g"

console.log(new RegExp('\n', 'g').toString());
// expected output (if your browser supports escaping): "/\n/g" 

console.log(new RegExp('\\n', 'g').toString());
// expected output: "/\n/g"
```

## regexp/regexp-prototype-unicode

```js
var regex1 = new RegExp('\u{61}');
var regex2 = new RegExp('\u{61}', 'u');

console.log(regex1.unicode);
// expected output: false

console.log(regex2.unicode);
// expected output: true

console.log(regex1.source);
// expected output: "a"

console.log(regex2.source);
// expected output: "a"
```

## set/set-prototype-@@iterator

```js
const set1 = new Set();

set1.add(42);
set1.add('forty two');

const iterator1 = set1[Symbol.iterator]();

console.log(iterator1.next().value);
// expected output: 42

console.log(iterator1.next().value);
// expected output: "forty two"
```

## set/set-prototype-add

```js
const set1 = new Set();

set1.add(42);
set1.add(42);
set1.add(13);

for (let item of set1) {
  console.log(item);
  // expected output: 42
  // expected output: 13
}
```

## set/set-prototype-clear

```js
const set1 = new Set();
set1.add(1);
set1.add('foo');

console.log(set1.size);
// expected output: 2

set1.clear();

console.log(set1.size);
// expected output: 0
```

## set/set-prototype-constructor

```js
const set1 = new Set([1, 2, 3, 4, 5]);

console.log(set1.has(1));
// expected output: true

console.log(set1.has(5));
// expected output: true

console.log(set1.has(6));
// expected output: false
```

## set/set-prototype-delete

```js
const set1 = new Set();
set1.add({x: 10, y: 20}).add({x: 20, y: 30});

// Delete any point with `x > 10`.
set1.forEach(function(point){
  if (point.x > 10) {
    set1.delete(point);
  }
});

console.log(set1.size);
// expected output: 1
```

## set/set-prototype-entries

```js
const set1 = new Set();
set1.add(42);
set1.add('forty two');

const iterator1 = set1.entries();

for (let entry of iterator1) {
  console.log(entry);
  // expected output: [42, 42]
  // expected output: ["forty two", "forty two"]
}
```

## set/set-prototype-foreach

```js
function logSetElements(value1, value2, set) {
  console.log('s[' + value1 + '] = ' + value2);
}

new Set(['foo', 'bar', undefined]).forEach(logSetElements);

// expected output: "s[foo] = foo"
// expected output: "s[bar] = bar"
// expected output: "s[undefined] = undefined"
```

## set/set-prototype-has

```js
const set1 = new Set([1, 2, 3, 4, 5]);

console.log(set1.has(1));
// expected output: true

console.log(set1.has(5));
// expected output: true

console.log(set1.has(6));
// expected output: false
```

## set/set-prototype-size

```js
const set1 = new Set();
var object1 = new Object();

set1.add(42);
set1.add('forty two');
set1.add('forty two');
set1.add(object1);

console.log(set1.size);
// expected output: 3
```

## set/set-prototype-values

```js
const set1 = new Set();
set1.add(42);
set1.add('forty two');

var iterator1 = set1.values();

console.log(iterator1.next().value);
// expected output: 42

console.log(iterator1.next().value);
// expected output: "forty two"
```

## sharedarraybuffer/sharedarraybuffer-bytelength

```js
// create a SharedArrayBuffer with a size in bytes
const buffer = new SharedArrayBuffer(8);

console.log(buffer.byteLength);
// expected output: 8
```

## sharedarraybuffer/sharedarraybuffer-constructor

```js
// create a SharedArrayBuffer with a size in bytes
const buffer = new SharedArrayBuffer(8);

console.log(buffer.byteLength);
// expected output: 8
```

## sharedarraybuffer/sharedarraybuffer-slice

```js
// create a SharedArrayBuffer with a size in bytes
const buffer = new SharedArrayBuffer(16);
const int32View = new Int32Array(buffer); // create the view
// produces Int32Array [0, 0, 0, 0]

int32View[1] = 42;
const sliced = new Int32Array(buffer.slice(4,12));

console.log(sliced);
// expected output: Int32Array [42, 0]
```

## statement/statement-async-for-in

```js
async function getFromList() {
  const url = 'https://www.random.org/decimal-fractions/?num=1&dec=10&col=1&format=plain&rnd=new';

  const arrayOfFetches = [
    doFetch(url),
    doFetch(url),
    doFetch(url)
  ];

  console.log('Regular iterator: promise objects are expected.');
  for (const item of arrayOfFetches) {
    console.log(item);
  }

  console.log('Async iterator: values from resolved promises are expected.');
  for await (const item of arrayOfFetches) {
    console.log(item);
  }
}

async function doFetch(url) {
  const response = await fetch(url);
  const text = await response.text();
  return Number(text);
}

getFromList();
```

## statement/statement-async-function-asterisk

```js
async function* randomNumbers() {
  const url = 'https://www.random.org/decimal-fractions/?num=1&dec=10&col=1&format=plain&rnd=new';

  console.log("Print randomly generated numbers until reset is clicked, or the random number exceeds 0.95");
  while (true) {
    const response = await fetch(url);
    const text = await response.text();
    yield Number(text);
  }
}

async function printRandoms() {
  for await (const number of randomNumbers()) {
    console.log(number);
    if (number > 0.95) { break; }
  }
}

printRandoms();
```

## statement/statement-async

```js
function resolveAfter2Seconds() {
  return new Promise(resolve => {
    setTimeout(() => {
      resolve('resolved');
    }, 2000);
  });
}

async function asyncCall() {
  console.log('calling');
  var result = await resolveAfter2Seconds();
  console.log(result);
  // expected output: 'resolved'
}

asyncCall();
```

## statement/statement-block

```js
var x = 1;
let y = 1;

if (true) {
  var x = 2;
  let y = 2;
}

console.log(x);
// expected output: 2

console.log(y);
// expected output: 1
```

## statement/statement-break

```js
var i = 0;

while (i < 6) {
  if (i === 3) {
    break;
  }
  i = i + 1;
}

console.log(i);
// expected output: 3
```

## statement/statement-class

```js
class Polygon {
  constructor(height, width) {
    this.area = height * width;
  }
}

console.log(new Polygon(4,3).area);
// expected output: 12
```

## statement/statement-const

```js
const number = 42;

try {
  number = 99;
} catch(err) {
  console.log(err);
  // expected output: TypeError: invalid assignment to const `number'
  // Note - error messages will vary depending on browser
}

console.log(number);
// expected output: 42
```

## statement/statement-continue

```js
var text = "";

for (var i = 0; i < 10; i++) {
  if (i === 3) {
    continue;
  }
  text = text + i;
}

console.log(text);
// expected output: "012456789"
```

## statement/statement-default

```js
var expr = 'Pears';
switch(expr) {
  case 'Oranges':
    console.log('Oranges are $0.59 a pound.');
  break;
  case 'Apples':
    console.log('Apples are $0.32 a pound.');
  break;
  default:
    console.log('Sorry, we are out of ' + expr + '.');
    // expected output: "Sorry, we are out of Pears."
}
```

## statement/statement-dowhile

```js
var result = "";
var i = 0;

do {
  i = i + 1;
  result = result + i;
} while (i < 5);

console.log(result);
// expected result: "12345"
```

## statement/statement-empty

```js
var array1 = [1, 2, 3];

// Assign all array values to 0
for (i = 0; i < array1.length; array1[i++] = 0) /* empty statement */ ;

console.log(array1);
// expected output: Array [0, 0, 0]
```

## statement/statement-for

```js
var str = "";

for (var i = 0; i < 9; i++) {
  str = str + i;
}

console.log(str);
// expected output: "012345678"
```

## statement/statement-forin

```js
const object = {a: 1, b: 2, c: 3};

for (const property in object) {
  console.log(`${property}: ${object[property]}`);
}

// expected output:
// "a: 1"
// "b: 2"
// "c: 3"
```

## statement/statement-forof

```js
const array1 = ['a', 'b', 'c'];

for (const element of array1) {
  console.log(element);
}

// expected output: "a"
// expected output: "b"
// expected output: "c"
```

## statement/statement-function

```js
function calcRectArea(width, height) {
  return width * height;
}

console.log(calcRectArea(5, 6));
// expected output: 30
```

## statement/statement-functionasterisk

```js
function* generator(i) {
  yield i;
  yield i + 10;
}

var gen = generator(10);

console.log(gen.next().value);
// expected output: 10

console.log(gen.next().value);
// expected output: 20
```

## statement/statement-ifelse

```js
function testNum(a) {
  if (a > 0) {
    return "positive";
  } else {
    return "NOT positive";
  }
}

console.log(testNum(-5));
// expected output: "NOT positive"
```

## statement/statement-label

```js
var str = "";

loop1:
for (var i = 0; i < 5; i++) {
  if (i === 1) {
    continue loop1;
  }
  str = str + i;
}

console.log(str);
// expected output: "0234"
```

## statement/statement-let

```js
let x = 1;

if (x === 1) {
  let x = 2;

  console.log(x);
  // expected output: 2
}

console.log(x);
// expected output: 1
```

## statement/statement-return

```js
function getRectArea(width, height) {
  if (width > 0 && height > 0) {
    return width * height;
  }
  return 0;
}

console.log(getRectArea(3, 4));
// expected output: 12

console.log(getRectArea(-3, 4));
// expected output: 0
```

## statement/statement-switch

```js
var expr = 'Papayas';
switch (expr) {
  case 'Oranges':
    console.log('Oranges are $0.59 a pound.');
    break;
  case 'Mangoes':
  case 'Papayas':
    console.log('Mangoes and papayas are $2.79 a pound.');
    // expected output: "Mangoes and papayas are $2.79 a pound."
    break;
  default:
    console.log('Sorry, we are out of ' + expr + '.');
}
```

## statement/statement-throw

```js
function getRectArea(width, height) {
  if (isNaN(width) || isNaN(height)) {
    throw "Parameter is not a number!";
  }
}

try {
  getRectArea(3, 'A');
}
catch(e) {
  console.error(e);
  // expected output: "Parameter is not a number!"
}
```

## statement/statement-trycatch

```js
try {
  nonExistentFunction();
}
catch(error) {
  console.error(error);
  // expected output: ReferenceError: nonExistentFunction is not defined
  // Note - error messages will vary depending on browser
}
```

## statement/statement-var

```js
var x = 1;

if (x === 1) {
  var x = 2;

  console.log(x);
  // expected output: 2
}

console.log(x);
// expected output: 2
```

## statement/statement-while

```js
var n = 0;

while (n < 3) {
  n++;
}

console.log(n);
// expected output: 3
```

## string/string-charat

```js
var sentence = 'The quick brown fox jumps over the lazy dog.';

var index = 4;

console.log('The character at index ' + index + ' is ' + sentence.charAt(index));
// expected output: "The character at index 4 is q"
```

## string/string-charcodeat

```js
var sentence = 'The quick brown fox jumps over the lazy dog.';

var index = 4;

console.log('The character code ' + sentence.charCodeAt(index) + ' is equal to ' + sentence.charAt(index));
// expected output: "The character code 113 is equal to q"
```

## string/string-codepointat

```js
var icons = '☃★♲';

console.log(icons.codePointAt(1));
// expected output: "9733"
```

## string/string-concat

```js
var str1 = 'Hello';
var str2 = 'World';

console.log(str1.concat(' ', str2));
// expected output: "Hello World"

console.log(str2.concat(', ', str1));
// expected output: "World, Hello"
```

## string/string-endswith

```js
const str1 = 'Cats are the best!';

console.log(str1.endsWith('best', 17));
// expected output: true

const str2 = 'Is this a question';

console.log(str2.endsWith('?'));
// expected output: false
```

## string/string-fromcharcode

```js
console.log(String.fromCharCode(189, 43, 190, 61));
// expected output: "½+¾="
```

## string/string-fromcodepoint

```js
console.log(String.fromCodePoint(65, 90, 48));
// expected output: "AZ0"
```

## string/string-includes

```js
var sentence = 'The quick brown fox jumps over the lazy dog.';

var word = 'fox';

console.log(`The word "${word}" ${sentence.includes(word)? 'is' : 'is not'} in the sentence`);
// expected output: "The word "fox" is in the sentence"
```

## string/string-indexof

```js
var paragraph = 'The quick brown fox jumps over the lazy dog. If the dog barked, was it really lazy?';

var searchTerm = 'dog';
var indexOfFirst = paragraph.indexOf(searchTerm);

console.log('The index of the first "' + searchTerm + '" from the beginning is ' + indexOfFirst);
// expected output: "The index of the first "dog" from the beginning is 40"

console.log('The index of the 2nd "' + searchTerm + '" is ' + paragraph.indexOf(searchTerm, (indexOfFirst + 1)));
// expected output: "The index of the 2nd "dog" is 52"
```

## string/string-iterator

```js
const str = 'The quick red fox jumped over the lazy dog\'s back.';

let iterator = str[Symbol.iterator]();
let theChar = iterator.next();

while(!theChar.done && theChar.value !== ' ') {
  console.log(theChar.value);
  theChar = iterator.next();
  // expected output: "T"
  //                  "h"
  //                  "e"
}  
```

## string/string-lastindexof

```js
var paragraph = 'The quick brown fox jumps over the lazy dog. If the dog barked, was it really lazy?';

var searchTerm = 'dog';

console.log('The index of the first "' + searchTerm + '" from the end is ' + paragraph.lastIndexOf(searchTerm));
// expected output: "The index of the first "dog" from the end is 52"
```

## string/string-length

```js
var str = 'Life, the universe and everything. Answer:';
  
console.log(str + ' ' + str.length);
// expected output: "Life, the universe and everything. Answer: 42"
```

## string/string-localecompare

```js
var a = 'réservé'; // with accents, lowercase
var b = 'RESERVE'; // no accents, uppercase

console.log(a.localeCompare(b));
// expected output: 1
console.log(a.localeCompare(b, 'en', {sensitivity: 'base'}));
// expected output: 0
```

## string/string-match

```js
var paragraph = 'The quick brown fox jumps over the lazy dog. It barked.';
var regex = /[A-Z]/g;
var found = paragraph.match(regex);

console.log(found);
// expected output: Array ["T", "I"]
```

## string/string-matchall

```js
let regexp = /t(e)(st(\d?))/g;
let str = 'test1test2';

let array = [...str.matchAll(regexp)];

console.log(array[0]);
// expected output: Array ["test1", "e", "st1", "1"]

console.log(array[1]);
// expected output: Array ["test2", "e", "st2", "2"]
```

## string/string-normalize

```js
var first = '\u212B';         // "Å"
var second = '\u0041\u030A';  // "Å"

console.log(first + ' and ' + second + ' are' +
   ((first === second)? '': ' not') + ' the same.');
   // expected output: "Å and Å are not the same."

console.log(first + ' and ' + second + ' can' +
   ((first.normalize('NFC') === second.normalize('NFC'))? '': ' not') + ' be normalized');
   // expected output: "Å and Å can be normalized"

var oldWord = 'mañana';
var newWord = oldWord.normalize('NFD');
console.log('The word did ' + ((oldWord != newWord)? '' : 'not ') + 'change.');
// expected output: "The word did change."
```

## string/string-padend

```js
const str1 = 'Breaded Mushrooms';

console.log(str1.padEnd(25, '.'));
// expected output: "Breaded Mushrooms........"

const str2 = '200';

console.log(str2.padEnd(5));
// expected output: "200  "
```

## string/string-padstart

```js
const str1 = '5';

console.log(str1.padStart(2, '0'));
// expected output: "05"

const fullNumber = '2034399002125581';
const last4Digits = fullNumber.slice(-4);
const maskedNumber = last4Digits.padStart(fullNumber.length, '*');

console.log(maskedNumber);
// expected output: "************5581"
```

## string/string-raw

```js
// Create a variable that uses a Windows
// path without escaping the backslashes:
const filePath = String.raw`C:\Development\profile\aboutme.html`;

console.log('The file was uploaded from: ' + filePath);
// expected output: "The file was uploaded from: C:\Development\profile\aboutme.html"
```

## string/string-repeat

```js
var chorus = 'Because I\'m happy. ';

console.log('Chorus lyrics for "Happy": ' + chorus.repeat(27));

// expected output: "Chorus lyrics for "Happy": Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. Because I'm happy. "
```

## string/string-replace

```js
var p = 'The quick brown fox jumps over the lazy dog. If the dog reacted, was it really lazy?';

var regex = /dog/gi;

console.log(p.replace(regex, 'ferret'));
// expected output: "The quick brown fox jumps over the lazy ferret. If the ferret reacted, was it really lazy?"

console.log(p.replace('dog', 'monkey'));
// expected output: "The quick brown fox jumps over the lazy monkey. If the dog reacted, was it really lazy?"
```

## string/string-search

```js
var paragraph = 'The quick brown fox jumps over the lazy dog. If the dog barked, was it really lazy?';

// any character that is not a word character or whitespace
var regex = /[^\w\s]/g;

console.log(paragraph.search(regex));
// expected output: 43

console.log(paragraph[paragraph.search(regex)]);
// expected output: "."
```

## string/string-slice

```js
var str = 'The quick brown fox jumps over the lazy dog.';

console.log(str.slice(31));
// expected output: "the lazy dog."

console.log(str.slice(4, 19));
// expected output: "quick brown fox"

console.log(str.slice(-4));
// expected output: "dog."

console.log(str.slice(-9, -5));
// expected output: "lazy"
```

## string/string-split

```js
var str = 'The quick brown fox jumps over the lazy dog.';

var words = str.split(' ');
console.log(words[3]);
// expected output: "fox"

var chars = str.split('');
console.log(chars[8]);
// expected output: "k"

var strCopy = str.split();
console.log(strCopy);
// expected output: Array ["The quick brown fox jumps over the lazy dog."]
```

## string/string-startswith

```js
const str1 = 'Saturday night plans';

console.log(str1.startsWith('Sat'));
// expected output: true

console.log(str1.startsWith('Sat', 3));
// expected output: false
```

## string/string-substr

```js
var str = 'Mozilla';

console.log(str.substr(1, 2));
// expected output: "oz"

console.log(str.substr(2));
// expected output: "zilla"
```

## string/string-substring

```js
var str = 'Mozilla';

console.log(str.substring(1, 3));
// expected output: "oz"

console.log(str.substring(2));
// expected output: "zilla"
```

## string/string-tolocalelowercase

```js
var dotted = 'İstanbul';

console.log('EN-US: ' + dotted.toLocaleLowerCase('en-US'));
// expected output: "i̇stanbul"

console.log('TR: ' + dotted.toLocaleLowerCase('tr'));
// expected output: "istanbul"
```

## string/string-tolocaleuppercase

```js
var city = 'istanbul';

console.log(city.toLocaleUpperCase('en-US'));
// expected output: "ISTANBUL"

console.log(city.toLocaleUpperCase('TR'));
// expected output: "İSTANBUL"
```

## string/string-tolowercase

```js
var sentence = 'The quick brown fox jumps over the lazy dog.';

console.log(sentence.toLowerCase());
// expected output: "the quick brown fox jumps over the lazy dog."
```

## string/string-tostring

```js
var stringObj = new String("foo");

console.log(stringObj);
// expected output: String { "foo" }

console.log(stringObj.toString());
// expected output: "foo"
```

## string/string-touppercase

```js
var sentence = 'The quick brown fox jumps over the lazy dog.';

console.log(sentence.toUpperCase());
// expected output: "THE QUICK BROWN FOX JUMPS OVER THE LAZY DOG."
```

## string/string-trim

```js
var greeting = '   Hello world!   ';

console.log(greeting);
// expected output: "   Hello world!   ";

console.log(greeting.trim());
// expected output: "Hello world!";
```

## string/string-trimend

```js
var greeting = '   Hello world!   ';

console.log(greeting);
// expected output: "   Hello world!   ";

console.log(greeting.trimEnd());
// expected output: "   Hello world!";
```

## string/string-trimstart

```js
var greeting = '   Hello world!   ';

console.log(greeting);
// expected output: "   Hello world!   ";

console.log(greeting.trimStart());
// expected output: "Hello world!   ";
```

## string/string-valueof

```js
var stringObj = new String("foo");

console.log(stringObj);
// expected output: String { "foo" }

console.log(stringObj.valueOf());
// expected output: "foo"
```

## symbol/symbol-constructor

```js
const symbol1 = Symbol();
const symbol2 = Symbol(42);
const symbol3 = Symbol('foo');

console.log(typeof symbol1);
// expected output: "symbol"

console.log(symbol3.toString());
// expected output: "Symbol(foo)"

console.log(Symbol('foo') === Symbol('foo'));
// expected output: false
```

## symbol/symbol-for

```js
console.log(Symbol.for('bar') === Symbol.for('bar'));
// expected output: true

console.log(Symbol('bar') === Symbol('bar'));
// expected output: false

const symbol1 = Symbol.for('foo');

console.log(symbol1.toString());
// expected output: "Symbol(foo)"
```

## symbol/symbol-hasinstance

```js
class Array1 {
  static [Symbol.hasInstance](instance) {
    return Array.isArray(instance);
  }
}

console.log([] instanceof Array1);
// expected output: true
```

## symbol/symbol-isconcatspreadable

```js
const alpha = ['a', 'b', 'c'];
const numeric = [1, 2, 3];
let alphaNumeric = alpha.concat(numeric);

console.log(alphaNumeric);
// expected output: Array ["a", "b", "c", 1, 2, 3]

numeric[Symbol.isConcatSpreadable] = false;
alphaNumeric = alpha.concat(numeric);

console.log(alphaNumeric);
// expected output: Array ["a", "b", "c", Array [1, 2, 3]]
```

## symbol/symbol-iterator

```js
const iterable1 = new Object();

iterable1[Symbol.iterator] = function* () {
  yield 1;
  yield 2;
  yield 3;
};

console.log([...iterable1]);
// expected output: Array [1, 2, 3]
```

## symbol/symbol-keyfor

```js
const globalSym = Symbol.for('foo'); // global symbol

console.log(Symbol.keyFor(globalSym));
// expected output: "foo"

const localSym = Symbol(); // local symbol

console.log(Symbol.keyFor(localSym));
// expected output: undefined

console.log(Symbol.keyFor(Symbol.iterator));
// expected output: undefined
```

## symbol/symbol-match

```js
const regexp1 = /foo/;
// console.log('/foo/'.startsWith(regexp1));
// expected output: (Chrome) Error: First argument to String.prototype.startsWith must not be a regular expression
// expected output: (Firefox) Error: Invalid type: first can't be a Regular Expression

regexp1[Symbol.match] = false;

console.log('/foo/'.startsWith(regexp1));
// expected output: true

console.log('/baz/'.endsWith(regexp1));
// expected output: false
```

## symbol/symbol-matchall

```js
let re = /[0-9]+/g;
let str = '2016-01-02|2019-03-07';
let result = re[Symbol.matchAll](str);

console.log(Array.from(result, x => x[0]));
// expected output: Array ["2016", "01", "02", "2019", "03", "07"]
```

## symbol/symbol-prototype-description

```js
console.log(Symbol('desc').description);
// expected output: "desc"

console.log(Symbol.iterator.description);
// expected output: "Symbol.iterator"

console.log(Symbol.for('foo').description);
// expected output: "foo"

console.log(Symbol('foo').description + 'bar');
// expected output: "foobar"
```

## symbol/symbol-prototype-tostring

```js
console.log(Symbol('desc').toString());
// expected output: "Symbol(desc)"

console.log(Symbol.iterator.toString());
// expected output: "Symbol(Symbol.iterator)

console.log(Symbol.for('foo').toString());
// expected output: "Symbol(foo)"

// console.log(Symbol('foo') + 'bar');
// expected output: Error: Can't convert symbol to string
```

## symbol/symbol-prototype

```js
Symbol.prototype.toString = function() {
  return ('SYMBOL');
}

var symbol1 = Symbol('foo');

console.log(symbol1.toString());
// expected output: "SYMBOL"
```

## symbol/symbol-replace

```js
class Replace1 {
  constructor(value) {
    this.value = value;
  }
  [Symbol.replace](string) {
    return `s/${string}/${this.value}/g`;
  }
}

console.log('foo'.replace(new Replace1('bar')));
// expected output: "s/foo/bar/g"
```

## symbol/symbol-search

```js
class Search1 {
  constructor(value) {
    this.value = value;
  }
  [Symbol.search](string) {
    return string.indexOf(this.value);
  }
}

console.log('foobar'.search(new Search1('bar')));
// expected output: 3
```

## symbol/symbol-species

```js
class Array1 extends Array {
  static get [Symbol.species]() { return Array; }
}

const a = new Array1(1, 2, 3);
const mapped = a.map(x => x * x);

console.log(mapped instanceof Array1);
// expected output: false

console.log(mapped instanceof Array);
// expected output: true
```

## symbol/symbol-split

```js
class Split1 {
  constructor(value) {
    this.value = value;
  }
  [Symbol.split](string) {
    var index = string.indexOf(this.value);
    return this.value + string.substr(0, index) + "/"
      + string.substr(index + this.value.length);
  }
}

console.log('foobar'.split(new Split1('foo')));
// expected output: "foo/bar"
```

## symbol/symbol-toprimitive

```js
const object1 = {
  [Symbol.toPrimitive](hint) {
    if (hint == 'number') {
      return 42;
    }
    return null;
  }
};

console.log(+object1);
// expected output: 42
```

## symbol/symbol-tostringtag

```js
class ValidatorClass {
  get [Symbol.toStringTag]() {
    return 'Validator';
  }
}

console.log(Object.prototype.toString.call(new ValidatorClass()));
// expected output: "[object Validator]"
```

## symbol/symbol-unscopables

```js
const object1 = {
  property1: 42
};

object1[Symbol.unscopables] = {
  property1: true
};

with (object1) {
  console.log(property1);
  // expected output: Error: property1 is not defined
}
```

## typedarray/typedarray-buffer

```js
// create an ArrayBuffer with a size in bytes
const buffer = new ArrayBuffer(8);
const uint16 = new Uint16Array(buffer);

console.log(uint16.buffer.byteLength);
// expected output: 8
```

## typedarray/typedarray-bytelength

```js
// create an ArrayBuffer with a size in bytes
const buffer = new ArrayBuffer(8);
const uint8 = new Uint8Array(buffer, 2);

console.log (uint8.byteLength);
// expected output: 6
```

## typedarray/typedarray-bytes-per-element

```js
console.log(Float64Array.BYTES_PER_ELEMENT);
// expected output: 8

console.log(Int8Array.BYTES_PER_ELEMENT);
// expected output: 1
```

## typedarray/typedarray-constructor

```js
// create a TypedArray with a size in bytes
const typedArray1 = new Int8Array(8);
typedArray1[0] = 32;

const typedArray2 = new Int8Array(typedArray1);
typedArray2[1] = 42;

console.log(typedArray1);
// expected output: Int8Array [32, 0, 0, 0, 0, 0, 0, 0]

console.log(typedArray2);
// expected output: Int8Array [32, 42, 0, 0, 0, 0, 0, 0]
```

## typedarray/typedarray-copywithin

```js
const uint8 = new Uint8Array([ 1, 2, 3, 4, 5, 6, 7, 8 ]);

// (insert position, start position, end position)
uint8.copyWithin(3, 1, 3);

console.log(uint8);
// expected output: Uint8Array [1, 2, 3, 2, 3, 6, 7, 8]
```

## typedarray/typedarray-entries

```js
const uint8 = new Uint8Array([10, 20, 30, 40, 50]);
eArr = uint8.entries();

eArr.next();
eArr.next();

console.log(eArr.next().value);
// expected output: Array [2, 30]
```

## typedarray/typedarray-every

```js
function isNegative(element, index, array) {
  return element < 0;
}

const int8 = new Int8Array([-10, -20, -30, -40, -50]);

console.log(int8.every(isNegative));
// expected output: true
```

## typedarray/typedarray-fill

```js
const uint8 = new Uint8Array([0, 0, 0, 0]);
// (value, start position, end position);
uint8.fill(4, 1, 3);

console.log(uint8);
// expected output: Uint8Array [0, 4, 4, 0]
```

## typedarray/typedarray-filter

```js
function isNegative(element, index, array) {
  return element < 0;
}

const int8 = new Int8Array([-10, 20, -30, 40, -50]);
const negInt8 = int8.filter(isNegative);

console.log(negInt8);
// expected output: Int8Array [-10, -30, -50]
```

## typedarray/typedarray-find

```js
function isNegative(element, index, array) {
  return element < 0;
}

const int8 = new Int8Array([10, 0, -10, 20, -30, 40, -50]);

console.log(int8.find(isNegative));
// expected output: -10
```

## typedarray/typedarray-findindex

```js
function isNegative(element, index, array) {
  return element < 0;
}

const int8 = new Int8Array([10, -20, 30, -40, 50]);

console.log(int8.findIndex(isNegative));
// expected output: 1
```

## typedarray/typedarray-from

```js
let uint16 = new Int16Array;
uint16 = Int16Array.from('12345');

console.log(uint16);
// expected output: Int16Array [1, 2, 3, 4, 5]
```

## typedarray/typedarray-includes

```js
const uint8 = new Uint8Array([10, 20, 30, 40, 50]);

console.log(uint8.includes(20));
// expected output: true

// check from position 3
console.log(uint8.includes(20, 3));
// expected output: false
```

## typedarray/typedarray-indexof

```js
const uint8 = new Uint8Array([10, 20, 30, 40, 50]);

console.log(uint8.indexOf(50));
// expected output: 4

// from position 3
console.log(uint8.indexOf(20, 3));
// expected output: -1

console.log(uint8.indexOf(51));
// expected output: -1
```

## typedarray/typedarray-join

```js
const uint8 = new Uint8Array([10, 20, 30, 40, 50]);

console.log(uint8.join());
// expected output: "10,20,30,40,50"

console.log(uint8.join(''));
// expected output: "1020304050"

console.log(uint8.join('-'));
// expected output: "10-20-30-40-50"
```

## typedarray/typedarray-keys

```js
const uint8 = new Uint8Array([10, 20, 30, 40, 50]);
const keys = uint8.keys();

keys.next();
keys.next();

console.log(keys.next().value);
// expected output: 2
```

## typedarray/typedarray-lastindexof

```js
const uint8 = new Uint8Array([10, 20, 50, 50, 50, 60]);

console.log(uint8.lastIndexOf(50, 5));
// expected output: 4

console.log(uint8.lastIndexOf(50, 3));
// expected output: 3
```

## typedarray/typedarray-length

```js
// create an ArrayBuffer with a size in bytes
const buffer = new ArrayBuffer(8);
const uint8 = new Uint8Array(buffer, 2);

console.log (uint8.length);
// expected output: 6
```

## typedarray/typedarray-map

```js
const uint8 = new Uint8Array([25, 36, 49]);
const roots = uint8.map(Math.sqrt);

console.log(roots);
// expected output: Uint8Array [5, 6, 7]
```

## typedarray/typedarray-name

```js
console.log(Uint8Array.name);
// expected output: "Uint8Array"

console.log(Float32Array.name);
// expected output: "Float32Array"
```

## typedarray/typedarray-of

```js
let uint16 = new Int16Array;
uint16 = Int16Array.of('10', '20', '30', '40' ,'50');

console.log(uint16);
// expected output: Int16Array [10, 20, 30, 40, 50]
```

## typedarray/typedarray-reduce

```js
const uint8 = new Uint8Array([0, 1, 2, 3]);

function sum(previousValue, currentValue) {
  return previousValue + currentValue;
}

console.log(uint8.reduce(sum));
// expected output: 6
```

## typedarray/typedarray-reverse

```js
const uint8 = new Uint8Array([1, 2, 3]);
uint8.reverse();

console.log(uint8);
// expected output: Uint8Array [3, 2, 1]
```

## typedarray/typedarray-set

```js
// create an ArrayBuffer with a size in bytes
const buffer = new ArrayBuffer(8);
const uint8 = new Uint8Array(buffer);

// Copy the values into the array starting at index 3
uint8.set([1, 2, 3], 3);

console.log(uint8);
// expected output: Uint8Array [0, 0, 0, 1, 2, 3, 0, 0]
```

## typedarray/typedarray-slice

```js
const uint8 = new Uint8Array([10, 20, 30, 40, 50]);
const array1 = uint8.slice(1, 3);

console.log(array1);
// expected output: Uint8Array [20, 30]
```

## typedarray/typedarray-some

```js
function isNegative(element, index, array) {
  return element < 0;
}

const int8 = new Int8Array([-10, 20, -30, 40, -50]);
const positives = new Int8Array([10, 20, 30, 40, 50]);

console.log(int8.some(isNegative));
// expected output: true

console.log(positives.some(isNegative));
// expected output: false
```

## typedarray/typedarray-sort

```js
const uint8 = new Uint8Array([40, 10, 50, 20, 30]);
uint8.sort();

console.log(uint8);
// expected output: Uint8Array [10, 20, 30, 40, 50]
```

## typedarray/typedarray-subarray

```js
const uint8 = new Uint8Array([10, 20, 30, 40, 50]);

console.log(uint8.subarray(1, 3));
// expected output: Uint8Array [20, 30]

console.log(uint8.subarray(1));
// expected output: Uint8Array [20, 30, 40, 50]
```

## typedarray/typedarray-tostring

```js
const uint8 = new Uint8Array([10, 20, 30, 40, 50]);

const uint8String = uint8.toString();

console.log(uint8String.startsWith('10'));
// expected output: true
```

## typedarray/typedarray-values

```js
const uint8 = new Uint8Array([ 10, 20, 30, 40, 50]);
const array1 = uint8.values();

array1.next();
array1.next();

console.log(array1.next().value); 
// expected output: 30
```

## weakmap/weakmap-prototype-delete

```js
const weakmap1 = new WeakMap();
const object1 = {};

weakmap1.set(object1, 42);

console.log(weakmap1.delete(object1));
// expected output: true

console.log(weakmap1.has(object1));
// expected output: false
```

## weakmap/weakmap-prototype-get

```js
const weakmap1 = new WeakMap();
const object1 = {};
const object2 = {};

weakmap1.set(object1, 42);

console.log(weakmap1.get(object1));
// expected output: 42

console.log(weakmap1.get(object2));
// expected output: undefined
```

## weakmap/weakmap-prototype-has

```js
const weakmap1 = new WeakMap();
const object1 = {};
const object2 = {};

weakmap1.set(object1, 'foo');

console.log(weakmap1.has(object1));
// expected output: true

console.log(weakmap1.has(object2));
// expected output: false
```

## weakmap/weakmap-prototype-set

```js
const weakmap1 = new WeakMap();
const object1 = {};
const object2 = {};

weakmap1.set(object1, 'foo');
weakmap1.set(object2, 'bar');

console.log(weakmap1.get(object1));
//expected output: "foo"

console.log(weakmap1.get(object2));
//expected output: "bar"
```

## weakset/weakset-prototype-add

```js
const weakset1 = new WeakSet();
const object1 = {};

weakset1.add(object1);
console.log(weakset1.has(object1));
// expected output: true

try {
  weakset1.add(1);
} catch(error) {
  console.log(error);
  // expected output: "Error: Invalid value used in weak set" in Chrome
  // expected output: "TypeError: WeakSet value must be an object, got the number 1" in Firefox
}
```

## weakset/weakset-prototype-delete

```js
const weakset1 = new WeakSet();
const object1 = {};

weakset1.add(object1);

console.log(weakset1.has(object1));
// expected output: true

weakset1.delete(object1);

console.log(weakset1.has(object1));
// expected output: false
```

## weakset/weakset-prototype-has

```js
const weakset1 = new WeakSet();
const object1 = {};
const object2 = {};

weakset1.add(object1);

console.log(weakset1.has(object1));
// expected output: true

console.log(weakset1.has(object2));
// expected output: false
```
