nested_list
============

Mixin for creation nested list(numbered) with sass, scss(like 1.4, 1.5.2 etc.).

Usage
============
1. Import nested_list mixin into your sass/scss file.

         @import 'nested_list'
         
2. Include +nested_list() with params.   
         
         For simple nested lists

         // @param {String} base class name of the ol list
         // @param {Integer} number of lists. 
         // It is generate class names 'nested-1', 'nested-2', ''nested-3' and styles for them.
         // You must past class names in ol elements. 
         // As result li included elements will started with 1.1, 1.2, etc for 'nested-1',
                                                             2,1, 2,2, etc for 'nested-2',
                                                             3,1, 3,2, etc for 'nested-3', etc.
         +nested_list('nested',3)
         
         For three and more levels lists( 1.1.4, 1.51.1)
                  
         // @param {String} base class name of the ol list
         // @param {Integer} number of lists
         // @param {String} piece of counter value in html
         // @param {String} piece of counter inner class name in css,
         //                 becouse classes not supported names like '.1' in css file
         // It is generate class names 'inner-nested-1-15-one', 'inner-nested-2-15-one' and styles for them
         // it is work the same way as the simple nested list
         +nested_list('inner-nested', 1, '.1', '15-one')
         +nested_list('inner-nested', 1, '.2', '15-two')
   
3. Paste class names into html.

        <ol class="nested-1">
           <li>First           
               <ol class="inner-nested-1-15-one">
         	  <li>First</li>
         	  <li>Second</li>
         	  <li>Third</li>
               </ol>
           </li>
          <li>Second           
                  <ol class="inner-nested-1-15-two">
         	  <li>First</li>
         	  <li>Second</li>
         	  <li>Third</li>
         	</ol>
           </li>
           <li>Third</li>
         </ol>
         
4. Output result <a href="http://jsfiddle.net/alexche8/UzXu3/9/">here</a>
