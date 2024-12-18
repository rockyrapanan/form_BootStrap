# Form with Validation

This project demonstrates a form with validation using Bootstrap's grid layout and validation states. The form includes fields for Name, Email, and Message, a radio button group to ask how the user found the site, and a dropdown for the reason for contacting. The collected data is simulated by pre-populating a table below the form with hard-coded values.

## Features

- **Form Fields**: Name, Email, and Message fields, all required.
- **Radio Button Group**: Asks how the user found the site.
- **Dropdown**: For the reason for contacting.
- **Validation**: Bootstrap's validation states applied to the form.
- **Responsive Layout**: Utilizes Bootstrap's grid layout and utility classes for margins, padding, and responsive styling.
- **Pre-populated Table**: Simulates collected data with hard-coded values.
- **Navbar**: Includes links to Home, About, and Contact sections, collapses into a hamburger menu on smaller screens.
- **Image**: Displays a centered image with rounded corners.

## Technologies Used

- HTML
- Bootstrap 4.5.2

## File Structure

- `index.html`: Contains the form, navbar, and table.

## Form Fields

- **Name**: Text input, required.
- **Email**: Email input, required.
- **Message**: Textarea, required.
- **How did you find our site?**: Radio button group, required.
- **Reason for contacting us**: Dropdown, required.

## Table

The table below the form is pre-populated with the following hard-coded values:

| #   | Name        | Email           | Message          | Found Site     | Reason     |
|-----|-------------|-----------------|------------------|----------------|------------|
| 1   | John Doe    | <john@example.com>| Great site!      | Search Engine  | Compliment |
| 2   | Jane Smith  | <jane@example.com>| I have a question.| Social Media   | Question   |

## Navbar

The navbar includes links to Home, About, and Contact sections and collapses into a hamburger menu on smaller screens.

## Image

A centered image with rounded corners is displayed below the table.

## How to Use

1. Open `index.html` in a web browser.
2. Fill out the form fields.
3. Submit the form to see the validation in action.
4. View the pre-populated table below the form.

## Screenshot

![Form Screenshot](https://dynamic.design.com/asset/logo/f0af4087-ffa7-453c-86f9-c192e14eb165/logo-search-grid-2x?logoTemplateVersion=1&v=638565286469030000)

## License

This project is licensed under the MIT License.
## Example

```html
<!DOCTYPE html>
<html lang="en">
<head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Form with Validation</title>
        <link href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>
        <!-- Navbar -->
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
        <div class="container mt-4">
                <!-- Form with validation -->
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
                <div class="table-responsive mt-4">
                        <table class="table table-striped table-hover table-bordered">
                                <thead class="thead-dark">
                                        <tr>
                                                <th>#</th>
                                                <th>Name</th>
                                                <th>Email</th>
                                                <th>Message</th>
                                                <th>Found Site</th>
                                                <th>Reason</th>
                                        </tr>
                                </thead>
                                <tbody>
                                        <tr>
                                                <td>1</td>
                                                <td>John Doe</td>
                                                <td>john@example.com</td>
                                                <td>Great site!</td>
                                                <td>Search Engine</td>
                                                <td>Compliment</td>
                                        </tr>
                                        <tr>
                                                <td>2</td>
                                                <td>Jane Smith</td>
                                                <td>jane@example.com</td>
                                                <td>I have a question.</td>
                                                <td>Social Media</td>
                                                <td>Question</td>
                                        </tr>
                                </tbody>
                        </table>
                </div>
        </div>
        <div class="container">
                <div class="row">
                        <div class="col-md text-center">
                                <img src="https://dynamic.design.com/asset/logo/f0af4087-ffa7-453c-86f9-c192e14eb165/logo-search-grid-2x?logoTemplateVersion=1&v=638565286469030000" alt="Dynamic Design Logo" class="img-fluid rounded-lg">
                        </div>
                </div>
        </div>
</body>
</html>
```


