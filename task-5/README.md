# Task \#5

This task is meant to gauge your knowledge of javascript promises. Consider the following code snippet:

```js
import time
function countdown ( seconds )
{
	var time
	for( var i = 5 ; i >= 0; i--)
	{
	 time += i + "!"
	 setTimeout(() => {console.log(' //wait 1 sec')}, 1000);
	}
	return Promise.resolve ()
}

(async function () {
	await countdown ( 5 )
		.then ( () => console.log ("done!") )
		.catch ( error => console.error ( error ) )
}) ()
```

Your task is to complete the `countdown` function and write any other helper function(s) that you need in order for the code to output the following:

```
5!
4!
3!
2!
1!
0!
done!
```

In addition to outputting the above, make sure there is a one second pause between your print statements in the following locations:

```
5!
// Wait 1 sec
4!
// Wait 1 sec
3!
// Wait 1 sec
2!
// Wait 1 sec
1!
// Wait 1 sec
0!
// Wait 1 sec
done!
```

Please use promises when formulating an answer! The `countdown` function is expected to return a promise!
