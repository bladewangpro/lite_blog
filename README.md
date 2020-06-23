# Lite Blog

> lite version of personal blog, provide features of categories and post.

Coding for this website give me more details about operation process of Jekyll, liquid, HTML and CSS.

## Notice

1. {{ page.content | markdownify | liquify }} will tell Jekyll to show web content with markdown and liquid code snippet.
2. Under _layout directory, try to use {{ content }} instead of {{ page.content }} in template HTML. I am not sure about inside logic of this problem.
