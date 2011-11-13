!SLIDE[tpl=title]
# Fancy Showoff with Templates #

~~~CONFIG:author~~~

November 2011

!SLIDE bullets incremental
# Showoff is great! #

* styling is complex
* no templates

!SLIDE 

# Showoff Templates #

* provide an easy way out
* can be configured per slide


!SLIDE center

# Activate Template #

	!SLIDE[tpl=special]
	
!SLIDE

# Default Template #

Default templates are used if no additional parameter is supplied,
templates are configured in the `showoff.json`. All paths are relative.

    @@@ javascript
    {
       "templates" : {
           "special" : "mytpl.tpl"
       }  
       /* ... */
    }

!SLIDE smbullets left

# Template Expressions #

Content markers can be replaced by special values identified by a triple `~`:

* `NUM_SLIDES` - total number of slides
* `CURRENT_SLIDE` - current slide number
* `CONFIG:*` - any configuration value from `showoff.json`

!SLIDE 

# Template Example - title#

!SLIDE code small

    @@@ html
    <div class="hpitemplate">
         <div class="redbarhor"><br /></div>
         <div class="redbarvert"><br /></div>
         <div class="yelbarhor"><br /></div>
         <div class="yelbarvert"><br /></div>
    </div>
    <div class="title">
        ~~~CONTENT~~~
    </div>


!SLIDE 

# Template Example - default#

!SLIDE code small

    @@@ html
    <div class="hpidefault">
       ~~~CONTENT~~~
    </div>
    <div class="lefter">
         <div class="redbarhor"><br /></div>
         <div class="redbarvert"><br /></div>
         <div class="yelbarhor"><br /></div>
         <div class="yelbarvert"><br /></div>
         <div class="pages">
	     ~~CURRENT_SLIDE~~~ / ~~NUM_SLIDES~~~
	 </div>
    </div>
   

!SLIDE

# Attention #

Replacement marker is a tripple `~`, the previous slides used a double `~` to avoid replacement...

!SLIDE

# Thanks #

