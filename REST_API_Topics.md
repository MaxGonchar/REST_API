# REST API - Complete Learning Guide

## 1. Foundational Concepts

### 1.1 REST Architecture Principles
- Client-Server separation
- Stateless communication
- Cacheable responses
- Uniform interface
- Layered system
- Code on demand (optional)

### 1.2 Resources
- Resource identification through URIs
- Resource representation (JSON, XML, HTML)
- Self-descriptive messages
- Resource manipulation through representations

### 1.3 Statelessness
- Server doesn't store client context
- Each request is independent
- Client maintains session state

## 2. HTTP Fundamentals

### 2.1 HTTP Methods
- **GET** - Retrieve resource(s)
- **POST** - Create new resource
- **PUT** - Update/replace entire resource
- **PATCH** - Partial update of resource
- **DELETE** - Remove resource
- **HEAD** - Get headers only
- **OPTIONS** - Describe communication options

### 2.2 HTTP Status Codes
- **1xx** - Informational
- **2xx** - Success
  - 200 OK
  - 201 Created
  - 204 No Content
- **3xx** - Redirection
  - 301 Moved Permanently
  - 304 Not Modified
- **4xx** - Client Errors
  - 400 Bad Request
  - 401 Unauthorized
  - 403 Forbidden
  - 404 Not Found
  - 422 Unprocessable Entity
- **5xx** - Server Errors
  - 500 Internal Server Error
  - 502 Bad Gateway
  - 503 Service Unavailable

### 2.3 HTTP Headers
- **Request Headers**: Authorization, Content-Type, Accept, User-Agent
- **Response Headers**: Content-Type, Cache-Control, ETag, Location
- **Custom Headers**: X-API-Key, X-Rate-Limit, etc.

## 3. Request/Response Structure

### 3.1 Endpoints and URIs
- Base URL structure
- Resource hierarchies
- Path parameters vs query parameters

### 3.2 Request Components
- URL/URI
- HTTP method
- Headers
- Body (for POST, PUT, PATCH)

### 3.3 Response Components
- Status code
- Headers
- Body (data payload)

### 3.4 Query Parameters
- Filtering: `?status=active`
- Sorting: `?sort=created_at&order=desc`
- Pagination: `?page=2&limit=20`
- Field selection: `?fields=name,email`

## 4. Best Practices

### 4.1 Naming Conventions
- Use nouns, not verbs
- Use plural forms for collections
- Use lowercase with hyphens
- Keep URLs simple and intuitive

### 4.2 Idempotency
- GET, PUT, DELETE should be idempotent
- POST is not idempotent
- Understanding safe vs idempotent methods

### 4.3 Versioning Strategies
- URI versioning: `/v1/users`
- Header versioning: `Accept: application/vnd.api.v1+json`
- Query parameter: `?version=1`

### 4.4 Error Handling
- Consistent error response format
- Meaningful error messages
- Error codes for client handling
- Include validation details

## 5. Security

### 5.1 Authentication Methods
- API Keys
- Bearer Tokens
- OAuth 2.0
- JWT (JSON Web Tokens)
- Basic Authentication

### 5.2 Authorization
- Role-based access control (RBAC)
- Permission scopes
- Resource-level permissions

### 5.3 Security Best Practices
- Always use HTTPS
- Validate input
- Sanitize output
- Rate limiting
- CORS configuration
- SQL injection prevention
- XSS protection

## 6. Advanced Topics

### 6.1 HATEOAS
- Hypermedia as the Engine of Application State
- Self-discoverable APIs
- Link relations

### 6.2 Rate Limiting
- Throttling strategies
- Rate limit headers
- Handling 429 Too Many Requests

### 6.3 Pagination
- Offset-based pagination
- Cursor-based pagination
- Page-based pagination
- Metadata in responses

### 6.4 Caching
- Cache-Control headers
- ETag and If-None-Match
- Last-Modified and If-Modified-Since
- CDN integration

### 6.5 Content Negotiation
- Accept header
- Content-Type header
- Supporting multiple formats (JSON, XML, CSV)

### 6.6 API Documentation
- OpenAPI/Swagger specification
- API reference documentation
- Interactive documentation
- Code examples

### 6.7 Testing
- Unit tests for endpoints
- Integration tests
- Load testing
- Security testing

### 6.8 Performance Optimization
- Database indexing
- Response compression (gzip)
- Efficient queries
- Caching strategies
- Async operations

## 7. Data Formats

### 7.1 JSON
- Structure and syntax
- Best practices
- JSON Schema validation

### 7.2 XML
- When to use XML
- Structure and namespaces

### 7.3 Other Formats
- CSV for data exports
- Protocol Buffers
- MessagePack

## 8. Real-World Considerations

### 8.1 Error Recovery
- Retry mechanisms
- Circuit breakers
- Graceful degradation

### 8.2 Monitoring and Logging
- Request/response logging
- Performance metrics
- Error tracking
- Analytics

### 8.3 Scalability
- Horizontal vs vertical scaling
- Load balancing
- Database replication
- Microservices architecture

### 8.4 Deprecation Strategy
- Announcing deprecation
- Sunset headers
- Migration guides
- Maintaining backwards compatibility

## 9. Tools and Technologies

### 9.1 Development Tools
- Postman
- Insomnia
- curl
- HTTPie

### 9.2 Testing Tools
- Jest, Mocha, pytest
- Supertest
- REST Assured

### 9.3 Documentation Tools
- Swagger/OpenAPI
- Postman Collections
- API Blueprint
- RAML

### 9.4 Monitoring Tools
- New Relic
- Datadog
- Prometheus + Grafana
- ELK Stack

## 10. Related Concepts

### 10.1 Alternative API Styles
- GraphQL
- gRPC
- SOAP
- WebSocket APIs

### 10.2 API Gateway
- Routing
- Authentication/Authorization
- Rate limiting
- Request transformation

### 10.3 Webhooks
- Push vs pull models
- Event-driven architecture
- Webhook security
