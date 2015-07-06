&lt;toast-er&gt;
====================

&lt;toast-er&gt; is a [Polymer][polymer_page] `paper-toast` with some swagg
features.

The toaster has a bin. So you can throw events without caring about
displaying, all messages will be displayed with respecting of each individual
configuration (text, duration, style...).

The toaster makes 4 types of toast (info, success, warning and error). Each
type sets a light at the bottom according to the level of 'dangerousity'.

You can also set the heat level (low, middle or high). The toast blink more or
less speedily.

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

	Just put the tag in the index page and fire the good events, that's all !

	```html
	<template id="app" is="dom-bind">
	  <toast-er></toast-er>
	</template>

	<script>
	function someMethod() {
	  app.fire('iron-signal', {
	    name: 'toaster-eject',
	    data: {
	      text: 'You are not allowed to do this.',
	      type: 'error',
	      duration: 5000
	    }
	  });
	}
	</script>
	```

##Audited events:

Name                        | Method called | Description
:---------------------------|:--------------|:-----------
`iron-signal-toaster-eject` | `_eject`      | Shows the toast with received data

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
