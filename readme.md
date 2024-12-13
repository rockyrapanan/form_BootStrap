# Form with Validation

This project demonstrates a simple form with validation using Bootstrap's grid layout and validation states. The form includes fields for Name, Email, and Message, a radio button group for how the user found the site, and a dropdown for the reason for contacting. The form is styled with Bootstrap and includes utility classes for margins, padding, and responsive styling.

## Features

- Name, Email, and Message fields (all required)
- Radio button group asking how the user found the site
- Dropdown for the reason for contacting
- Bootstrap grid layout and validation states
- Pre-populated table with hard-coded values to simulate collected data
- Utility classes for margins, padding, and responsive styling

## Technologies Used

- HTML
- Bootstrap 4.5.2

## Usage

To use this form, simply open the `forms.html` file in your browser. Fill out the required fields and submit the form. The form includes validation to ensure all required fields are filled out correctly.

## Code Example

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Form with Validation</title>
    <link href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css" rel="stylesheet">
</head>
<style>
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
</style>
<body>
    <div class="container mt-4">
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
    </div>
</body>
</html>
```

## License

This project is licensed under the MIT License.