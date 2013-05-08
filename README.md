compass_list
============

Mixin for creation a nested lists with sass (like 1.4, 1.5.2 etc.).

Usage
============
1. Import nested_list into your sass/scss file

         @import 'nested_list'
         
2. Include +nested_list   
   
         +nested_list('nested',3)
   
3. Paste class names into html
<ol class="nested-1">
  <li>First</li>
  <li>Second</li>
  <li>Third</li>
</ol>
4. See the result
