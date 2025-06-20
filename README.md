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

After some prodding, I found that the paragraph (<p>) element next to the icons were giving themselves margins that would forcibly expand the grid cell height, thus why the grid kept overflowing. For whatever reason, the "margin:0" I had on the ":root" did not apply here so I just had to manually do so onto the <p> element. 