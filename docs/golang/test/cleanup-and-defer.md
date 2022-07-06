# Cleanup and defer

[go playground](https://go.dev/play/p/KcETY2o3ZWi)

- `defer` is called before `cleanup`.
- `cleanup` is called in last added, first called order.(LIFO)
    - [go.dev](https://pkg.go.dev/testing#T.Cleanup)

```go
package main

import (
	"fmt"
	"testing"
)

func Test_main(t *testing.T) {
	t.Cleanup(func() {
		fmt.Println("called last")
	})
	t.Cleanup(func() {
		fmt.Println("called last-1")
	})
	defer func() {
		fmt.Println("called before cleanup")
	}()

	tc := []struct {
		name string
	}{
		{
			name: "c1",
		},
		{
			name: "c2",
		},
	}
	for _, tt := range tc {
		t.Run(tt.name, func(t *testing.T) {
			t.Cleanup(func() {
				fmt.Printf("called on [%s]\n", tt.name)
			})
			defer func() {
				fmt.Println("called before sub cleanup")
			}()
		})
	}
}
```
