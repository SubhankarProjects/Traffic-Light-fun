# Traffic Light Project

This project is a simple web-based traffic light created using HTML and CSS.

## HTML (`index.html`)

**Recommendation:**

* **Add IDs for JavaScript Interaction:** For dynamic behavior with JavaScript, add unique `id` attributes to each light `div`.

    ```html
    <div class="red" id="redLight">RED</div>
    <div class="yellow" id="yellowLight">YELLOW</div>
    <div class="green" id="greenLight">GREEN</div>
    ```

## CSS (`style.css`)

**Recommendations:**

* **Text Centering within Circles:** For consistent vertical centering within light circles, consider:

    * **Flexbox (on light elements):**

        ```css
        .red, .yellow, .green {
            /* ... other styles ... */
            display: flex;
            justify-content: center;
            align-items: center;
        }
        ```

    * **Adjusting Padding:** Experiment with equal top and bottom padding on light elements.

* **Initial "Off" State:** For realism, start with inactive lights, controlling active state with JavaScript. Achieve this by:

    * **Lowering initial `opacity`:**

        ```css
        .red, .yellow, .green {
            /* ... other styles ... */
            opacity: 0.3;
        }
        ```

    * **Using darker initial background colors:** Change to bright colors with JavaScript.

* **Consistent Styling with Common Class:** Improve organization using a common `.light` class for shared styles, with specific classes for background colors.

    ```css
    .light {
        height: 80px;
        width: 80px;
        margin: 10px auto;
        border: 2px solid white;
        border-radius: 50px;
        /* Add other common properties here */
    }

    .red.light {
        background-color: red;
    }

    .yellow.light {
        background-color: yellow;
    }

    .green.light {
        background-color: green;
    }
    ```

    **Update HTML:**

    ```html
    <div class="red light" id="redLight">RED</div>
    <div class="yellow light" id="yellowLight">YELLOW</div>
    <div class="green light" id="greenLight">GREEN</div>
    ```

* **Improved Color Contrast for Yellow Light:** Change yellow light text color to black for better readability.

    ```css
    .yellow {
        /* ... other styles ... */
        color: black;
    }
    ```
