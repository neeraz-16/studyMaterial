200
400
401
402
403
500
### 400 Bad Request:
when requested is not valid like invalid json format
### 401 Unauthorized:

This status code is returned when the client's request is missing valid authentication credentials or the provided credentials are invalid.
It indicates that the client must authenticate itself to access the requested resource.
Example scenarios: Accessing a protected resource without providing valid credentials, expired or revoked tokens.
### 403 Forbidden:

This status code is returned when the client's request is valid, but the server refuses to authorize the request due to insufficient permissions.
Unlike 401, where authentication is required, in a 403 response, the client's credentials are valid, but they don't have the necessary permissions.
Example scenarios: Attempting to access a resource with lower privileges than required, accessing a resource that's restricted to certain roles.
### 404 Not Found:

This status code is returned when the server couldn't find the requested resource. It indicates that the resource does not exist at the given URL.
Example scenarios: Trying to access a URL that doesn't correspond to any existing endpoint or resource.
