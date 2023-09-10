# The website for [H2TC](https://h2tc.github.io/)

## Files
- _config.yml: configuration file for the website layout and structure, such as site description, logo, site navigation and footer. 
- index.md: the `Home` page. 
- dataset.md: the `Dataset` page. 
- tools.md: the `Tools` page. 
- recorder.md: the `Recorder` page. 
- pose.md: the `Pose` page. [todo]
- about.md: team member page. [not shown on the website yet]
- search.md: site researching page. [not shown on the website yet]
- 404.md: default Not Found page. [it appears when something gets wrong]
- offline.md: default offline page. [it appears when users are offline]
- LICENSE: the website template LICENSE, not ours. 
- Gemfile, alembic-jekyll-theme.gemspec: the file to deploy a local website. 
- CNAME: DNS record that maps an alias name to a true or canonical domain name. 

## Folders
- assets: the location for our used images and videos.
<!-- - site: the local website files. -->
- _sass: the style sheets for the current template. 
- _includes: the `include` tag allows you to include the content from another file stored in the `_includes` folder.
- _layouts: the location for various template pages. 

## How to check the website in real-time
You need to deploy a local website following the [official docs](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll?platform=linux). It includes:

1. Install Jekyll, Ruby and Bundler
3. Build your site locally: 1) Open the terminal. 2) Navigate to this folder. 3) Run `bundle install`. 4) Run `bundle exec jekyll serve --port 4000`. 5) To preview your site, in your web browser, navigate to http://localhost:4000.

Note: 
1. The default port is 4000. You can change it to avoid conflict. 
2. The local website content will update synchronously when you change the source codes. **If the local website is not updated synchronously**<!--  -->, you need to rerun the `bundle exec jekyll serve --port 4000` and reopen the site. 



