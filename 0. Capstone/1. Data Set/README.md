<h1 align="left">Capstone Project</h1>
<h2 align="left">Data Set</h2>

- The <b>Data Set</b> was sourced from <img src="https://www.vectorlogo.zone/logos/kaggle/kaggle-icon.svg" alt="Kaggle" width="16" height="16"/> <b>Kaggle</b>. The live data set can be sourced <a href="https://www.kaggle.com/datasets/nnthanh101/aws-saas-sales">here 🡵</a>.<br>
Please note, the data set may be updated over time, so be sure to access the specific version utilised for this Project using the applicable sources below.
- The <b>RAW</b>, <b>unedited</b> <img src="https://cdn.worldvectorlogo.com/logos/google-sheets-logo-icon.svg" alt="Google Sheets" width="16" height="16"/> Google's <b>Sheets</b> file can be accessed <a href="https://docs.google.com/spreadsheets/d/1_9q8J4xBGtjmUJIOE2TanIc4ZVWjS2i4jfwfD2dRk_E/"> here 🡵</a>, or alternatively accessed within this repository, <a href="https://github.com/njvrensburg/Turing-College/blob/main/0.%20Capstone/1.%20Data%20Set/3.%20AWS%20Sales%20-%20SaaS-Sales%20%5Braw%5D.csv">here 🡥</a>.
- The dataset was assessed and the necessary <b>Cleaning</b> and <b>Transformation</b> actions were taken. An annotated <img src="https://cdn.worldvectorlogo.com/logos/google-sheets-logo-icon.svg" alt="Google Sheets" width="16" height="16"/> Google's <b>Sheets</b> file illustrating these steps can be accessed <a href="https://docs.google.com/spreadsheets/d/1Sqz9zZosJTisRn-SGSmIo3v_DOIqhEqL8tiAcHn0pWU/edit?gid=1513097115/"> here 🡵</a>, and within this repository, <a href="https://github.com/njvrensburg/Turing-College/blob/main/0.%20Capstone/1.%20Data%20Set/2.%20AWS%20SaaS%20-%20SaaS-Sales%20%5Bcleaning%5D.xlsx">here 🡥</a>.
- The <b>CLEAN</b> <img src="https://cdn.worldvectorlogo.com/logos/google-sheets-logo-icon.svg" alt="Google Sheets" width="16" height="16"/> Google's <b>Sheets</b> file can be accessed <a href="https://docs.google.com/spreadsheets/d/1_ulTM3ghsKK_dYNrKhC2C9eIadxpVzl3n-mfnF7liB0/"> here 🡵</a> and in the repository, <a href="https://github.com/njvrensburg/Turing-College/blob/main/0.%20Capstone/1.%20Data%20Set/0.%20AWS%20Sales%20-%20SaaS-Sales%20%5Bclean%5D.csv">here 🡥</a>.
<br>This data was then used as the primary source and uploaded to <img src="https://cdn.worldvectorlogo.com/logos/google-bigquery-logo-1.svg" alt="Google Bigquery" width="18" height="18"/> Google's <b>Bigquery</b>.
<h3 align="left">Cleaning</h2>

- All data in the <b>RAW</b> data set was listed in <b>Text</b> format thus relevant <b>Numerical</b>, <b>Date</b> and <b>Text</b> formatting applied for appropriate recognition in the <b>SQL</b> environment of <img src="https://cdn.worldvectorlogo.com/logos/google-bigquery-logo-1.svg" alt="Google Bigquery" width="18" height="18"/> Google's <b>Bigquery</b>.
- The <b>RAW</b> data set contains <b>2 Date</b> columns: '<i>Order Date</i>' and '<i>Date Key</i>'.
  - for illustration purposes, it is exemplified how we can apply <img src="https://cdn.worldvectorlogo.com/logos/google-sheets-logo-icon.svg" alt="Google Sheets" width="16" height="16"/> Spreadsheet <b>formula techniques</b> to produce a relevant '<i>Date</i>' column derived from <b>each</b>, to later be used in <b>SQL</b>.
<h3 align="left">Transformations</h2>

- Assessing the data, minor field name changes were applied for readability (removal of spaces) and applicability.
  - '<i>Row ID</i>' → '<i>ID_key</i>'.
  - <b>note!</b>, the field name '<i>Segment</i>' was later renamed to '<i>CustomerTier</i>' within the SQL code as seen here 🡥.
- It was also deemed necessary to organise the relevant data fields.
  - The unique values within the applicable columns were extracted and organised alphabetically.
  - Relevant, unique and sequential numerical <b>ID</b>s were assigned to the organised values.
- The unique data within the following fields were extracted, and the values assigned <b>ID</b>s in separate tables to be uploaded to <img src="https://cdn.worldvectorlogo.com/logos/google-bigquery-logo-1.svg" alt="Google Bigquery" width="18" height="18"/> Google's <b>Bigquery</b>, in the below order:
  - Location fields <a href="https://docs.google.com/spreadsheets/d/1UaDQwfg59lEl-MB6BQczs2dXQHvRwoDFQQPteBwvoxk/"><img src="https://cdn.worldvectorlogo.com/logos/google-sheets-logo-icon.svg" alt="Google Sheets" width="16" height="16"/>🡵</a>:
    - '<i>Region</i>' <a href="https://github.com/njvrensburg/Turing-College/blob/main/0.%20Capstone/1.%20Data%20Set/1.1.1.%20AWS%20SaaS%20-%20custom_Region.csv">🡥</a>
    - '<i>Subregion</i>' <a href="https://github.com/njvrensburg/Turing-College/blob/main/0.%20Capstone/1.%20Data%20Set/1.1.2.%20AWS%20SaaS%20-%20custom_Subregion.csv">🡥</a>
    - '<i>Country</i>' <a href="https://github.com/njvrensburg/Turing-College/blob/main/0.%20Capstone/1.%20Data%20Set/1.1.3.%20AWS%20SaaS%20-%20custom_CountryCoordinates.csv">🡥</a>
    - '<i>City</i>' <a href="https://github.com/njvrensburg/Turing-College/blob/main/0.%20Capstone/1.%20Data%20Set/1.1.4.%20AWS%20SaaS%20-%20custom_CityCoordinates.csv">🡥</a>
  - Other fields <a href="https://docs.google.com/spreadsheets/d/1IGgGCb_orJ6MY1epOr1jpqTmo39HpNWmz1QeaqvOtBI/"><img src="https://cdn.worldvectorlogo.com/logos/google-sheets-logo-icon.svg" alt="Google Sheets" width="16" height="16"/>🡵</a>:
    - '<i>Segment</i>' (later aliased to <i>CustomerTier</i>) <a href="https://github.com/njvrensburg/Turing-College/blob/main/0.%20Capstone/1.%20Data%20Set/1.2.1.%20AWS%20SaaS%20-%20custom_Segment.csv">🡥</a> 
    - '<i>Industry</i>' <a href="https://github.com/njvrensburg/Turing-College/blob/main/0.%20Capstone/1.%20Data%20Set/1.2.2.%20AWS%20SaaS%20-%20custom_Industry.csv">🡥</a>
    - '<i>Product</i>' <a href="https://github.com/njvrensburg/Turing-College/blob/main/0.%20Capstone/1.%20Data%20Set/1.2.3.%20AWS%20SaaS%20-%20custom_Product.csv">🡥</a>
                                                                                                                                                                       
<h4 align="left">Location Coordinates</h4>

- For the purposes of accurate map visualisations later within the <a href="https://lookerstudio.google.com/reporting/b4b877b4-6944-4def-9352-a088029cb075/page/p_46lp7a9dbd"><b>Dashboard</b></a>, it was required to add <b>Location Coordinates</b>.
- This was done by utilising a free <b>extension</b> available in the <img src="https://cdn.worldvectorlogo.com/logos/google-sheets-logo-icon.svg" alt="Google Sheets" width="16" height="16"/> Google's <b>Sheets</b> Marketplace called <a href="https://workspace.google.com/u/0/marketplace/app/geocode_by_awesome_table/"> <img src="https://lh3.googleusercontent.com/qKpvj2OMxqy604I4Nx-iGyM_XrvT1s_yhAmGW6GCulg8tew-gc9SVhemivdUxrktvVQRJHT7CNk" alt="Geocode by Awesome Table logo" width="16" height="16"> <b>Geocode by Awesome Table</b></a>.
  - the extension allowed for the addition of <b>Latitude</b> and <b>Longitude</b> coordinates for the '<i>Country</i>' and '<i>City</i>' fields.
  - the '<i>Region</i>' and '<i>Subregion</i>' are not recognised inputs by the extension and thus were late aggregated using alternative means to display accurate location visualisations.
