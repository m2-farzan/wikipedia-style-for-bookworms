# Preview
![Preview Image](https://raw.githubusercontent.com/m2-farzan/wikipedia-style-for-bookworms/master/preview.jpg)

# Introduction
I'm not a web designer, nor a typography expert. So most of what follows are mostly my personal opinions. I'm a bookworm. I spend a fair amount of time reading books and e-books but when it comes to Wikipedia, I've caught myself just skipping through the lines, never reading anything carefully.

I know that Wikipedia articles come naturally less consistent compared to actual books. But I think poor visual styling is also a disturbing factor. Those 250-character long lines, written in a sans-serif font, with a mess of blue-colored words here and there that emphasize unimportant parts of the sentence, and so on. Again, I'm not a web designer but come on!

Fortunately, Wikipedia can be totally customized after logging in. So if you're ready to have a bookwormish Wikipedia experience, follow these steps.

# Steps
- Login in to your account.
- Go to your preferences page https://en.wikipedia.org/wiki/Special:Preferences
- Go to tab *Appearance*
- Select *MinervaNeue* Theme.
- In the line after *Shared CSS/JavaScript for all skins:* select *Custom CSS*
- Start creating/editing the page
- Enter the following CSS into the page:
    ```
    /* rest */
    @font-face {
      font-family: 'medium-content-serif-font';
      font-weight: 700;
      font-style: normal;
      src: url('https://glyph.medium.com/font/f50d520/3k-4f_4h-6bt_6bv-6c3_6c5-6c7_6ca-6cb_6ce-6ch_6cj-6cl_6cn-nvnj/charter-700-normal.woff') format('woff');
      unicode-range: U+80-9F,U+A1-2009,U+200B-2013,U+2015-2017,U+201A-201B,U+201E-2021,U+2023-2025,U+2027-10FFFF;
    }

    /* rest */
    @font-face {
      font-family: 'medium-content-sans-serif-font';
      font-weight: 400;
      font-style: normal;
      src: url('https://glyph.medium.com/font/d8659c9/3k-4f_4h-6bt_6bv-6c3_6c5-6c7_6ca-6cb_6ce-6ch_6cj-6cl_6cn-nvnj/marat-sans-400-normal.woff') format('woff');
      unicode-range: U+80-9F,U+A1-2009,U+200B-2013,U+2015-2017,U+201A-201B,U+201E-2021,U+2023-2025,U+2027-10FFFF;
    }

    body {
        font-family: "medium-content-serif-font";
        font-size: 21px;
        font-style: normal;
        letter-spacing: -0.003em;
        line-height: 32px;
    }
    .header-container.header-chrome {
        background-color: #eaecf0 !important;
        border: 0 !important;
        box-shadow: inset 0 -1px 3px rgba(0, 0, 0, 0.08) !important;
    }
    a:link {
        color: #000000;
    }
    p > a:link {
        color: #000000;
        font-family: 'medium-content-serif-font';
        font-weight: 700;
        font-style: normal !important;
    }
    a:visited {
        color: #000000;
    }
    a:hover {
        color: #000000;
    }

    a:active {
        color: #000000;
    }
    .content {
        max-width: 47em;
    }
    .header-container.header-chrome {
        background-color: #e9eaa4;
    }
    .anonymous-show {
        display: none !important;
    }
    div.user-show,
    p.user-show {
        display: block !important;
    }
    span.user-show,
    small.user-show {
        display: inline !important;
    }
    table.user-show {
        display: table !important;
    }
    li.user-show {
        display: list-item !important;
    }
    ```
- Save the page
- Reload (Hold *Shift* and click browser reload button. This will load the new style.)
- Enjoy! If you know CSS, you can tune the page down to the last nuts and bolts. BTW, if you find any problem caused by this CSS or can improve it, don't hesitate. Just create an issue or pull request.

Extra tips:
- Go to your browser settings and set a respectable font as your default serif font! *Times New Roman* is an old friend but give others a chance. Your eyes will thank you. I'm using *Noto Serif* from Google.
- You can use the great extension *Dark Reader* that enables you to read any page in night mode.
