# nginx-dynamic-dir-list

Run:

```bash
git clone https://github.com/Lirt/nginx-dynamic-dir-list ~/nginx-dynamic-dir-list
echo '127.0.1.1 my-awesome-xml-site.com' >> /etc/hosts

docker run -it \
           -p 8080:80 \
           -v ~/nginx-dynamic-dir-list/my-awesome-xml-site.conf:/etc/nginx/conf.d/my-awesome-html-site.conf \
           -v ~/nginx-dynamic-dir-list/site/:/usr/share/nginx/my-awesome-html-site/ \
           nginx

# Open URL my-awesome-xml-site.com:8080 in browser
#   - URL my-awesome-xml-site.com:8080/yum?format=xml - lists directory yum/ in xml listing format
#   - URL my-awesome-xml-site.com:8080/yum?format=html - lists directory yum/ in html listing format
```

