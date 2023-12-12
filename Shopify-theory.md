===========================================================================================================
1.What is Liquid?
2.What is Objects,Tags and Filters?
3.What is Operators?
4.What are Liquid Objects Types?

5.Liquid Basics
        1.Handles
            1.what is a handle?
            2.How are my handles created?
        2.Operators
            1. ==
            2. !=
            3. >
            4. <
            5. >=
            6. <=
            7. or
            8. and
            9. contains
        3.Types
            Liquid objects can return one of six types: String, Number, Boolean, Nil, Array, or EmptyDrop. Liquid variables can be initialized by using the assign or capture tags
                1.Strings
                2.Numbers
                3.Booleans
                4.Nil
                5.Arrays
                6.EmptyDrop
        4.Truthy and Falsy
            What is truthy?
            WHat is falsy?
        5.Whitespace Control

6.Liquid Tags
        1.Conditional Tags
            1.if 
            2.elsif   else
            3.case    when
            4.unless
        2.HTML Tags
            1.form
            2.style
        3.Iteration Tags
            1.for
            2.else
            3.break
            4.continue
            5.cycle
            6.paginate
            7.tablerow
        4.Syntax Tags
            1.comment
            2.echo
            3.liquid
            4.raw
        5.Theme Tags
            1.include
            2.javascript
            3.layout
            4.render
            5.section
            6.sections
            7.stylesheet
        6.Variable Tags
            1.assign
            2.capture
            3.increment
            4.decrement
   
7.Liquid Filters
    1.Array filters
    2.Cart filters
    3.Collection filters
    4.Color filters
    5.Customer filters
    6.Default filters
    7.font filters
    8.format filters
    9.HTML filters
    10.Hosted file filters
    11.Localization filters
    12.Math filters
    13.Media filters
    14.Metafield Filters
    15.Money filters
    16.Payment filters
    17.String Filters
8.Liquid Objects
    1.additional_checkout_buttons
    2.address
    3.all_country_option_tags
    4.all_products
    5.app
    6.articles
    7.block
    8.blog
    9.blogs
    10.brand
    11.brand_color
    12.canonical_url
    13.cart
    14.checkout
    15.collection
    16.collections
    17.color
    18.color_scheme
    19.color_scheme_group
    20.comment
    21.company
    22.company_address
    23.company_location
    24content_for_additional_checkout_buttons
    25.content_for_header
    26.content_for_index
    27.content_for_layout
    28.country
    29.country_option_tags
    30.currency
    31.current_page
    32.current_tags
    33.customer_address
    34.customer
    35.date
    36.discount
    37.discount allocation
    38.discount application
    39.external_vedio
    40.filter
    41.filter_value
    42.focal_point
    43.font
    44.forloop
    45.form
    46.form_errors
    47.fulfillment
    48.generic_file
    49.gift_card
    50.group
    51.handle
    52.image
    53.image_presentation
    54.images
    55.line_item
    56.link
    57.linklist
    58.linklists
    59.localization
    60.location
    61.measurement
    62.media
    63.metafield
    64.metaobject
    65.metaobject_definition
    66.metaobject_system
    67.model
    68.model_source
    69.money
    70.order
    71.page
    72.page_description
    73.page_image
    74.page_title
    75.pages
    76.paginate
    77.part
    78.pending_payment_instruction_input
    79.policy
    80.powered_by_link
    81.predictive_search
    82.predictive_search_resources
    83.product
    84.product_option
    85.quantity_rule
    86.rating
    87.recipient
    88.recommendations
    89.request
    90.robots
    91.routes
    92.rule
    93.script
    94.scripts
    95.search
    96.section
    97.selling_plan
    98.selling_plan_option
    99.selling_plan_price_adjustment
    100.selling_plan_allocation
    101.selling_plan_allocation_price_adjustment
    102.selling_plan_checkout_charge
    103.selling_plan_group
    104.selling_plan_group_option
    105.settings
    106.shipping_method
    107.shop
    108.shop_locale
    109.sitemap
    110.sort_option
    111.store_availability
    112.tablerow
    113.tax_line
    114.template
    115.theme
    116.transaction
    117.transaction_payment_details
    118.unit_price_measurement
    119.user
    120.user_agent
    121.variant
    122.video
    123.video_source

9.URL
https://shopify.dev/docs/api/liquid

10.shopify Input settings
https://shopify.dev/docs/themes/architecture/settings/input-settings





Liquid Cheat Sheet
=============================================================================================================================

Four Types 
~~~~~~~~~~~~~~~~~~~
1.Basic   2.Tags  3.Filters  4.Objects 


1.Basics
====================================================================================================================================
 Basics
      * Handles
      * Truthy and Falsy
      * Operators
      * Whitespace Control
      * Types
 
1.Handles:
     The handle is used to access the attributes of a Liquid object.
     By default, it is the object’s title in lowercase with any spaces 
     and special characters replaced by hyphens (-). Every object in Liquid 
     (product, collection, blog, menu) has a handle. Learn more

what is a handle?
      The handle is used to access the attributes of a Liquid object. By default,
      it is the object’s title in lowercase with any spaces and special characters 
      replaced by hyphens (-). Every object in Liquid (product, collection, blog, menu) 
      has a handle. Learn more

<!-- the content of the About Us page -->
{{ pages.about-us.content }}

How are my handles created?
      A product with the title ‘shirt’ will automatically be given the handle shirt. 
      If there is already a product with the handle ‘shirt’, the handle will auto-increment. 
      In other words, all ‘shirt’ products created after the first one will receive the handle 
      shirt-1, shirt-2, and so on. Learn more
 
2.Truthy and falsy:
      In programming, we describe “truthy” and “falsy” as anything that returns true or false,
      respectively, when used inside an if statement. Learn more

what is truthy?
      All values in Liquid are truthy, with the exception of nil and false. In this example,
      the variable is a string type but it evaluates as true. Learn more

     {% assign tobi = 'tobi' %}
     {% if tobi %}
     This will always be true.
     {% endif %}

what is falsy?
     The only values that are falsy in Liquid are nil and false. nil is returned when a 
     Liquid object doesn’t have anything to return. For example, if a collection doesn’t 
     have a collection image, collection.image will be set to nil. Learn more

     {% if collection.image %}
     <!-- output collection image -->
     {% endif %}

3.Operators:
     Liquid has access to all of the logical and comparison operators. These can be used in tags such as if and unless. Learn more
(==)?

equals Learn more

{% if product.title == 'Awesome Shoes' %}
  These shoes are awesome!
{% endif %}

(!=)?

does not equal Learn more

(>)?

greater than Learn more

(<)?

less than Learn more

(>=)?

greater than or equal to Learn more

(<=)?

less than or equal to Learn more

(or)?

condition A or condition B Learn more

(and)?

condition A and condition B Learn more

(contains)?

checks for the presence of a substring inside a string or array Learn more

{% if product.title contains 'Pack' %}
  This product’s title contains the word Pack.
{% endif %}

4.Whitespace control:
       In Liquid, you can include a hyphen in your tag syntax {{-, -}}, {%-, and -%} to strip whitespace from the left or right side of a rendered tag. Normally, even if it doesn’t output text, any line of Liquid in your template will still output an empty line in your rendered HTML. Learn more

Whitespace Control?

   Using hyphens, the assign statement doesn't output a blank line. Learn more

   {%- assign my_variable = "tomato" -%}
   {{ my_variable }}
   tomato

5.Types:
  Liquid objects can return one of six types: String, Number, Boolean, Nil, Array, or EmptyDrop. Liquid variables can be initialized by using the assign or capture tags. Learn more

strings?
   Strings are declared by wrapping the variable’s value in single or double quotes. Learn more

{% assign my_string = 'Hello World!' %}

numbers?
    Numbers include floats and integers. Learn more

{% assign my_num = 25 %}

booleans?
    Booleans are either true or false. No quotations are necessary when declaring a boolean. Learn more

{% assign foo = true %}
{% assign bar = false %}

nill?
  Nil is an empty value that is returned when Liquid code has no results. It is not a string
  with the characters ‘nil’. Nil is treated as false in the conditions of {% if %} blocks and 
  other Liquid tags that check for the truthfulness of a statement. Learn more

arrays?
   Arrays hold a list of variables of all types. To access items in an array, you can loop
   through each item in the array using a for tag or a tablerow tag. Learn more

  {% for tag in product.tags %}
  {{ tag }}
  {% endfor %}

emptydrop?
    An EmptyDrop object is returned whenever you try to access a non-existent object
   (for example, a collection, page or blog that was deleted or hidden) by a handle. Learn more








2.HTML Tags :
====================================================================================================================================
1.HTML tags render HTML elements using Shopify-specific attributes. Learn more
  
  --> {% form %} :
  --> {% style %} 
    
	  --> {% form %} :
	      Generates an HTML form tag, including any required input tags to submit the form to a specific endpoint. Learn more
	      -- Syntax :
	          {% form 'form_type' %}
	 		 content
		     {% endform %}
	  
	  --> {% style %} :
	      Generates an HTML style tag with an attribute of data-shopify. Learn more
	      -- Syntax :
	          {% style %}
			  .h1 {
	   		  color: {{ settings.colors_accent_1 }};
	  		  }
		     {% endstyle %}
		     
		     (or)
		     
		     <style data-shopify>
	  		  .h1 {
	   		  color: #121212;
	  		}
			</style>
		
2.Iteration Tags :
  Iteration Tags are used to run a block of code repeatedly. Learn more
  --> {% for %} 
  --> {% else %} 
  --> {% break %} 
  --> {% continue %} 
  --> {% cycle %} 
  --> {% paginate %} 
  --> {% tablerow %} 

	  --> {% for %} :
	      Repeatedly executes a block of code. Learn more
	      -- Syntax :
	         {% for product in collection.products %}
  			{{ product.title }}
		    {% endfor %}
	      
	  --> {% else %} :
	      Specifies a fallback case for a for loop which will run if the loop has zero length (for example, you loop over a collection that has no products). Learn more
	  	 -- Syntax :
	  	    {% for product in collection.products %}
    			{{ product.title }}
			{% else %}
  			This collection is empty.
		    {% endfor %}

	  --> {% break %} :
	      Causes the loop to stop iterating when it encounters the break tag. Learn more
	  	 -- Syntax :
	  	    	{% for i in (1..5) %}
  				{% if i == 4 %}
    				{% break %}
  				{% else %}
    				{{ i }}
  				{% endif %}
		     {% endfor %}
		     
	  --> {% continue %} :
	      Causes the loop to skip the current iteration when it encounters the continue tag. Learn more
	  	 -- Syntax :
	  	    {% for i in (1..5) %}
  				{% if i == 4 %}
    				{% continue %}
  				{% else %}
   			     {{ i }}
  				{% endif %}
   		    {% endfor %}
   		    ------------------
   		    1 2 3 5
   		    
	  --> {% cycle %} :
	      Loops through a group of strings and outputs them in the order that they were passed as parameters. Each time cycle is called, the next string that was passed as a parameter is output. Learn more
	  	 -- Syntax :
	  	    {% cycle 'one', 'two', 'three' %}
		    {% cycle 'one', 'two', 'three' %}
		    {% cycle 'one', 'two', 'three' %}
 		    {% cycle 'one', 'two', 'three' %}
 		    -----------------------------------
 		    one
		    two
  		    three
  		    one
  		    
	  --> {% paginate %} :
	      Splits an array's items across multiple pages. Learn more
	  	 -- Syntax :
	  	    {% paginate array by page_size %}
  			{% for item in array %}
   			forloop_content
  			{% endfor %}
		    {% endpaginate %}
		    
	  --> {% tablerow %} :
	      Generates an HTML <table>. Must be wrapped in an opening <table> and closing </table> HTML tags. Learn more
	  	 -- Syntax :
	  	    <table>
  			{% tablerow product in collection.products %}
    			{{ product.title }}
  			{% endtablerow %}
		    </table>
		    ----------------------------------------------
		    <table>
  			<tr class="row1">
	    			<td class="col1">
	      		  Cool Shirt
	    			</td>
			    <td class="col2">
			      Alien Poster
			    </td>
			    <td class="col3">
			      Batman Poster
			    </td>
			    <td class="col4">
			      Bullseye Shirt
			    </td>
			    <td class="col5">
			      Another Classic Vinyl
			    </td>
			    <td class="col6">
			      Awesome Jeans
			    </td>
  			</tr>
		   </table>
	
3.Conditional Tags :
  Conditional tags define conditions that determine whether blocks of Liquid code get executed. Learn more
  --> {% if %}
  --> {% elsif %} / {% else %}
  --> {% case %} / {% when %}
  --> {% unless %}
  
	  --> {% if %}:
	      Executes a block of code only if a certain condition is met. Learn more
	      -- Syntax :
	         {% if product.title == 'Awesome Shoes' %}
  			These shoes are awesome!
		    {% endif %}

	  --> {% elsif %} / {% else %}:
	      Adds more conditions within an if or unless block. Learn more
	      -- Syntax :
	         <!-- If customer.name is equal to 'anonymous' -->
			{% if customer.name == 'kevin' %}
	  			Hey Kevin!
				{% elsif customer.name == 'anonymous' %}
				  Hey Anonymous!
				{% else %}
				  Hi Stranger!
		     {% endif %}
		     --------------------------------------
		     Hey Anonymous!

	  --> {% case %} / {% when %} :
	      Creates a switch statement to compare a variable with different values. case initializes the switch statement and when compares its values. Learn more
	      -- Syntax :
	         {% assign handle = 'cake' %}
			{% case handle %}
			  {% when 'cake' %}
			     This is a cake
			  {% when 'cookie' %}
			     This is a cookie
			  {% else %}
			     This is not a cake nor a cookie
			{% endcase %}
			----------------------------------
			This is a cake
			
	  --> {% unless %} :
	      Similar to if, but executes a block of code only if a certain condition is not met. Learn more
	      -- Syntax :
	         {% unless product.title == 'Awesome Shoes' %}
		      These shoes are not awesome.
		   {% endunless %}
		   ----------------------------------------------
		   These shoes are not awesome.

4.Theme Tags :
  Theme Tags have various functions including: outputting template-specific HTML markup, telling the theme which layout and snippets to use, and splitting a returned array into multiple pages. Learn more
  --> {% include %}
  --> {% javascript %}
  --> {% layout %}
  --> {% render %}
  --> {% section %}
  --> {% sections %}
  --> {% sections 'name' %}
  --> {% stylesheet %}
  
	  --> {% include %}:
	      Inserts a snippet from the snippets folder of a theme. Learn more
	        
	  --> {% javascript %} :
	      JavaScript code included in a section file. Learn more
	      -- syntax :
	         {% javascript %}
  			javascript_code
		    {% endjavascript %}

	  --> {% layout %} :
	      Loads an alternate template file from the layout folder of a theme. If no alternate layout is defined, the theme.liquid template is loaded by default. Learn more

	  --> {% render %} :
	      Renders a snippet from the snippets folder of a theme.
		When a snippet is rendered, the code inside it does not have access to the variables assigned within its parent template. Similarly, variables assigned within the snippet can't be accessed by the code outside of the snippet. This encapsulation increases performance and helps make theme code easier to understand and maintain. Learn more
	        
	  --> {% section %} :
	      Inserts a section from the sections folder of a theme. Learn more
	      -- syntax :
	         {% section 'footer' %}
	         ----------------------
	         <div id="shopify-section-footer" class="shopify-section">
			  <!-- content of sections/footer.liquid -->
		    </div>

	  --> {% sections %} :
	      Renders a section group. Use this tag to render section groups as part of the theme's layout content. Place the sections tag where you want to render it in the layout. Learn more
	      -- syntax :
	         {% sections 'name' %}
	        
	  --> {% stylesheet %} :
	      CSS styles included in a section file. Learn more
	      -- syntax :
	         {% stylesheet %}
			  css_styles
		    {% endstylesheet %}

5.Variable Tags :
  Variable Tags are used to create new Liquid variables. Learn more
  --> {% assign %}
  --> {% capture %}
  --> {% increment %}
  --> {% decrement %}
  
	  --> {% assign %} :
	      Creates a new variable. Learn more
	      -- Syntax :
	         {% assign my_variable = false %}
			{% if my_variable != true %}
			  This statement is valid.
			{% endif %}
			--------------------------------
			This statement is valid.
			
	  --> {% capture %} :
	      Captures the string inside of the opening and closing tags and assigns it to a variable. Variables created through {% capture %} are strings. Learn more
	      -- Syntax :
	         {% capture my_variable %}I am being captured.{% endcapture %}
		    {{ my_variable }}
		    -------------------------------
		    I am being captured.

	  --> {% increment %} :
	      Creates a new number variable, and increases its value by one every time it is called. The initial value is 0. Learn more
	      -- Syntax :
	         {% increment variable %}
			{{ variable }}
			{% increment variable %}
			{{ variable }}
			{% increment variable %}
			{{ variable }}
			----------------------------
			0
			1
			2

	  --> {% decrement %} :
	      Creates a new number variable and decreases its value by one every time it is called. The initial value is -1. Learn more
	      -- Syntax :
	         {% decrement variable %}
			{{ variable }}
			{% decrement variable %}
			{{ variable }}
			{% decrement variable %}
			{{ variable }}
			----------------------
			-1
			-2
			-3

6.Syntax Tags :
  Syntax tags control how Liquid code is processed and rendered. Learn more
  --> {% comment %}
  --> {% echo %}
  --> {% liquid %}
  --> {% raw %}

	  --> {% comment %} :Syntaxes 
	      Prevents an expression from being rendered or output. Any text inside comment tags won't be output, and any Liquid code will be parsed, but not executed. Learn more
	      -- Syntax :
	         {% comment %}
			  content
		    {% endcomment %}
	         
	  --> {% echo %} :
	      Outputs an expression. Learn more
	      -- Syntax :
	         {% echo product.title %}
				{% liquid
				  echo product.price | money
				%}
		    ---------------------
		    Health potion

		    $10.00

	  --> {% liquid %} :
	      Allows you to have a block of Liquid without delimeters on each tag. Learn more
	      -- Syntax :
	         {% liquid
			  # Show a message that's customized to the product type
			
			  assign product_type = product.type | downcase
			  assign message = ''
			
			  case product_type
			    when 'health'
			      assign message = 'This is a health potion!'
			    when 'love'
			      assign message = 'This is a love potion!'
			    else
			      assign message = 'This is a potion!'
			  endcase
			
			  echo message
			%}
	        -----------------------------
	        This is a health potion!

	  --> {% raw %} :
	      Outputs any Liquid code as text instead of rendering it. Learn more
	      -- Syntax :
	         {% raw %}
			  {{ 2 | plus: 2 }} equals 4.
		    {% endraw %}
		-------------------
		{{ 2 | plus: 2 }} equals 4.    


  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  


