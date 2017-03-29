# rails-module-paginator
> Rails module for paginator based on kaminari.

## Step by step:
+ Add gem to Gemfile:
```bash
# gem 'kaminari'
bundle install
```

+ scaffold Controller & model & views:
```bash
rails generate scaffold Post name:string title:string content:text
```

## resouces:
+ https://github.com/kaminari/kaminari

+ config your paginator:
```bash
rails g kaminari:config
# create  config/initializers/kaminari_config.rb
# config this file: kaminari_config.rb
```

+ i18n to zh.yml
```yaml
en:
  views:
    pagination:
      first: "&laquo; First"
      last: "Last &raquo;"
      previous: "&lsaquo; Prev"
      next: "Next &rsaquo;"
      truncate: "&hellip;"
  helpers:
    page_entries_info:
      one_page:
        display_entries:
          zero: "No %{entry_name} found"
          one: "Displaying <b>1</b> %{entry_name}"
          other: "Displaying <b>all %{count}</b> %{entry_name}"
      more_pages:
        display_entries: "Displaying %{entry_name} <b>%{first}&nbsp;-&nbsp;%{last}</b> of <b>%{total}</b> in total"
```