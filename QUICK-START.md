# FlowViz Quick Start Guide

This guide provides basic instructions to get up and running with FlowViz quickly.

## Installation

1. Make sure you have Node.js installed (v14+)
2. Clone or download the FlowViz repository
3. Open a terminal and navigate to the FlowViz-Desktop directory
4. Run: `npm install` to install dependencies

## Running the Application

From the FlowViz-Desktop directory, run:
```
npm start
```

## Visualizing Your AWS Network

### Method 1: Import JSON Data
1. Click on the "Import JSON" tab
2. Click the "Open JSON File" button
3. Navigate to and select the sample-data.json file (or your own data file)
4. Click "Generate Network Diagram"

### Method 2: Manual Input
1. Click on the "Manual Input" tab
2. Add resources using the "Add Another Resource" button
3. Fill in the details for each resource
4. Click "Generate Diagram"

## Using the Path Analysis Simulator

1. Import or generate a network diagram
2. In the "Path Analysis Simulator" section:
   - Select a source
   - Choose a destination type
   - Select or enter a destination
   - Set port and protocol
3. Click "Simulate Path"
4. Review the path analysis results

## Tips for Better Results

- For best visualization, use hierarchical layout (default)
- Click on nodes to see detailed information
- Use the "Reset View" button if your diagram becomes hard to read
- Turn physics on temporarily to reorganize nodes, then off for stable viewing
- Export your diagram as an image using the "Export Diagram" button

## Troubleshooting

If the application doesn't start:
- Ensure you're in the FlowViz-Desktop directory
- Verify that all dependencies are installed
- Check for error messages in the terminal

If importing JSON fails:
- Confirm the file follows the required format structure
- Check sample-data.json for reference

## Getting Help

Refer to the full README.md for detailed information about all features and options. 