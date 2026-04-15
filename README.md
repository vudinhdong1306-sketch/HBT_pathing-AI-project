# HBT_pathing-AI-project
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
