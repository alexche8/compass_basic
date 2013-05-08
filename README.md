compass_list
============

Mixin for creation a nested lists with sass (like 1.4, 1.5.2 etc.).

Usage
============
1. Import nested_list into your sass/scss file

         @import 'nested_list'
         
2. Include +nested_list   
         
         For simple nested lists

         // @param {String} base class name of the ol list
         // @param {Integer} number of lists. So on output we have 3 classes that will contain names 'nested-1', 'nested-2', ''nested-3'      
         +nested_list('nested',3)
         
         For inner nested lists( 1.1.4, 1.51.1)
                  
         // @param {String} base class name of the ol list
         // @param {Integer} number of lists. So on output we have 3 classes that will contain names 'nested-1', 'nested-2', ''nested-3'
         // @param {String} inner nested list value
         // @param {String} aplha-numeric synonym for inner nested list value, 
         //                 becouse class names not support class names like '.1' in css file
         +nested_list('inner-nested', 2, '.1', '15-one')
   
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

4. Complate files

   index.sass

        +nested_list('nested',3)  
        
   index.html
                  
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
         
5. Output result <a href="http://jsfiddle.net/alexche8/UzXu3/2/">here</a>
