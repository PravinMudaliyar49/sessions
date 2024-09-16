# 11th Sept '24 session

#### Agenda

> Wrap up the **Specificity** concept.

#### Resources

- [Visual guide to CSS concepts](https://cssreference.io/)
- [Flexbox game](https://flexboxfroggy.com/)
- [Specificity calculator](https://specificity.keegan.st/)
- [Frontend mentor](https://www.frontendmentor.io/)

#### Cascade revision

- Simple definition to remember: _"Last Rule Wins"_.
- The last CSS rule encountered by the browser will be applied to the specified element.
- External stylesheet, internal CSS, and inline styling somewhat follow cascade styling. 
- Remember that internal CSS isn’t more important than external CSS. It’s the order in which they are declared matters. 
- Cuz the inline CSS is the last one.. it is the most effective.

#### Intro to Specificity

- Usually, the styling mentioned at the last wins cuz of **Cascade**.
- But the cascade fails when the specificity is low. 
- Specificity describes how specific our CSS rule is. The more specific we’re, the more important rule will the selectors impose.
- Think of specificity as a score/rank that determines which style declaration is ultimately applied to an element.
- We can calculate the score using the calculator provided above.

#### Specificity calculation

- Start at 0, add 1 for each `element selector`, add 10 for each `class` value (or pseudo-class or attribute selector), 100 for each `ID` value. 
- The universal selector `*` and inherited values have a specificity of 0 and both are ignored!
- `Inline style` gets a specificity value of 1000, and is always given the highest priority!

#### `!important`

- The `!important` rule in CSS is used to add more importance to a rule i.e. to increase specificity of a styling.
- In fact, it even overrides inline stylings.
- Even though `!important` rule overrides everything... only use it in rare unavoidable circumstances. 
- Cuz, it again creates the whole confusing specificity situation when overused

#### User agent stylesheet

- A user agent stylesheet is a pre-defined set of CSS rules that are built into a web browser and applied to web pages automatically. 
- The purpose of the user agent stylesheet is to provide a consistent and standardized visual rendering of HTML elements across different web pages and websites.

#### CSS resets

- Every browser loads a style file called the User-Agent-Stylesheet, which defines default styles for HTML elements. 
- The problem is that different browsers might define different default styles.
- CSS resets were invented to solve this problem.
- Ex: The `* { margin: 0; padding: 0 }` we write at the top. 
    - Since we don't need the default margin-padding applied by the browser.
- There are other popular resets made available by senior developers like **Eric meyer**, [**normalise CSS**](https://necolas.github.io/normalize.css/) (I regularly use for my projects). 

#### Best practices

- Use element selectors for resets, and write them at the top for later overriding. Ex: 
```html
img {
    max-width: 100%;
    object-fit: cover;
}
```
- classes are meant for styling and IDs are meant for JS. 
    - ids are more specific than classes.
    - This makes it styling unbeatable with any use of nested class. 
    - Hence in general, avoid using id for styling as it adds a layer of overriding confusion.
- Apply nested styling consciously, only when necessary.
- Always use `!important` sparingly.

## FAQS

- What happens when two rules targeting the same element have equal specificity?
    - Cascade wins in this case.
- How to override `!important` rule? 
    - With another `!important` rule
- Can 11 classes combined beat a single id?
    - No.
    - IMP gotcha: Like math, the digits don’t carry on to the next place.
    - Can use the specificity calculator to verify this.
```html
#random >> .nothing.something.something.something.something.something.something.something.something.something.something
```
