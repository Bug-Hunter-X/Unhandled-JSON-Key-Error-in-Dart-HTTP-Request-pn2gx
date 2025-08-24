# Unhandled JSON Key Error in Dart HTTP Request

This repository demonstrates a common error in Dart applications when handling JSON responses from HTTP requests. The code attempts to access a key that might not exist in the JSON data, leading to an exception.

## Bug Description

The `fetchData` function makes an HTTP GET request. If the request is successful (status code 200), it parses the JSON response. However, it directly tries to access the value associated with the key 'nonExistentKey' without checking if the key exists. If this key is absent, a runtime exception occurs.

## Solution

The improved version of `fetchData` adds a check to see if the key exists before attempting to access it, preventing the exception and providing a more robust way to handle missing keys.