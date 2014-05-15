This is a copy of Filament Group's jQuery UI selectToUISlider plugin, with additional patches added on top of it. 

This repository was created from the original source download from: http://www.filamentgroup.com/lab/update_jquery_ui_slider_from_a_select_element_now_with_aria_support/

## Usage Example
``` html
<h1>Range select</h1>
<form action="#">
	<fieldset>
		<label for="demo3a">From:</label>
		<select name="demo3a" id="demo3a">

			<optgroup label="2010">
				<option value="01/10">Jan</option>
				<option value="02/10">Feb</option>
				<option value="03/10" data-markers='["Q"]'>Mar</option>
				<option value="04/10">Apr</option>
				<option value="05/10">May</option>
				<option value="06/10" data-markers='["Q"]'>Jun</option>
				<option value="07/10">Jul</option>
				<option value="08/10">Aug</option>
				<option value="09/10" data-markers='["Q"]'>Sep</option>
				<option value="10/10">Oct</option>
				<option value="11/10">Nov</option>
				<option value="12/10" data-markers='["Q","A"]'>Dec</option>
			</optgroup>

			<optgroup label="2011">
				<option value="01/11" selected="selected">Jan</option>
				<option value="02/11">Feb</option>
				<option value="03/11" data-markers='["Q"]'>Mar</option>
				<option value="04/11">Apr</option>
				<option value="05/11">May</option>
				<option value="06/11" data-markers='["Q"]'>Jun</option>
				<option value="07/11">Jul</option>
				<option value="08/11">Aug</option>
				<option value="09/11" data-markers='["Q"]'>Sep</option>
				<option value="10/11">Oct</option>
				<option value="11/11">Nov</option>
				<option value="12/11"  data-markers='["Q","A"]'>Dec</option>
			</optgroup>

			<optgroup label="2012">
				<option value="01/12">Jan</option>
				<option value="02/12">Feb</option>
				<option value="03/12" data-markers='["Q"]' disabled="disabled">Mar</option>
				<option value="04/12" disabled="disabled">Apr</option>
				<option value="05/12" disabled="disabled">May</option>
				<option value="06/12" data-markers='["Q"]' disabled="disabled">Jun</option>
				<option value="07/12" disabled="disabled">Jul</option>
				<option value="08/12" disabled="disabled">Aug</option>
				<option value="09/12" data-markers='["Q"]' disabled="disabled">Sep</option>
				<option value="10/12" disabled="disabled">Oct</option>
				<option value="11/12" disabled="disabled">Nov</option>
				<option value="12/12" data-markers='["Q","A"]' disabled="disabled">Dec</option>
			</optgroup>
		</select>

		<label for="demo3b">To:</label>
		<select name="demo3b" id="demo3b">

			<optgroup label="2010">
				<option value="01/10">Jan</option>
				<option value="02/10">Feb</option>
				<option value="03/10" data-markers='["Q"]'>Mar</option>
				<option value="04/10">Apr</option>
				<option value="05/10">May</option>
				<option value="06/10" data-markers='["Q"]'>Jun</option>
				<option value="07/10">Jul</option>
				<option value="08/10">Aug</option>
				<option value="09/10" data-markers='["Q"]'>Sep</option>
				<option value="10/10">Oct</option>
				<option value="11/10">Nov</option>
				<option value="12/10" data-markers='["Q","A"]'>Dec</option>
			</optgroup>

			<optgroup label="2011">
				<option value="01/11">Jan</option>
				<option value="02/11">Feb</option>
				<option value="03/11" data-markers='["Q"]'>Mar</option>
				<option value="04/11">Apr</option>
				<option value="05/11">May</option>
				<option value="06/11" data-markers='["Q"]'>Jun</option>
				<option value="07/11">Jul</option>
				<option value="08/11">Aug</option>
				<option value="09/11" data-markers='["Q"]'>Sep</option>
				<option value="10/11">Oct</option>
				<option value="11/11">Nov</option>
				<option value="12/11"  data-markers='["Q","A"]'>Dec</option>
			</optgroup>

			<optgroup label="2012">
				<option value="01/12">Jan</option>
				<option value="02/12" selected="selected">Feb</option>
				<option value="03/12" data-markers='["Q"]' disabled="disabled">Mar</option>
				<option value="04/12" disabled="disabled">Apr</option>
				<option value="05/12" disabled="disabled">May</option>
				<option value="06/12" data-markers='["Q"]' disabled="disabled">Jun</option>
				<option value="07/12" disabled="disabled">Jul</option>
				<option value="08/12" disabled="disabled">Aug</option>
				<option value="09/12" data-markers='["Q"]' disabled="disabled">Sep</option>
				<option value="10/12" disabled="disabled">Oct</option>
				<option value="11/12" disabled="disabled">Nov</option>
				<option value="12/12" data-markers='["Q","A"]' disabled="disabled">Dec</option>
			</optgroup>
		</select>
	</fieldset>
</form>
```

``` javascript
$('select#demo3a, select#demo3b').selectToUISlider({
	labels: 25,
	labelSrc: 'text',
	tooltipSrc: 'value',
	minRange: 3,
	sliderOptions: {
		animate: 'slow'
	}
})
.bind('change',function(event){
	// If you want to check range, just get the values from the select boxes themselves
	// or look at the event.uiSliderContext
	console.debug(event.uiSliderContext);
});
```
