# Layouts

Layouts is a lightweight layout framework.  
It is a convention over configuration library,  
and has a lot of shorthands built for almost every layout needs.

For e.g.
```
let parentLayout = 
layout(parent)
	// Height constraint of 50
	.height(50)
	// flexbox rows, essentially
	.stackHorizontal([
		// item 1
		layout(labelLeft)
			// 12px right margin
			.right(12),
		// item 2
		layout(labelRight)
	])
	// Align items vertically, if stacking vertically, align horizontally
	.alignItems(.center)
	.install()
```

... will add the two labels to parent, and stack them horizontally, similar to flexbox rows 

To uninstall / animate, simply keep the reference of the LayoutBuilder object: 

```
// let parentLayout = layout(parent).stackHorizontal([
// ...

// Update height to 200, it's still flexboxing
parentLayout.height(200).reinstall()

// Remove all constraints installed
parentLayout.uninstall()
```

### Why use Layouts

Layouts simplifies layout by sacrificing flexibility.  
It has a shorthands like stack which is similar to flexbox

However, there is no shortage of great layout libraries on Github, here're just a few libraries I took inspirations from:  
[SnapKit](https://github.com/SnapKit/SnapKit)  
[PureLayout](https://github.com/PureLayout/PureLayout)  
[LayoutKit](https://github.com/linkedin/LayoutKit)  

### Documentation

Full documentation here: [link](https://will3.github.io/layoutsdoc/)

### TODO

- Mac support    
- Better documentation, with pictures explaining each layout property  