# amdWebsite

### There will be 4 docker services
- Wordpress CMS
- Gatsby App
- Mysql for CMS
- Node server watching for changes to rebuild static site

### Deployment Plan
- AWS EC2 instance for all services
- S3 bucket for static site
- Cloudfront for routing to CMS and S3

#### Wordpress-cms Structure Plan
wordpress will have in it 2 folders
one will have all the plugins needed for this to work

the other will be the volume mapped to the /var/www/html of the docker container as specified in the docker-compose.yml

```
wordpress_cms
  |- engine // where wordpress will live
  |- starter_content // plugins for project
    |- plugins
    |- themes
  |- Dockerfile
  |- uploads.ini
```
