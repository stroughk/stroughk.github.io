---
layout: post
title:      "My First CLI Project at Flatiron"
date:       2019-07-14 19:41:27 +0000
permalink:  my_first_cli_project_at_flatiron
---


    At the end of the Object-Oriented Ruby unit, we were required to create a new command-line interface data gem for Flatiron School’s Online Web Developer program. The objective of this Ruby gem was to provide a CLI to an external data source. What an exciting opportunity it was to put everything together we learned thus far and apply our knowledge into creating an actual program that we build from scratch!

    For a long time I was in a planning phase and could not decide which website I would like to use. The task of scraping a website using Nokogiri was overwhelming at first. I did not want to start building a program until I was confident that I landed on a scrapable site. I tested out a few sites that came to mind. I used Repl to play around with Nokogiri and try to parse and search for specific data on various sites. After a few tests, I decided to build my gem on a fairly easy site https://millercenter.org/president.

    I liked how I could easily select the whole block of presidents and then use Nokogiri to parse html and extract specific data about presidents’ names, inauguration and end of presidency dates. Thus, my new Ruby gem ‘US_Presidents’ was born! 

    Next step was creating a Gem in the Learn IDE. This was the easiest part of the project. All I had to do was to type  ‘bundle gem us_presidents” in my IDE and hit enter. The frame of the gem was automatically created for me with all the basic files I needed. After a few adjustments such as renaming the ‘us_presidents’ file to ‘environment’ file, adding a ‘cli’, ‘scraper’ and ‘story’ files, it was time to test to ensure that my program was working. I created a simple code in my lib directory to put out a phrase “It’s working!” and was testing the executable bin file to ensure that it can run the code. I had to add the shebang line in the executable file to ensure that this code provided the shell (BASH) with the absolute path to the Ruby interpreter. I called the CLI class and provided a path to the lib/environment file. I also needed to add a few dependencies gemspec files and require relative in my environment files. 

    Once I was able to see the “It’s working!” phrase on the console, I created a new repository on GitHub so I would not lose my code. I used this regularly throughout my project to commit and push my code up to the cloud as I was making progress. 

    Now, I could confidently move on to my next and the most challenging part of my project – building the actual program. After watching several tutorial videos from Flatiron’s video archives, I understood well that I needed to separate my classes and give each class its own functionality and responsibility to do something. My CLI class was responsible to interact with the user, my Scraper class was responsible for scraping data from external source, while my Story class was responsible to store data about the US presidents and provide functionalities for them. 
After many days of brainstorming, debugging, testing, and perfecting, my program was finally working! 

    The result of my program was this: the user is greeted with a welcome message and an image of an American flag. The user is given a list of all US presidents listed with an index and is asked to pick one of the presidents by typing the number. Once the user selected a president, a quick information was displayed to the user. Then the user is prompted if they would like additional information on the same president. If user typed in ‘YES’, then more detailed information was displayed. The user then had a choice to either list the presidents again or exit the program. The program also had anti-error built in features when the user typed in something other than what they were asked. The program would throw an error message “Invalid input” and ask the user to enter the correct information instead. Since I used a patriotic theme for my program, I utilized the 'colorize' gem to display my program in red, white and blue.

    Overall, this was a great challenge to me as a beginner in coding. I am incredibly proud of myself for being able to create this project and can’t wait to see what other more complex programs I will build in the future. Until the next time…

https://github.com/stroughk/us_presidents






