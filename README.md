<!-- WIP Header -->
<div align="center">

<img alt="Work in Progress" src="https://img.shields.io/badge/Status-Work_in_Progress-red?style=for-the-badge" />

<h2>⚠️ ACHTUNG / WARNING</h2>

<strong>DE:</strong> Dieses Repository ist noch im Aufbau. Einige/mehrere Notebooks sind derzeit nur Platzhalter und werden laufend ergänzt.<br/>
<strong>EN:</strong> This repository is still under construction. Several notebooks are placeholders and will be filled over time.

</div>

---

**Setup (in Fabric-Notebooks)**
- In Fabric-Notebooks sind Auth-Tokens i. d. R. **vorautorisiert** (keine manuellen MSAL-Flows nötig).
- Für REST/Administration: **SemPy-Clients** oder **Fabric/Power BI REST APIs** verwenden.

---

## Umgang mit Workspaces
Typische Aufgaben:
- Workspaces **auflisten, filtern, inventarisieren**
- **Rollen & Berechtigungen** (Viewer/Contributor/Admin, SPNs, Gruppen) prüfen
- **Deployment Pipelines** & **Git-Integration** orchestrieren
- **Naming/Tagging** durchsetzen, Domänen/Projekte konsolidieren

**Notebook-Vorlagen**
- [`notebooks/workspaces/01_list_workspaces.ipynb`](notebooks/workspaces/01_list_workspaces.ipynb)
- [`notebooks/workspaces/02_workspace_inventory.ipynb`](notebooks/workspaces/02_workspace_inventory.ipynb)
- [`notebooks/workspaces/03_roles_and_membership_report.ipynb`](notebooks/workspaces/03_roles_and_membership_report.ipynb)
- [`notebooks/workspaces/04_git_integration_basics.ipynb`](notebooks/workspaces/04_git_integration_basics.ipynb)
- [`notebooks/workspaces/05_deployment_pipelines_overview.ipynb`](notebooks/workspaces/05_deployment_pipelines_overview.ipynb)

---

## Grundkonzepte (REST API, `semPy.fabric`, SemPy Labs)
- **Fabric/Power BI REST APIs**  
  Programmgesteuerter Zugriff auf Workspaces & Items (Listen, Metadaten, Operationen).  
  *Core-Endpunkte* sind rollenbasiert; *Admin-Endpunkte* erfordern **Fabric-Admin** oder **Service Principal**.

- **`semPy.fabric` (Semantic Link – SemPy)**  
  Python-Bibliothek für Fabric-Notebooks; stellt **REST-Clients** (u. a. Power BI, Fabric) und semantische Hilfen bereit. Tokens werden aus der Notebook-Umgebung bezogen.

- **SemPy Labs**  
  **Erweiterungs-Bibliothek** für Fabric-Notebooks mit zusätzlichen, praxisnahen Helfern rund um SemPy/Semantic Link.

**Beispiel-Notebooks**
- [`notebooks/concepts/01_rest_basics.ipynb`](notebooks/concepts/01_rest_basics.ipynb)
- [`notebooks/concepts/02_semPy_clients.ipynb`](notebooks/concepts/02_semPy_clients.ipynb)
- [`notebooks/concepts/03_semPy_labs_toolbox.ipynb`](notebooks/concepts/03_semPy_labs_toolbox.ipynb)

---

## Item-Types – Übersicht & Notebook-Vorlagen

> Unter jeder Überschrift findest du **Kurzbeschreibung** und **Platzhalter-Notebooks** (einfach anlegen & füllen).

### Lakehouse
**Kurz:** Delta-/Parquet-Speicher in OneLake inkl. SQL-Endpoint & Notebooks; ideal für ELT/DE-Workloads.  
**Notebooks**
- [`notebooks/items/lakehouse/01_list_lakehouses.ipynb`](notebooks/items/lakehouse/01_list_lakehouses.ipynb)
- [`notebooks/items/lakehouse/02_tables_delta_manage.ipynb`](notebooks/items/lakehouse/02_tables_delta_manage.ipynb)
- [`notebooks/items/lakehouse/03_shortcuts_manage.ipynb`](notebooks/items/lakehouse/03_shortcuts_manage.ipynb)
- [`notebooks/items/lakehouse/04_sql_endpoint_queries.ipynb`](notebooks/items/lakehouse/04_sql_endpoint_queries.ipynb)

### Warehouse (Fabric Data Warehouse)
**Kurz:** Vollständig verwaltetes MPP-SQL-Warehouse (T-SQL, ELT, Reporting).  
**Notebooks**
- [`notebooks/items/warehouse/01_list_warehouses.ipynb`](notebooks/items/warehouse/01_list_warehouses.ipynb)
- [`notebooks/items/warehouse/02_execute_sql_tasks.ipynb`](notebooks/items/warehouse/02_execute_sql_tasks.ipynb)
- [`notebooks/items/warehouse/03_maintenance_and_monitoring.ipynb`](notebooks/items/warehouse/03_maintenance_and_monitoring.ipynb)

### KQL Database (Real-Time Intelligence)
**Kurz:** Kusto-basierte DB für Logs/Telemetry & Zeitreihen-Analysen.  
**Notebooks**
- [`notebooks/items/kql-database/01_list_kql_databases.ipynb`](notebooks/items/kql-database/01_list_kql_databases.ipynb)
- [`notebooks/items/kql-database/02_create_and_ingest.ipynb`](notebooks/items/kql-database/02_create_and_ingest.ipynb)
- [`notebooks/items/kql-database/03_query_basics.ipynb`](notebooks/items/kql-database/03_query_basics.ipynb)

### Eventhouse (Real-Time Intelligence)
**Kurz:** Speicher & Analyse für Echtzeit-Daten, optimiert für Stream-Ingestion & Near-Real-Time.  
**Notebooks**
- [`notebooks/items/eventhouse/01_list_eventhouses.ipynb`](notebooks/items/eventhouse/01_list_eventhouses.ipynb)
- [`notebooks/items/eventhouse/02_ingest_and_explore.ipynb`](notebooks/items/eventhouse/02_ingest_and_explore.ipynb)

### Eventstream (Real-Time Intelligence)
**Kurz:** Stream-Ingestion & Routing (z. B. in **Lakehouse** oder **KQL DB**).  
**Notebooks**
- [`notebooks/items/eventstream/01_list_eventstreams.ipynb`](notebooks/items/eventstream/01_list_eventstreams.ipynb)
- [`notebooks/items/eventstream/02_routes_to_lakehouse_kql.ipynb`](notebooks/items/eventstream/02_routes_to_lakehouse_kql.ipynb)

### Data Pipeline (Data Factory)
**Kurz:** No-/Low-Code-Pipelines für ELT/ETL, Orchestrierung & Scheduling.  
**Notebooks**
- [`notebooks/items/data-pipeline/01_list_pipelines.ipynb`](notebooks/items/data-pipeline/01_list_pipelines.ipynb)
- [`notebooks/items/data-pipeline/02_run_and_monitor.ipynb`](notebooks/items/data-pipeline/02_run_and_monitor.ipynb)
- [`notebooks/items/data-pipeline/03_bulk_parameterized_runs.ipynb`](notebooks/items/data-pipeline/03_bulk_parameterized_runs.ipynb)

### Dataflow Gen2 (Data Factory)
**Kurz:** Power Query (Gen2) für wiederverwendbare Aufbereitung auf Fabric-Ebene.  
**Notebooks**
- [`notebooks/items/dataflow-gen2/01_list_dataflows.ipynb`](notebooks/items/dataflow-gen2/01_list_dataflows.ipynb)
- [`notebooks/items/dataflow-gen2/02_refresh_control.ipynb`](notebooks/items/dataflow-gen2/02_refresh_control.ipynb)

### Notebook (DE/DS)
**Kurz:** Py/Spark-Notebook-Ausführung für Automationsskripte & Admin-Tasks.  
**Notebooks**
- [`notebooks/items/notebook/01_inventory_and_metadata.ipynb`](notebooks/items/notebook/01_inventory_and_metadata.ipynb)
- [`notebooks/items/notebook/02_job_scheduling_patterns.ipynb`](notebooks/items/notebook/02_job_scheduling_patterns.ipynb)

### Spark Job Definition
**Kurz:** Wiederverwendbare Spark-Jobs, planbar & pipeline-fähig.  
**Notebooks**
- [`notebooks/items/spark-job-definition/01_list_spark_jobs.ipynb`](notebooks/items/spark-job-definition/01_list_spark_jobs.ipynb)
- [`notebooks/items/spark-job-definition/02_submit_and_monitor.ipynb`](notebooks/items/spark-job-definition/02_submit_and_monitor.ipynb)

### Environment
**Kurz:** Verwaltete Umgebungen (Pakete/Dependencies) für reproduzierbare Runs.  
**Notebooks**
- [`notebooks/items/environment/01_list_environments.ipynb`](notebooks/items/environment/01_list_environments.ipynb)
- [`notebooks/items/environment/02_package_management.ipynb`](notebooks/items/environment/02_package_management.ipynb)

### Semantic Model (Power BI)
**Kurz:** Datasets/Semantic Models; per **SemPy** (DAX, Measures, Metadaten) zugreifbar.  
**Notebooks**
- [`notebooks/items/semantic-model/01_list_models.ipynb`](notebooks/items/semantic-model/01_list_models.ipynb)
- [`notebooks/items/semantic-model/02_read_evaluate_measures.ipynb`](notebooks/items/semantic-model/02_read_evaluate_measures.ipynb)
- [`notebooks/items/semantic-model/03_export_metadata_annotations.ipynb`](notebooks/items/semantic-model/03_export_metadata_annotations.ipynb)

### Report (Power BI)
**Kurz:** Berichte inventarisieren, Verknüpfungen & Metadaten prüfen.  
**Notebooks**
- [`notebooks/items/report/01_list_reports.ipynb`](notebooks/items/report/01_list_reports.ipynb)
- [`notebooks/items/report/02_dataset_binding_checks.ipynb`](notebooks/items/report/02_dataset_binding_checks.ipynb)

### Dashboard (Power BI)
**Kurz:** Kachel-Dashboards überwachen (Bindings, Aktualität).  
**Notebooks**
- [`notebooks/items/dashboard/01_list_dashboards.ipynb`](notebooks/items/dashboard/01_list_dashboards.ipynb)

### Mirroring
**Kurz:** Spiegelung externer Quellen (z. B. DBs, Kataloge) nach Fabric.  
**Notebooks**
- [`notebooks/items/mirroring/01_list_mirrored_sources.ipynb`](notebooks/items/mirroring/01_list_mirrored_sources.ipynb)

### Shortcuts (OneLake)
**Kurz:** Virtuelle Verweise auf externe Speicher (ADLS/OneLake-Bereiche).  
**Notebooks**
- [`notebooks/items/shortcuts/01_list_and_validate_shortcuts.ipynb`](notebooks/items/shortcuts/01_list_and_validate_shortcuts.ipynb)

> **Hinweis:** Unterstützungsumfang für **Deployment Pipelines**/**Git-Integration** kann je Item-Type variieren.

---

## Spezielle Anwendungsfälle / Fertige Lösungen
- [`notebooks/solutions/workspace_audit_all_items.ipynb`](notebooks/solutions/workspace_audit_all_items.ipynb)  
  *Inventar aller Items je Workspace: Owner, Rechte, Refresh-Status, Health.*
- [`notebooks/solutions/permissions_report_workspace_and_items.ipynb`](notebooks/solutions/permissions_report_workspace_and_items.ipynb)  
  *Vollständiger Rollen-/Mitglieder-Report (User, Gruppen, SPNs).*
- [`notebooks/solutions/dataset_refresh_orchestration.ipynb`](notebooks/solutions/dataset_refresh_orchestration.ipynb)  
  *Geplante/Ad-hoc-Refreshes koordinieren, Logging, Abhängigkeiten.*
- [`notebooks/solutions/eventstream_to_lakehouse_and_kql.ipynb`](notebooks/solutions/eventstream_to_lakehouse_and_kql.ipynb)  
  *Streams aufnehmen, routen, in Lakehouse/KQL verfügbar machen.*
- [`notebooks/solutions/semantic_model_quality_checks.ipynb`](notebooks/solutions/semantic_model_quality_checks.ipynb)  
  *Measures evaluieren, Annotationen prüfen, Export.*

---

## Sicherheit & Berechtigungen
- **Core REST** (z. B. List Items/Reports): mind. **Viewer**-Rolle im Ziel-Workspace.
- **Admin REST** (Tenant/Workspace/Access): **Fabric-Admin** oder **Service Principal** mit passenden Scopes.
- **Notebook-Kontext** in Fabric: Tokens werden typischerweise **automatisch bereitgestellt** (SemPy-Clients greifen darauf zu).

---

## Namenskonventionen
- **Notebooks**: `NN_<kurzbeschreibung>.ipynb` (z. B. `01_list_workspaces.ipynb`)
- **Ordner**: wie oben (kebab-case für Item-Types, z. B. `data-pipeline`)
- **Konfiguration**: `config/<env>.json` (IDs, Filter, Defaults)
- **Helper**: Gemeinsame Funktionen in `lib/` kapseln (z. B. REST-Client, Paging, Retry, Logging)

---

## Beitragen
1. Neues Notebook im passenden Ordner anlegen (siehe **Item-Types**).  
2. Am Kopf kurz Ziel, Inputs, Outputs & benötigte Rollen dokumentieren.  
3. Bei REST-Nutzung: Endpunkte, Pagination & Retry notieren.  
4. Bei SemPy/SemPy Labs: Version & wichtige Funktionen erwähnen.  
5. PR erstellen – **Ordnerstruktur & Namenskonventionen** einhalten.

---

## Verwandte Repositories (GitHub)

**Offiziell**
- [microsoft/fabric-samples] – Lern- & Feature-Samples inkl. Notebooks und API-Beispiele.  
- [microsoft/fabric-toolbox] – Tools, Accelerators, **Admin-/Monitoring-Notebooks**, CI/CD.  
- [microsoft/semantic-link-labs] – Python-Lib + **Wrapper für Fabric/Power BI/Graph REST**; Beispiel-Notebooks.  
- [microsoft/semantic-link-functions] – Erweiterte semantische Funktionen für DataFrames.  
- [microsoft/fabricrealtimelab] – End-to-End-Workshop (RTI, KQL, DW/Lakehouse) mit Notebooks.

**Community**
- [m-kovalsky/Fabric] – Praktische **Notebook-Snippets** rund um SemPy & Labs (Admin/BI).  
- [GT-Analytics/fuam-basic] – **Fabric Unified Admin Monitoring** (Pipelines + Notebooks + Reports).  
- [ProdataSQL/Fabric] – Code-Snippets (Auth, SQL-Endpoint, etc.).  
- [gronnerup/Fabric] – Diverse Fabric-Samples.  
- [DaSenf1860/ms-fabric-sdk-core] – Community-**Python SDK** (REST/ARM Wrapper).  
- [PowerBiDevCamp/FabricUserApiDemo] – C#-Sample zur Fabric **User API** (Automation).

> Tipp: Für „Notebook-first“-Automatisierung in Fabric besonders relevant:
> **fabric-toolbox** (Monitoring/CI/CD) und **semantic-link-labs** (REST-Wrappers & Admin).


---

**Happy Fabric-ing!**
