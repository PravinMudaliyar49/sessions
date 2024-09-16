# 2nd Sept '24 session


> "HTML is the easiest to get started with, but the most difficult to master."
>
> — [Kevin Powell](https://www.youtube.com/@KevinPowell)

#### HTML

- Hypertext is a fancy way of saying the text is linked to some other thing like text, pages, websites, etc.
- A markup language is used to present information whereas programming language is used to give instructions to the computer.

#### tags vs elements

- Tags are the most fundamental concept of HTML. It's a container for our content or other HTML tags.
- Element means ``` Opening tag + Content + Closing tag. ```
- In general, the tags are lowercase as recommended by [W3C](https://cbe.anu.edu.au/about/professional-organisations-accreditation/w3c-world-wide-web-consortium#:~:text=The%20World%20Wide%20Web%20Consortium,term%20growth%20of%20the%20Web.).

#### Attributes

- Attributes are used to add more information to the tag. Ex: ```<html lang=”en”>``` which means that the language we’ll use is English.
- Attributes are always specified in the start tag and usually come in name/value pairs.
- ```alt``` for image
  - For an ```<img>``` tag to be valid and best accessible, we need to mention the attribute ```alt```. 
  - It stands for alternate text. 
  - This is handy when a visually paired user is using a screen reader, due to slow internet the image didn’t load, the URL we’re trying to render is invalid, the user disabled the option of loading any image in the browser, SEO, etc.
- ```title``` attribute for tooltip
  - Tooltip is something that gives additional on hovering.
  - Example: [Gabriel](https://www.gabrielny.com/14k-yellow-gold-round-bezel-set-diamond-engagement-ring-er16526r8y4jjj#:~:text=%241%2C450-,Product%20Details,-*All%20engagement%20ring).
  - To build something like this is a bit time-consuming. So for something simpler, we can use the ```title``` attribute.

#### HTML text formatting

- Even though we can have normal text on our webpage, HTML contains several elements for defining text with a special meaning.
- To make the text bold, we have ```strong```.
- Making a text italic means that we’re putting more emphasis. Hence, use ```<em>``` for italic text.
- These will affect the screen reader's tone.
- ```<b></b>``` and ```<i></i>``` do the same. The problem with them is that there’s no meaning or importance behind them and they are just for visual representation.
- Also, there are subscript(H20) and superscript(a^2) tags as ```<sub></sub>``` and ```<sup></sup>``` respectively.

#### Empty elements

- Tags with no closing tags are called Empty elements.
- Ex: ```<br>```, ```<img>```, ```<hr>```
  - ```<hr>``` (horizontal rule) tag is used to display a horizontal ruler for separating contents.
- These are called Empty elements because these elements can't have any contents (unlike, say ```<a>``` or ```<div>```). 
- Therefore there is no syntactic reason why they should need to be closed in HTML.

#### pre tag

- ```<pre>``` tag is used to display text as it is, without ignoring spaces and line breaks.

#### Forms

- One of the most important elements is form. It’s used to collect data from the user.
- As we all know the form element itself acts as a container for different types of input elements such as: text fields, checkboxes, radio buttons, submit buttons, etc.
- The ```<label>``` tag defines a label for many form elements. 
- The ```for``` attribute of the ```<label>``` should be equal to the ```id``` attribute of the ```<input>``` for binding them together, so that the screen reader can figure out that those two are the same.
- The 2 major uses of labels in our form element.
- First, the screen readers will read out loud the label, when the user is focused on the element.
- 💡 **Tip:** The value we put in the id attribute should be unique throughout the page.
- The second importance of labels is that it’s beneficial for users who have difficulty clicking on very small regions (checkboxes or radio buttons)- 
- Because when a user clicks the text within the ```<label>``` element, it toggles the corresponding input (this increases the hit area).
- **H.W**: Importance of the ```name``` attribute.

#### HTML symbol

- Many basic mathematical, technical, and currency symbols, are not present on a normal keyboard.
- In such basic cases, instead of downloading image or SVG, we can use the provided HTML symbols.
- Examples: ```&copy;``` &copy;, ```&trade;``` &trade;, ```&larr;``` &larr;

#### Favicons

- A favicon is a browser icon that represents a brand or website.
- [Favicon generator](https://favicon.io/)
- Add this to the ```<head>```
```html
<link rel="shortcut icon" href="favicon.ico" type="image/x-icon">
```



#### There are many more elements like ```<table>```, but since we rarely use them... it's better to learn them when tackled.
