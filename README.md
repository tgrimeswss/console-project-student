# Project: Recreate the console

![Sample](./assets/sample.gif)

### Abstract

At this point, you have some experience with the chrome developer tools, most particularly the **console.** In this project, you will be tasked with making a simple console in terms of the UI (user interface). This means displaying a blinking cursor as well as showing a list of entered commands after a user presses the enter key.

<br>

### Objectives

<table>
  <tr>
    <td><b>Task</b></td>
    <td><b>Detail</b></td>
  </tr>
  <tr>
    <td>Style</td>
    <td>
    - <b>Container</b> needs to be color <b>#1F221E</b>
    <br>
    - <b>Text cursor</b> color needs to be color <b>#F6F6F6</b>
    <br>
    - <b>Text color</b> needs to be color <b>#F6F6F6</b>
    <br>
    - <b>Left arrow</b> needs to be placed on the left side of the input text box
    <br>
    - <b>Input text box</b> should have no border or outline
    </td>
  </tr>
  <tr>
    <td>Functionality</td>
    <td>
    - User should be able to type in the input text box
    <br>
    - Input text should be stored in global state
    <br>
    - Hitting the enter key will append the current state of the text box to a list item displayed underneath the text box
    </td>
  </tr>
</table>

<br>

### Specific directions

#### Part 1/4: Establishing the architecture

1. Create an index.html file inside the root of the directory (console_project)
1. Within the html file, add the simple boiler plate (DOCTYPE, html, head, body, title = **console**)
1. Create a new directory inside the root called **styles**
1. Inside the styles directory, create a new file called **index.css**
1. Link the css file from within the head [How to link an external style sheet](https://www.w3schools.com/css/css_howto.asp)
1. You will notice some additional links in the head. This is installing a special font offered by Google called **Roboto Mono**. Keep this there.
1. Create a new directory inside the root called **scripts**
1. Inside the scripts directory, create a new file called **script.js**
1. Link the script from within the bottom of the body

<br>

#### Part 2/4: Creating the HTML markup

1. Navigate to your **index.html** file

1. Create a new div from inside your body and provide an id attribute named **container** (<div id="container></div>)

1. Inside your "container" div, create two children elements. The first element will be an HTML image tag. Give the image tag three attributes:
   <br>src=**FIND & LINK THE ARROW.PNG FILE** (Link attribute to arrow image)
   <br>alt="Left arrow" (Description attribute of image for screen reader)
   <br>id="left-arrow" (id attribute)

   <br>

1. The second element that is a sibling to your image tag will be a div with an id = "content"

1. Inside the "content" div, there will be two children.

1. This first child will be a textarea element [See here](https://www.w3schools.com/tags/tag_textarea.asp)

1. The textarea will get get an id = "console-input"

1. The second child after the textarea will be an unordered list. Do not add any list elements [See here](https://www.w3schools.com/html/html_lists_unordered.asp)

1. The unordered list will receive an id = "items"

<br>

#### Part 3/4: Creating the style

1. Navigate to your **index.css** file from inside the styles directory you created

1. Provide the following styles to the corresponding elements. <br>

**NOTE**: Some elements are selecting complete html elements (body, li) and some are identifying elements by id

<br>

<table>
  <tr>
    <td><b>Element</b></td>
    <td><b>Style</b></td>
  </tr>
  <tr>
    <td>* <br> (All elements on page) <br> <a href="https://www.w3schools.com/cssref/sel_all.asp">See here</a>
    </td>
    <td>
      - Text color: #f6f6f6 <br>
      - Font family: "Roboto Mono", monospace
    </td>
  </tr>
  <tr>
    <td>body</td>
    <td>
      - Margin: 0 <a href="https://www.w3schools.com/css/css_margin.asp"><em>What is margin?</em></a><br>
      - Background color: #1f221e
    </td>
  </tr>
  <tr>
    <td>li <br> (All list elements)</td>
    <td>
      - List style: none <br>
    </td>
  </tr>
  <tr>
    <td>#container</td>
    <td>
      - Display: flex <a href="https://www.w3schools.com/css/css3_flexbox.asp">See here</a>
    </td>
  </tr>
  <tr>
    <td>#content</td>
    <td>
      - Width: 100% <br>
      - Padding: 10px; <a href="https://www.w3schools.com/cssref/pr_padding.asp">See here</a>
    </td>
  </tr>
  <tr>
    <td>#left-arrow</td>
    <td>
      - Height: 20px <br>
      - Padding: 10px; <a href="https://www.w3schools.com/cssref/pr_padding.asp">See here</a>
    </td>
  </tr>
  <tr>
    <td>#console-input</td>
    <td>
      - Width: 100% <br>
      - Height: 30px <br>
      - Background color: transparent <br>
      - Outline: none <br>
      - Border: none
    </td>
  </tr>
</table>

#### Part 4/4: Creating the functionality (JavaScript)

1. Navigate to your **script.js** file from inside the scripts directory you created

1. Attach a "keyup" listener to the **console-input** element

1. Inside the keyup listener, write the following logic

- If the key pressed is the enter key, clear the input, append a list element child to the "items" unordered list with the current state as the list element content. After hitting enter, both the state and input field must be cleared.

EX: If the user types "Hi my name is" then presses enter, "Hi my name is" will be displayed as a new list element underneath

[HINT: event.code](https://developer.mozilla.org/en-US/docs/Web/API/KeyboardEvent/code)

