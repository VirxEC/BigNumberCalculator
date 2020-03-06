## Navigation
<a href="https://www.virxcase.ga">VirxEC Showcase</a><br>
<a href="https://www.virxcase.ga/CP-P">Preview CalcPlus ES6</a><br>
<a href="https://www.virxcase.ga/CP-S">CalcPlus Source Code</a><br>
<a href="https://repl.it/github/VirxEC/CalcPlus">Test latest Node.js version on Repl.it</a>

## What is ES6?
Whenever ES6 is mentioned, Module JavaScript is what's acutally being talked about. If you don't know what ModuleJS is, you can read about it <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules">here</a>.

If you want to ever write in ES6, then just do this: `<script type="module">/*ModuleJS here*/</script>`. ES6 is currently unsupported in Internet Explorer (big surprise there) but it has been support for a long time in Chrome, Edge, Firefox, Opera, and Safari.


## About

This is a ES6 Library that let's numbers be calculated up to:

  64 bit OS: 2<sup>64</sup>-1 digits <i><b>long</b></i>, or 10<sup>(2<sup>64</sup>-1)</sup>-1.
  
  32 bit OS: 2<sup>32</sup>-1 digits <i><b>long</b></i>, or 10<sup>(2<sup>32</sup>-1)</sup>-1.

Please note that the ES6 version of this Library is extremely RAM efficient. Only about 100 megabytes of free RAM is required for the heaviest of tasks (measured by doing 10<sup>2<sup>64</sup></sup> and leaving it for 2 days with no threshold). The speed of your RAM may also limit the speed of the program, but the biggest bottleneck (for speed) is most often going to be your CPU. This is a change from built-in systems in programming languages, which hog tons of RAM but are very CPU efficient.

It is planned that once the ES6 version is done, it will be ported to be a Python 3 Library.

Want to see this library in action? Just go [here](https://www.virxcase.ga/Pages/CP-P)!

## Advantages of using this library
Normally, you can only calculate numbers on a 64-bit OS as long as the final result is less than 18,446,744,073,709,551,616. (4,294,967,296 for a 32-bit OS.) Or, if your language supports using more RAM to calculate huge numbers without losing precision, (like Python,) then the max number is 10<sup>custom_max_integer</sup>-1.

In most modern languages, when you go over the limit (we're using a 64-bit OS as an example) it just starts to lose it's precision. For example, to it, 18,446,744,073,709,551,621,573 is just 18,446,744,073,709,551,620,000. That's not the case with this library. Now, you might work in some languages like Python where your language is magically able to calculate huge numbers in an instant without losing precision. However, these languages are tricking you: the larger the number gets, the more RAM it takes. With JavaScript, this hasn't been implemented yet, so this program is still extremely viable. However, even when this comes to JavaScript, it won't matter. There's a feature in CalcPlus that lets you set a threshold. Above x number, the library will kick in, saving your RAM & instead of using your CPU. Don't worry, though - If you're using a high threshold and you do something like 10<sup>2<sup>64</sup></sup>, it won't have to start from the beginning. It will instantly calculate 2<sup>64</sup> with the language (using a bit of RAM) and from there multiply 18,446,744,073,709,551,616 by itself ten times (because it's faster than multiplying ten by itself 18,446,744,073,709,551,616 times, and 2<sup>4</sup> = 4<sup>2</sup>.) If your threshold is double 2<sup>64</sup>, or 2<sup>65</sup>, then it will multiply 18,446,744,073,709,551,616 by 18,446,744,073,709,551,616 and then the algorithm will kick in - even then, the threshold will continue to speed up the process, but it's a little more complicated and I don't feel like explaining. In short, in languages that increase the max number by using up more RAM, setting the threshold is like striking the perfect balance between how much RAM you want to use, and letting the CPU take over for the missing RAM that's needed.

## How does CalcPlus work?
In short, it does basic function like addition & subtraction like a human would - breaking it down, solving it column by column:
<pre>
  302
+ 138
-----
  420
</pre>

And from there, multiplication is just repeated addition, division is just repeated subtraction, exponents are just repeated multiplication and that kind of thing. Of course, this is very inefficient, so there are a number of optimizations to vastly speed up the process. Weak computers can instantaneously calculate 2<sup>256</sup>, which is 115792089237316195423570985008687907853269984665640564039457584007913129639936.

## What coding languages does CalcPlus support?
For now, it only supports ES6/NodeJS. I have plans to eventually port it to Python 3, and then from there who knows where.

## How can I install CalcPlus?

ES6 JavaScript Library:<br>
&nbsp;&nbsp;<a href="https://github.com/VirxEC/CalcPlus/releases">Download latest beta</a><br>
&nbsp;&nbsp;<a href="https://www.virxcase.ga/CalcPlus/CalcPlus.js" download="CalcPlus_ALPHA_ES6.js">Download latest alpha</a><br>
&nbsp;&nbsp;`<script type="module">import * as calcplus from "https://www.virxcase.ga/CalcPlus/bin/calcplus.js"; /*Import latest alpha*/</script>`

NodeJS Library:<br>
&nbsp;&nbsp;`npm install @virxec/calcplus@0.4.3`

## What's the larget number CalcPlus can understand, written out?

I can't put it here. It's WAY to big. If you want to get an idea of just how big it is, go to the [one million digits of pi page](https://www.piday.org/million/) and try to get to the bottom. Then multiply the length of that page by trillions of trillions of times. That's why it can't be here, it's just a really damn big number.

## Contact me!
  Visit meh [discord](https://discord.gg/538CZWf)
  
  Email: <a href="mailto:virx@virxcase.ga">virx@virxcase.ga</a>
  
  Or just leave a question in the issues tab, each will get about the same response time.
  
  I'm in the EST timezone.
