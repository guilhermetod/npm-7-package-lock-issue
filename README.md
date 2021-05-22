# NPM 7 package-lock issue

## Steps to reproduce the problem:

1. Clone the repository within a Windows machine

### Test it with npm v7.x
2. Use npm v7.x and run `npm install`. Verify that line 23 of package-lock is modified with double backslashes, but other references to the same file are not.

### Test it with npm v6.x

3. Change to npm v6.x and run `git checkout . && mv package-lock.json package-lock-v7.json && mv package-lock-v6.json package-lock.json && git add . && npm install`. Verify that package-lock doesn't get modified.
