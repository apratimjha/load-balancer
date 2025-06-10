Load Balancer Simulator
A Python-based load balancer simulation that implements and compares three different load balancing algorithms:

Round Robin: Distributes requests evenly across servers in rotation
Least Connections: Routes requests to the server with the fewest active connections
Load Aware: Intelligently distributes based on server capacity and current load

Features

🔄 Multiple Algorithms: Compare performance across different load balancing strategies
📊 Performance Visualization: Built-in matplotlib charts for performance analysis
🧵 Thread-Safe: Implements proper threading and locking mechanisms
🔍 Real-time Monitoring: Track request assignments and server loads
⚡ Health Checks: Automatic server health monitoring and failover

Requirements
python >= 3.6
matplotlib
Installation

Clone this repository:

bashgit clone https://github.com/yourusername/load-balancer-simulator.git
cd load-balancer-simulator

Install dependencies:

bashpip install matplotlib
Usage
Run the simulation:
bashpython load_balancer.py
The program will:

Generate random client requests
Process them through each load balancing algorithm
Display performance metrics and a comparison chart

Load Balancing Algorithms
Round Robin
Cycles through servers in order, ensuring equal distribution of requests.
Least Connections
Routes new requests to the server currently handling the fewest connections.
Load Aware
Considers both server capacity and current load, with built-in request queuing and health monitoring.
Example Output
Round Robin:
Request 234 assigned to web-01
Request 45 assigned to web-02
...

Least Connections:
Request 156 assigned to web-03
✅ Request of size 89 completed on web-01
...

Load-Aware Balancer:
Request 267 (req_id 1) assigned to web-02
Request 134 (req_id 2) queued
...
Configuration
Modify the server configuration in the main section:
pythonservers = {
    "web-01": 100,  # capacity
    "web-02": 150,  # capacity
    "web-03": 400   # capacity
}
Contributing

Fork the repository
Create a feature branch (git checkout -b feature/amazing-feature)
Commit your changes (git commit -m 'Add amazing feature')
Push to the branch (git push origin feature/amazing-feature)
Open a Pull Request

License
This project is open source and available under the MIT License.
Author
Created as a demonstration of load balancing algorithms and distributed system concepts.
