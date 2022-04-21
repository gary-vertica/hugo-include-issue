# hugo-include-issue
Reproducer of issue with including a MarkDown file using an include shortcode.

The appearance of the code example changes depending on whether you view the directly-rendered file (`_includes/included.md`) or the same file included via a shortcode. When viewed directly, the example code in the `included.md` file appears correctly. However, when this file is included in `regular_page.md`, part of the exampel code seems to be have interprested as a heading. 

The include shortcode was [published in the Hugo Discourse thread](https://discourse.gohugo.io/t/include-file-shortcode-for-including-files-with-shortcode-calls/16699). I've modified this code a bit, but the basic core functionality (use .GetPage to get the content of the included file and then render it via markdownify) is the asme. I've played with the code a bit, using RenderString instead of markdownify. That shows teh same result.

