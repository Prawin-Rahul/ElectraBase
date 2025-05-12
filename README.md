# ElectraBase
This is a Data Visualization application to display insights on Elections across various levels in India , based on already conducted election data . 
This Helps us to understand previous trends and patterns , and helps us indentify behaviour and make informed decisions .

```
ElectraBase/
│
├── config/
│   └── settings.py           # DB credentials, file paths, constants
│
├── db/
│   ├── base.py               # SQLAlchemy base and engine setup
│   ├── models.py             # Table definitions (shared between ETL & API)
│   └── schema.sql            # (Optional) raw SQL schema
│
├── etl/
│   ├── __init__.py
│   ├── load_party.py         # ETL script for dim_party
│   ├── load_state.py         # ETL script for dim_state
│   ├── load_pc.py            # ETL script for dim_pc
│   ├── load_phase.py         # ETL script for dim_phase
│   └── run_etl.py            # Orchestrator to run all ETL jobs
│
├── api/
│   ├── __init__.py
│   ├── main.py               # FastAPI or Flask app
│   ├── routes/
│   │   └── pc.py             # Route to get PCs
│   ├── services/
│   │   └── pc_service.py     # Logic to fetch from DB
│   └── schemas/
│       └── pc.py             # Pydantic schema for API response
│
├── utils/
│   └── helpers.py            # Common utilities (hashing, cleaning)
│
├── requirements.txt
└── README.md
```
