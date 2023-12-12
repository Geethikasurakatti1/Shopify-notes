1.What is shopify?
2.shopify used for?
3.Major difference between shopify and Amazon?
4.How many types of ecommerce businesses do we have?
5.what is liquid?
6.shopify pricing?
7.core aspects of shopify admin for business?
8.shopify admin by using the sidebar?
    1.Home
    2.Order 
        Drafts 
        Abandoned checkouts
    3.products 
        Inventory
        Transfers
        Collections
        Gift Cards
        Price lists
    4.Customers
        companies
    5.Analytics
        Reports
        Live view
    6.Marketing
        campaigns
        Automations
    7.Discounts
    8.Online Store
        Themes
        Blog posts
        Pages
        Navigation
        Preferences
    9.Settings 
        1.Store details
        2.Plan
        3.Billing
        4.Users and Permissions
        5.Payments
        6.Checkout and accounts
        7.Shipping and delivery
        8.Taxes and duties
        9.Locations
        10.Gift Cards
        11.Markets
        12.Apps and Sales Channels
        13.Domains
        14.Customers Events
        15.Brand
        16.Notification
        17.Meta Fields
        18.Files
        19.Language
        20.Policies
9.Payments Status
   1.Pending
   2.Expiring
   3.Refunded
   4.Voided
   5.Authorized
   6.Expired
   7.Partially Refunded
   8.unpaid
   9.overdue
   10.paid
   11.Partially paid
10.Fulfillment Status
   1.Fulfilled
   2.Unfulfilled
   3.Partially Fulfilled
   4.Scheduled
   5.Onhold
11.Shopify URL structures
12.Collections
   Two types
   1.Automated Collections
   2.Manual Collections
13.Sales Channels
   1.Shop
   2.Facebook
   3.Buy Button
   4.Instagram
   5.Shopify Inbox
   6.Wholesale Channels
   7.HandShake
14.Discounts
15.Blogs
16.Pages
   1.Product Pages
   2.Collection Pages
   3.Collection List Pages
   4.Blog pages
   5.Blog Post Pages
   6.Cart Page
   7.Password Page
   8.404 Page
   9.Search Page
17.Navigation
   1.Main menu
   2.Footer menu
18.Section Can contain 3 Main types of Content
   1.Main Content
   2.Assets 
   3.Section Schema
     1.Name
     2.Tag
     3.Class
     4.Limit
     5.Settings
     6.Blocks ------ type
     7.max-Blocks
     8.presets
     9.Default
19.Section Object
   1.type
   2.Setting
   3.Blocks
20.Scheme Settings
    1.Input settings
    2.sidebar settings
21.Iteration Tag
   cycle         reversed    cyclegroup
   cycle group   break       for
   continue      limit       table row
   offset        cycle

22.Variable Tag
   assign
   increment
   decrement
   capture
   assign
   capture

23.Theme Tag
  include       includewith      render      renderwith         section             raw      layout 
  layoutname    paginate         schema      stylesheet         stylesheet_scss

24.Money filters
money
money_with_currency
money_without_trailing_zeros
money_without_currency

25.Layout
26.Templates
27.Sections
28.Snippets
29.Assets
30.Config
31.Local
32.Shopify Theme Editor
33.Shopify theory Questions
34.Collection filtering & sorting
35.Email consent
36.Recently Viewed products
37.Product Recommendations
38.Product upselling

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


