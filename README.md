# test-devops-site
The site for test-devops. (based on Hugo)

- dev: [http://dev.kaleo.run](http://dev.kaleo.run)
- staging: [http://staging.kaleo.run](http://staging.kaleo.run)

## How it works?

This repo has 3 branches:

- `master`: the post data (markdown files) and site config file.
- `dev-gh-pages`: pages for dev site.
- `staging-gh-pages`: pages for staging site.

`*-gh-pages` has only the files built by Hugo.


To publish this site:

1. Create a new post.
2. Update the config file, such as replacing `baseurl` from `http://kaleo.run` to `http://dev.kaleo.run`, upgrading `version`.
2. Create `public` dir and checkout `*-gh-pages` into it (use `git worktree add`).
3. Use Hugo to build.
4. Commit and push both `master` and `*-gh-pages`.
5. Pull `*-gh-pages` to the web server.
