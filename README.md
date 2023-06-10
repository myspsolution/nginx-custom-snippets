# nginx custom snippets
Collections of nginx custom snippets to be included in (sub)domain nginx conf files

## Usage:
Copy/extract files to:

**/etc/nginx/snippets**

Put it under `server { ... }` block in nginx conf file,

examples:

```
server {
  # ...your initial nginx conf

  # add protection from nginx common security problem
  include /etc/nginx/snippets/security.common.conf;

  # handle patch traversal security
  include /etc/nginx/snippets/security.path-traversal.conf;

  # custom error pages
  include /etc/nginx/snippets/custom-error-pages.conf;

  # ...your rest nginx conf
}
```
