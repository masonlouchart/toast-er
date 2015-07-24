&lt;toast-er&gt;
====================

&lt;toast-er&gt; is a [Polymer][polymer_page] `paper-toast` with some swagg
features.

The toaster has a bin. So you can throw events without caring about
displaying, all messages will be displayed with respecting of each individual
configuration (text, duration, style, position...).

The toaster makes 4 types of toast (info, success, warning and error). Each
type sets a light at the bottom according to the level of 'dangerousity'.

You can also set the heat level (low, middle or high). The toast blink more or
less speedily according to the defined level.

You can choose on which shelf placing the toaster. There are 4 possibilities of
course, the shelf at bottom-left (default), bottom-right, top-left and
top-right.

> Maintained by [Mason Louchart][profile_page].

## Demo & Doc

See the [Component Page][component_page]

## Usage

1. Install The Component:

  ```sh
  bower install toast-er --save
  ```

2. Import Custom Element:

  ```html
  <link rel="import" href="PATH/TO/BOWER/COMPONENTS/toast-er/toast-er.html">
  ```

3. Start using it!

  Just put the tag in the index page...

  ```html
  <toast-er></toast-er>
  <toast-er duration="5000"></toast-er>
  <toast-er type="info"></toast-er>
  <toast-er type="warning" heat="middle"></toast-er>
  <toast-er shelf="top-right"></toast-er>
  ```

  ...and fire some events, that's all !

  ```html
  <script>
  function someMethod() {
     this.fire('iron-signal', {
       name: 'toaster-bake',
       data: {
         text: 'You are not allowed to do this.',
         type: 'error',
         duration: 5000,
         heat: 'high',
         shelf: 'top-right'
       }
     });
  }
  </script>
  ```
  There are no required options excepted `text` !

##Audited events:

Name                        | Method called | Description
:---------------------------|:--------------|:-----------
`iron-signal-toaster-bake`  | `_bake`       | Shows the toast with received data

##Event detail properties:

Property   | Value           | Description
:----------|:----------------|:------------
`text`     | 'What you want' | The text shown by the toaster
`type`     | 'info'          | Sets the color of toaster bottom to #00baff (cyan)
`type`     | 'success'       | Sets the color of toaster bottom to #0bdb00 (green)
`type`     | 'warning'       | Sets the color of toaster bottom to #ffa800 (orange)
`type`     | 'error'         | Sets the color of toaster bottom to #fb0000 (red)
`duration` | 5000 (millisec) | Sets the toast duration to 5 seconds (default: 3000)
`heat`     | 'low'           | The toaster blinks with a transition in 3 seconds
`heat`     | 'middle'        | The toaster blinks with a transition in 2 seconds
`heat`     | 'high'          | The toaster blinks with a transition in 1 second
`shelf`    | 'top-right'     | Sets the toaster position to the top-right corner
`shelf`    | 'top-left'      | Sets the toaster position to the top-left corner
`shelf`    | 'bottom-right'  | Sets the toaster position to the bottom-right corner
`shelf`    | 'bottom-left'   | Sets the toaster position to the bottom-left corner

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

_Don't forget add your name into the [CONTRIBUTORS.txt][contributors] file._

## License

[Apache License 2.0][license]

<!-- links -->
[polymer_page]: https://www.polymer-project.org/1.0/
[profile_page]: https://github.com/LM450N
[component_page]: http://louchart-mason.fr/toast-er
[contributors]: https://github.com/LM450N/toast-er/blob/master/CONTRIBUTORS.txt
[license]: http://opensource.org/licenses/Apache-2.0
