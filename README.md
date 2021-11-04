# Counter

A counter app that uses Test Driven Development.

|                                         |                                         |                                                   |
| :-------------------------------------: | :-------------------------------------: | :-----------------------------------------------: |
|        [Introduction](#counter)         | [Table of Contents](#table-of-contents) | [Development Highlights](#development-highlights) |
|      [Installation](#installation)      |    [Page Directory](#page-directory)    |       [Code Hightlights](#code-highlights)        |
| [Technologies Used](#Technologies-Used) |           [Credits](#Credits)           |                [License](#License)                |

## Development Highlights

- Create tests to make sure the text content is correct.
- Create tests for the functionality of the counter
- Add `beforeEach` to reuse creating the component for each test.
- Use fireEvents from test library.

## Installation

Install dependencies.

```
npm i
```

Start app.

```
npm start
```

## Page Directory

A `__test__` folder is created within the component to be tested.

## Code Highlights

Render the counter component before each test.

```JavaScript
beforeEach(() => {
    const component = render(<Counter />)
    getByTestId = component.getByTestId
})
```

Testing that the values can be changed. `5` is used as the example of what the value is being changed to.

```JavaScript
test('change value of input works correctly', () => {
    const inputEl = getByTestId('input')

    expect(inputEl.value).toBe('1')

    fireEvent.change(inputEl, {
        target: {
            value: '5'
        }
    })

    expect(inputEl.value).toBe('5')
})
```

## Technologies

- @testing-library](https://reactjs.org/docs/testing.html)

## Credits

The React testing [tutorial](https://www.youtube.com/watch?v=GLSSRtnNY0g) by Laith Harb.

|                           |                                                                                                                                                                                                       |
| ------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **David Anusontarangkul** | [![Linkedin](https://i.stack.imgur.com/gVE0j.png) LinkedIn](https://www.linkedin.com/in/anusontarangkul/) [![GitHub](https://i.stack.imgur.com/tskMh.png) GitHub](https://github.com/anusontarangkul) |

## License

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/)
