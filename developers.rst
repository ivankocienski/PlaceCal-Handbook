Developer Guide
===============
.. toctree::
   :hidden:
   
   glossary
   developers/user-access
   developers/roadmap

Getting started
---------------

Read the `Glossary <glossary.md>`__.

Tools
~~~~~

We use:

-  `Trello for project
   management <https://trello.com/b/mA4Rwzum/dev-backlog>`__
-  Sketch + Dropbox for UI files (get Kim to set you up).
-  `GitHub for
   code <https://github.com/geeksforsocialchange/PlaceCal>`__
-  Rollbar for error reporting
-  `Sign up on PlaceCal <https://placecal.org/users>`__ and get Kim to
   make you an admin.

Hosting / Environment
~~~~~~~~~~~~~~~~~~~~~

-  Rails 5 / Ruby 2.4 / postgresql
-  ``rails db:setup db:migrate seed:migrate``
-  ``rails import:all_events``
-  To log in you need to go to ``/users`` and then ``/superadmin`` (for
   now!)
-  Prod server is a `Digital Ocean box running this
   setup <https://gist.github.com/kimadactyl/5c277d2698f754edf3daa5fd84488851>`__
-  ``master`` branch auto-deploys to our staging server
   http://placecal-staging.org. ``production`` branch deploys manually
   to the production server.

Notes
~~~~~

We’re using the `Mountain
View <https://github.com/devnacho/mountain_view>`__ gem for frontend
components. Anything and everything reusable should be encapsulated in a
component and given some mocks to test it. Components are at
https://placecal.org/styleguide. For each component add a line to
``test/controllers/components_test.rb``: easy tests!

Important information should be added in a `seed
migration <https://github.com/harrystech/seed_migration>`__.

Ideally the Sketch art should export directly into our repo file
structure somehow, so if we can work towards having a master Sketch file
for anything live then take the time to do it.

User access
-----------

See the `User Access Guide <developers/user-access.md>`__

Roadmap
-------

See the current `Roadmap <developers/roadmap.md>`__

Getting API access
------------------

This is still in development. Drop us an email to have a chat about it.
