# DATA TYPES

## Declaring variables

```
import "fmt"

func main(){

	var flag bool
	var isAwesome bool = !flag

	fmt.Println(isAwesome)

	var i int = 42
	fmt.Println(i)
}	
```

## Boolean types

- default value of boolean is false

## Numeric types

- int8, int16, int32, int64, uint8, uint16, uint32, uint64
- uint only allows positive numbers and 0, otherwise, int accepts positive and negative integer numbers.

- uint8 is the byte type
- rarely see variables declared as uint8, better user **byte** name

- int could be int32 or int64, it depends on your computer architecture.
- can appear an error if you try to compare int variables with int32, int64, for the examples described before.
- Integer values are setted with the **int** type

