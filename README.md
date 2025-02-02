# wise


### Architecture Overview

1. **Project Structure**
- Uses a feature-based architecture with clean separation of concerns
- Core functionality is organized in the `lib/src/core` directory
- Follows Flutter best practices for state management and routing

2. **Key Components**

#### Navigation & Routing
- Uses `go_router` for navigation with named routes
- Implements custom page transitions
- Centralized navigation service with global navigator key
- Route names are constants for type safety

#### State Management & DI
- Uses Riverpod for state management
- GetIt for dependency injection
- Clean separation of repositories and services

#### Network Layer
- Robust error handling with custom `NetworkExceptions` class
- Token-based authentication with interceptors
- Freezed for immutable network response models
- Comprehensive API result handling

#### Storage
- Local storage implementation using SharedPreferences
- Singleton pattern for storage access
- Handles theme preferences, tokens, and onboarding state

### Notable Features

1. **Error Handling**
```dart
class NetworkExceptions {
  static NetworkExceptions getDioException(error) {
    // Comprehensive error mapping
    // Handles various network scenarios
  }
}
```

2. **Token Management**
```dart
class TokenInterceptor extends Interceptor {
  // Handles token injection and refresh
  // Auto-logout on 401 errors
}
```

3. **Theme Management**
- Dark/light mode support
- Persistent theme preferences
- Custom theme configurations

### Best Practices Implemented

1. **Code Organization**
- Clear separation of concerns
- Consistent file naming conventions
- Modular architecture

2. **Security**
- Secure token storage
- Proper token refresh handling
- Session management

3. **UI/UX**
- Custom transitions
- Loading states
- Error feedback
- Responsive design

### Areas for Potential Improvement

1. **Testing**
- Could add more unit tests
- Integration testing coverage
- Widget testing

2. **Documentation**
- More inline documentation
- API documentation
- Architecture documentation



