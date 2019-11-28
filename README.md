# AntiDisposmail
Detecting Disposable Email Addresses

Antbot.pw provides a free, open API endpoint for checking a domain or email address against a frequently-updated list of disposable domains. ```CORS is enabled for all originating domains, so you can call the API directly from your client-side code.```

```GET https://antibot.pw/api/disposable?email=radenvodka@0815.su HTTP/1.1```

The response will be JSON with one boolean property, e.g. ```{"disposable":false}```

`Using jQuery?`

```<script>
    $( "#email" ).change(function() {
      var val = $("#email").val();
      $.get('https://antibot.pw/api/disposable?email='+val,
        function (data, textStatus) {  
            if(data['disposable'] == true){
              alert("email disposable");
            }
      });
    });
</script>```
