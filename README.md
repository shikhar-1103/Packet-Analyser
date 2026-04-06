# Packet Analyzer

A high-performance network packet analysis tool with Deep Packet Inspection (DPI) capabilities, multi-threaded processing, and rule-based packet filtering.

## Features

- **Deep Packet Inspection (DPI)**: Analyze network traffic at the application layer
- **Multi-threaded Processing**: Load-balanced packet processing for high performance
- **Connection Tracking**: Monitor and track network connections
- **SNI Extraction**: Extract Server Name Indication from TLS packets
- **PCAP Support**: Read and analyze packet capture files
- **Rule-based Filtering**: Define and apply custom rules for packet analysis
- **Fast Path Processing**: Optimized packet processing pipeline

## Project Structure

```
Packet_analyzer/
├── include/              # Header files
│   ├── dpi_engine.h
│   ├── packet_parser.h
│   ├── connection_tracker.h
│   ├── rule_manager.h
│   ├── sni_extractor.h
│   └── ...
├── src/                  # Source files
│   ├── main.cpp
│   ├── dpi_engine.cpp
│   ├── packet_parser.cpp
│   └── ...
├── CMakeLists.txt        # Build configuration
└── README.md             # This file
```

## Requirements

- C++11 or later
- CMake 3.10+
- libpcap (for packet capture)
- pthreads (for multi-threading)

## Building

### Linux/macOS

```bash
mkdir build
cd build
cmake ..
make
```

### Windows

See [WINDOWS_SETUP.md](WINDOWS_SETUP.md) for detailed instructions.

## Usage

Run the packet analyzer with:

```bash
./dpi_engine <pcap_file>
```

## Features in Detail

### DPI Engine
Performs deep packet inspection to identify protocols and extract application-layer information.

### Connection Tracker
Maintains state information about active network connections for stateful analysis.

### Rule Manager
Defines and applies rules for packet classification and filtering.

### Multi-threading
Uses load balancing to distribute packet processing across multiple threads for improved performance.

## License

This project is provided as-is for educational and research purposes.
