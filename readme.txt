jQuery ช่วยให้เขียน javascipt สั้น

ตัวอย่าง
<body>
    <input type="text" id="hello">
    <script>
        // example 1
        var pureJS = document.querySelector('#hello').value
        var jQuery = $('#hello').val()

        // example 2
        document.querySelector('#hello').value = 'hello world'
        $('#hello').val('hello world')
    </script>
</body>
</html>

0. CDN (content delivery network)
<head>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.7.1/jquery.min.js"></script>
</head>

1. Syntax
    แบ่งเป็นตัว 1. selector, 2. function

    <input type="text" id="hello">
    $('...').function()
    $('#hello').val()

    1.1 selector

        <ul>
            <li>
                <a id = "hello" href="#">Click me</a>
            </li>
        </ul>
        <script>
            $('#hello')
            $('ul li hello')
            $('ul li a#hello')
        </script>

    1.2 function

        - รับค่า input
            <!-- function -->
            <input type="text" id="myName" value = "woramet">
            <script>
            //document.querySelector('#hello').value
                $('#myName').val()

                //document.querySelector('#hello').value = 'hello'
                $('#myName').val('hello world')

                //document.querySelector('#hello').focus()
                $('#myName').focus()
            </script>

        -แก้ไขข้อความใน tag, css property
            <span id="game">me game</span>
            <span id="game2"></span>
            <script>
                var txt = $('#game').text()
                console.log(txt);
                $('#game').text('my name is game').css('background', '#f1c40f')
                $('#game').text('my name is game').css({
                    'background' : '#f1c40f',
                    'color': '#000'
                })
            </script>

        -innerhtml
            <div id="age"></div>
            <script>
                var htmlstr = '<div>20 year<div>'
                //document.querySelector('#hello').innerHTML = htmlstr
                $('#age').html(htmlstr)
            </script>

        -event click
            <div id="clickme">click!</div>
            <div id="clickme2">click!</div>
            <script>
                $('#clickme').click(function(){
                    $(this).text('omg clicked')
                })
                $('#clickme2').on('click', function(){
                    $(this).text('omg clicked')
                })
            </script>

        -append, create, remove node

            <ul id="render"></ul>
            <script>
                var htmlstr = '<li id="list' + numlist + '" onclick=removelist(this)>' + $('#inputId').val()+'</li>'
                    $('#render').append(htmlstr)
            <script>