# orderbird Senior Frontend Tech Challenge

Hey Front End developer. Welcome. Your mission, should you decide to accept it, is to carve out 3 hours and create a SPA using [Laravel](https://laravel.com/), [Tailwind](https://tailwindcss.com/), and your JavaScript library of preference.

The objective of the challenge is to display a table of users. It has to be sortable (both asc. and desc.) by first name, last name, and email address.

The table on the view must be responsive: it should be centered vertically and horizontally on desktop and tablet, with a max. width of `768px`, but occupy the entire screen on mobile devices. Allow horizontal scroll to prevent breaking the rows only when necessary.

## Desired outcome

- It must be a Single Page Application
- Do not use jQuery
- Go all the way with the latest ECMAScript specs (you'll possibly need to update `webpack` config)
- Include tests (at least unit tests)
- Modularize whenever possible, avoid creating files with hundred of lines
- Your submission for this challenge runs without issues nor warnings

## Important!

We hope you can spend about three hours on this project. If you can finish faster, great! If not, limit yourself and don't spend much longer.

You'll need the `WWWUSER` and `WWWGROUP` env vars to set the correct permissions in the docker containers. Either:  
- export them from your shell (inline or in your .\*rc file): `export WWWUSER=${WWWUSER:-$UID} && export WWWGROUP=${WWWGROUP:-$(id -g)}` or
- run `docker-compose` this way: `WWWUSER=${WWWUSER:-$UID} WWWGROUP=${WWWGROUP:-$(id -g)} docker-compose <YOUR_SUBCOMMAND_HERE>`.

## Required steps for a valid solution

1. Create your own base branch, branch out from it by feature, and squash merge back into your base branch when you complete each feature
1. Run the containers for the development environment using `docker-compose`. Running the stack on a non-dockerized environment is not a valid approach  
1. Add Tailwind as a project dependency and use it on the views
1. Write a migration to create ten (10) users with: first name, last name and email address. The migration should be able to rollback
1. Write a seed to populate the users
1. Write a view to display the users data from the database in a table. Fetch the data from `/users`
1. Write a JavaScript solution to sort the users table by any of the fields: you can use any library (React, Vue, etc), but you **can't implement** a pre-made package with this functionality (e.g. [DataTables](https://www.datatables.net/))

## We'll take into consideration:

- Your git commit history:

  The log of the repository should follow [this guideline](https://chris.beams.io/posts/git-commit/). Please read at least [The Seven Rules](https://chris.beams.io/posts/git-commit/#seven-rules) listed in the article and apply them.

- The quality of your code; keep it tidy, linted, and DRY:
  - Use *only* spaces for indentation (no tabs allowed): this repo contains an [editorconfig](https://editorconfig.org/) file, please use it in your editor/IDE 
  - **HTML/Blade**: indent the code with 2 spaces and avoid long lines in the code. You can set one HTML attribute per line (think React style for JSX) and split the values in multiple lines
  - **JavaScript**: use [eslint](https://www.npmjs.com/package/eslint) with the config provided on this repo
  - **PHP**: follow the [PSR-12](https://www.php-fig.org/psr/psr-12/) coding style. [php-cs-fixer](https://github.com/FriendsOfPhp/PHP-CS-Fixer) can help you to enforce this style
  - Keep files and folders unrelated to the project out of the repo: .idea, \*.swp, .vscode, .DS\_Store, vendor, etc. **should not** be commited. Update `.gitignore` if necessary

## Nice to have

- Anything else you would like to add

## When you finish

Please send your solution as a zipped package to [tech-challenge@orderbird.com](mailto:tech-challenge@orderbird.com), **including** your `.git` folder.
