# Hello World

 # h1 Heading 😎
 ## h2 Heading
 ### h3 Heading
 #### h4 Heading
 ##### h5 Heading
 ###### h6 Heading


 ## Horizontal Rules

 ___

 ---

 ***


 ## Emphasis

 **This is bold text**

 __This is bold text__

 *This is italic text*

 _This is italic text_

 ~~Strikethrough~~


 ## Blockquotes


 > Blockquotes can also be nested...
 >> ...by using additional greater-than signs right next to each other...
 > > > ...or with spaces between arrows.


 ## Lists

 Unordered

 + Create a list by starting a line with `+`, `-`, or `*`
 + Sub-lists are made by indenting 2 spaces:
   - Marker character change forces new list start:
     * Ac tristique libero volutpat at
     + Facilisis in pretium nisl aliquet
     - Nulla volutpat aliquam velit
 + Very easy!

 Ordered

 1. Lorem ipsum dolor sit amet
 2. Consectetur adipiscing elit
 3. Integer molestie lorem at massa


 1. You can use sequential numbers...

 Start numbering with offset:

 57. foo
 1. bar

## Code

Indented code

    // Some comments
    line 1 of code
    line 2 of code
    line 3 of code


Block code "fences"

```
Sample text here...
```

Syntax highlighting

```js
var foo = function (bar) {
  return bar++;
};

console.log(foo(5));
```

# Nix
```nix
devShells.default = devenv.lib.mkShell {
  inherit inputs pkgs;
  modules = [
    {
      name = "jmfv-portfolio";
      # name = pname;
      languages.javascript = {
        enable = true;
        package = pkgs.nodejs_20;
        corepack.enable = true;
      };
      packages = with pkgs; [ chromium ];
      env = with pkgs; {
          PUPPETEER_SKIP_DOWNLOAD = true;
          PUPPETEER_EXECUTABLE_PATH = "\${chromium}/bin/chromium";
      };
    }
  ];
};
```

[i am a link](https://www.google.com)

