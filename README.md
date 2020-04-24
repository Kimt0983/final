# final
test
javascript
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1>Press key</h1>
    <p id="show"></p>
    <h2 id="show"></h2>
</body>
</html>
<script src="jquery-3.4.1.js"></script>
<script>
    $(document).keydown(function(e){
        $("#show").html(e.which);
    });
</script>
<script>
    $(document).keydown(function(e){
        switch(e.which){
            case 76:$('#show').html('Lao');
            break;
            case 84:$('#show').html('Top');
            break;
            case 67:$('#show').html('College');
            break;
            default:$('#show').html('Lao-Top College');
        }
    });
</script>
<script src="jquery-3.4.1.js"></script>
<script>
    var keys={}
    $(document).keydown(function(e){
        keys[e.keyCode]=ture;
    });
    $(document).keyup(function(e){
        delete keys[e.keyCode];
    });
    for(var driection in keys){
        if(driection==76){
            $("#show").append("Lao");
        }
        if(driection==84){
            $("#show").append("Top");
        }
        if(driection==67){
            $("#show").append("College");
        }
    }
</script>
