### Issue: [NNNN](https://github.com/ArgDevs/school-admin/issues/NNNN)

### Description

Describe the changes, unless evident from the title.

### TODO:

(if any)
- [ ] ...
- [ ] ...
- [ ] ...

### How to test this PR manually?

- *(Add the steps describing how to test your changes manually)*
- Add any new `.env` variables needed for testing:
  ```ini
  FOO_URL=http://foo.test.com
  ```
- Example **curl** command for testing:
    ```bash
    curl -X POST 'http://localhost:8000/api/v1/foo/' \
    --header 'Authorization: Token xxx' \
    --header 'Content-Type: application/json' \
    --data-raw '{
      "foo": "bar"
    }'
    ```
- Expected result:
    ```json
    {"success":  "ok"}
    ```

### Pre-review checklist

- [ ] Unit / integration tests are updated.
- [ ] Test manually.
- [ ] Verify that PR has clear testing instructions
- [ ] Verify that documentation is updated.
- [ ] Get approval from stakeholders.
- [ ] Verify that feature branch is up-to-date with `main` (if not - rebase it).

### Pre-merge checklist

- [ ] Verify that external dependencies for this commit are fulfilled (eg: new env setup is complete)
- [ ] Squash related commits together.
- [ ] Double-check the quality of [commit messages](http://chris.beams.io/posts/git-commit/).
- [ ] This PR can be deployed to production without breaking anything

### Other

Any additional information...
