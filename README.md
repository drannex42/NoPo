NoPo
====

NoPo - No Post, Allows you to block a specific tagged post from being seen on your tumblr homepage. 
Created by Macleod Sawyer [(link to tumblr here)](http://itsmemacleod.tumblr.com/)

## How to Install: 
##### 1. Go to the theme editor for your blog. 
##### 2. Click on "Edit Theme"
##### 3. Scroll Down till you see <code></ head></code> (trust me its there)
##### 4. Insert the following code:
```css
<style>
.x {
display: none
}

.tagpages .x {
display: block
}

.permapages .x {
display: block
}
</style>
```
(be sure to change 'x' to the tag name you are going to tag the posts to hide from your theme):
##### 5. Now, find the div tag thats directly before the {block:Posts}, For example: 
```
<div id="posts"> <--- THIS RIGHT HERE (commonly called <article> as well)
{block:Posts}
```
('posts' may be called something else depending on the theme)
##### 6. Add the following code:
```
{block:TagPage} class=”tagpages” {/block:TagPage}{block:PermalinkPage}class=”permapages”{/block:PermalinkPage}
```
so it looks similar to this:
```
<div id="(what the id you found in step 5 was)" {block:TagPage} class=”tagpages” {/block:TagPage}{block:PermalinkPage}class=”permapages”{/block:PermalinkPage}>
```
##### 7. Directly after {block:Posts} there is a second div, like this
```
<div class="post">  (commonly called <article> as well)
```
(the value of 'post' may be called something different as well)
##### 8. Add to the 'post' class (or whatever your theme has instead called it) the following:
```
 {block:IndexPage}{TagsAsClasses}{block:IndexPage}
```
so it looks similar to this:
```
 <div class="(whatever you found in step 7) {block:IndexPage}{TagsAsClasses}{block:IndexPage} ">
```
That space between <code>)</code> and <code>{</code> is very important.
### You're done! 

Now anything you tag with the tag you selected in step four in the css will no longer show up on the first page on your blog! (but will show up on permalinks like /post/94769233934/x/, and tagged pages like /tagged/x/!  

## If you use a two+ column theme and the above only loaded one column.

Follow ALL of the above steps and then please continue on: 

In some themes that are 2+ columns we arriver with a bug and as per my usual self, I made a work around, that does just that, it works around the issue instead of fixing it.

##### 9. Right before {block:Posts} paste one of the following:
```
{block:IndexPage}
<div class="(insert whatever you found in step 7)">
<small><a href=""></a></h2></small>
</div>
{/block:IndexPage}
```
or
```
{block:IndexPage}
<div class="(insert whatever you found in step 7)" style="visibility:none;">
<small><a href=""></a></h2></small>
</div>
{/block:IndexPage}
```

### You're done! (hopefully)

If you have any issues please contact me on the issues page on here, on facebook, or on my tumblr (although I may or may not respond on there).

*Follow me on tumblr: http://[ItsMeMacleod](http://itsmemacleod.tumblr.com).tumblr.com* <br>
*Follow me on twitter: twitter.com/[@ItsMeMacleod](http://twitter.com/itsmemacleod)*
