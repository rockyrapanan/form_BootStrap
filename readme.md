# Form with Validation

This project demonstrates a form with validation using Bootstrap's grid layout and validation states. The form includes fields for Name, Email, and Message, a radio button group for how the user found the site, and a dropdown for the reason for contacting. The form is styled using Bootstrap and includes utility classes for margins, padding, and responsive styling.

## Features

- **Form Fields**:
    - Name (required)
    - Email (required)
    - Message (required)
    - Radio button group for how the user found the site (required)
    - Dropdown for the reason for contacting (required)

- **Styling**:
    - Bootstrap grid layout
    - Validation states
    - Utility classes for margins, padding, and responsive styling

- **Navbar**:
    - Links to Home, About, and Contact sections
    - Collapses into a hamburger menu on smaller screens

## Usage

1. **Clone the repository**:
     ```bash
     git clone <repository-url>
     ```

2. **Open the `forms.html` file in your browser** to view the form with validation.

## Dependencies

- [Bootstrap 4.5.2](https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css)

## Code Overview

### HTML Structure

- **Navbar**:
    ```html
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
            <a class="navbar-brand" href="#">Navbar</a>
            <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                    <ul class="navbar-nav">
                            <li class="nav-item active">
                                    <a class="nav-link" href="#">Home</a>
                            </li>
                            <li class="nav-item">
                                    <a class="nav-link" href="#">About</a>
                            </li>
                            <li class="nav-item">
                                    <a class="nav-link" href="#">Contact</a>
                            </li>
                    </ul>
            </div>
    </nav>
    ```

- **Form**:
    ```html
    <form>
            <div class="form-group">
                    <label for="name">Name</label>
                    <input type="text" class="form-control" id="name" name="name" required>
                    <div class="invalid-feedback">
                            Please enter your name.
                    </div>
            </div>
            <div class="form-group">
                    <label for="email">Email</label>
                    <input type="email" class="form-control" id="email" name="email" required>
                    <div class="invalid-feedback">
                            Please enter a valid email address.
                    </div>
            </div>
            <div class="form-group">
                    <label for="message">Message</label>
                    <textarea class="form-control" id="message" name="message" rows="3" required></textarea>
                    <div class="invalid-feedback">
                            Please enter a message.
                    </div>
            </div>
            <div class="form-group">
                    <label>How did you find our site?</label>
                    <div class="form-check form-check-inline">
                            <input class="form-check-input" type="radio" name="found" id="search" value="search" required>
                            <label class="form-check-label" for="search">Search Engine</label>
                    </div>
                    <div class="form-check form-check-inline">
                            <input class="form-check-input" type="radio" name="found" id="social" value="social" required>
                            <label class="form-check-label" for="social">Social Media</label>
                    </div>
                    <div class="form-check form-check-inline">
                            <input class="form-check-input" type="radio" name="found" id="friend" value="friend" required>
                            <label class="form-check-label" for="friend">Friend</label>
                    </div>
                    <div class="invalid-feedback d-block">
                            Please select an option.
                    </div>
            </div>
            <div class="form-group">
                    <label for="reason">Reason for contacting us</label>
                    <select class="form-control" id="reason" name="reason" required>
                            <option value="" disabled selected>Select a reason</option>
                            <option value="question">Question</option>
                            <option value="compliment">Compliment</option>
                            <option value="complaint">Complaint</option>
                    </select>
                    <div class="invalid-feedback">
                            Please select a reason.
                    </div>
            </div>
            <button type="submit" class="btn btn-primary">Submit</button>
    </form>
    ```

### CSS Styling

- **Button Styling**:
    ```css
    button {
            transition: background-color 0.3s, color 0.3s;
    }

    form:valid button[type="submit"] {
            background-color: #28a745;
            color: #fff;
            border-color: #28a745;
    }

    form:valid button[type="submit"]:hover {
            background-color: #218838;
            border-color: #1e7e34;
    }
    ```

## License

This project is licensed under the MIT License.
