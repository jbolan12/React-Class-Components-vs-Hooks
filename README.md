# React-Class-Components-vs-Hooks

# React Components Counter App

This React app demonstrates the use of both class-based and functional components to implement a simple counter. Users can increment the counter by clicking a button, showcasing state management in both component types.

## Features

- **Class-Based Component**: Uses `ClassComponent` to implement a counter with class-based state management.
- **Functional Component**: Implements a counter in `FunctionalComponent` using React Hooks for state management.
- **Reusability**: The components are structured to allow easy modification and reuse.

## Files

### `App.jsx`

- The main `App` component renders `ClassComponent`, providing an example of class-based state management.

### `ClassComponent.jsx`

- Implements a counter using a class-based component.
  - `this.state.count` is used to track the counter value.
  - The `increase` method, bound in the constructor, increments the counter and updates the state.
  - Displays the counter value in an `<h1>` element and a `+` button to increment.

### `FunctionalComponent.jsx`

- Implements a counter using a functional component with React Hooks.
  - `useState` manages the counter state.
  - The `increase` function is defined to update the count.
  - Similar structure with an `<h1>` element for displaying the count and a `+` button.

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/jbolan12/React-Class-Components-vs-Hooks.git
    ```
2. Navigate to the project directory:
    ```bash
    cd react-components-counter-app
    ```
3. Install the dependencies:
    ```bash
    npm install
    ```

## Usage

1. Start the development server:
    ```bash
    npm start
    ```
2. Open your browser and go to `http://localhost:3000` to view the app.

## Code Overview

- **State Management**:
  - In `ClassComponent`, state is managed with `this.state` and `this.setState`.
  - In `FunctionalComponent`, `useState` hook provides state management in a functional component.
- **Event Handling**:
  - Both components include a button to increment the counter value, demonstrating different approaches to event handling in React.
 
## Dependencies:
- React: 18.3.1
- React-DOM: 18.3.1
- React-Scripts 5.0.1

  
## License
This project is licensed under the MIT License. See the LICENSE file for details.

### Code Example

#### Class Component Counter

```javascript
class ClassComponent extends React.Component {
  constructor() {
    super();
    this.state = {
      count: 0
    };
    this.increase = this.increase.bind(this);
  }

  increase() {
    this.setState({ count: this.state.count + 1 });
  }
}
