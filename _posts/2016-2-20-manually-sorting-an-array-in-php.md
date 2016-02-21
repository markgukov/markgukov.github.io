---
layout: post
title: Manually sorting an array in PHP
---

Another interview question that often comes up is sorting a list of numbers. Normally you would use something like [sort()](http://php.net/manual/en/function.sort.php) but that's not what the interviewer wants to see.

The following is a very short implementation of the bubble sort algorithm in PHP: 

```php
$to_sort = array(4, 1, 3, 2, 5);

while (list($key, $value) = each($to_sort)) {
    $curr = $to_sort[$key];
    $next = isset($to_sort[$key+1]) ? $to_sort[$key+1] : 0;
    
    if ($next && $curr > $next) {
        $to_sort[$key] = $next;
        $to_sort[$key+1] = $curr;
        reset($to_sort);
    }
}

print_r($to_sort);
```
