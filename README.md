jquery.multistep
================

Turns any form into a multistep form. based on http://www.jankoatwarpspeed.com/turn-any-webform-into-a-powerful-wizard-with-jquery-formtowizard-plugin/

Implementation
--------------

Define your form markup, separating the fields with a step separator
	
	<form id='#myform'>
		<div class='step'>
			<input type='text' ... />
			<input type='text' ... />
			<input type='text' ... />
		</div>
	
		<div class='step'>
			<input type='text' ... />
			<input type='text' ... />
			<input type='text' ... />
		</div>
	</form>

Initialise and configure the multistep form plugin with the optional settings

	$('#myform').multistep({
  		stepSelector            : '.step', // jquery select for the element used to define the forms steps
        actions                 : '.actions', // the element that contains the forms submit actions 
        onAfterShowStep         : function(step){}, // callback function 
        onBeforeShowNextStep    : function(step){}, // callback function - useful for hooking in validation rules!
        onBeforeShowPrevStep    : function(step){}, // callback function
        prevButtonText          : 'Back', // text on the previous button
        nextButtonText          : 'Next' // text on the next button
	});
