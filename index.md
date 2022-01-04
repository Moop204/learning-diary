# Moop204's Learning Diary

To keep track of what I'm learning on my own (and make sure I'm not slacking off) I will log the things I learn for each day of January 2022. This includes new knowledge, revision of old concepts and niche tidbits.

### 4/1/22 - Bits!

#### Leetcode - [Complement of Base 10 Integer](https://leetcode.com/problems/complement-of-base-10-integer/)
_Task_: Obtain complement of given int.

_Notes_: It might be obvious to just apply the bitwise not on the provided int. However this fails to consider the two's complement used to sign ints (in C++20 onwards) which will produce a negative number when a bitwise-not is applied to a positive int. To treat the number as its binary representation we build the solution as we divide the provided int by two and check its even-ness. This means the given int is read right-to-left while the solution is generated left-to-right by bit shifting and using OR operations to insert 1s. As a result a reversal of bits is needed. By creating a mask at the opposite left-right positions we can obtain whether or not the values match and if they do a XOR operation is applied with a 1 at the position checked.   

### 3/1/22 - CSS Shapes
Getting familiar with some simple shapes you can make in CSS helps add some more interesting simple looks. [CSS Tricks](https://css-tricks.com/the-shapes-of-css/) [Shark Coder](https://sharkcoder.com/visual/shapes) [Mozilla](https://developer.mozilla.org/en-US/docs/Web/CSS/basic-shape)

#### CSS - Circles
Make border-radius property 50% for a round circle. 

#### CSS - Z-Index 
Z-index is compared for the first stacking context encountered. All children's z-index is drawn relative to their parents' stacking context if there exists otherwise their z-index is compared. 

### 2/1/22 - Returning to Carousel Component
For a recently dead project I was looking for a carousel component that could 1. present multiple pictures, 2. have fade in edges. This turned out to not exist and so instead I wrote one with my limited CSS knowledge. Now that I know better I am thinking of reviving that component and designing it to be much more reusable.   

#### Leetcode - [Pair of Songs with Duration Divisible by 60](https://leetcode.com/problems/pairs-of-songs-with-total-durations-divisible-by-60/)
_Task_: Return the number of pairs of songs for which their total duration in seconds is divisible by 60.

_Identification of Requirements_: Count number of pairs where sum is divisible by 60. 

_Implementation_: Going for the brute force approach would have us iterate through in two loops comparing each pair of elements. This would net an O(n^2) algorithm. However using the limit of 60 seconds we can improve this approach by grouping times based on their remainder after dividing by 60. After this grouping you can determine which pairs are valid based on their complement. This is faster as the grouping requires one pass (O(n)) to figure out how much each time remains and then iterating through the hashmap or array of 60 would take at most half of n (O(n)) as we can ignore checking half the range as they are the complement of the other half. One notable edge cases exists where the complement is equivalent to the original key. Instead of multiplying the number of elements available, you must instead calculate nC2 where n is the number of elements with the self-referencing complement. 

#### CSS - Absolute
Absolute positioning should be treated as where a normal flow would be but that other elements do not recognise. 
```
 position: absolute;
```
Absolute positioning acts on the closest parent with a position mode set. Otherwise it goes back all the way to the viewport. 

Padding is ignored with absolute positions. Margins are still considered.

#### CSS - 

### 1/1/22 - New Year
I guess this is my new years resolution now.

#### JS - String to Array
Useful for accessing array features like map and reduce.

 ```
 Array.from(str);
 ```

#### Leetcode - [Group Anagrams](https://leetcode.com/problems/group-anagrams/)
_Task_: Given an array of strings strs, group the anagrams together. You can return the answer in any order.

_Identification of Requirements_: One invariant is that anagrams are grouped together. Properties of an anagram include equal lengths and an equivalent frequency table. 

_Implementation_: Using hashmaps to place strings into heaps to group them and build the frequency table. However the frequency table had to be sorted in order to ensure that strings with matching anagrams are mapped consistently as the mapping is dependant on the order at which characters are first encountered. An improvement to speed was achieved by replacing this method with the sorting of strings before mapping. This would sort a simpler data structure. 

### 31/12/21 - NYE Practice
Starting a day early to test the format and see what would need to be changed in further blogs. 

#### CSS - Sizing to Fit Elements
To overwrite block behaviour you can force elements to shrink down to the right size by using

```css
width: fit-content;
```

You can also force elements to never have line breaks with max-content.

```
width: max-content;
```

Min-content works well for sizing wraps around an image.
```
width: min-content;
```

#### CSS - Inline spacing 
Browsers treat inline elements as typography. This adds extra spacing around elements. Setting line-height value for the element to 0 should remove this problem. 

#### CSS - Inline wrapping padding
Applying padding on inline elements only occurs on the ends. To apply them across all lines apply this setting:
```css
box-decoration-break: clone;
```

#### CSS - Inline block
Display modes include inline blocks which avoid the automatic fit to content of inlines and allows customisation like a block but also allows adjacent elements to appear left and right of it. The inline-block element is unable to line wrap.
```css
  display: inline-block;
```

#### CSS - Height 100%
By default height is set to fit the content. When using height: 100%, it takes their parent height which is usually just enough to fit the content and appears as if nothing changed.  

#### CSS - Media Query Limits
* Mobile - (max-width: 480px)
* Tablets - (max-width: 1024px)
