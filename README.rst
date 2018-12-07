So if you run::

    $ bazel test //:one_test --test_output streamed

Then it fails because the harpoon script can't find harpoon.yml even though it
should be there

Also it fails because I don't have .git in the temp directory. In this example
I don't need that option but in my realworld application I do
