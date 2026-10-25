# Assignment 4.1 — Solution: Student Registration Form

## Steps
1. Create `registration.html` and paste the code below.
2. Open it with Live Server.
3. Test: click **Register** with empty fields (the browser shows "Please fill out this field"), then with an invalid email, and finally with valid data.
4. Take a screenshot of the form (optionally one showing a validation message).

## registration.html
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Student Registration Form</title>
  </head>

  <body>
    <main>
      <h1>Student Registration</h1>
      <p>Fields marked with <strong>*</strong> are required.</p>

      <form action="#" method="post">
        <!-- Full Name -->
        <p>
          <label for="full-name">Full Name *</label><br />
          <input type="text" id="full-name" name="full_name" placeholder="Enter your full name" required />
        </p>

        <!-- Email -->
        <p>
          <label for="email">Email *</label><br />
          <input type="email" id="email" name="email" placeholder="you@example.com" required />
        </p>

        <!-- Password -->
        <p>
          <label for="password">Password *</label><br />
          <input type="password" id="password" name="password" minlength="8" placeholder="At least 8 characters" required />
        </p>

        <!-- Phone Number -->
        <p>
          <label for="phone">Phone Number *</label><br />
          <input type="tel" id="phone" name="phone" pattern="[0-9]{10}" placeholder="10-digit mobile number" required />
        </p>

        <!-- Age -->
        <p>
          <label for="age">Age *</label><br />
          <input type="number" id="age" name="age" min="16" max="100" placeholder="Your age" required />
        </p>

        <!-- Submit -->
        <p>
          <button type="submit">Register</button>
        </p>
      </form>
    </main>
  </body>
</html>
```

## Requirements Checklist
| Requirement | Where it is met |
|-------------|-----------------|
| Inside `<form>` | `<form action="#" method="post">` |
| `<label>` for each field | `<label for="...">` matches each input's `id` |
| Correct input types | `text`, `email`, `password`, `tel`, `number` |
| Unique `id` + meaningful `name` | `full-name`/`full_name`, `email`, `password`, `phone`, `age` |
| `required` on mandatory fields | All five inputs |
| Submit button | `<button type="submit">Register</button>` |

## Key Concepts
- **`label for` + `input id`**: link the text to the field; clicking the label focuses the input and screen readers announce it.
- **`type="email"`** validates the email format; **`type="password"`** hides characters; **`type="tel"`** shows a phone keypad on mobile; **`type="number"`** accepts only numbers (with `min`/`max`).
- **`id`** must be unique on the page; **`name`** is the key sent to the server with the value.
- **`required`** blocks submission when the field is empty; **`minlength`**, **`pattern`**, **`min`/`max`** add extra rules.

## Submission
- ✅ `registration.html` (attached)
- 📸 Screenshot of the working form in the browser
