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
    <li>
      <a href="#store-key-value-pairs-in-a-list">Store Key-Value Pairs In A List</a>
      <details>
        <summary>8a</summary>
        <ul>
          <li><a href="#8a-examples">8a Examples</a></li>
          <li><a href="#8a-description">8a Description</a></li>
        </ul>
      </details>
    </li>
    <li>
      <a href="#create-a-node-priority-queue-with-comparator">Create A Node Priority Queue With Comparator</a>
      <details>
        <summary>9a</summary>
        <ul>
          <li><a href="#9a-examples">9a Examples</a></li>
          <li><a href="#9a-description">9a Description</a></li>
        </ul>
      </details>
      <details>
        <summary>9b</summary>
        <ul>
          <li><a href="#9b-examples">9b Examples</a></li>
          <li><a href="#9b-description">9b Description</a></li>
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

We used the ```keySet()``` method of the ```HashMap``` class to get a set view of the keys contained in our map, then we create a new stream from those keys so we could apply common stream operations like ```mapToInt()``` which maps a stream to an ```IntStream``` where we could also do things like ```Integer.intValue()``` which returns the value of the specified ```Integer``` object as an ```int``` primitive data type.  
  
We also used ```Integer.parseInt()``` on the last example to return an ```int``` from a given string representation and applied ```Arrays.copyOfRange()``` to it so that the resulting array would only contain the first 3 keys of our map. For all our examples, we used the ```toArray()``` method at the end to get an array of all the elements of the ```IntStream```.

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
  
### 7a Description

To use the ```Collectors.toMap()``` method we have to box the ```int``` primitives into ```Integer``` objects first. To preserve the element order, use the extended version of ```Collectors.toMap()``` together with the ```LinkedHashMap::new``` function as the argument for the ```mapSupplier``` parameter which was shown in the second example.  
  
For the third example, we used the ```Comparator.comparing``` method to compare values from the positions array and sort them in ascending order; note how we also used the ```LinkedHashMap::new``` function as well for this example and the fifth example to maintain the sorted values when collecting them into a map.  
  
We created a ```TreeMap``` with a ```Comparator.reverseOrder``` and use it as the ```mapSupplier``` for the fourth example to get a hashmap that has a descending order based on the values of the positions array. Finally, we used the speeds array as the basis for the sorting of the fifth example.      

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- STORE KEY-VALUE PAIRS IN A LIST -->
## Store Key-Value Pairs In A List

The info I used for these examples can be found on [Techie Delight](https://www.techiedelight.com/implement-pair-class-java/) which shows how to implement a ```Pair``` class.

### 8a Examples

  ```java
  import java.util.List;
  import java.util.Arrays;
  import java.util.HashMap;
  import java.util.ArrayList;

  class Main {
    public static void main(String[] args) {
      Main main = new Main();
      Main.TimeMap map = main.new TimeMap();
      map.set("Server1", "User1", 145);
      map.set("Server1", "User2", 565);
      map.set("Server1", "User3", 35);
      map.set("Server1", "User4", 13);
      map.set("Server1", "User5", 145);
      map.set("Server2", "User1", 23);
      map.set("Server2", "User2", 19);
      map.set("Server2", "User3", 61);
        
      System.out.println(map.get("Server1"));
      // [User1, 145] [User2, 565] [User3, 35] [User4, 13] [User5, 145]
        
      System.out.println(map.get("Server2"));
      // [User1, 23] [User2, 19] [User3, 61]
    }
    
    class TimeMap {
      HashMap<String, List<Pair<String, Integer>>> map;
    
      public TimeMap() {
        map = new HashMap<>();
      }
    
      public void set(String key, String value, int timestamp) {
        if (!map.containsKey(key)) {
          map.put(key, new ArrayList<>());
        }
      
        map.get(key).add(new Pair(value, timestamp));
      }
    
      public String get(String key) {
        String res = "";
        List<Pair<String, Integer>> list = map.getOrDefault(key, new ArrayList<>(0)); 
            
        for (Pair<String, Integer> p : list) {
          res += "[" + p.getKey() + ", " + p.getValue() + "] ";
        }
            
        return res;
      }
    }
    
    class Pair<T, V> {
      private final T key;
      private final V value;

      public Pair(T key, V value) {
        this.key = key;
        this.value = value;
      }

      public T getKey() {
        return key;
      }

      public V getValue() {
        return value;
      }
    }
  }
  ```
  
### 8a Description
  
Java's ```List``` does not support key-value pairs, so we have to create a ```Pair``` custom class to be able to store them as elements. We can do this by using generics, so we can use different kinds of data for our keys and values. The created ```List``` would then be used by our ```HashMap``` to store values while also assigning its own key as shown in the examples.    

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- CREATE A NODE PRIORITY QUEUE WITH COMPARATOR -->
## Create A Node Priority Queue With Comparator
  
The info I used for these first examples can be found on [GitHub](https://github.com/neetcode-gh/leetcode/blob/main/java/0973-k-closest-points-to-origin.java) which is the Java solution for the LeetCode problem [K Closest Points to Origin](https://leetcode.com/problems/k-closest-points-to-origin/). 

### 9a Examples
  
  ```java
  import java.util.Arrays;
  import java.util.PriorityQueue;

  class Main {
    public static void main(String[] args) {
      Main main = new Main();
      int[][] points = {{3, 3}, {5, -1}, {-2, 4}};
        
      System.out.println(Arrays.deepToString(main.kClosestMinHeap(points, 2)));
      // [[3, 3], [-2, 4]]
        
      System.out.println(Arrays.deepToString(main.kClosestMaxHeap(points, 2)));
      // [[-2, 4], [3, 3]]
    }
    
    public int[][] kClosestMinHeap(int[][] points, int k) { 
      PriorityQueue<int[]> pq = new PriorityQueue<>((a, b) -> 
        Double.compare(
          Math.pow(a[0], 2) + Math.pow(a[1], 2),
          Math.pow(b[0], 2) + Math.pow(b[1], 2)
        )
      );

      for (int[] point : points) {
        pq.offer(point);
      }

      int[][] res = new int[k][2]; 

      for (int i = 0; i < k; i++) {
        int[] cur = pq.poll();
        res[i][0] = cur[0];
        res[i][1] = cur[1];
      }

      return res;
    }
    
    public int[][] kClosestMaxHeap(int[][] points, int k) { 
      PriorityQueue<int[]> pq = new PriorityQueue<>((a, b) -> 
        Double.compare(
          Math.pow(b[0], 2) + Math.pow(b[1], 2),
          Math.pow(a[0], 2) + Math.pow(a[1], 2)
        )
      );

      for (int[] point : points) {
        pq.offer(point);

        if (pq.size() > k) {
          pq.poll();
        }
      }

      int[][] res = new int[k][2]; 

      for (int i = 0; i < k; i++) {
        int[] cur = pq.poll();
        res[i][0] = cur[0];
        res[i][1] = cur[1];
      }

      return res;
    }
  }
  ```

### 9a Description

The examples above return the k closest points to the origin of an X-Y plane (0, 0) from a given set of coordinates. To solve the problem, we'll use a heap binary tree data structure, which is implemented as the ```PriorityQueue``` in Java. We could then pass a ```Comparator``` when instantiating to give rules on how we would want to order the elements that would be stored inside the ```PriorityQueue```.
        
Instead of creating a new ```Comparator``` object, we could just use Java 8's lambda expression feature to declare how our comparisons would work. We also used the Euclidean formula to calculate the distance of the points from the origin (note that we didn't apply the square root to the formula because it wouldn't affect our desired results). In the first example, we created what's called a min heap because the points would be ordered in an ascending order based on the results of the formula. We then continuously popped the head of the ```PriorityQueue``` and assigned its values to the indexes of our ```res``` 2D array until we had enough k elements, which we would then finally return as our result.  
        
We could save more space by using a max heap instead of a min heap, as shown in the second example; we were able to convert the comparator for the max heap by flipping the conditions where we have the second array in our lambda expression as the first argument in our ```Double.compare()``` method (note that we used ```Double``` instead of ```Integer``` because the ```Math.pow()``` method returns a ```double``` value).
        
<p align="right">(<a href="#top">back to top</a>)</p>

        
        
The info I used for the next examples can be found on [Stack Overflow Link 1](https://stackoverflow.com/questions/45167365/java-listinteger-sort-comparator-and-overflow) which shows why using the commented line (see code below) would cause an overflow when trying to get the difference of two large arbitrary signed integers thus causing unexpected behaviors. [Stack Overflow Link 2](https://stackoverflow.com/questions/26963158/inserting-nodes-into-a-priority-queue-java) shows how to implement the ```Comparable``` interface to avoid such problems.

### 9b Examples

  ```java
  import java.util.PriorityQueue;

  class Main {
    public static void main(String[] args) {
      Main main = new Main();
      
      // List Node 1
      Main.ListNode list1Tail = main.new ListNode(5);
      Main.ListNode list1N = main.new ListNode(4, list1Tail);
      Main.ListNode list1Head = main.new ListNode(1, list1N);
      
      // List Node 2
      Main.ListNode list2Tail = main.new ListNode(4);
      Main.ListNode list2N = main.new ListNode(3, list2Tail);
      Main.ListNode list2Head = main.new ListNode(1, list2N);
      
      // List Node 3
      Main.ListNode list3Tail = main.new ListNode(6);
      Main.ListNode list3Head = main.new ListNode(2, list3Tail);
      
      ListNode[] lists = {list1Head, list2Head, list3Head};
      ListNode mergedListsHead = main.mergeKLists(lists);
  
      System.out.println(mergedListsHead.toString());
      // 1 -> 1 -> 2 -> 3 -> 4 -> 4 -> 5 -> 6 ->
    }
    
    public ListNode mergeKLists(ListNode[] lists) {
      if (lists == null || lists.length == 0) {
        return null;
      }

      // PriorityQueue<ListNode> queue = new PriorityQueue<>((a, b) -> a.val - b.val);
      PriorityQueue<ListNode> queue = new PriorityQueue<>((a, b) -> a.compareTo(b));

      for (ListNode n : lists) {
        if (n != null) {
          queue.offer(n);  
        } 
      }

      ListNode dummy = new ListNode(0);
      ListNode curr = dummy;
    
      while (!queue.isEmpty()) {
        ListNode n = queue.poll();
        curr.next = n;
        curr = curr.next;

        if (n.next != null) {
          queue.offer(n.next);
        }
      }

      return dummy.next;
    }
    
    class ListNode implements Comparable<ListNode> {
      int val;
      ListNode next;
      ListNode() {}
      ListNode(int val) { this.val = val; }
      ListNode(int val, ListNode next) { this.val = val; this.next = next; }
      
      @Override
      public int compareTo(ListNode n) {
        if (this.val < n.val) {
          return -1;
        }
                             
        else if (this.val > n.val) {
          return 1;
        }
  
        else {
          return 0;
        }
      }

      @Override
      public String toString() {
        String result = val + " -> ";
      
        if (next != null) {
          result += next.toString();
        }
      
        return result;
      }
    }
  }
  ```
  
### 9b Description
  
The example above merges sorted list nodes together, where List Nodes 1 and 2 have three nodes while List Node 3 only has a head and a tail. We can implement the code in two ways, but the commented line does not work in general because there's a chance that it would cause an overflow when the variable ```a``` in the lambda expression is a large positive number while the ```b``` variable is a large negative number, resulting in having to add the two large numbers together, which the ```int``` data type might not be able to hold, and the answer would instead be a negative integer instead of a positive one, giving the opposite of the intended behavior.  
  
To solve the previous problem, we must implement the ```Comparable``` interface on our ```ListNode``` class, which allows us to implement our own ```compareTo``` function without having to subtract two integers to get a positive or negative result.

This method of creating a comparator for the ```PriorityQueue``` is preferred over the examples in 9a when the elements used are not ```Comparable``` out of the box (e.g., custom classes).

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
