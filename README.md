# F1-SQL-Query-Tool

F1 SQl Quer Tool is an AI tool designed to provide F1 race statistics through natural language queries. Utilizing Langchain and a Language Model (LLM), it converts natural language inputs into SQL queries to fetch relevant data from an SQLite database.

## Key Features

- **Natural Language Interface:** Users can ask questions in plain English, such as "Which driver has won the most races?"
- **Query Generation:** The LLM generates SQL queries from natural language inputs, ensuring accuracy in responses.
- **Data Source:** The project relies on a SQLite table structured as follows:

  | Track    | Position | No | Driver         | Team                         | Starting Grid | Laps | Time/Retired | Points | Set Fastest Lap | Fastest Lap Time |
  |----------|----------|----|----------------|------------------------------|---------------|------|--------------|--------|-----------------|------------------|
  | Bahrain  | 1        | 1  | Max Verstappen | Red Bull Racing Honda RBPT   | 1             | 57   | 1:33:56.736  | 25     | No              | 1:36.236         |

## Example Usage

- **Natural Language Query:** "What is the fastest lap time by Sergio Perez?"
- **Generated SQL Query:** `SELECT FastestLapTime FROM F1Data WHERE Driver LIKE '%Sergio Perez%';`
- **Response:** 1:08.111


## Scope for Improvements

- **Larger Dataset Utilization:** Enhance the tool's capabilities by incorporating larger and more diverse datasets. This could include historical race data, driver performance over multiple seasons, and detailed qualifying statistics. A more extensive dataset could provide deeper insights and support more complex queries.
- **Integration of Real-Time Data:** Explore ways to integrate real-time data updates during live F1 events, allowing the tool to provide up-to-date statistics and insights.
