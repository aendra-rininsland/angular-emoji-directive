# angular-emoji-directive
## 2015 Ændrew Rininsland ([@aendrew](http://www.twitter.com/aendrew))

This is a simple directive to validate a form input against [Tim Whitlock's Emoji
Tables](http://apps.timwhitlock.info/emoji/tables/unicode).

### Usage:

Install via Bower:
```
bower install times/angular-emoji-directive
```

Add `times.emoji` to your app dependencies:
```
angular.module('yourApp', [
  'times.emoji'
])
```

Use as such:
```
<form name="form" class="css-form" novalidate>
  <div class="form-group" ng-class="{'has-error': form.submission.$error.emoji, 'has-success': !form.submission.$error.emoji}">
    <textarea emoji name="submission" class="form-control" type="text" ng-model="userSubmission"></textarea>
    <label class="control-label" for="submission" ng-show="form.submission.$error.emoji">Please use emoji only!</label>
  </div>
</form>
```
