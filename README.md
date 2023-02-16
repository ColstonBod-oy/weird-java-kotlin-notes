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

  <h3 align="center">Weird Java Notes</h3>

  <p align="center">
    My lifelong notes about the weird 😵‍💫 and wild 🤪 features of Java!
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
      <details>
        <summary>1a</summary>
        <ul>
          <li><a href="#readme-template">README Template</a></li>
        </ul>
      </details>
    </li>
    <li>
      <a href="#get-an-array-of-maps-keys">Get An Array Of Map's Keys</a>
      <details>
        <summary>2a</summary>
        <ul>
          <li><a href="#2a-examples">2a Examples</a></li>
          <li><a href="#2a-description">2a Description</a></li>
        </ul>
      </details>
    </li>
    <li>
      <a href="#swap-keys-and-values-in-a-map">Swap Keys And Values In A Map</a>
      <details>
        <summary>3a</summary>
        <ul>
          <li><a href="#3a-examples">3a Examples</a></li>
          <li><a href="#3a-description">3a Description</a></li>
        </ul>
      </details>
    </li>
    <li>
      <a href="#convert-array-of-primitives-to-a-list-or-set">Convert Array Of Primitives To A List Or Set</a>
      <details>
        <summary>4a</summary>
        <ul>
          <li><a href="#4a-examples">4a Examples</a></li>
          <li><a href="#4a-description">4a Description</a></li>
        </ul>
      </details>
    </li>
    <li>
      <a href="#compare-wrapper-types">Compare Wrapper Types</a>
      <details>
        <summary>5a</summary>
        <ul>
          <li><a href="#5a-examples">5a Examples</a></li>
          <li><a href="#5a-description">5a Description</a></li>
        </ul>
      </details>
    </li>
    <li>
      <a href="#nest-methods">Nest Methods</a>
      <details>
        <summary>6a</summary>
        <ul>
          <li><a href="#6a-examples">6a Examples</a></li>
          <li><a href="#6a-description">6a Description</a></li>
        </ul>
      </details>
    </li>
    <li>
      <a href="#map-two-arrays-to-a-hashmap">Map Two Arrays To A HashMap</a>
      <details>
        <summary>7a</summary>
        <ul>
          <li><a href="#7a-examples">7a Examples</a></li>
          <li><a href="#7a-description">7a Description</a></li>
        </ul>
      </details>
    </li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

![Banner][java-logo]

Hello! My name is Colston D. Bod-oy, I'm a React developer, and I would be taking my 3rd year of college at the time that I made this repo. I'm an aspiring developer and I would like to work for the big FAANG companies someday 😉.  
  
I created this project so I could keep track of and recall things that I didn't know I could do in Java as I've just recently started learning it, hope you'll find these notes useful! 😎.


### README Template

Here's where I got this template btw, also don't forget to follow me on my social media links.

👉 [📒](https://github.com/othneildrew/Best-README-Template)

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- GET AN ARRAY OF MAPS KEYS -->
## Get An Array Of Map's Keys 

I found these examples on [Stack Overflow](https://stackoverflow.com/questions/39891112/get-an-array-from-a-map-and-convert-the-keys) which converts a set of map keys into an array.

### 2a Examples

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

### 2a Description

We used the ```keySet()``` method of the ```HashMap``` class to get a set view of the keys contained in our map, then we create a new stream from those keys so we could apply common stream operations like ```mapToInt()``` which maps a stream to an ```IntStream``` where we could also do things like ```Integer.intValue()``` which returns the value of the specified Integer object as an int primitive data type.  
  
We also used ```Integer.parseInt()``` on the last example to return an int from a given string representation and applied ```Arrays.copyOfRange()``` to it so that the resulting array would only contain the first 3 keys of our map. For all our examples, we used the ```toArray()``` method at the end to get an array of all the elements of the ```IntStream```.

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- SWAP KEYS AND VALUES IN A MAP -->
## Swap Keys And Values In A Map 

I found these examples on [Stack Overflow](https://stackoverflow.com/questions/4436999/how-to-swap-keys-and-values-in-a-map-elegantly) which swaps the keys and values contained in a map. I also got additional information about the ```Collectors.groupingBy()``` method on [Stack Abuse](https://stackabuse.com/guide-to-java-8-collectors-groupingby/).

### 3a Examples

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

### 3a Description

First, the set view of the mappings was obtained to create a new stream then we apply the ```Stream.collect()``` method which performs a mutable reduction operation on the elements of the stream. A mutable reduction operation collects input elements into a mutable container, such as a ```Collection```, as it processes the elements of the stream.  
  
We use the ```Collectors.groupingBy()``` method to return a ```Collector``` that groups objects by a given specific property and store the end result in a map. The ```Collector``` makes a Map<K, List<T>>, whose keys are the values resulting from applying the classification function on the input elements. Each value of those keys are a ```List``` containing the input elements which map to the associated key.  
  
In the first example, we used ```Entry.getValue()``` as our classification function and ```Collectors.mapping()``` to apply a reduction operation on the values associated with a given key. Using ```Entry.getKey()``` as our mapping function, we we're able to reduce our data to only use keys as values. Finally, ```Collectors.toList()``` was used as the downstream collector to accept the mapped values.  
  
By doing all of the operations, we ended up with a ```Map``` instance that has the swapped key-value pairs from the initial map. Notice how we have duplicate values from our previous map, so when they're converted to keys, each of their previously associated keys are added inside a ```List```. The second example was pretty much the same as the first, the only difference is that we've added a supplier method - ```TreeMap::new``` which specifies the exact implementation of ```Map``` we want to use. This time it uses a ```TreeMap``` implementation so the keys for our new map are automatically sorted.     

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- CONVERT ARRAY OF PRIMITIVES TO A LIST OR SET -->
## Convert Array Of Primitives To A List Or Set

The info I used for these examples can be found on [HowToDoInJava](https://howtodoinjava.com/java8/java8-boxed-intstream/) which allows me to create a ```List``` or a ```Set``` from a stream of primitives.

### 4a Examples

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
  
### 4a Description

The array was first converted to a stream and since it's a stream of primitives we also needed to use the ```boxed()``` method to return a stream consisting of the elements of the given stream, each boxed to an object of the corresponding wrapper class, ```Integer``` in this case. Then we just apply the ```Stream.collect()``` method to create a ```List``` or use the result inside a constructor like the one from ```HashSet```.     

<p align="right">(<a href="#top">back to top</a>)</p>
  


<!-- COMPARE WRAPPER TYPES -->
## Compare Wrapper Types

The info I used for these examples can be found on [Stack Overflow](https://stackoverflow.com/questions/4428774/why-java-does-not-see-that-integers-are-equal) which shows why the ```Integer``` objects are not equal.

### 5a Examples

  ```java
  import java.util.HashMap;

  class Main {
    public static void main(String[] args) {
      HashMap<Character, Integer> map1 = new HashMap<>();
      HashMap<Character, Integer> map2 = new HashMap<>();
        
      map1.put('N', 127);
      map2.put('N', 127);
      System.out.println(map1.get('N') == map2.get('N')); // true
        
      map1.put('N', 128);
      map2.put('N', 128);
      System.out.println(map1.get('N') == map2.get('N')); // false
      System.out.println(map1.get('N').equals(map2.get('N'))); // true
  
      Integer num = new Integer(2);
      System.out.println(num == Integer.valueOf(2)); // false
    }
  }
  ```
  
### 5a Description

When comparing wrapper types such as ```Integer```, ```Long```, or ```Boolean```, using ```==``` or ```!=```, we're comparing them as references, not as values. The first example produces a value of ```true``` because in Java, numeric values within the range of -128 to 127 are cached, so they would have an identical memory location. For ```Integer``` use ```intValue()```, ```compareTo()```, or ```equals()``` when making comparisons. If using wrapper classes like ```Integer``` can't be avoided, we can use the ```Integer.valueOf()``` method, which guarantees, as per the Java specs, the reuse of the first 256 ```Integer``` objects from -128 to 127, while ```new Integer()``` forces the creation of a new object as shown in the last example.  

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- NEST METHODS -->
## Nest Methods

The info I used for these examples can be found on [GeeksforGeeks](https://www.geeksforgeeks.org/method-within-method-in-java/) which shows the different ways we could nest methods in Java.

### 6a Examples

  ```java
  class Main {
    interface Build {
      int factorial(int n);
    }
    
    public static void buildStr() {
      StringBuilder sb = new StringBuilder(5);
      Build builder = new Build() {
        @Override
        public int factorial(int n) {
          if (n == 0 || n == 1) {
            return 1;
          }
                
          return n * factorial(n - 1);
        };
      };
        
      for (int i = 0; i < 5; i++) {
        sb.append(builder.factorial(i));
      }    
        
      System.out.println(sb.toString());
    }
    
    public static void main(String[] args) {
      buildStr(); // 112624
    }
  }
  ```
  
### 6a Description

Java does not support nested methods, so we used an anonymous subclass from the example above to achieve a similar structure. An anonymous class is an inner class without a name that usually extends subclasses or implements interfaces, and only a single object can be created from it.

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- MAP TWO ARRAYS TO A HASHMAP -->
## Map Two Arrays To A HashMap

The info I used for these examples can be found on [Stack Overflow Link 1](https://stackoverflow.com/questions/30339679/how-to-map-two-arrays-to-one-hashmap-in-java) and [Stack Overflow Link 2](https://stackoverflow.com/questions/58998826/java-stream-collect-to-treemap-in-reverse-order) which allows sorting of the map as well.

### 7a Examples

  ```java
  import java.util.Map;
  import java.util.TreeMap;
  import java.util.LinkedHashMap;
  import java.util.stream.IntStream;
  import java.util.function.Supplier;
  import static java.util.Comparator.comparing;
  import static java.util.Comparator.reverseOrder;
  import static java.util.stream.Collectors.toMap;

  class Main {
    public static void main(String[] args) {
      int[] positions = {10, 8, 0, 5, 3};
      int[] speeds = {2, 4, 1, 1, 3};
      Map<Integer, Integer> velocities = IntStream.range(0, positions.length)
        .boxed().collect(toMap(i -> positions[i], i -> speeds[i]));
      Map<Integer, Integer> velocitiesOrdered = IntStream.range(0, positions.length)
        .boxed().collect(toMap(i -> positions[i], i -> speeds[i],
        (i, j) -> i, LinkedHashMap::new));
      Map<Integer, Integer> velocitiesSorted = IntStream.range(0, positions.length)
        .boxed().sorted(comparing(i -> positions[i])).collect(toMap(
        i -> positions[i], i -> speeds[i], (i, j) -> i, LinkedHashMap::new));
      Supplier<TreeMap<Integer, Integer>> mapSupplier = () -> 
        new TreeMap<>(reverseOrder());
      Map<Integer, Integer> velocitiesReverseSorted = IntStream.range(0, positions.length)
        .boxed().collect(toMap(i -> positions[i], i -> speeds[i],
        (i, j) -> i, mapSupplier));
      Map<Integer, Integer> velocitiesSpeedSorted = IntStream.range(0, positions.length)
        .boxed().sorted(comparing(i -> speeds[i])).collect(toMap(
        i -> positions[i], i -> speeds[i], (i, j) -> i, LinkedHashMap::new));

      System.out.println(velocities);
      // {0=1, 3=3, 5=1, 8=4, 10=2}
      
      System.out.println(velocitiesOrdered);
      // {10=2, 8=4, 0=1, 5=1, 3=3}
      
      System.out.println(velocitiesSorted);
      // {0=1, 3=3, 5=1, 8=4, 10=2}
    
      System.out.println(velocitiesReverseSorted);
      // {10=2, 8=4, 5=1, 3=3, 0=1}
    
      System.out.println(velocitiesSpeedSorted);
      // {0=1, 5=1, 10=2, 3=3, 8=4}
    }
  }
  ```



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[github-shield]: https://img.shields.io/github/followers/ColstonBod-oy?style=social
[github-url]: https://github.com/ColstonBod-oy
[twitter-shield]: https://img.shields.io/twitter/follow/OyColston?style=social
[twitter-url]: https://twitter.com/OyColston
[reddit-shield]: https://img.shields.io/reddit/user-karma/combined/Coldz-Stone?style=social
[reddit-url]: https://www.reddit.com/user/Coldz-Stone
[java-logo]: images/java-logo.png
