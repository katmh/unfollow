# unfollow

## Twitter

Follow the instructions for this [Twitter CLI](https://github.com/sferik/t).

Personally I ran this command a bunch of times (with larger numbers for `head -#`) since it was interesting to see who hadn't tweeted in the longest time.

```
t followings -l --sort=tweeted | head -10 | awk '{print $1}' | xargs t unfollow -i
```

## LinkedIn

From: [How can I unfollow all my contacts on LinkedIn at once?](https://webapps.stackexchange.com/questions/92383/how-can-i-unfollow-all-my-contacts-on-linkedin-at-once)

This snippet uses jQuery (`$` selectors). To get jQuery in your browser's console, copy all the [source code](https://code.jquery.com/jquery-3.4.1.min.js) and paste it into the console 🙃

```
var buttons = $("button"),
 interval = setInterval(function(){
 var btn = $('.is-following');
 console.log("Clicking:", btn);
 btn.click();
 if (buttons.length === 0) {
    clearInterval(interval);
 }
 window.scrollTo(0,document.body.scrollHeight);
}, 1000);
```

This might take a sessions (refresh and enter the code again).
