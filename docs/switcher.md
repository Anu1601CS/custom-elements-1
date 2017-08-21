# Switcher

In order to use the switcher custom element you need to import the element in the document's head:
```html
<script src="joomla-switcher.min.js"></script>
```

The simplified version of the custom element
```html
<joomla-switcher>
	<span class="switcher">
		<input name="switcher" id="sw1" value="0" type="radio" class="active" checked>
		<input name="switcher" id="sw2" value="1" type="radio">
		<span class="switch"></span>
	</span>
	<span class="switcher-labels">
		<span class="switcher-label-0 active">No</span>
	<span class="switcher-label-1">Yes</span>
	</span>
</joomla-switcher>

```

### Switcher demo:
<joomla-switcher>
	<span class="switcher">
		<input name="switcher1" id="sw12" value="0" type="radio" class="active" checked>
		<input name="switcher1" id="sw22" value="1" type="radio">
		<span class="switch"></span>
	</span>
	<span class="switcher-labels">
		<span class="switcher-label-0 active">No</span>
		<span class="switcher-label-1">Yes</span>
	</span>
</joomla-switcher>

<joomla-switcher>
	<span class="switcher switcher-primary">
		<input name="switcher2" id="sw13" value="0" type="radio" class="active" checked>
		<input name="switcher2" id="sw23" value="1" type="radio">
		<span class="switch"></span>
	</span>
	<span class="switcher-labels">
		<span class="switcher-label-0 active">Hide</span>
		<span class="switcher-label-1">Show</span>
	</span>
</joomla-switcher>

<joomla-switcher>
	<span class="switcher switcher-danger">
		<input name="switcher3" id="sw14" value="0" type="radio" class="active" checked>
		<input name="switcher3" id="sw24" value="1" type="radio">
		<span class="switch"></span>
	</span>
	<span class="switcher-labels">
		<span class="switcher-label-0 active">Stable</span>
		<span class="switcher-label-1">Alpha</span>
	</span>
</joomla-switcher>

## Attibutes
Control the design and functionality of the custom element through attributes.

## Events
The custom element exposes a few events for hooking into switcher functionality.


|Event					|Description								     												|
|-----------------------|-----------------------------------------------------------------------------------------------|
|joomla.switcher.toggle	|This event fires when the switcher has been switched "on" or "off"								|
|joomla.switcher.on		|This event fires when the switcher has been switched "on"										|
|joomla.switcher.off	|This event fires when the switcher has been switched "off"										|


Example:
Add some functonality when the switcher has been toggled
```js
element.addEventListener('joomla.switcher.toggle', function() {alert('Toggled!')} )
```

Add some functonality when the switcher has been switched "on"
```js
element.addEventListener('joomla.switcher.on', function() {alert('Switched on!')} )
```

Add some functonality when the switcher has been switched "off"
```js
element.addEventListener('joomla.switcher.off', function() {alert('Switched off!')} )
```