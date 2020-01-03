# Newsoft Test - Part C

## Answer:

```
    $minion_id = getMinionId(100);
    
    function getMinionId($n)
    {
        $num = 10005;
        $prime = '';
        for ($j = 2; strlen($prime) < $num; $j++) {
            for ($k = 2; $k < $j; $k++) {
                if ($j % $k == 0) {
                    break;
                }
            }

            if ($k == $j) {
                $prime .= $j;
            }
        }

        $new_prime = substr($prime, $n, strlen($prime));
        $minion_id = substr($new_prime, 0, 5);

        return $minion_id;
    }
```
