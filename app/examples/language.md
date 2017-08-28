---
title: Multi-Language Forms
layout: vtabs
section: examples
weight: 301
---
### Muli-Language Forms
With Form.io, you can provide multiple langauges for the forms that are rendered within your application. This
is done like the following.

```html
<link rel="stylesheet" href="https://unpkg.com/formiojs@latest/dist/formio.full.min.css">
<script src="https://unpkg.com/formiojs@latest/dist/formio.full.min.js"></script>
<div class="btn-group">
  <button type="button" class="btn btn-default" onclick="setLanguage('en')">English</button>
  <button type="button" class="btn btn-default" onclick="setLanguage('sp')">Español</button>
  <button type="button" class="btn btn-default" onclick="setLanguage('ch')">中文</button>
</div>
<div id="formio"></div>
```

<div class="row">
<div class="col col-sm-6">

<pre>
Formio.createForm(document.getElementById('formio'), {
  components: [
    {
      type: 'textfield',
      key: 'firstName',
      label: 'First Name',
      placeholder: 'Enter your first name',
      input: true
    },
    {
      type: 'textfield',
      key: 'lastName',
      label: 'Last Name',
      placeholder: 'Enter your last name',
      input: true
    },
    {
      type: 'button',
      action: 'submit',
      label: 'Submit',
      theme: 'primary'
    }
  ]
}, {
  i18n: {
    sp: {
      'First Name': 'Nombre de pila',
      'Last Name': 'Apellido',
      'Enter your first name': 'Ponga su primer nombre',
      'Enter your last name': 'Introduce tu apellido',
      'Submit': 'Enviar'
    },
    ch: {
      'First Name': '名字',
      'Last Name': '姓',
      'Enter your first name': '输入你的名字',
      'Enter your last name': '输入你的姓氏',
      'Submit': '提交'
    }
  }
}).then(function(form) {
  window.setLanguage = function(lang) {
    form.language = lang;
  };
});
</pre>

</div>
<div class="col col-sm-6">
<h3>Result</h3>
<div class="well">
<div class="btn-group">
  <button type="button" class="btn btn-default" onclick="setLanguage('en')">English</button>
  <button type="button" class="btn btn-default" onclick="setLanguage('sp')">Español</button>
  <button type="button" class="btn btn-default" onclick="setLanguage('ch')">中文</button>
</div>
<div id="formio" style="margin-top: 20px;"></div>
<script type="text/javascript">
Formio.createForm(document.getElementById('formio'), {
  components: [
    {
      type: 'textfield',
      key: 'firstName',
      label: 'First Name',
      placeholder: 'Enter your first name',
      input: true
    },
    {
      type: 'textfield',
      key: 'lastName',
      label: 'Last Name',
      placeholder: 'Enter your last name',
      input: true
    },
    {
      type: 'button',
      action: 'submit',
      label: 'Submit',
      theme: 'primary'
    }
  ]
}, {
  i18n: {
    sp: {
      'First Name': 'Nombre de pila',
      'Last Name': 'Apellido',
      'Enter your first name': 'Ponga su primer nombre',
      'Enter your last name': 'Introduce tu apellido',
      'Submit': 'Enviar'
    },
    ch: {
      'First Name': '名字',
      'Last Name': '姓',
      'Enter your first name': '输入你的名字',
      'Enter your last name': '输入你的姓氏',
      'Submit': '提交'
    }
  }
}).then(function(form) {
  window.setLanguage = function(lang) {
    form.language = lang;
  };
});
</script>
</div>
</div>
</div>

