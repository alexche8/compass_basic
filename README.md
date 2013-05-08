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
           <li>First</li>
           <li>Second</li>
           <li>Third</li>
         </ol>
          <ol class="nested-2">
           <li>First</li>
           <li>Second</li>
           <li>Third</li>
         </ol>
          <ol class="nested-3">
           <li>First</li>
           <li>Second</li>
           <li>Third</li>
         </ol>
         
4. See the result
