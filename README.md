# checkboxes-select-all
***Simple to check and uncheck checkboxes***
***

Select_all-rails is gem for implementing '**select-all**' functionality in more simple and effective way in your ruby-on-rails application.
## Functionalities
* [***Basic Usage***](http://radhikabhatt.github.io/checkboxes-select-all/#basic_usage) - Selecting/Unselecting multiple checkboxes.
* [***Multiple Seletions***](http://radhikabhatt.github.io/checkboxes-select-all/#multiple_selections) - Implementing more than one select-all functionalities in a page.
* [***Ajax Added Checkboxes***](http://radhikabhatt.github.io/checkboxes-select-all/#ajax_added_checkboxes) - Implementing select-all functionality to new checkboxes added by an Ajax call.
* [***Show Selection/Count***](http://radhikabhatt.github.io/checkboxes-select-all/#show_selected_count) - Display selected checkboxes count or checkboxes remaining to select count or selected checkboxes count out of total checkboxes.

## Installation

Add this line to your application's **Gemfile**:

```ruby
gem 'checkboxes-select-all'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install checkboxes-select-all

And add the following line to your **application.js** file after jquery:

    //= require select_all.js

## Usage
Call the function **select_all()** on main checkbox and add class **'selectable'** to sub-checkboxes.

HTML example:
```html
<input type="checkbox" id="selectAll">All Items</input>

<input type="checkbox" class="selectable">Item 1</input>
<input type="checkbox" class="selectable">Item 2</input>
<input type="checkbox" class="selectable">Item 3</input>

<script type="text/javascript">
    $("#selectAll").select_all();
</script>
```
***For more usage checkout*** [**Demo**](http://radhikabhatt.github.io/checkboxes-select-all/)


Rails haml example:
```haml
= check_box_tag 'checkAll'
= check_box_tag 'selected_ids[]', "1", false, class: 'selectable'
= check_box_tag 'selected_ids[]', "2", false, class: 'selectable'
= check_box_tag 'selected_ids[]', "3", false, class: 'selectable'

:javascript
    $("#checkAll").select_all();
```


## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release` to create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

1. Fork it ( https://github.com/[my-github-username]/checkboxes-select-all/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
