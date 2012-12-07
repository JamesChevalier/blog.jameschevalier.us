## About

My blog is designed with [Zurb Foundation](http://foundation.zurb.com). It's automatically built into a static site by [Jekyll](http://jekyllrb.com/) and deployed to [Linode](http://www.linode.com/?r=4b85e2ea3c6b78b139cc41e341ae37fdac438c54) each time I `rake deploy`. I keep it in GitHub as another Jekyll example, and as a backup.

Everything in `_site/` and `assets/attachments/` is mine. The rest of the stuff is either somebody else's, or free for you to use.

### Rake Tasks

There are a few rake tasks (kept in `Rakefile`) available to help make common tasks easier:

* See all available rake tasks: `rake -T`
* Build the site: `rake build`
* Build & deploy the site: `rake deploy` (customized for my server)
* Run Jekyll server: `rake dev` (equivalent to `jekyll --server --auto`)
* List all draft posts: `rake drafts`
* Create a new draft post: `rake post`
