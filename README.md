# HBT_pathing-AI-project
This project is a web-based dynamic pathfinding application built with FastAPI (Python) and React (JavaScript), utilizing the A algorithm and a custom cost function to provide optimal routing that intelligently avoids real-time traffic congestion and flood zones.

```bash
## 🗂️ Project Structure
hbt-routing-system/
├── data/                         
│   ├── raw/                      
│   │   └── map.osm              
│   └── processed/               
│       ├── hbt_graph.pkl         
│       └── spatial_index.pkl     
├── src/                          
│   ├── data_processing/          
│   │   ├── osm_parser.py         
│   │   ├── spatial_index.py      
│   │   └── traffic_manager.py    
│   ├── algorithms/              
│   │   ├── astar.py             
│   │   └── cost_functions.py     
│   ├── api/                      
│   │   └── main.py              
│   └── utils/                    
│       └── geo_utils.py         
├── frontend/                     
│   ├── public/                   
│   └── src/                      
│       ├── components/           
│       │   ├── MapView.js       
│       │   ├── SearchPanel.js    
│       │   └── TrafficLegend.js  
│       ├── api.js                
│       └── App.js                
├── main.py                       
├── requirements.txt             
└── package.json                  
