pQuery
======

PHP Framework for jQuery and jQuery UI.

jQuery UI widgets are easily defined in the Controller, and rendered from the View.

Widgets are rendered and tracked by PHP through form state. jQuery handles all front-end events.

Easily extensible through plugins and UI widget extensions.

DB code generated ORM and CRUD drafts allow for rapid application development.

Familiar jQuery API in PHP.

A Button with events.
---------------------
    $options = array("Primary"=>true);
    $this->formButton = new UIButton($options, 'MyButton');
    $this->formButton->On("click", $this, "callback");
    $this->formButton->AppendTo($this->body);
    
    public function callback(){
      pQuery::Alert("You clicked $this->formButton->Id .");
    }

Or a Dialog.
------------
    $myDialog = new UIDialog($this);
    $myDialog->AutoOpen = false;
    
    $body->Append($myDialog);