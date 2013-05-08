compass_list
============

Mixin for creation a nested lists with sass (like 1.4, 1.5.2 etc.).

Usage
============
1. Import nested_list into your sass/scss file

         @import 'nested_list'
         
2. Include +nested_list   

         // @param {String} base class name of the ol list
         // @param {Integer} number of lists. So on output we have 3 classes that will contain names 'nested-1', 'nested-2', ''nested-3'      
         +nested_list('nested',3)
   
3. Paste class names into html

        <ol class="nested-1">
           <li>First           
           	<ol class="inner-nested-1-15-one">
         	  <li>First</li>
         	  <li>Second</li>
         	  <li>Third</li>
         	</ol>
           </li>
           <li>Second</li>
           <li>Third</li>
         </ol>
<style>
/* line 5, ../sass/nested_list.sass */
.nested-1 {
  counter-reset: nested-1;
}
/* line 7, ../sass/nested_list.sass */
.nested-1 > li {
  list-style-type: none;
}
/* line 9, ../sass/nested_list.sass */
.nested-1 > li:before {
  counter-increment: nested-1;
  content: '1.' counter(nested-1) " ";
}

/* line 5, ../sass/nested_list.sass */
.nested-2 {
  counter-reset: nested-2;
}
/* line 7, ../sass/nested_list.sass */
.nested-2 > li {
  list-style-type: none;
}
/* line 9, ../sass/nested_list.sass */
.nested-2 > li:before {
  counter-increment: nested-2;
  content: '2.' counter(nested-2) " ";
}

/* line 5, ../sass/nested_list.sass */
.inner-nested-1-15-one {
  counter-reset: inner-nested-1-15-one;
}
/* line 7, ../sass/nested_list.sass */
.inner-nested-1-15-one > li {
  list-style-type: none;
}
/* line 9, ../sass/nested_list.sass */
.inner-nested-1-15-one > li:before {
  counter-increment: inner-nested-1-15-one;
  content: '1.1.' counter(inner-nested-1-15-one) " ";
}

/* line 5, ../sass/nested_list.sass */
.inner-nested-2-15-one {
  counter-reset: inner-nested-2-15-one;
}
/* line 7, ../sass/nested_list.sass */
.inner-nested-2-15-one > li {
  list-style-type: none;
}
/* line 9, ../sass/nested_list.sass */
.inner-nested-2-15-one > li:before {
  counter-increment: inner-nested-2-15-one;
  content: '2.1.' counter(inner-nested-2-15-one) " ";
}
</style>

<ol class="nested-1">
  <li>First           
  <ol class="inner-nested-1-15-one">
  <li>First</li>
  <li>Second</li>
  <li>Third</li>
</ol>
  </li>
  <li>Second</li>
  <li>Third</li>
</ol>
         
4. See the result
