---
layout: page
title: "Random Ideas"
---
{% include JB/setup %}

This is a page, where I can list ideas as I have them. Then post links to either the project when I build it, or more likely the link to a existing project when I find someone already implemented it. I might also convert some ideas into blog posts about why I decided it was a bad idea after I researching a project. The ideas here are just brainstorming or quick little thoughts, not full thought out just sentence or two I jot down to refresh my memory or for me to collect related thoughts.

Project Ideas
===

* coverband could collect for this http://tenderlovemaking.com/2015/02/13/predicting-test-failues.html
* pre git commit hook spellcheck, cmd-line likely using aspell or something build in osx 
* Sinatra app that just polls mysql slow and displays it with history etc
* github -> kindle reader format the code for kindle readability and have links / section browsing for the files.
* remote ping pong pair programming over a shared updated git repo or gist.
* combiner allows multiple micro apps / apis to be combined by connecting them feeding one into another JSON can be uploaded or output nice html wysiwyg interface, has a container app for app running.
* google map game... point on a map, red virus starts to spread... survive as long as possible, traveling and trying to be in the last city overtaken by the virus... Like the opposite of pandemic 2
* community chess play as a team. (you make random moves in games with a collective group of people, your score is the aggregate of how many games you win. You never end up making a move in a game against yourself, but you can be in N/2 total games at any time.)
* build something like this but perhaps for stocks or ruby community projects / posts / tweets? http://disqus.com/gravity/
* Test results collector api, just a API that collects test time, speed, # failures, which tests failed, etc and reports over time
* paid version of http://www.free-ocr.com/ using open source OCR tools
* web app that crawls site and finds common errors like mixed content warnings, missing images, broken links, etc, etc
* crawler to find dead CSS
* crawler to find dead JS
* counters app, just tiny up down counters users can create and increment with icons and images private / public, user only or public can increment / decrement
* App that allows you to turn any ruby object into an api call. Preferably with persistence via serialization.
  * look at https://github.com/madx/roy
  * look at http://rubydoc.info/gems/apiary/0.0.5/frames
  * possibly allow JSON
* Improved hash my superhash ideas, and this https://github.com/koleksiuk/parsable_hash and hashie::mash etc
* Small offline mobile app for Safari Bingo
   * generate cards so folks can play bingo while on safari together
   * animals and possible other common things like songs, beer, etc
* Animal recognition (sound, picture, offline)
   * So you can figure out what things are on safari and such
* Safari checklist
   * mark off all the things you see and add things you want to make sure you see before your trip.
* trip itinerary advice per city... custom research based on location, likes, actives, etc... $200 per city.
* webhook reformatter. Often you have a system that sends a webhook in one format, but the system you want to integrate expects a different format. Allow this service to receive one format and convert it to another.
* Scratch That my markdown scratch file and history      

Posts for API reviews
===

* review https://www.codeship.io/
* review nitrous.io 
* review some of the online schools / code academy
* review travis CI
* review https://kraken.io/ image optimization
* review/try http://www.iron.io/ possibly to make ebook https://github.com/harrisj/iron_ebooks 
* Blog post on some work related to the "[ruby-6] Metaprogramming challenge" search email for details but
    * New Relic is looking for another "Ruby Instrumentation Engineer" chellange
    * https://gist.github.com/3631742
    
          Your challenge, should you choose to accept it, is to write a Ruby library that will modify an existing program to output the number of times a specific method is called. 

          You solution library should be required at the top of the host program, or via ruby's -r flag (i.e. ruby -r ./solution.rb host_program.rb)

          Your solution library should read the environment variable COUNT_CALLS_TO to determine the method it should count.  Valid method signatures are Array#map!, ActiveRecord::Base#find, Base64.encode64, etc.

          Your solution library should count calls to that method, and print the method signature and the number of times it was called when the program exits.

          Also, your solution should have a minimal impact on the program's running time.  Sorry set_trace_func"

# Post Ideas
===

A generic, Today I learned: 

To export data from redshift, you can send it to S3

`UNLOAD ('select * from table') TO 's3://redshift-export/table_name_' credentials 'aws_access_key_id=XXX;aws_secret_access_key=XXX';`

If you need to sync data after exporting a bunch of Redshift data you can pull it down using AWS sync.

`aws s3 sync s3://redshift-export .`


Thoughts
===

live cheap
demand what your worth
if you want to spend more
increase your value and worth first

phone camera thought:
 A ring around the lenses that only goes around the lenses. I like not having a case but my camera now sucks show before and after photos of the same nexus model as proof... Also recommend phone makes built something in or support we'll ng them
 
TripAdvisor filters:

you want to be able to filter the reviews to those who have only been to X or more countries (reviewed in X or more). Also a filter to find not super popular. If the avg number of reviews on a restaurant is 30 I want to throw out places with 90+ reviews as clearly they are the major tourist stops, looking for smaller more local food.

also open now as a filter to hide all the restaurants not running available.



The Spreadsheet problem:
  * people love excel because they can get the data and manipulate it to their needs without a dev
  * accuracy, keeping up to date, bugs, data size
  * trying to replace that flexibility in an app means you have to build all the functions people love and need from excel
  * what about google docs hooked to an API? 2-way sync, ability to push results back into the system. Some ability to validate data?
  * could be an interesting compromise to trying to replace a flexible user driven excel process with completely custom software.




Solved Past Ideas
===

* [churn as a tiny app / service run on deferred-servers](http://churn.picoappz.com), I ended up completing this project.
* Better local development environment configuration: 
  * One problem with database.yml if the development configuration file is checked it, it really can't be used for local environment configuration, allow for local overrides. All systems will not be setup the same
  * How to allow better overrides for multiple systems different dev configurations possibly different server deployments?
  * Looks like best solution is [figaro rails configuration](https://github.com/laserlemon/figaro)
* Tiny micro services from people, this is pretty cool [fiverr](http://fiverr.com/)
* Code language detection https://help.github.com/articles/my-repository-is-marked-as-the-wrong-language, I could use this for churn language detection and possibly to break down % of a file that is html, js, CSS
