---
layout: post
title:  "windows下安装jekyll中遇到的坑"
img: actice_pic01.jpg # Add image post (optional)
date:   2018-01-25 17:44:35 +0800
categories: jekyll update
description: You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. # Add post description (optional)
tag: [Travel, Blogging, Mountains]
---
windows下安装jekyll中遇到的坑（首先注意版本，版本最好选择相对稳定的版本）（注意ruby、gem等一切安装组件的版本）
jekyll在blog中遇到jekyll serve 安装失败（可以写一个blog） 执行serve命令失败后 

如果有报错，比如下面之类的
E:/Ruby23/lib/ruby/gems/2.3.0/gems/bundler-1.13.2/lib/bundler/resolver.rb:366:in `block in verify_gemfile_dependencies_a
re_found!': Could not find gem 'jekyll-sitemap x86-mingw32' in any of the gem sources listed in your Gemfile or availabl
e on this machine. (Bundler::GemNotFound)
        from E:/Ruby23/lib/ruby/gems/2.3.0/gems/bundler-1.13.2/lib/bundler/resolver.rb:341:in `each'
        from E:/Ruby23/lib/ruby/gems/2.3.0/gems/bundler-1.13.2/lib/bundler/resolver.rb:341:in `verify_gemfile_dependenci
es_are_found!'
        from E:/Ruby23/lib/ruby/gems/2.3.0/gems/bundler-1.13.2/lib/bundler/resolver.rb:199:in `start'
        from E:/Ruby23/lib/ruby/gems/2.3.0/gems/bundler-1.13.2/lib/bundler/resolver.rb:181:in `resolve'
        from E:/Ruby23/lib/ruby/gems/2.3.0/gems/bundler-1.13.2/lib/bundler/definition.rb:250:in `resolve'
        from E:/Ruby23/lib/ruby/gems/2.3.0/gems/bundler-1.13.2/lib/bundler/definition.rb:174:in `specs'
        from E:/Ruby23/lib/ruby/gems/2.3.0/gems/bundler-1.13.2/lib/bundler/definition.rb:233:in `specs_for'
        from E:/Ruby23/lib/ruby/gems/2.3.0/gems/bundler-1.13.2/lib/bundler/definition.rb:222:in `requested_specs'
        from E:/Ruby23/lib/ruby/gems/2.3.0/gems/bundler-1.13.2/lib/bundler/runtime.rb:118:in `block in definition_method
'
        from E:/Ruby23/lib/ruby/gems/2.3.0/gems/bundler-1.13.2/lib/bundler/runtime.rb:19:in `setup'
        from E:/Ruby23/lib/ruby/gems/2.3.0/gems/bundler-1.13.2/lib/bundler.rb:99:in `setup'
        from E:/Ruby23/lib/ruby/gems/2.3.0/gems/jekyll-3.2.1/lib/jekyll/plugin_manager.rb:36:in `require_from_bundler'
        from E:/Ruby23/lib/ruby/gems/2.3.0/gems/jekyll-3.2.1/exe/jekyll:9:in `<top (required)>'
        from E:/Ruby23/bin/jekyll:23:in `load'
        from E:/Ruby23/bin/jekyll:23:in `<main>'
       
 则因为缺少相应的模块，根据提示“Could not find gem 'jekyll-sitemap x86-mingw32' in any of the gem sources listed”安装相应模块即可。即输入 gem install jekyll-sitemap

安装中 出现提示缺少组件的，则根据相应的情况缺少什么装什么。
