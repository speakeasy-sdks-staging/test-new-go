# Pets
(*Pets*)

### Available Operations

* [CreatePets](#createpets) - Create a pet
* [ListPets](#listpets) - List all pets
* [ShowPetByID](#showpetbyid) - Info for a specific pet

## CreatePets

Create a pet

### Example Usage

```go
package main

import(
	"context"
	"log"
	testnewgo "github.com/speakeasy-sdks-staging/test-new-go"
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

### Parameters

| Parameter                                             | Type                                                  | Required                                              | Description                                           |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| `ctx`                                                 | [context.Context](https://pkg.go.dev/context#Context) | :heavy_check_mark:                                    | The context to use for the request.                   |


### Response

**[*operations.CreatePetsResponse](../../models/operations/createpetsresponse.md), error**


## ListPets

List all pets

### Example Usage

```go
package main

import(
	"context"
	"log"
	testnewgo "github.com/speakeasy-sdks-staging/test-new-go"
)

func main() {
    s := testnewgo.New()


    var limit *int = 21453

    ctx := context.Background()
    res, err := s.Pets.ListPets(ctx, limit)
    if err != nil {
        log.Fatal(err)
    }

    if res.Pets != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                             | Type                                                  | Required                                              | Description                                           |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| `ctx`                                                 | [context.Context](https://pkg.go.dev/context#Context) | :heavy_check_mark:                                    | The context to use for the request.                   |
| `limit`                                               | **int*                                                | :heavy_minus_sign:                                    | How many items to return at one time (max 100)        |


### Response

**[*operations.ListPetsResponse](../../models/operations/listpetsresponse.md), error**


## ShowPetByID

Info for a specific pet

### Example Usage

```go
package main

import(
	"context"
	"log"
	testnewgo "github.com/speakeasy-sdks-staging/test-new-go"
)

func main() {
    s := testnewgo.New()


    var petID string = "string"

    ctx := context.Background()
    res, err := s.Pets.ShowPetByID(ctx, petID)
    if err != nil {
        log.Fatal(err)
    }

    if res.Pet != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                             | Type                                                  | Required                                              | Description                                           |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| `ctx`                                                 | [context.Context](https://pkg.go.dev/context#Context) | :heavy_check_mark:                                    | The context to use for the request.                   |
| `petID`                                               | *string*                                              | :heavy_check_mark:                                    | The id of the pet to retrieve                         |


### Response

**[*operations.ShowPetByIDResponse](../../models/operations/showpetbyidresponse.md), error**

