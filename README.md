# Statamic

## Pages
In the control panel under the collections tab, there will be a collection with pages already made and by default there is a ‘home’ page. You are able to enter in content on this page and select a template to use.

In VScode there will be templates such as ‘home.antlers.html’ and this will be an html file template that is already there but what it is essentially is an html template. 

In the Statamic dashboard, you are able to select one of these templates that you created in VScode. If there is content that is entered inside of the dashboard you can grab that data from statamic and use it inside of your html template with the `{{ }}` In the default home page template, the textarea box is named content which is also the variable used to extract info from statamic and to use within your html template. 

## Partials
You can add another partial template into another partial by this syntax `{{ partial: [partial filename] }}`, ignore the brackets when implementing this, also, the file name is imported will follow this naming convention: ‘_nav.antlers.html’

## Blueprint
- It looks like you’re able to create a mock up of the desired ‘form’ essentially. A blueprint is an instance of something and what makes up a blueprint is fields, that’s the content that will be inside of each blueprint. Think of blogposts. You’ll have a collection of blog which are blog posts and the blueprint of each blog post will have an author, content, picture, etc. 

## How to loop
1. You will need to reference what you want to loop so if you want to loop a blog collection you will insert this in your partial. `{{ collection:blog }}`, note that you will need a closing tag. This acts as a tag. `{{ /collection:blog }}`
2. Once you have done the first step you are able to just access the variables that make up a blog. So like the url, title…will just be accessed as `{{ url }}`

When creating a blueprint, you are essentially creating fields that make up that blueprint, in this case what a blog post will have/look like. So the variables that you’re using in this loop will be those ‘fields’ that you created for the blueprint. 

## Paginate
1. In the opening tag of what you want to loop you will include a paginate attribute and set it to the number of instances that you want to allow per page. Include an ‘as’ attribute so that you can specify what each instance will be called as. 
2. You will then create an opening and closing tag with the ‘posts’ name and insert the html content that you wish inside of the tags. 
3. You will need to include the pagination after this. And this will be following the closing tag of ‘posts’