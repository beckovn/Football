Football system, created on Oracle Database 11g Express and Oracle Application Express 4.0.2.00.09
The system accepts .txt files with load data for matches - played and scheduled, and betting coeficients for 1, 2, X, Over 2.5 and Under 2.5 goals.
Tournaments include English Premier League and Championship, French League 1 and 2, Italian Serie A and B, German Bundesleague 1 and 2, Spanish League 1 and 2, Bulgarian League 1 and 2, Russian Premiere League and Dutch Eredivisie. Data is available for seasons 2021-2022 (match results only), 2022-2023, 2023-2024, 2024-2025 and 2025-2026 (results and coeficients for most of the leagues).

Instructions:
Install Oracle Database 11g Express Edition (or another version of Oracle Database). Import MY_SCHEMA.DMP (impdp system/password@XE schemas=schema_name(football) directory=DATA_PUMP_DIR dumpfile=my_schema.dmp logfile=import_schema.log) through sqlplus in CMD console (first put "my_schema.dmp" into directory set in "SELECT directory_path FROM dba_directories WHERE directory_name = 'DATA_PUMP_DIR';" and create the necessary user and privilleges: "CREATE USER football IDENTIFIED BY football; GRANT CONNECT, RESOURCE, DBA TO football;")
Upload "f101.sql" as an APEX application.
