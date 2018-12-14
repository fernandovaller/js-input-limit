# JS Input Limit

Limite de caracter em input

* Limite de caracteres definido no codigo html _maxlength="10"_
* Retorno da contagem na tag _class="inputLog"_

> HTML
```html
...
<small class="inputLog"></small>
<input type="text" maxlength="10" class="form-control inputLimit">
...
```

> JS
```js
$('.inputLimit').keyup(function() {
    var maxLength = $(this).attr('maxlength');
    if(maxLength){
        var textlen = maxLength - $(this).val().length;
        msg = 'Limite: ' + textlen + '/' + maxLength;
    } else {
        msg = 'Limite nao definido para esse campo';
    }
    
    $(this).parent().find('.inputLog').text(msg);
});
```

> Screenshot

![js-input-limit](https://raw.githubusercontent.com/fernandovaller/js-input-limit/master/screenshot.png)