# Java Search Engine

A lightweight yet powerful search engine implementation in Java that enables efficient full-text search capabilities for documents and web content.

## Features

- Full-text search with ranking algorithm
- Support for multiple document formats (PDF, TXT, HTML)
- Inverted index for fast query processing
- Boolean search operations (AND, OR, NOT)
- Term frequency-inverse document frequency (TF-IDF) scoring
- Result highlighting and snippet generation
- Configurable stopword filtering
- Stemming and lemmatization support
- Concurrent indexing for improved performance

## Requirements

- Java JDK 11 or higher
- Maven 3.6+

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/java-search-engine.git
cd java-search-engine
```

2. Build the project:
```bash
mvn clean install
```

## Usage

### Basic Search
```java
SearchEngine engine = new SearchEngine();
engine.addDocument("doc1", "path/to/document1.txt");
engine.addDocument("doc2", "path/to/document2.txt");
SearchResults results = engine.search("your query here");
```

### Advanced Configuration
```java
SearchConfig config = new SearchConfig.Builder()
    .setMaxResults(10)
    .enableStopwords(true)
    .setStemming(true)
    .setBoostRecent(true)
    .build();

SearchEngine engine = new SearchEngine(config);
```

## Configuration Options

- `maxResults`: Maximum number of search results (default: 100)
- `stopwordsEnabled`: Enable/disable stopword filtering (default: true)
- `stemmingEnabled`: Enable/disable word stemming (default: true)
- `boostRecent`: Boost score of more recent documents (default: false)
- `snippetLength`: Length of result snippets in characters (default: 150)

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## Support

- Submit bug reports via GitHub Issues
- Join our community Discord server for discussions
- Check out the wiki for advanced usage examples
