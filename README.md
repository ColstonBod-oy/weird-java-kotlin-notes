<div id="top"></div>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![GitHub][github-shield]][github-url]&ensp;
[![Twitter][twitter-shield]][twitter-url]&ensp;
[![Reddit][reddit-shield]][reddit-url]&ensp;



<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/othneildrew/Best-README-Template">
    <img src="images/logo.png" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">Functional Java Snippets</h3>

  <p align="center">
    My lifelong snippets about the functional interfaces 🤖⚙️ and stream API 🧵 features of Java 8 onwards!
    <br />
    <a href="https://docs.oracle.com/en/java/"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://java-8-tips.readthedocs.io/en/stable/quickintro.html">Stream API Docs</a>
    ·
    <a href="https://philvarner.github.io/pages/modern-java.html">Java 8 Cheat Sheet</a>
    ·
    <a href="https://www.logicbig.com/tutorials/core-java-tutorial/java-util-stream/stream-cheat-sheet.html">Stream API Cheat Sheet</a>
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#readme-template">README Template</a></li>
      </ul>
    </li>
    <li>
      <a href="#get-an-array-of-maps-keys">Get An Array Of Map's Keys</a>
      <ul>
        <li><a href="#2a-snippets">Snippets</a></li>
        <li><a href="#2b-explanation">Explanation</a></li>
      </ul>
    </li>
    <li>
      <a href="#immediately-invoked-function-expression">Immediately Invoked Function Expression</a>
      <ul>
        <li><a href="#3a-examples">Examples</a></li>
        <li><a href="#3b-practical-uses">Practical Uses</a></li>
      </ul>
    </li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

![Banner][java-logo]

Hello! my name is Colston D. Bod-oy, I'm a React developer and would be taking my 3rd year of college on the time that I made this repo. I'm an aspiring developer and I would like to work for the big FAANG companies someday 😉.  
  
I created this project so I could keep track and recall snippets about Java's functional interfaces and stream API as I've just recently started learning it, hope you'll find these notes useful! 😎.


### README Template

Here's where I got this template btw, also don't forget to follow me on my social media links.

👉 [📒](https://github.com/othneildrew/Best-README-Template)

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- GET AN ARRAY OF MAPS KEYS -->
## Get An Array Of Map's Keys 

This is a snippet I found on [Stack Overflow](https://stackoverflow.com/questions/39891112/get-an-array-from-a-map-and-convert-the-keys) which converts a set of map keys into an array.

### 2a Snippets

  ```java
  import java.util.Arrays;
  import java.util.HashMap;

  class Main {
    public static void main(String[] args) {
      HashMap<String, Integer> stringsMap = new HashMap<>();
      stringsMap.put("!V$q", 16087526);
      stringsMap.put("lW@$", 64992058);
      stringsMap.put("V*tx", 61656601);
      stringsMap.put("W*Ru", 77778805);
      stringsMap.put("b#Oo", 44708273);
    
      HashMap<Integer, String> integersMap = new HashMap<>();
      integersMap.put(16087526, "!V$q");
      integersMap.put(64992058, "lW@$");
      integersMap.put(61656601, "V*tx");
      integersMap.put(77778805, "W*Ru");
      integersMap.put(44708273, "b#Oo");
    
      HashMap<String, String> strNumsMap = new HashMap<>();
      strNumsMap.put("16087526", "!V$q");
      strNumsMap.put("64992058", "lW@$");
      strNumsMap.put("61656601", "V*tx");
      strNumsMap.put("77778805", "W*Ru");
      strNumsMap.put("44708273", "b#Oo");
    
      System.out.println(Arrays.toString(stringsMap.keySet().stream().toArray()));  
      // [!V$q, b#Oo, lW@$, W*Ru, V*tx]
      
      System.out.println(Arrays.toString(integersMap.keySet().stream().mapToInt(Integer::intValue).toArray()));  
      // [16087526, 64992058, 61656601, 77778805, 44708273]
      
      System.out.println(Arrays.toString(strNumsMap.keySet().stream().mapToInt(Integer::parseInt).toArray())); 
      // [61656601, 44708273, 77778805, 64992058, 16087526]
    }
  }
  ```

### 2b Practical Uses

_Below is a basic example of how we could use this feature when working with React's useReducer hook._

  ```js
  const initialState = {
    username: "",
    password: "",
  }
  
  export default function LoginForm() {
    const [state, dispatch] = useReducer((state, action) => {
      switch (action.type) {
        case "TEXT_FIELD":
          // Decoupling fieldType property from dispatch
          return { ...state, [action.fieldType]: action.payload }; 
        default:
          return state;
      }
    }, initialState);
    
    const { username, password } = state;
    
    return (
      <div className="App">
        <form className="form">
          <p>Please Login!</p>
          <input 
            type="text" 
            value={username} 
            onChange={(e) => 
              dispatch({ 
                type: "TEXT_FIELD", 
                fieldType: "username", 
                payload: e.currentTarget.value, 
              })
            }
          />
          <input 
            type="password" 
            value={password} 
            onChange={(e) => 
              dispatch({ 
                type: "TEXT_FIELD", 
                fieldType: "password", 
                payload: e.currentTarget.value, 
              })
            }
          />
        </form>
      </div>
    );
  }
  ```

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- IMMEDIATELY INVOKED FUNCTION EXPRESSION -->
## Immediately Invoked Function Expression 

We can create and call a function expression at the same time.

### 3a Examples

_Notice the different ways we can create an IIFE. For an IIFE to work, we first needed to change the context of the function keyword to be an expression either by enclosing it inside parentheses or using operators. Note that the ! operator will negate the returned boolean value of the IIFE and if the expression doesn't return anything, it would just result to true, while the + operator will try to add the returned value but since it would always have no value on the left-hand side of the operator, no further actions would be executed._

  ```js
  var functionEx;
  (functionEx = function() {
    console.log("✔️")
  })(); // ✔️

  (function() {
    console.log("✔️")
  })(); // ✔️

  !function() {
    console.log("✔️")
  }(); // ✔️

  +function() {
    console.log("✔️")
  }(); // ✔️
  ```

### 3b Practical Uses

_If your code doesn't support ES6, you can't use the new let and const keywords for creating block-scoped local variables. You'll have to resort to classic function scoping offered by IIFEs._

  ```js
  {
    let part = "🦾";
    console.log(part); // 🦾
  }

  part; // ReferenceError: part is not defined

  (function() {
    var part = "🦾";
    console.log(part);
  })(); // 🦾

  part; // ReferenceError: part is not defined
  ```

_IIFEs can also be used to manage private data by returning functions that create closures for the local variables._

  ```js
  const robot = (function() {
    let part = "⚙️";
    return {
      getPart: () => part,
      setPart: (newPart) => part = newPart
    };
  })();

  console.log(robot.getPart()); // ⚙️
  robot.setPart("🤖");
  console.log(robot.getPart()); // 🤖
  ```

_Let's say you're using jQuery and another library that also assigns to the $ global variable, we can resolve this naming conflict by wrapping the other piece of code with an IIFE that uses $ as a parameter name. We can also do a similar thing if we wanted to capture the global object no matter where we run our code. For example, the global object in the browser is window while Node.js uses global. Aliasing variable names can also be used to optimize code such that it can be minified more efficiently where a JavaScript minifier like UglifyJS can shorten the function's parameter names to single-letter identifiers._

  ```js
  window.$ = function somethingElse() {
    // ...
  };

  (function($) {
    // ...
  })(jQuery);
  
  (function(global) {
    // ...
  })(this);
  
  (function(window, document, undefined) {
    // ...
  })(window, document);

  (function(w, d, u) {
    // ...
  })(window, document);
  ```

_Not having the let keyword of ES6 can also cause unexpected results when running asynchronous tasks inside a loop as the value for i would immediately be changed until the loop condition wasn't fulfilled anymore, we can use IIFEs again for this case._

  ```js
  for (var i = 0; i < 3; i++) {
    setTimeout(() => console.log(`Current index: ${i}`), 100);
    // Current index: 3
    // Current index: 3
    // Current index: 3
  }

  for (var i = 0; i < 3; i++) {
    (function(index) {
      setTimeout(() => console.log(`Current index: ${index}`), 100);
    })(i);
    // Current index: 0
    // Current index: 1
    // Current index: 2
  }
  ```

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[github-shield]: https://img.shields.io/github/followers/ColstonBod-oy?style=social
[github-url]: https://github.com/ColstonBod-oy
[twitter-shield]: https://img.shields.io/twitter/follow/OyColston?style=social
[twitter-url]: https://twitter.com/OyColston
[reddit-shield]: https://img.shields.io/reddit/user-karma/combined/Coldz-Stone?style=social
[reddit-url]: https://www.reddit.com/user/Coldz-Stone
[java-logo]: images/java-logo.png
