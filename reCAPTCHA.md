reCAPTCHA-V2





```python
from utils.recaptcha import check_recaptcha_fn

class JustForm(UserCreationForm):
	...
    
    def clean(self):
        ecaptcha_response = self.data.get('g-recaptcha-response')
        result = check_recaptcha_fn(recaptcha_response)
        if result == False:
            raise forms.ValidationError(
                'reCAPTCHA 를 다시 시도해 주세요',
                code='invalid_captcha',
            )	
            
       ...
```



```html

...
<script src='https://www.google.com/recaptcha/api.js'></script>
<div class="g-wrap">
    <div class="g-box">
        <div class="g-recaptcha" style="transform-origin: left top;" 
             data-sitekey="6LdoJosaAAAAAFyVMjAQHdigkpfEXYiVfY4Pv2qf"></div>
    </div>
</div>
...
```

