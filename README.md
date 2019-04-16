# Counter-of-selected-checkboxes
<h3>Счётчик выбранных чекбоксов</h3>

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Счётчик выбранных чекбоксов</title>
</head>
<body>

  <div class="unique-class">
    <input type="checkbox" class="have-check">
    <input type="checkbox" class="have-check">
    <input type="checkbox" class="have-check">
    <input type="checkbox" class="have-check">
    <input type="checkbox" class="have-check">
  </div><br>

  Выбрано: <span class="how-many">0</span>


  <script src="http://code.jquery.com/jquery-3.4.0.min.js" integrity="sha256-BJeo0qm959uMBGb65z40ejJYGSgR7REI4+CW1fNKwOg=" crossorigin="anonymous"></script>

  <script>
    $('.unique-class input[type=checkbox]').change(function() {

      var chn = 0;

      $('.unique-class input[type=checkbox]').each(function(index) {
        if ( $(this).is(':checked') ) {
          chn++;
        }
      });

      $('.how-many').text(chn);

      if (chn == 2) {
        $( '.unique-class input[type=checkbox]' ).each(function(index) {
          if ( $(this).is(':checked') ) {}
          else { $(this).attr('disabled', 'disabled'); }
        })
      } else {
        $( '.unique-class input[type=checkbox]' ).each(function(index) {
          $(this).removeAttr('disabled');
        });
      }

    });
  </script>
  
</body>
</html>
```
