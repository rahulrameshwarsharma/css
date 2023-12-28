
##  css changes priority defined by the order of tag in head tag
<head>
if styles tag is written first, then it will be excuted first and then external css, which gives output of external css
because in css, changes will be display as per the last executed code.
<style>
    body{
        color: blue;
    }
</style>
<link rel="stylesheet">

</head>

## css properties
    Font-weight ranges between 100 - 900 (lighter, bold , bolder)