# Moop204's Learning Diary

To keep track of what I'm learning on my own (and make sure I'm not slacking off) I will log the things I learn for each day of January 2022. This includes new knowledge, revision of old concepts and niche tidbits.

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
