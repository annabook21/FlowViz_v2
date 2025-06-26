# FlowViz - AWS Network Visualization and Analysis

FlowViz is a powerful desktop application designed to help network engineers visualize, understand, and analyze traffic flows in AWS environments. By generating interactive network diagrams and providing detailed path analysis, FlowViz simplifies complex AWS networking concepts and makes troubleshooting easier.

![FlowViz Screenshot](https://placeholder-for-screenshot.png)

## Features

### Interactive Network Visualization
- **Hierarchical Layout**: Clear left-to-right traffic flow visualization
- **Color-coded Components**: Intuitive visual representation of different AWS resources
- **Dynamic Interaction**: Click, highlight, focus, and zoom on network components
- **Component Details Panel**: View detailed information about selected resources
- **Traffic Flow Display**: Visualize actual or potential traffic paths in your AWS environment

### Path Analysis Simulator
- **Source-Destination Selection**: Choose traffic source and destination via dropdown menus
- **Multiple Destination Types**: Support for internal, external, VPC endpoints, and VPC peering
- **Comprehensive Traffic Evaluation**: Analysis based on security groups, NACLs, and route tables
- **Hop-by-Hop Analysis**: Detailed evaluation of each step in the traffic path
- **Visual Path Highlighting**: See the exact route through your AWS infrastructure

### Data Integration
- **JSON Import**: Import network data from FlowViz-compatible JSON files
- **Manual Input**: Option to manually input AWS resources and their relationships
- **Export Capabilities**: Save diagrams as images or network details as text files

## Installation

### Prerequisites
- Node.js (version 14 or later)
- npm (version 6 or later)

### Install from Source
1. Clone the repository or download the source code
   ```
   git clone https://github.com/username/flowviz.git
   ```

2. Navigate to the project directory
   ```
   cd FlowViz-Desktop
   ```

3. Install dependencies
   ```
   npm install
   ```

### Build for Your Platform
FlowViz can be packaged for Windows, macOS, and Linux platforms:

- **For macOS**:
  ```
  npm run package-mac
  ```

- **For Windows**:
  ```
  npm run package-win
  ```

- **For Linux**:
  ```
  npm run package-linux
  ```

## Running FlowViz

### From Source
Navigate to the project directory and run:
```
npm start
```

### From Packaged Application
After building the application, you can find the packaged application in the `dist` directory. Run the appropriate file for your platform:
- macOS: `FlowViz Desktop.app`
- Windows: `FlowViz Desktop.exe`
- Linux: `FlowViz Desktop.AppImage` or `flowviz-desktop.deb`

## Using FlowViz

### Import Network Data
1. Launch FlowViz
2. Select the "Import JSON" tab
3. Click "Open JSON File" and select a FlowViz-compatible JSON file
4. Click "Generate Network Diagram" to visualize your network

### Manual Network Input
1. Select the "Manual Input" tab
2. Add resources using the "Add Another Resource" button
3. Fill in details for each resource (type, ID, VPC association, etc.)
4. Click "Generate Diagram" to create your visualization

### Interact with the Network Diagram
- **Select Resource**: Click on any node to view its details
- **Reset View**: Use the "Reset View" button to return to the default view
- **Toggle Physics**: Enable/disable the physics engine to reposition nodes
- **Export Diagram**: Save the current diagram as a PNG image

### Use the Path Analysis Simulator
1. Select a source resource from the dropdown menu
2. Choose a destination type (internal, external, VPC endpoint, or VPC peering)
3. Select or enter a specific destination
4. Specify port and protocol
5. Click "Simulate Path" to perform the analysis
6. Review the path and any allow/deny decisions along the way

## Data Format

FlowViz uses a specific JSON structure to represent AWS network components. A sample data file is included in the application. Key elements include:

- **metadata**: Information about the analysis (instance ID, VPC ID, timestamp)
- **network_components**: AWS resources (VPC, subnets, route tables, gateways, security groups)
- **traffic_flows**: Actual or potential traffic paths with detailed hop information

For full schema details, see the included sample-data.json file.

## Generating Compatible Data

FlowViz-compatible data can be generated using:

1. **AWS CloudFormation Template**: Use the included NAS_Template.yaml to deploy a solution that automatically analyzes your AWS environment and generates FlowViz-compatible data.

2. **Manual Creation**: Create JSON files manually following the format in sample-data.json.

## Technical Architecture

FlowViz is built using:
- **Electron**: Cross-platform desktop application framework
- **vis.js**: Network visualization library
- **HTML/CSS/JavaScript**: Front-end implementation

The application consists of:
- **main.js**: Electron main process script
- **preload.js**: Secure bridge between renderer and main processes
- **src/index.html**: Main application interface
- **src/style.css**: Application styling

## Contributing

Contributions to FlowViz are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## Disclaimer

Path analysis is based solely on AWS configuration (Security Groups, NACLs, Route Tables) captured in the imported data. This analysis cannot account for customer firewalls, proxies, or other network conditions outside of AWS that may restrict traffic. Results should be considered theoretical until validated in the actual environment.

## License

This project is licensed under the ISC License - see the LICENSE file for details.

## Credits

Created by Anna Booker © 2024
- GitHub: [annabook21](https://github.com/annabook21?tab=repositories)
- LinkedIn: [annadbooker](https://linkedin.com/in/annadbooker) 