---
layout: post
title: Clipster compatibility updates
comments: true
---
Today we worked on some compatibility upgrades. The currently released version of Clipster (0.5.3) requires Rails 3.2.8, this is a result of the version of rails development started on. Our goal is to support rails from Rails 3.0 on. As of right now the development branch of clipster has been upgraded to support all the way back to 3.1.0. 

While you probably wouldn't want to be running such old versions of Rails, we wanted to support as many as we could because we know sometimes upgrading isn't in the cards. The oldest version of Rails we could potentially support is 3.0 due to the fact that Clipster itself is an engine. 

As part of this upgrade we are also working to improve our continuous integration testing with travis-ci. As part of these improvements, after we certify that old versions of Rails are compatible we will hopefully have travis-ci test new improvements in the latest versions of 3.2, 3.1, and 3.0.

One thing of note as a result of this compatibility upgrade is that we discovered that Rails versions before 3.2 will potentially fail with just `self.primary_key = :column_name` in models. We didn't want to change back to a deprecated method, so we added a conditional call to `set_primary_key`. We accomplished that by creating a ModelUtilities mixin so that we can reuse our version testing logic. You can view the code for that mixin [here](https://github.com/kwbock/clipster/blob/develop/lib/clipster/model_utilities.rb) and the usage in a model [here](https://github.com/kwbock/clipster/blob/develop/app/models/clipster/clip.rb). While this may not be the most elegant way to fix that error, it works and gets or compatibility changes moving along.
