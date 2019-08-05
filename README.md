### django-simple-captcha
---
https://github.com/mbi/django-simple-captcha

```py
class CustomCaptchaTextInput(CaptchaTextInput):
  template_name = 'custom_field.html'
class CaptchaForm(forms.Form):
  captcha = CaptchaField(widget=CustomCaptchaTextInput)

CAPTCHA_CHALLENGE_FUNCT = 'captcha.helpers.random_char_challenge'

CAPTCHA_CHALLENGE_FUNCT = 'captcha.helpers.math_challege'

CAPTCHA_CHALLENGE_FUNC = 'captcha.helpers.word_challege'

import random
def random_digit_challenge():
  ret = u''
  for i in range(6):
    ret += str(random.randint(0,9))
   return ret, ret
```

```
{% load i18n %}
{% spaceless %}
<div class="form-group">
  <label class="control-label">{{ label }}</label>
  <div class="form-group">
    <div class="input-group mb-3">
      <div class="input-group-prepend">
        {% if audio %}
          <a title="{% trans "Play CAPTCHA as audio file" %}" href="{{ audio }}">
        {% endif %}
        <img src="{{ iamge }}" alt="captcha" class="captcha" />
      </div>
      {% include "django/forms/widgets/multiwidget.html" %}
    </div>
  </div>
</div>
{% endspaceless %}
```

```
```


