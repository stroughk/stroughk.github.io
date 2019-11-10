---
layout: post
title:      "Smartdesk - Rails Application"
date:       2019-11-10 20:48:31 +0000
permalink:  smartdesk_-_rails_application
---


As we moved from Sinatra to Rails, I kept reading about how “magical” Rails was. Not having much programming background and haven’t used any other MVC framework before, I did not have a sense of reference whether this statement was true or not. I personally found working in Rails quite challenging. Since we were not able to use scaffold for our project (which is truly magical), I had to truly think through each step while building this project. In the beginning, the implicitness of controllers was a bit confusing to me. I got used to it overtime that I don’t have to specifically render the views but Rails knows what to do as long as the files are named the proper way.  

There were quite a few requirements added for this project. I had to include many-to-many associations, reasonable validations for simple model objects, a class level ActiveRecord scope method, nested resources, login and logout via third party, and many more.  

I decided to create a help desk ticket tracker and named it Smartdesk. This application is a great tool to keep track of Smartdesk tickets submitted by users. Users have the option to select a category before submitting a ticket. Once Smartdesk agents complete the tickets, they are marked as 'completed'. Smartdesk agents have the capability to edit and delete users and their tickets. Although, users can see other users' tickets, they only have the option to create, edit and delete their own tickets.

There were quite a few challenges on the way. I literally had to go back to our curriculum, scroll through numerous postings on stackoverflow.com, Youtube and Google my way though to finish building this project. I received much needed support and encouragement from my Flatiron instructor – Michael. At the end, the project came together by the deadline. I did my best to keep it DRY using partials and helper methods throughout my project. I used Bootstrap and CSS for styling.  

You can take a look at my project at this link on Github: https://github.com/stroughk/smartdesk and/or watch the demo of it on Youtube: https://www.youtube.com/watch?v=sidlc9OkF_0

