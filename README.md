# Highlight js integration in Laravel Vue Project

## By using cdn
Add cdn link to head tag
``` 
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0" />
    {{--    Highlight js --}}
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.9.0/styles/atom-one-dark.min.css">
    <script src="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.9.0/highlight.min.js"></script>

    @vite('resources/js/app.js')
    @inertiaHead
</head>
<body>
@inertia

<script>hljs.highlightAll();</script>
</body>
</html>
```

## By using NPM
Install hightlight js
``` 
npm install highlight.js
# or
yarn add highlight.js
```
Add this css cdn link for theme to head tag
``` 
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.9.0/styles/atom-one-dark.min.css">

```

Import highlight js and initialize it in your preferred component

``` 
<script setup>
import {onMounted,onUpdated} from "vue";
import hljs from 'highlight.js';

onMounted(()=> {
    hljs.highlightAll();
})

onUpdated(()=>{
    hljs.highlightAll();
})

</script>
```

## Contributing

Please see [Highlight js](https://highlightjs.org/) for details.
