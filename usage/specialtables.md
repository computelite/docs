(specialtables)=

# Special Tables

## Log Tables

### Task Logs

**Navigation**: **HomePage** > **Log Tables** > **Task Logs**

This table displays the status of all code executions, indicating whether they were successfully executed or resulted in an error.

**Columns Description**

**TaskName** - Name of the file added to the homepage for direct execution.
**TaskStatus** - Indicates whether the code execution was successful or encountered an error.
**StartDate** - The timestamp when the code execution started.
**EndDate** - The timestamp when the code execution ended.
**ErrorMsg** - Displays the error message, if any, for failed executions.   

### Solver Logs

**Navigation**: **HomePage** > **Log Tables** > **Solver Logs**

User can view logs for solver if any in this table.


## Setups

### Table Group 

**Navigation**: **HomePage** > **Setups** > **Table Group**

This table allows users to define table names and group them into categories for display on the homepage.

**Columns Description** 

**GroupName** - Defines the group name (e.g., Log Tables, Setups, etc.).
**TableName** - Specifies the table name to be added to the group.
**TableDisplayName** -  Allows displaying a table with a custom name on the homepage (e.g., displaying S_TableGroup as "Table Group").
**TableType** - Specifies whether the table is editable (set to "Input") or read-only (defaulted as an output table).
**ColumnOrder** - Defines the display order of columns on the table display page; users can update this from the table itself.
**Table_Status** - Hides the table from the homepage by setting the status to "Inactive."
**Freeze_col_Num** - Specifies the number of columns to freeze on the table display page.
 

### Table Parameters 

**Navigation**: **HomePage** > **Setups** > **Table Parameters**

This table contains configuration settings for tables, such as applying decimal places, thousand separators, or sorting preferences.

**Columns Description** 

**TableName** - The table name for which settings are being defined.
**ColumnName** - The column name to which the settings apply.
**ParameterType** - Specifies the type of parameter to apply (e.g., List of Values (LOV), Decimals, Sort, etc.).
**ParameterValue** - The value of the parameter to apply (e.g., "Date" for date formatting, "asc/desc" for sorting, etc.).

### Task Master

**Navigation**: **HomePage** > **Setups** > **Task Master**

This table lists all files added to the homepage for direct execution via the Python Editor.

**Columns Description**

**TaskName** - The name of the execution file
**TaskDisplayName** - The name displayed on the homepage under the "Run" dropdown; users can update this as needed.
**TaskLastRunDate** - The last execution date of the task.

### Code Files

**Navigation**: **HomePage** > **Setups** > **Code Files**

This table lists all files available in the Python Editor.

**Columns Description** 

**FileName** - The name of the file as displayed in the Python Editor.
**FilePath** - The directory path of the file, showing its folder structure.
**FileData** - Contains the full content of the file.

## All Other

### Temp View

**Navigation**: **HomePage** > **All Other** > **Temp View**

This table displays the results of any SQLite fetch queries (e.g., SELECT * FROM D_Items) executed in the SQL Editor.

### Data Files

**Navigation**: **HomePage** > **All Other** > **Data Files**

This table lists all files uploaded via **Upload Files** under the **Files** dropdown on the homepage.


### PackageWheels

**Navigation**: **HomePage** > **All Other** > **PackageWheels**

This table displays all Python wheel files uploaded via **HomePage > Upload Package**.
