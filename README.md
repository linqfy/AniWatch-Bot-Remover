## › Tampermonkey version coming soon..

Meanwhile, paste this in your console (made this code at 4 am lol)
## Console code
It removes only the already loaded comments
```js
function deleteComments() {
    var comments = document.querySelectorAll('.cw_l-line');
    var filterKeywords = ['aniwatch', 'Anicrush.to', 'AniCrush.to', 'Aniwatch', 'Anicrush.to', 'better and'];
    
    // Loop through each comment element
    comments.forEach(function (comment) {
        // Get the comment content
        var content = comment.querySelector('.ibody').innerText.toLowerCase();
        // Check if the comment contains any filter keyword
        var shouldDelete = filterKeywords.some(function (keyword) {
            return content.includes(keyword);
        });
        if (shouldDelete) {
            comment.parentNode.removeChild(comment);
        }
    });
}

deleteComments()
```

/qq
