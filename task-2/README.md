# Task \#2

Consider the following snippet of PHP code:

```php
<?php

	function task_2 ( $data ) {
		return $data;
	}

	$data = [ "-- foo --", "-- bar --", "-- --", "--", "-- foo -- bar --" ];
	$transformed = task_2 ( $data );

	echo implode ( $transformed, "\n" ) . "\n";

?>
```

Your task is to implement the `task_2` function. This function will transform the passed array of strings and will remove and prefixed and postfixed instances of `-- ` and ` --` respectively. It will also remove any empty elements once the transformation is complete. The output should look like the following:

```plain
foo
bar
foo -- bar
```

Notice that there are only 3 elements in the output. Functional programming is preferred for this task.
