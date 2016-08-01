# Bench

Small class to profile code.


## API

```php
public void Bench::startMemory ( [ string $name ] )

public integer Bench::stopMemory ( [ string $name ] )

public void Bench::startTime ( [ string $name ] )

public float Bench::stopTime ( [ string $name ] )
```


## Usage

```php
<?php

use SurrealCristian\Bench;

$bench = new Bench;

$bench->startMemory();
$dt = new DateTime();
$memory = $bench->stopMemory();

echo sprintf("Memory usage: %s bytes." . PHP_EOL, $memory);

$bench->startTime();
sleep(1);
$time = $bench->stopTime();

echo sprintf("Time: %s seconds." . PHP_EOL, $time);
```

```
Memory usage: 624 bytes.
Time: 1.0001759529114 seconds.
```


## License

MIT
