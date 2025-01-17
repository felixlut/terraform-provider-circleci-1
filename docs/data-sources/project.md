---
page_title: "circleci_project Data Source - terraform-provider-circleci"
subcategory: ""
description: |-
  Fetches the information for a project
---

# circleci_project (Data Source)

Fetches the information for a project

## Example Usage

```terraform
data "circleci_project" "test" {
  slug = "github/acmeorg/foobar"
}

output "url" {
  description = "project_url"
  value       = data.circleci_project.test.vcs_url
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `slug` (String) Project slug in the form `vcs-slug/org-name/repo-name`. The / characters may be URL-escaped.

### Read-Only

- `id` (String) Unique identifier of this project
- `name` (String) Name of the project
- `organization_id` (String) The id of the organization the project belongs to
- `organization_name` (String) The name of the organization the project belongs to
- `organization_slug` (String) The slug of the organization the project belongs to
- `vcs_default_branch` (String) Default branch of this project
- `vcs_provider` (String) VCS provider (either GitHub, Bitbucket or CircleCI)
- `vcs_url` (String) URL to the repository hosting the project's code
