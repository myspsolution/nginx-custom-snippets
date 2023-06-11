# nginx custom snippets

Collections of nginx custom snippets to be included in (sub)domain nginx conf files

## Copy/Installation

Clone this repo to: **/etc/nginx/snippets/sps** :

```
sudo git clone https://github.com/myspsolution/nginx-custom-snippets.git /etc/nginx/snippets/sps

```

Put within `server { ... }` block in nginx conf file,

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
