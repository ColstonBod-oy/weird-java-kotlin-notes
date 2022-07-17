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
    My lifelong snippets about the functional interfaces 🤖⚙️ and Stream API 🧵 features of Java 8 onwards!
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
      <a href="#sort-a-string-of-characters">Sort A String Of Characters</a>
      <ul>
        <li><a href="#3a-snippets">Snippets</a></li>
        <li><a href="#3b-explanation">Explanation</a></li>
      </ul>
    </li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

![Banner][java-logo]

Hello! my name is Colston D. Bod-oy, I'm a React developer and would be taking my 3rd year of college on the time that I made this repo. I'm an aspiring developer and I would like to work for the big FAANG companies someday 😉.  
  
I created this project so I could keep track and recall snippets about Java's functional interfaces and Stream API as I've just recently started learning them, hope you'll find these notes useful! 😎.


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
      
      System.out.println(Arrays.toString(Arrays.copyOfRange(strNumsMap.keySet().stream().mapToInt(Integer::parseInt).toArray(), 0, 3)));  
      // [61656601, 44708273, 77778805]
    }
  }
  ```

### 2b Explanation

We used the ```keySet()``` method of the ```HashMap``` class to get a set view of the keys contained in our map, then we create a new stream from those keys so we could apply common stream operations like ```mapToInt()``` which maps a stream to an ```IntStream``` where we could also do things like ```Integer.intValue()``` which returns the value of the specified Integer object as an int primitive data type.  
  
We also used ```Integer.parseInt()``` on the last example to return an int from a given string representation and applied ```Arrays.copyOfRange()``` to it so that the resulting array would only contain the first 3 keys of our map. For all our examples, we used the ```toArray()``` method at the end to get an array of all the elements of the ```IntStream```.

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- SORT A STRING OF CHARACTERS -->
## Sort A String Of Characters 



### 3a Snippets



### 3b Explanation



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
