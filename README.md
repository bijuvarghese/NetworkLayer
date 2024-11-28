# NetworkLayer

## Overview
NetworkLayer is a Swift-based library designed to simplify network operations in iOS applications. It provides a clean and concise API for making network requests, handling responses, and managing errors.

## Features
- Asynchronous network requests using Combine framework
- Support for GET, POST, PUT, DELETE methods
- JSON decoding and error handling
- Customizable request headers

## Installation
### Swift Package Manager
Add the following dependency to your `Package.swift` file:
```swift
dependencies: [
    .package(url: "https://github.com/bijuvarghese/NetworkLayer.git", from: "1.0.0")
]
Usage
Making a GET Request
import NetworkLayer

let url = URL(string: "https://api.example.com/data")!
let apiHandler = APIHandler()

apiHandler.get(url: url) { (result: Result<MyDataModel, Error>) in
    switch result {
    case .success(let data):
        print("Data received: \(data)")
    case .failure(let error):
        print("Error: \(error)")
    }
}
Making a POST Request
import NetworkLayer

let url = URL(string: "https://api.example.com/data")!
let apiHandler = APIHandler()
let parameters = ["key": "value"]

apiHandler.post(url: url, parameters: parameters) { (result: Result<MyDataModel, Error>) in
    switch result {
    case .success(let data):
        print("Data received: \(data)")
    case .failure(let error):
        print("Error: \(error)")
    }
}
License
This project is licensed under the MIT License - see the LICENSE file for details.
