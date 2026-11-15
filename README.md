# BookHaven

BookHaven is a simple HTML5 digital book catalog created for the Software Development Practices Staff Graded Assessment 2. It demonstrates a disciplined Git workflow and documents a login-system test design.

## Features

- Semantic HTML5 catalog landing page.
- Featured Books list: *The Great Gatsby*, *1984*, and *Atomic Habits*.
- About page with Contact & Support information.
- Git history with `main`, `feature`, a merge commit, ignore-rule verification, and a safe revert.

## Project Structure

```text
BookHaven/
├── index.html
├── about.html
├── .gitignore
├── git_commands.txt
├── README.md
└── BookHaven_Assignment_Report.pdf
```

Ignored verification files are `debug.log` and `temp/cache.txt`.

## Verified Commit Graph

```text
*   c405971 Merge feature branch
|\
| * 5959b83 Add contact and support section
|/
* 42fddfb Add featured books catalog
* d71228e Initial BookHaven catalog
```

The later commits add `.gitignore`, a temporary file commit, its revert, and this documentation.

## Login System Test Case Design

| Test Case ID | Test Scenario | Input Data | Expected Output |
|---|---|---|---|
| TC_01 | Valid Login | Username="user1", Password="password123" | Login successful; redirected to user dashboard. |
| TC_02 | Boundary: Exact 6 Characters | Username="user1", Password="pass12" (length = 6) | Login successful; minimum character requirement met. |
| TC_03 | Invalid Username | Username="unregistered_user", Password="password123" | Login denied; Error message displayed: "Invalid username or password". |
| TC_04 | Invalid Password | Username="user1", Password="wrongpassword" | Login denied; Error message displayed: "Invalid username or password". |
| TC_05 | Boundary: Less than 6 Characters | Username="user1", Password="12345" (length = 5) | Form submission blocked; Validation message displayed: "Password must be at least 6 characters long". |
| TC_06 | Edge Case: Empty Username | Username="", Password="password123" | Form submission blocked; Validation message displayed: "Username must not be empty". |
| TC_07 | Edge Case: Empty Password | Username="user1", Password="" | Form submission blocked; Validation message displayed: "Password must not be empty". |
| TC_08 | Security: Account Lockout | Username="user1", 3 consecutive failed login attempts | Account locked; Error message displayed: "Account locked due to 3 consecutive failed login attempts. Please try again after 15 minutes." |

## Remote Preparation

The repository has not been pushed. After creating the public GitHub repository, run the commands shown in `git_commands.txt` to add `origin` and push both branches.
