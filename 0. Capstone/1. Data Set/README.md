<h1 align="left">Capstone Project</h1>
<h2 align="left">Data Set</h2>

- The <b>Data Set</b> was sourced from <img src="https://www.vectorlogo.zone/logos/kaggle/kaggle-icon.svg" alt="Kaggle" width="16" height="16"/> <b>Kaggle</b>. The live data set can be sourced <a href="https://www.kaggle.com/datasets/nnthanh101/aws-saas-sales">here 🡵</a>.<br>
Please note, the data set may be updated over time, so be sure to access the specific version utilised for this Project using the applicable sources below.
- The <b>RAW</b>, <b>unedited</b> <img src="https://cdn.worldvectorlogo.com/logos/google-sheets-logo-icon.svg" alt="Google Sheets" width="16" height="16"/> Google's <b>Sheets</b> file can be accessed <a href="https://docs.google.com/spreadsheets/d/1_9q8J4xBGtjmUJIOE2TanIc4ZVWjS2i4jfwfD2dRk_E/"> here 🡵</a>, or alternatively accessed within this repository, here 🡵.
- The dataset was assessed and the necessary <b>Cleaning</b> and <b>Transformation</b> actions were taken. An annotated <img src="https://cdn.worldvectorlogo.com/logos/google-sheets-logo-icon.svg" alt="Google Sheets" width="16" height="16"/> Google's <b>Sheets</b> file illustrating these steps can be accessed <a href="https://docs.google.com/spreadsheets/d/1Sqz9zZosJTisRn-SGSmIo3v_DOIqhEqL8tiAcHn0pWU/edit?gid=1513097115/"> here 🡵</a>, and within this repository, here 🡵.
- The <b>CLEAN</b> <img src="https://cdn.worldvectorlogo.com/logos/google-sheets-logo-icon.svg" alt="Google Sheets" width="16" height="16"/> Google's <b>Sheets</b> file can be accessed <a href="https://docs.google.com/spreadsheets/d/1_ulTM3ghsKK_dYNrKhC2C9eIadxpVzl3n-mfnF7liB0/"> here 🡵</a> and in the repository, here 🡵.
<br>This data was then used as the primary source and uploaded to <img src="https://cdn.worldvectorlogo.com/logos/google-bigquery-logo-1.svg" alt="Google Bigquery" width="18" height="18"/> Google's <b>Bigquery</b>.
<h3 align="left">Cleaning</h2>

- All data in the <b>RAW</b> data set was listed in <b>Text</b> format thus relevant <b>Numerical</b>, <b>Date</b> and <b>Text</b> formatting applied for appropriate recognition in the <b>SQL</b> environment of <img src="https://cdn.worldvectorlogo.com/logos/google-bigquery-logo-1.svg" alt="Google Bigquery" width="18" height="18"/> Google's <b>Bigquery</b>.
- The <b>RAW</b> data set contains <b>2 Date</b> columns: '<i>Order Date</i>' and '<i>Date Key</i>'
  - for illustration purposes, it is exemplified how we can apply <img src="https://cdn.worldvectorlogo.com/logos/google-sheets-logo-icon.svg" alt="Google Sheets" width="16" height="16"/> Spreadsheet <b>formula techniques</b> to produce a relevant '<i>Date</i>' column derived from <b>each</b>, to later be used in <b>SQL</b>.
<h3 align="left">Transformations</h2>

- Assessing the data, minor field name changes were applied for readability (removal of spaces) and applicability.
  - '<i>Row ID</i>' → '<i>ID_key</i>'
  - <b>note!</b>, the field name '<i>Segment</i>' was later renamed to '<i>CustomerTier</i>' within the SQL code as seen here 🡵
- It was also deemed necessary to organise the relevant data fields.
  - The unique values within the applicable columns were extracted and organised alphabetically.
  - Relevant, unique and sequential numerical <b>ID</b>s were assigned to the organised values.
- The data within the following fields were assigned <b>ID</b>s and the unique values with <b>ID</b>s were extracted to separate tables to be uploaded to <img src="https://cdn.worldvectorlogo.com/logos/google-bigquery-logo-1.svg" alt="Google Bigquery" width="18" height="18"/> Google's <b>Bigquery</b>, in the below order:
  - Location fields:
    - '<i>Region</i>' (later aliased to <i>CustomerTier</i>) 🡵
    - '<i>Subregion</i>' 🡵
    - '<i>Country</i>' 🡵
    - '<i>City</i>' 🡵
  - Other fields:
    - '<i>Segment</i>' 🡵 
    - '<i>Industry</i>' 🡵
    - '<i>Product</i>' 🡵
