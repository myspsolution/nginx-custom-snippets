# nginx custom snippets

Collections of nginx custom snippets to be included in (sub)domain nginx conf files

## Usage:

Create dir:

`[sudo] mkdir /etc/nginx/snippets/sps`

Copy/extract files to:

**/etc/nginx/snippets/sps**

Put it within `server { ... }` block in nginx conf file,

examples:

```
server {
  # ...your initial nginx conf

  # add protection from nginx common security problem
  include /etc/nginx/snippets/sps/security.common.conf;

  # handle patch traversal security
  include /etc/nginx/snippets/sps/security.path-traversal.conf;

  # custom error pages
  # must also include: https://github.com/myspsolution/nginx-custom-error-pages
  include /etc/nginx/snippets/sps/custom-error-pages.conf;

  # ...your rest nginx conf
}
```
