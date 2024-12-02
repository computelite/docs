(specialtables)=

# Special Tables  

Special Tables provide a structured way to manage logs, configurations, and uploaded files, ensuring seamless operation and enhanced visibility in the system.  

---

## Log Tables  

### Task Logs  

**Navigation**: `HomePage > Log Tables > Task Logs`

The **Task Logs** table (T_TaskLogs) displays the execution status of all tasks, helping users identify successful and failed operations.  

#### **Columns Description**  

- **TaskName**: Name of the file executed.  
- **TaskStatus**: Indicates whether the code execution was successful or encountered an error.  
- **StartDate**: The timestamp when the code execution started.  
- **EndDate**: The timestamp when the code execution ended.  
- **ErrorMsg**: Displays the error message for failed executions (if any).  

---

### Solver Logs  

**Navigation**: `HomePage > Log Tables > Solver Logs`  

The **Solver Logs** table (T_SolverLog) allows users to review logs specific to task-related operations.  

---

## Setups  

### Table Group  

**Navigation**: `HomePage > Setups > Table Group`  

The **Table Group** table (S_TableGroup) helps users categorize and define table names for display on the homepage.  

#### **Columns Description**  

- **GroupName**: Defines the group name (e.g., Log Tables, Setups, etc.).  
- **TableName**: Specifies the table name to be added to the group.  
- **TableDisplayName**: Customizes the table's display name on the homepage (e.g., displaying `S_TableGroup` as "Table Group").  
- **TableType**: Indicates whether the table is editable (`Input`) or read-only (default as `Output`).  
- **ColumnOrder**: Sets the display order of columns on the table display page, which users can update from the table itself.  
- **Table_Status**: Hides the table from the homepage by setting its status to `Inactive`.  
- **Freeze_col_Num**: Specifies the number of columns to freeze on the table display page.  

---

### Table Parameters  

**Navigation**: `HomePage > Setups > Table Parameters`  

The **Table Parameters** table (S_TableParameters) allows users to configure table settings such as decimal places, thousand separators, or sorting preferences.  

#### **Columns Description**  

- **TableName**: The table name for which settings are being defined.  
- **ColumnName**: The column to which the settings apply.  
- **ParameterType**: Specifies the type of parameter (e.g., List of Values (LOV), Decimals, Sort, etc.).  
- **ParameterValue**: Defines the value of the parameter (e.g., `Date` for date formatting, `asc/desc` for sorting).  

---

### Task Master  

**Navigation**: `HomePage > Setups > Task Master`  

The **Task Master** table (S_TaskMaster) lists all executable files available for direct execution from the HomePage.  

#### **Columns Description**  

- **TaskName**: The name of the execution file.  
- **TaskDisplayName**: The display name shown under the "Run" dropdown on the homepage (editable).  
- **TaskLastRunDate**: The most recent execution date of the task.  

---

### Code Files  

**Navigation**: `HomePage > Setups > Code Files`  

The **Code Files** table (S_ExecutionFiles) lists all files accessible in the Python Editor.  

#### **Columns Description**  

- **FileName**: The name of the file as displayed in the Python Editor.  
- **FilePath**: The directory path of the file, showing its folder structure.  
- **FileData**: The full content of the file.  

---

## All Other  

### Temp View  

**Navigation**: `HomePage > All Other > Temp View`  

The **Temp View** view (V_TEMPV) displays the results of SQLite fetch queries (e.g., `SELECT * FROM D_Items`) executed in the SQL Editor.  

---

### Data Files  

**Navigation**: `HomePage > All Other > Data Files`  

The **Data Files** table (S_DataFiles) lists all files uploaded via **Upload Files** under the **Files** dropdown on the homepage.  

---

### Package Wheels  

**Navigation**: `HomePage > All Other > Package Wheels`  

The **Package Wheels** table (S_PackageWheels) displays all Python wheel files uploaded via `HomePage > Upload Package`.  

---  