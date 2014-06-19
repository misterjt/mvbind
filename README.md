Backbone MVbind
======

Backbone MVbind is simple data bind tool to connect Model and View.

```javascript

var User=Backbone.Model;
var View=Backbone.View.extend({
	initialize:function(){
		this.mvbind() // To start data binding you need to call this.mvbind();
	},
	bind:{
		'input.name':'name'// You can use jQuery selectors in left-hand side. In right-hand type key for model;
	}
})

$(function(){// Dont forget to wait for DOMContentLoaded
	var user=new User({name:'Jack'});
	var view=new View({model:user});
	/* After this your input.name fields will automatically content 'Jack'. 
 	* and if you will change smth in input, your model changes too. Vice versa.
	*/
}) 

```
