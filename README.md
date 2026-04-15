# HBT_pathing-AI-project

## 🗂️ Project Structure
hbt-routing-system/
├── data/                         # Chứa dữ liệu bản đồ
│   ├── raw/                      # Dữ liệu gốc tải về
│   │   └── map.osm               # File bản đồ Hai Bà Trưng (OpenStreetMap)
│   └── processed/                # Dữ liệu đã qua tiền xử lý (Binary/Pickle)
│       ├── hbt_graph.pkl         # Đồ thị Graph (Adjacency List)
│       └── spatial_index.pkl     # Cấu trúc KD-Tree để tìm Node nhanh
├── src/                          # Mã nguồn chính (Backend focus)
│   ├── data_processing/          # Lớp xử lý dữ liệu (Data Engineering)
│   │   ├── osm_parser.py         # Chuyển .osm sang cấu trúc Graph
│   │   ├── spatial_index.py      # Tìm Node gần nhất từ tọa độ GPS
│   │   └── traffic_manager.py    # Quản lý hệ số tắc đường/ngập lụt
│   ├── algorithms/               # Lớp thuật toán cốt lõi
│   │   ├── astar.py              # Cài đặt thuật toán A* (Priority Queue)
│   │   └── cost_functions.py     # Định nghĩa hàm chi phí động w(e, t)
│   ├── api/                      # Giao tiếp Backend (FastAPI)
│   │   └── main.py               # Endpoint nhận tọa độ và trả về Path
│   └── utils/                    # Các hàm bổ trợ 
│       └── geo_utils.py          # Tính khoảng cách Haversine, xử lý tọa độ
├── frontend/                     # Giao diện người dùng (React focus)
│   ├── public/                   # Tài nguyên tĩnh (index.html, icons)
│   └── src/                      # Source code React
│       ├── components/           # Các thành phần giao diện
│       │   ├── MapView.js        # Hiển thị bản đồ Leaflet & Polyline
│       │   ├── SearchPanel.js    # Bảng điều khiển và tìm kiếm
│       │   └── TrafficLegend.js  # Chú giải màu sắc và ký hiệu
│       ├── api.js                # Quản lý các lệnh gọi Axios tới Backend
│       └── App.js                # Thành phần gốc điều phối ứng dụng
├── main.py                       # Script khởi chạy hệ thống (Python)
├── requirements.txt              # Danh sách thư viện (fastapi, networkx...)
└── package.json                  # Quản lý thư viện Frontend (React)
