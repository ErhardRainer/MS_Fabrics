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
- [microsoft/fabric-samples](https://github.com/microsoft/fabric-samples) – Lern- & Feature-Samples inkl. Notebooks und API-Beispiele.  
- [microsoft/fabric-toolbox](https://github.com/microsoft/fabric-toolbox) – Tools, Accelerators, **Admin-/Monitoring-Notebooks**, CI/CD.  
- [microsoft/semantic-link-labs](https://github.commicrosoft/semantic-link-labs) – Python-Lib + **Wrapper für Fabric/Power BI/Graph REST**; Beispiel-Notebooks.  
- [microsoft/semantic-link-functions](https://github.com/microsoft/semantic-link-functions) – Erweiterte semantische Funktionen für DataFrames.  
- [microsoft/fabricrealtimelab](https://github.com/microsoft/fabricrealtimelab) – End-to-End-Workshop (RTI, KQL, DW/Lakehouse) mit Notebooks.

**Community**
- [m-kovalsky/Fabric](https://github.com/m-kovalsky/Fabric) – Praktische **Notebook-Snippets** rund um SemPy & Labs (Admin/BI).  
- [GT-Analytics/fuam-basic](https://github.com/GT-Analytics/fuam-basic) – **Fabric Unified Admin Monitoring** (Pipelines + Notebooks + Reports).  
- [ProdataSQL/Fabric](https://github.com/ProdataSQL/Fabric) – Code-Snippets (Auth, SQL-Endpoint, etc.).  
- [gronnerup/Fabric](https://github.com/gronnerup/Fabric) – Diverse Fabric-Samples.  
- [DaSenf1860/ms-fabric-sdk-core](https://github.com/DaSenf1860/ms-fabric-sdk-core) – Community-**Python SDK** (REST/ARM Wrapper).  
- [PowerBiDevCamp/FabricUserApiDemo](https://github.com/PowerBiDevCamp/FabricUserApiDemo) – C#-Sample zur Fabric **User API** (Automation).

> Tipp: Für „Notebook-first“-Automatisierung in Fabric besonders relevant:
> **fabric-toolbox** (Monitoring/CI/CD) und **semantic-link-labs** (REST-Wrappers & Admin).

---
## Weitere Ressourcen: Relevante Internetquellen & YouTube

### Offizielle Microsoft Learn / Produktseiten
- [Microsoft Fabric – Doku-Startseite](https://learn.microsoft.com/en-us/fabric/)
- [Microsoft Fabric – Fundamentals (Grundlagen)](https://learn.microsoft.com/en-us/fabric/fundamentals/)
- [Was ist Microsoft Fabric?](https://learn.microsoft.com/en-us/fabric/fundamentals/microsoft-fabric-overview)
- [Was ist neu? (What's new)](https://learn.microsoft.com/en-us/fabric/fundamentals/whats-new)
- [Release Plan / Roadmap-Übersicht](https://learn.microsoft.com/en-us/fabric/release-plan/overview)
- [Fabric Roadmap (öffentliche Roadmap-Site)](https://roadmap.fabric.microsoft.com/)
- [Microsoft Fabric – Produktseite](https://www.microsoft.com/en-us/microsoft-fabric)

### REST & APIs
- [Microsoft Fabric REST API – Übersicht](https://learn.microsoft.com/en-us/rest/api/fabric/articles/)
- [Power BI REST API – Datasets](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets)
- [Power BI REST API – Reports](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/get-reports)

### SemPy / Semantic Link (für Notebooks)
- [Semantic Link (Python) – Overview](https://learn.microsoft.com/en-us/python/api/semantic-link/overview-semantic-link?view=semantic-link-python)
- [Semantic Link – Fabric Data Science Overview](https://learn.microsoft.com/en-us/fabric/data-science/semantic-link-overview)
- [PyPI: semantic-link-sempy](https://pypi.org/project/semantic-link-sempy/)
- [SemPy Labs – Funktionsdoku](https://semantic-link-labs.readthedocs.io/en/stable/sempy_labs.html)
- [SemPy Labs – GitHub](https://github.com/microsoft/semantic-link-labs)

### Workspaces, Rollen, Sicherheit & Governance
- [Rollen in Workspaces](https://learn.microsoft.com/en-us/fabric/fundamentals/roles-workspaces)
- [Permission Model (Fabric)](https://learn.microsoft.com/en-us/fabric/security/permission-model)
- [Governance & Compliance in Fabric – Überblick](https://learn.microsoft.com/en-us/fabric/governance/governance-compliance-overview)
- [Purview + Fabric – Integration](https://learn.microsoft.com/en-us/fabric/governance/microsoft-purview-fabric)
- [Purview Hub in Fabric](https://learn.microsoft.com/en-us/fabric/governance/use-microsoft-purview-hub)
- [Purview – Data Governance Overview](https://learn.microsoft.com/en-us/purview/data-governance-overview)

### Git-Integration & Deployment Pipelines (ALM)
- [Git-Integration – Überblick](https://learn.microsoft.com/en-us/fabric/cicd/git-integration/intro-to-git-integration)
- [Git-Integration – Get started](https://learn.microsoft.com/en-us/fabric/cicd/git-integration/git-get-started)
- [Deployment Pipelines – Überblick](https://learn.microsoft.com/en-us/fabric/cicd/deployment-pipelines/intro-to-deployment-pipelines)
- [Deployment Pipelines – Prozess & Incremental Refresh](https://learn.microsoft.com/en-us/fabric/cicd/deployment-pipelines/understand-the-deployment-process)

### OneLake & Shortcuts
- [OneLake Shortcuts – Überblick](https://learn.microsoft.com/en-us/fabric/onelake/onelake-shortcuts)
- [OneLake Shortcut erstellen](https://learn.microsoft.com/en-us/fabric/onelake/create-onelake-shortcut)

### Real-Time Intelligence (RTI): Eventhouse, Eventstreams, KQL DB
- [Real-Time Intelligence – Doku-Start](https://learn.microsoft.com/en-us/fabric/real-time-intelligence/)
- [Eventhouse – Überblick](https://learn.microsoft.com/en-us/fabric/real-time-intelligence/eventhouse)
- [Eventstreams – Überblick](https://learn.microsoft.com/en-us/fabric/real-time-intelligence/event-streams/overview)
- [Eventstream erstellen & verwalten](https://learn.microsoft.com/en-us/fabric/real-time-intelligence/event-streams/create-manage-an-eventstream)
- [KQL Database – Erstellen](https://learn.microsoft.com/en-us/fabric/real-time-intelligence/create-database)
- [KQL Database – Verwalten & Monitoren](https://learn.microsoft.com/en-us/fabric/real-time-intelligence/manage-monitor-database)
- [Training: Use real-time eventstreams in Fabric](https://learn.microsoft.com/en-us/training/modules/explore-event-streams-microsoft-fabric/)
- [RTI Tutorial – Teil 1: Eventhouse aufsetzen](https://learn.microsoft.com/en-us/fabric/real-time-intelligence/tutorial-1-resources)

### Data Warehouse & Data Factory (Pipelines)
- [Fabric Data Warehouse – Doku](https://learn.microsoft.com/en-us/fabric/data-warehouse/)
- [Data Factory: Pipeline REST-Fähigkeiten](https://learn.microsoft.com/en-us/fabric/data-factory/pipeline-rest-api-capabilities)
- [KQL Database Connector (Pipelines)](https://learn.microsoft.com/en-us/fabric/data-factory/connector-kql-database-overview)

### Offizielle Blogs & Updates
- [Microsoft Fabric Blog – Updates & Ankündigungen](https://blog.fabric.microsoft.com/)
- [Monatliche Updates / Zusammenfassungen](https://support.fabric.microsoft.com/en-in/blog/category/monthly-update)

### Community / Foren
- [Microsoft Fabric Community (Foren, Q&A, Ressourcen)](https://community.fabric.microsoft.com/)

---

## YouTube – ausgewählte Kanäle, Playlists & Videos

**Offiziell**
- [Microsoft Fabric – offizieller YouTube-Kanal](https://www.youtube.com/@MicrosoftFabric/videos)
- [Microsoft Mechanics (IT-Pros & Architekten)](https://www.youtube.com/channel/UCJ9905MRHxwLZ2jeNQGIWxA/videos)

**Creator / Community**
- [Guy in a Cube – Kanal (Fabric & Power BI)](https://www.youtube.com/guyinacube)
- [Getting Started with Microsoft Fabric – Playlist (GiAC)](https://www.youtube.com/playlist?list=PLv2BtOtLblH1RhbtfTpp9ovi3Y-3HiRO2)
- [All this Microsoft Fabric… what about Power BI? (GiAC)](https://www.youtube.com/watch?v=rqOJSogcIhk)

**Real-Time Intelligence (Eventstreams, KQL, Dashboards)**
- [End-to-End Streaming Analytics in Fabric (ISS Tracker, KQL, PBI)](https://www.youtube.com/watch?v=iWepPEUUO_4)
- [Getting Started with Real-Time Intelligence](https://www.youtube.com/watch?v=XaKEvEUjiwo)
- [Eventstream → KQL – „Create your first Eventstream“](https://www.youtube.com/watch?v=SyRDll6OvX0)
- [Eventstream Transformations → Data Activator & KQL](https://www.youtube.com/watch?v=_Q_0By0wc8M)

**Warehouse & Pipelines**
- [Create your first Data Warehouse in Fabric](https://www.youtube.com/watch?v=StIBBb69wDw)
- [Full Course: Learn Microsoft Fabric Data Pipelines (2025)](https://www.youtube.com/watch?v=1PGE9bWqY2g)
- [Learn the Fundamentals of Microsoft Fabric (≈38 min)](https://www.youtube.com/watch?v=J4i5lcROJcs)
- [Learn Together: Get started with data warehouses in Fabric](https://www.youtube.com/watch?v=m6wJPxlYCrs)

**SemPy / Semantic Link**
- [Semantic Link – 1-Stunden-Workshop](https://www.youtube.com/watch?v=Xj0AnZ8qT58)
- [Advancing Fabric – Power BI meets Spark with Semantic-Link](https://www.youtube.com/watch?v=4AG8_PilrYY)


---

**Happy Fabric-ing!**
