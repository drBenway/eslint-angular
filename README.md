# eslint-angular
Custom rules to enforce Angular best practices.

one file
========
By default every controller, directive, factory or service should be in a
separate file.The file should start with angular setters.

Don't assign angular to a variable.
===================================
A basic example looks like this:
<pre><code>
angular
    .module('myapp')
    .controller('myCtrl',myCtrl);

function myCtrl(){
    ...
}
</code></pre>
The name of the controllers,directives,... should point to a named function that we define below.

Attach to vm
============
Assign the scope of the functions to "vm"

expl.
angular
    .module('myapp')
    .controller('myCtrl',myCtrl);

function(){
    var vm = this;
}