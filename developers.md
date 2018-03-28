# Developer Setup

## Tools

* Trello for project management / tasks: https://trello.com/b/mA4Rwzum/dev-backlog 
* Dropbox for UI files which use Sketch \(need to figure out how to label current files\).
* GitHub for code: https://github.com/geeksforsocialchange/PlaceCal
* Rollbar for bug reporting
* Add new admin to https://placecal.org/users 

## Hosting / Environment

* Rails 5 / Ruby 2.4 / postgresql
* `rails db:setup db:migrate db:seed`
* `rails import:all_events`
* To log in you need to go to `/users` and then `/superadmin` \(for now!\)
* Prod server is a [Digital Ocean box running this setup](https://gist.github.com/kimadactyl/5c277d2698f754edf3daa5fd84488851)

## Notes

We’re using the [Mountain View](https://github.com/devnacho/mountain_view) gem for frontend components. Anything and everything reusable should be encapsulated in a component and given some mocks to test it. Components are at [https://placecal.org/styleguide](https://placecal.org/styleguide).  For each component add a line to `test/controllers/components_test.rb`: easy tests!

Ideally the Sketch art should export directly into our repo file structure somehow, so if we can work towards having a master Sketch file for anything live then take the time to do it.

Currently using Travis but not really, need to move to dev ops



