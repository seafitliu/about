有关jQuery2.1.4源码分析

----------

**73~77：**
	
	jQuery = function( selector, context ) {
		// The jQuery object is actually just the init constructor 'enhanced'
		// Need init if jQuery is called (just allow error to be thrown if not included)
		return new jQuery.fn.init( selector, context );
	},


**92~175：**
	
	jQuery.fn = jQuery.prototype = {}


**177~240：**

	jQuery.extend = jQuery.fn.extend = function() {}


**2615~2621：**

	jQuery.find = Sizzle;
	jQuery.expr = Sizzle.selectors;
	jQuery.expr[":"] = jQuery.expr.pseudos;
	jQuery.unique = Sizzle.uniqueSort;
	jQuery.text = Sizzle.getText;
	jQuery.isXMLDoc = Sizzle.isXML;
	jQuery.contains = Sizzle.contains;


**2735~2832：**

	init = jQuery.fn.init = function( selector, context ) {}

**2835：**

	init.prototype = jQuery.fn;

**9202：**

	window.jQuery = window.$ = jQuery;