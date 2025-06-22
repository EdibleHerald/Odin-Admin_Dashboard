# Odin-Admin_Dashboard

This is a project following the cirriculum of [The Odin Project](https://www.theodinproject.com/). You can find the project details [here](https://www.theodinproject.com/lessons/node-path-intermediate-html-and-css-admin-dashboard)

## Issues

#### Issue 1:

When attempting to make sidebar icons and text smaller, the grid refuses to shorten each grid row for whatever reason. I am using clamp and relative measurements for each item but the grid just overflows instead of forcing the items to be smaller. 

Here is a screenshot of the issue:
![Screenshot of issue](./IssuePicture/Issue1.png)

Here is what I want (more or less):
![Screenshot of preferred layout](./IssuePicture/Issue1ExamplePic.png)

Resolution:

After some prodding, I found that the paragraph (< p >) element next to the icons were giving themselves margins that would forcibly expand the grid cell height, thus why the grid kept overflowing. For whatever reason, the "margin:0" I had on the ":root" did not apply here so I just had to manually do so onto the < p > element. 
UPDATE 6/20/25: Took me far too long to realize that ":root"'s applied "margin:0" do not apply to children without specifying it.  

#### Issue 2:
NO SCREENSHOT

In short, the html element wasn't acknowledging content that didn't seem to be overflowing. I had the right sidebar go under the posts whenever the screen width was <1024px but the sidebar overflowed and because of that, the left sidebar didn't grow to fill the missing space because the html element wouldn't acknowledge the overflow element. 

Solution:
I just accepted this and added overflow: scroll behavior so that the content was still viewable on mobile without looking outright ugly with the white space on the left side. I applied this to the .content-main class where the posts and right sidebar were at. 