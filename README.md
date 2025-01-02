Imperium Nomad Assistant
========================

Overview
--------

The **Imperium Nomad Assistant** is a travel assistant for digital nomads, inspired by the Dune universe. It leverages **Langflow** and **Astra DB** to demonstrate a **Retrieval-Augmented Generation (RAG)** flow for querying destinations, workspaces, and events. This project was completed as part of a Langflow challenge and fulfills the requirements to earn the associated badge.

This repository includes documentation, screenshots, and a recorded demo of the assistant in action. It was implemented entirely in **Gitpod**, using Astra DB for vector storage and Langflow for flow configuration.

* * * * *

Features
--------

-   **Data Loading**: Creates a collection (`imperium_nomad_brochure`) within a specified keyspace (`imperium_nomad_keyspace`) in Astra DB.
-   **Retrieval-Augmented Generation**: Supports interactive queries with context retention across successive questions.
-   **Custom Keyspace Handling**: Modified underlying code to allow specifying keyspaces other than default keyspace, thus overcoming template limitations.
-   **Interactive UI**: Built with Langflow's visual editor, enabling drag-and-drop component wiring.
-   **Flexible Embedding Models**: Integrated OpenAI embeddings for text processing.

* * * * *

Getting Started
---------------

### Prerequisites

-   Python 3.12+
-   Gitpod account (or local machine setup)
-   Astra DB account
-   OpenAI API key

### Installation

1.  Clone the repository:

    ```
    git clone <repo-url>
    cd <repo-name>

    ```

2.  Install dependencies:

    ```
    pip install uv
    uv pip install langflow --system
    uv run langflow run

    ```

3.  Launch Langflow:

    ```
    uv run langflow run

    ```

4.  Access Langflow in your browser (URL provided in the terminal).

* * * * *

Workflow Setup
--------------

### 1\. Load Data into Astra DB

-   Prepare a combined input data file (brochure) for **destinations**, **workspaces**, and **events**.
-   Use the **File** and **Split Text** components in Langflow to ingest the data.

### 2\. Configure Database Connection

-   Add your **Astra DB Application Token** and **API Endpoint**.
-   Set the **Collection Name** as `imperium_nomad_brochure`.
-   Specify the **Keyspace** as `imperium_nomad_keyspace`.

### 3\. Set Up Embeddings

-   Add an **OpenAI Embedding** component.
-   Enter your **OpenAI API Key**.

### 4\. Create Retrieval-Augmented Generation Flow

-   Connect components for embedding generation, search input, and results retrieval.
-   Test queries in the **Playground**.

* * * * *

Screenshots
-----------

Key steps and configuration screenshots can be found in the `screenshots/` folder.

* * * * *

Demo Video
----------

The full demo recording, showing how the assistant handles sequential queries, is available in the `demo/` folder.

* * * * *

References
----------

-   Langflow Quickstart: [docs.langflow.org/get-started-quickstart](https://docs.langflow.org/get-started-quickstart)
-   Installation Guide: [docs.langflow.org/get-started-installation](https://docs.langflow.org/get-started-installation)
-   Example Walkthrough: [YouTube Video](https://www.youtube.com/watch?v=BYiq_2rOXO8)

* * * * *

Lessons Learned
---------------

-   **Hands-On Exploration**: Langflow's visual editor simplifies complex AI workflows.
-   **Flexibility**: Customizing keyspaces and adapting flows showcases the adaptability of Langflow.
-   **Ease of Use**: Combining components in Langflow accelerates prototyping, making AI development intuitive and engaging.

* * * * *

Future Improvements
-------------------

-   Expand datasets with richer context and metadata.
-   Enhance query patterns to handle more complex workflows.
-   Integrate additional embedding models and APIs.

* * * * *

Badge
-----

The criteria for the Langflow Challenge found here:
https://badgr.com/public/badges/xceu7dd7RJSEdiGV_5oe2Q

* * * * *