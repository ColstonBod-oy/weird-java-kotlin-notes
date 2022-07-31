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
      <a href="#swap-keys-and-values-in-a-map">Swap Keys And Values In A Map</a>
      <ul>
        <li><a href="#3a-snippets">Snippets</a></li>
        <li><a href="#3b-explanation">Explanation</a></li>
      </ul>
    </li>
    <li>
      <a href="#convert-array-of-primitives-to-a-list-or-set">Convert Array Of Primitives To A List Or Set</a>
      <ul>
        <li><a href="#4a-snippets">Snippets</a></li>
        <li><a href="#4b-explanation">Explanation</a></li>
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
      
      System.out.println(Arrays.toString(integersMap.keySet().stream()  
        .mapToInt(Integer::intValue).toArray()));  
      // [16087526, 64992058, 61656601, 77778805, 44708273]
      
      System.out.println(Arrays.toString(Arrays
        .copyOfRange(strNumsMap.keySet().stream()
        .mapToInt(Integer::parseInt).toArray(), 0, 3)));  
      // [61656601, 44708273, 77778805]
    }
  }
  ```

### 2b Explanation

We used the ```keySet()``` method of the ```HashMap``` class to get a set view of the keys contained in our map, then we create a new stream from those keys so we could apply common stream operations like ```mapToInt()``` which maps a stream to an ```IntStream``` where we could also do things like ```Integer.intValue()``` which returns the value of the specified Integer object as an int primitive data type.  
  
We also used ```Integer.parseInt()``` on the last example to return an int from a given string representation and applied ```Arrays.copyOfRange()``` to it so that the resulting array would only contain the first 3 keys of our map. For all our examples, we used the ```toArray()``` method at the end to get an array of all the elements of the ```IntStream```.

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- SWAP KEYS AND VALUES IN A MAP -->
## Swap Keys And Values In A Map 

This is a snippet I found on [Stack Overflow](https://stackoverflow.com/questions/4436999/how-to-swap-keys-and-values-in-a-map-elegantly) which swaps the keys and values contained in a map. I also got additional information about the ```Collectors.groupingBy()``` method on [Stack Abuse](https://stackabuse.com/guide-to-java-8-collectors-groupingby/).

### 3a Snippets

  ```java
  import java.util.Map;
  import java.util.List;
  import java.util.HashMap;
  import java.util.TreeMap;
  import java.util.stream.Collectors;

  class Main {
    public static void main(String[] args) {
      HashMap<String, Integer> cityMap = new HashMap<>();
      cityMap.put("New York", 20220928);
      cityMap.put("Chicago", 20220812);
      cityMap.put("Boston", 20220928);
      cityMap.put("Los Angeles", 20220928);
      cityMap.put("Seattle", 20221103);
    
      Map<Integer, List<String>> dateMap = cityMap  
        .entrySet().stream().collect(Collectors  
        .groupingBy(Map.Entry::getValue, Collectors  
        .mapping(Map.Entry::getKey, Collectors.toList()))); 
      TreeMap<Integer, List<String>> sortedDateMap = cityMap  
        .entrySet().stream().collect(Collectors  
        .groupingBy(Map.Entry::getValue, TreeMap::new, Collectors  
        .mapping(Map.Entry::getKey, Collectors.toList())));
    
      System.out.println(dateMap);
      // {20220928=[New York, Los Angeles, Boston], 20220812=[Chicago], 20221103=[Seattle]}
    
      System.out.println(sortedDateMap);
      // {20220812=[Chicago], 20220928=[New York, Los Angeles, Boston], 20221103=[Seattle]}
    }
  }
  ```

### 3b Explanation

First, the set view of the mappings was obtained to create a new stream then we apply the ```Stream.collect()``` method which performs a mutable reduction operation on the elements of the stream. A mutable reduction operation collects input elements into a mutable container, such as a ```Collection```, as it processes the elements of the stream.  
  
We use the ```Collectors.groupingBy()``` method to return a ```Collector``` that groups objects by a given specific property and store the end result in a map. The ```Collector``` makes a Map<K, List<T>>, whose keys are the values resulting from applying the classification function on the input elements. Each value of those keys are a ```List``` containing the input elements which map to the associated key.  
  
In the first example, we used ```Entry.getValue()``` as our classification function and ```Collectors.mapping()``` to apply a reduction operation on the values associated with a given key. Using ```Entry.getKey()``` as our mapping function, we we're able to reduce our data to only use keys as values. Finally, ```Collectors.toList()``` was used as the downstream collector to accept the mapped values.  
  
By doing all of the operations, we ended up with a ```Map``` instance that has the swapped key-value pairs from the initial map. Notice how we have duplicate values from our previous map, so when they're converted to keys, each of their previously associated keys are added inside a ```List```. The second example was pretty much the same as the first, the only difference is that we've added a supplier method - ```TreeMap::new``` which specifies the exact implementation of ```Map``` we want to use. This time it uses a ```TreeMap``` implementation so the keys for our new map are automatically sorted.     

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- CONVERT ARRAY OF PRIMITIVES TO A LIST OR SET -->
## Convert Array Of Primitives To A List Or Set

The info I used for this snippet can be found on [HowToDoInJava](https://howtodoinjava.com/java8/java8-boxed-intstream/) which allows me to create a ```List``` or a ```Set``` from a stream of primitives.

### 4a Snippets

  ```java
  import java.util.List;
  import java.util.Arrays;
  import java.util.HashSet;
  import java.util.stream.Collectors;

  class Main {
    public static void main(String[] args) {
      int[] nums = {1, 2, 3, 4, 5};
      HashSet<Integer> set = new HashSet<>(Arrays.stream(nums).boxed().collect(Collectors.toSet()));
      List<Integer> list = Arrays.stream(nums).boxed().collect(Collectors.toList());
        
      System.out.println(set);
      // [1, 2, 3, 4, 5]
        
      System.out.println(list);
      // [1, 2, 3, 4, 5]
    }
  }
  ```
  
### 4b Explanation

The array was first converted to a stream and since it's a stream of primitives we also needed to use the ```boxed()``` method to return a stream consisting of the elements of the given stream, each boxed to an object of the corresponding wrapper class, ```Integer``` in this case. Then we just apply the ```Stream.collect()``` method to create a ```List``` or use the result inside a constructor like the one from ```HashSet```.     

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
