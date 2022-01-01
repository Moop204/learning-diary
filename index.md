# Moop204's Learning Diary

To keep track of what I'm learning on my own (and make sure I'm not slacking off) I will log the things I learn for each day of January 2022. This includes new knowledge, revision of old concepts and niche tidbits.

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
