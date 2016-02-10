---
layout: post
title: CracklePop in PHP
---

>Write a program that prints out the numbers 1 to 100 (inclusive). If the number is divisible by 3, print Crackle instead of the number. If it’s divisible by 5, print Pop. If it’s divisible by both 3 and 5, print CracklePop. - [recurse.com](https://www.recurse.com/apply/start)

CracklePop is a common interview question. The following is one way of doing it: 

```php
for ($i = 1; $i <= 100; $i++) {
    if ($i % 3 === 0) {
      echo 'Crackle';
    }
    
    if ($i % 5 === 0) {
      echo 'Pop';
    }
    
    if ($i % 3 !== 0 && $i % 5 !== 0) {
      echo $i;
    }
    
    echo "\n"; //new line
}
```
