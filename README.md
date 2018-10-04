# kubecuddler

A simple Go package wrapping `kubectl` invocations. It only depends on the stdlib and overall has a minimal footprint.

First, make sure you've got the package installed, for example, in a global scope:

```bash
$ go get -u github.com/mhausenblas/kubecuddler
```

A minimal usage example would look like the following:

```
package main

import github.com/mhausenblas/kubecuddler

func main() {
	res, _ := kubecuddler.Kubectl(true, true, "", "get", "po,svc")
	fmt.Println(res)
}
```
