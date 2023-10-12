# Steamwebapi GoLang API Wrapper

![GitHub](https://img.shields.io/github/license/oguzhantasimaz/steam-web-api-go)
![GitHub Release (latest by date)](https://img.shields.io/github/v/release/oguzhantasimaz/steam-web-api-go)
![GitHub Go Module Version](https://img.shields.io/github/go-mod/go-version/oguzhantasimaz/steam-web-api-go)
![GitHub issues](https://img.shields.io/github/issues/oguzhantasimaz/steam-web-api-go)

## Description

Steamwebapi is a free and open-source API wrapper for interacting with the Steam Web API. It provides easy access to various Steam services such as Inventory, Profile, CS:GO Items, Rust Items, Dota Items, Team Fortress Items, and more without the risk of Steam blocking.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)

## Installation

To use this API wrapper in your Go project, you can add it as a dependency in your `go.mod` file.

```go
require github.com/your-username/steamwebapi-golang v1.0.0
```

## Usage

Before making API requests, you need to obtain an API key from [steamwebapi.com](https://www.steamwebapi.com/api/list). Once you have your API key, you can initialize the wrapper and make requests to the Steam Web API.

```go
import "github.com/your-username/steamwebapi-golang"

func main() {
    apiKey := "your-api-key"
    client := steamwebapi.NewClient(apiKey)

    // Use client to make API requests
}
```

## API Endpoints

The API wrapper supports the following endpoints:

- **Currency**
  - Get a list of currencies
  - Get exchange rates for currencies

- **Explore**
  - Get random data
  - Get the last data
  - Get a toplist of data

- **Float**
  - Get float values for items

- **Items**
  - Get Steam items
  - Get information about Steam items
  - Find Steam items
  - Get details of a specific Steam item
  - Get item history

- **Inventory**
  - Get Steam inventory
  - Get Steam inventory tracked by day

- **Profile**
  - Get Steam IDs
  - Get Steam profiles
  - Get Steam friend lists

- **Collections**
  - Get CS:GO collections

- **Collection**
  - Get a specific CS:GO collection by slug

For detailed information on each endpoint and their usage, please refer to the [official API documentation](https://www.steamwebapi.com/api/list).

## Examples

Here are some example usages of the API wrapper:

```go
// Get a list of currencies
currencies, err := client.GetCurrencies()

// Find Steam items
items, err := client.FindSteamItems("gameName", "searchTerm")

// Get a CS:GO collection by slug
collection, err := client.GetCSGOCollections("collectionSlug")
```

For more examples, check the [examples directory](https://github.com/your-username/steamwebapi-golang/tree/main/examples).

## Contributing

Contributions to this project are welcome! If you encounter a bug or have a feature request, feel free to open an issue. Pull requests with improvements or new features are also appreciated.

## License

This API wrapper is licensed under the [MIT License](LICENSE).

---

Feel free to replace placeholders like `your-username` and `v1.0.0` with the appropriate information for your specific project. Additionally, provide more specific examples and usage instructions for your wrapper as needed.
Steamwebapi is a free and open-source API wrapper for interacting with the Steam Web API. It provides easy access to various Steam services such as Inventory, Profile, CS:GO Items and more without the risk of Steam blocking.

For detailed information on each endpoint and their usage, please refer to the [official API documentation](https://www.steamwebapi.com/api/list).

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)

## Installation

To use this API wrapper in your Go project, you can add it as a dependency in your `go.mod` file.

```
go get github.com/oguzhantasimaz/steam-web-api-go
```

## Usage

Before making API requests, you need to obtain an API key from [steamwebapi.com](https://www.steamwebapi.com/api/list). Once you have your API key, you can initialize the wrapper and make requests to the Steam Web API.

```go
import "github.com/oguzhantasimaz/steam-web-api-go/swa"

func main() {
    apiKey := "your-api-key"
    client := swa.NewClient(apiKey)

    // Get Item History for P250 Crimson Kimono Factory New
    
    ih, err := client.Items().GetItemPriceHistory("P250 | Crimson Kimono (Factory New)")
    if err != nil {
        panic(err)
    }
    
    log.Println(ih)
}
```

## API Endpoints

The API wrapper supports the following endpoints:

- **Currency**
    - Get a list of currencies
    - Get exchange rates for currencies

- **Profiles**
    - Get random steam profile
    - Get a steam profile with high valued inventory 

- **Items**
    - Get Steam items
    - Get information about Steam items
    - Find Steam items
    - Get details of a specific Steam item
    - Get item history

- **Inventory**
    - Get Steam inventory
    - Get Steam inventory tracked by day

- **Profile**
    - Get Steam IDs
    - Get Steam profiles
    - Get Steam friend lists

## Examples

For more examples check the [examples directory](https://github.com/oguzhantasimaz/steam-web-api-go/tree/main/examples).

## Contributing

Contributions to this project are welcome! If you encounter a bug or have a feature request, feel free to open an issue. Pull requests with improvements or new features are also appreciated.

## License

This API wrapper is licensed under the [MIT License](LICENSE).
