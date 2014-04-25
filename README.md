# (BTIG) YeoPress

Thie is a fork of [Wesley Todd](http://wesleytodd.com/)'s [YeoPress](https://github.com/wesleytodd/YeoPress)

## How To Use

If you do not already have the Yeoman toolset installed do so now, and might as well install me at the same time *(NOTE: don't type the `$`)*:

	$ npm install -g git://github.com/BoomtownIG/YeoPress.git@master

And run me:

	$ yo btig-wordpress

Follow the prompts

### Advanced Usage

By specifying the `--advanced` flag you get access to more features:

- Vagrant: Sets up a Vagrant box using Puppet with all the requirements for running a WordPress site.
- WP version: Select a specific WordPress version to install
- Block external requests: Adds the `WP_HTTP_BLOCK_EXTERNAL` setting to config to lock down the admin
- Add core files to gitignore: Adds rules to the `.gitignore` file for the WordPress core files

### Reusing common settings

You can define any custom defaults you want in `~/.yeopress`.  This file is just a json file with key-value pairs for the config settings you want.  Here is a base default:

```json
{
    "tablePrefix": "wp_",
    "dbHost": "localhost",
    "git": true,
    "submodule": true,
    "wpDir": "wordpress",
    "contentDir": "wp-content",
    "installTheme": true,
    "themeDir": "roots-sass",
    "themeType": "git",
    "themeUser": "BoomtownIG",
    "themeRepo": "roots-sass",
    "themeBranch": "master",
    "customDirs": true,
}

```

## Installing WordPress Plugins

	$ yo btig-wordpress:plugin

An example response would be:

	wordpress-seo, w3-total-cache, disable-all-wordpress-updates

### Visual Learner??

[Watch the video](http://www.youtube.com/watch?v=Em-NMCgNhhY).

ADD Visual Learner?  [Watch the shorter video](http://www.youtube.com/watch?v=WSG0P5VpSUk).

[Also see the wiki](https://github.com/wesleytodd/YeoPress/wiki)

[And here is the boring write-up...](http://wesleytodd.com/2013/5/yeopress-a-yeoman-generator-for-wordpress.html)
