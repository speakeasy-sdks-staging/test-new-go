<!-- Start SDK Example Usage -->


```go
package main

import (
	"context"
	testnewgo "github.com/speakeasy-sdks-staging/test-new-go"
	"log"
)

func main() {
	s := testnewgo.New()

	ctx := context.Background()
	res, err := s.Pets.CreatePets(ctx)
	if err != nil {
		log.Fatal(err)
	}

	if res.StatusCode == http.StatusOK {
		// handle response
	}
}

```
<!-- End SDK Example Usage -->