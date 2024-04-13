# Str::limitNoBreak Macro
```
Str::macro('limitNoBreak', function ($value, $limit, $end = '...') {
    if (empty($value) || mb_strwidth($value, 'UTF-8') <= $limit) {
        return $value;
    }

    return preg_replace('/\s+?(\S+)?$/', '', substr($value, 0, $limit - strlen($end) + 1)) . $end;
});
```
