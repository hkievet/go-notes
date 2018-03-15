## If Statements

```
if x < 0 {
  // no parenthesis
}
```

```
if v := math.Pow(2, 6); v <= 64 {
  return v
} else {
  // won't pass here
}

fmt.Printf("%s", v); // will fail
```


## Loops
```
for i := 0; i < 10; i++ {
  // stuff
} 
```

Infinite loop:
```
for {
  // infinite loop
}
```

## Switch
```
switch a := "100"; a {
  case "2":
    fmt.Println("blam")
  case "bloomer"
    fmt.Println("damnnnn")
  default:
    fmt.Printf("%s", a)
}
```

## Defer

defer is LIFO
```
defer fmt.Println(i)
```


## Struct

```
type Vertex struct {
  X int
  Y int
}
```

instantiation:

```
v := Vertex{1, 2}
fmt.Println(v) // {1 2}
v.X = 25
v.Y = 26
fmt.Printf(v) // {25 26}
p := v
p.X = 2
(*p).Y = 4
fmt.Println(v) // {2 4}
v2 = Vertex{X: 1} // Y is 0 implicitly
fmt.Println(v2) // {1 0}
```

## Slices (%v)

```
s := []int{2, 3, 5, 7, 11, 13}
len(s) // number of elements it contains
cap(s) // number of elements in its underlying array
```

```
a := make([]int, 5) // len(a)=5
```

```
a := []int{0, 1, 2, 3, 4, 5}
// a[:1] === a[0] === 0
// a[5:] === a[5] === 5

```

## Range

```
var pow = []int{1, 2, 4, 8, 16}

func main() {
  for i, v := range pow {
    fmt.Printf("2**%d = %d\n", i, v)
  }

  for _, v := range pow {
    // only value
  }

  for i := range pow {
    // ... only index
  }
}


```


## Maps

Maps are kind of like the dicts from python.  They have key value mappings..

```
words = make(map[string]string)
words["hello"] = "world"
fmt.Println(words["hello"]) // world
```

```
m[key] = elem         // insert
elem = m[key]         // retrieve
delete(m, key)        // delete
elem, okay = m[key]   // test (okay == true or false)


```





