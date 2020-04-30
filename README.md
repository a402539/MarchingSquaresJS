## Пример для [Бориса](https://OriginalSin.github.io/MarchingSquaresJS/boris.html) с изображением

## Пример [Бориса](https://a402539.github.io/MarchingSquaresJS/boris.html) с ромбом и овалом

Пример с ромбом и овалом работает неправильно, т.к. алгоритм рассчитан на работу с каналом Alpha, причем фоном считается нулевое значние, картинкой - ненулевое,
но файл содержит данные и каналов RGB:

<<<<<<< HEAD
<img src="4.png"></img>
=======
<<<<<<< HEAD
<img id="img1" src="4.png"></img>
=======
<!--
<img id="img1" src="4.png"></img>
>>>>>>> 4d79a63470a0d02080428d71b714778e656ee8dd
>>>>>>> 386ac73e4bbeee8993c5054f44bbf81a7f5bf483
ar=context.getImageData(0, y, canvas.width, canvas.height).data;
ap={};
{}
for(i=0;i<ar.length;i+=4){if (ap.hasOwnProperty([ar[i],ar[i+1],ar[i+2],ar[i+3]])) ap[[ar[i],ar[i+1],ar[i+2],ar[i+3]]]++; else ap[[ar[i],ar[i+1],ar[i+2],ar[i+3]]]=1;};
ap
{0,0,0,0: 766, 255,255,255,255: 28935, 255,242,0,255: 2212, 255,174,201,255: 853}
<<<<<<< HEAD
=======
<<<<<<< HEAD
>>>>>>> 386ac73e4bbeee8993c5054f44bbf81a7f5bf483
Здесь нулевые точки 0,0,0,0 добавляет алгоритм по краям,
точки 255,255,255,255 - это фон
точки 255,242,0,255 - ромб
точки 255,174,201,255 - овал
<<<<<<< HEAD
=======
=======
-->
>>>>>>> 4d79a63470a0d02080428d71b714778e656ee8dd
>>>>>>> 386ac73e4bbeee8993c5054f44bbf81a7f5bf483

Проверим скан из картографии

<!--<img id="img1" src="993hole.png"></img>-->


## Optimized implementation of the [Marching Squares](http://users.polytech.unice.fr/~lingrand/MarchingCubes/algo.html) algorithm in Javascript

![canvas](https://cloud.githubusercontent.com/assets/8630763/18348811/e2d33b10-75cd-11e6-8131-9d57140d5508.png)

Computation times for 20 iterations:

|            | old  | new | optimized |
|------------|------|-----|-----|
| time in ms | 3876 | 443 | 20  |
| time in %  | 873  | 100 | **4**   |

The optimized version is approximately 217 times faster than the "old version" and **24 times faster** than the "new version" implemented by [sakri](https://github.com/sakri).

[ES2015](http://www.ecma-international.org/ecma-262/6.0/) [features](https://kangax.github.io/compat-table/es6/) like TypedArrays, const and local scoping are used to gain this speed up.

Test it yourself with this online [benchmark / demo](http://htmlpreview.github.io/?https://github.com/mamrehn/MarchingSquaresJS/blob/master/marchingSquaresTest.html).

## Original README

Marching squares outlines blobs of non-transparent pixels inside a bitmap.

This is a straight forward port from this excellent implementation by Phill Spiess:

http://devblog.phillipspiess.com/2010/02/23/better-know-an-algorithm-1-marching-squares/

This is a Javascript implementation designed to be used with Html5 Canvas.

Check out the code in marchingSquaresTest.html for usage example.

http://htmlpreview.github.io/?https://github.com/sakri/MarchingSquaresJS/blob/master/marchingSquaresTest.html


Here's a few codepen demos using it:

A visualization of the algo as it executes
http://codepen.io/sakri/full/aIirl

Text Edge Flare
http://codepen.io/sakri/full/vIKJp

Ghost text
http://codepen.io/sakri/full/zbqti

He-Man effect
http://codepen.io/sakri/full/wsiLC


Here's a demo that tackles "blobs with holes" as in getting the outline for characters such as "O" "8" "&" etc.
http://codepen.io/sakri/pen/LCrDe

If there is interest, I can include the required code in this repo (floodFill, basic threshold etc.)



Have a good day!
