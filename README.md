# Caching Abstraction + Implementation [![codecov](https://codecov.io/gh/bocato/Caching/branch/master/graph/badge.svg)](https://codecov.io/gh/bocato/Caching)


## Setup

- Use as an abstraction and implement your own cache service or use the provided `DiskCacheService` or `MemoryCacheService`.

## Usage

### Instantiate Service

```swift
let cacheService: CacheServiceProvider = MemoryCacheService()
```

### Save Data

```swift
cacheSevice.save(data: Data(), key: "someKey") { saveResult in
    // Do something with the result, or ignore it
}
```

### Load Data

```swift
cacheService.loadData(from: "someKey") { loadResult in
    // do something with the loading result 
}
```

### Clear Cache

```swift
cacheService.clear { clearResult in
    // Do something with the result, or ignore it
}
```


