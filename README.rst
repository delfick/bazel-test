So if you run::

    $ bazel test //:one_test --test_output streamed

Then it fails because the harpoon script can't find harpoon.yml.

This is because the sh_test rule makes a copy of docker/harpoon as one_test in
the root of the sandbox and so it sets HARPOON_CONFIG to point at harpoon.yml in
the root of sandbox rather than in the docker folder where it expects to have
been run from
