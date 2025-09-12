# 📌 College Schedule Data Pipeline  

This project automates the process of collecting, transforming, and serving **college schedule data**.  
Instead of relying on manual updates, the pipeline scrapes data from the official college website, cleans and structures it, stores it in **MongoDB**, and makes it accessible through a backend API that powers a **schedule website**.  

---

## 🚀 Features  
- **Web Scraping** → Extract raw course and schedule data directly from the college website using Python & BeautifulSoup.  
- **Data Cleaning & Transformation** → Process and structure the scraped data with Pandas in Jupyter Notebook.  
- **Database** → Store the cleaned data in **MongoDB Atlas** for scalable access.  
- **Backend API** → Fetch data from MongoDB and serve it in JSON format (Node.js / Python).  
- **Frontend Website** → Display schedules dynamically for students.  

---

## 🔄 Workflow  
```mermaid 
flowchart TD
    A[🌐 College Website] -->|HTML Data| B(Web Scraper<br>Python + BeautifulSoup)
    B -->|Raw Unstructured Data| C[Jupyter Notebook]
    C -->|Pandas<br>Data Cleaning & Transformation| D[💾 MongoDB Atlas]
    D -->|Query Data| E[🔧 Backend API<br>Node.js/Python]
    E -->|JSON Data| F[📅 Scheduling Website<br>Frontend]
    F -->|User Search Request| E
    E -->|Query| D

    %% Styling for clarity
    classDef source fill:#cde4ff,stroke:#007bff,stroke-width2px
    classDef process fill:#ffebcc,stroke:#ff9800,stroke-width2px
    classDef storage fill:#d7f4d7,stroke:#28a745,stroke-width2px
    classDef backend fill:#e8d7f4,stroke:#6f42c1,stroke-width2px
    classDef frontend fill:#ffd7e8,stroke:#e91e63,stroke-width2px

    class A source
    class B,C process
    class D storage
    class E backend
    class F frontend
