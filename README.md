# SQL-Data-Exploration-Parch-and-Posey-DB

The Parch and Posey is the sales data of different types papers (standard, gloss, poster) of a hypothetical paper company containing 5 tables with information about the company's sales channels, advertisements, accounts, primary point of contact(POC), orders, representatives, and regions. The dataset includes a table for channels and advertisements, two tables for accounts and primary POC, a third table for orders organized by quantity and total, a fourth table for representatives, and a fifth table for regions. The dataset provides valuable insights into the sales performance of Parch and Posey accross different channels, regions and representatives.

The clients of Parch and Posey are large firms using their advertisement skills for Google/Facebook and twitter ads. The company wants to analyse their progress, they want to know which accounts made the hiest purchases in terms of value and volume. What kind of paper was ordered from which client.

We will try analysing some of the aspects of this database related to the sales and how can what would affect growth and how can the same be implemented by Parch and Posey.

## Data Dictionary:
<ol><li><b>Accounts</b> (contains the details of the accounts of all the large firms handled by Parch and Posey) - </li>
    <ul><li>id - unique identifier of all accounts.</li>
        <li>name - Name of all the accounts.</li>
        <li>website - web link for all the accounts managed by the company.</li>
        <li>lat - latitude detail of the client/account.</li>
        <li>long - longitude detail of the client/account.</li>
        <li>primary_poc - primary point of contact from the accounts/firms.</li>
        <li>sales_rep_id - representative from the team handling the operations of the account.</li></ul>
    <li><b>orders</b> (details for order placed by the firms for different types of papers -Standard, Glossy or Poster) - </li>
    <ul><li>id - unique identifier of the recorded order.</li>
        <li>account_id - account id of the firms.</li>
        <li>standard_qty - total quantity of standard paper ordered on that particular date.</li>
        <li>gloss_qty - total quantity of gloss papers ordered on that particular date.</li>
        <li>poster_qty - total quantity of posters ordered on that particular date.</li>
        <li>total - total quantity of orders placed for all 3 papers on that particular date.</li>
        <li>standard_amt_usd - total amount of standard paper ordered by an account for the qty order placed.</li>
        <li>gloss_amt_usd - total amount of gloss paper ordered by an account for the qty order placed.</li>
        <li>poster_amt_usd - total amount of posters ordered by an account for the qty order placed.</li>
        <li>total_amount_usd - total amount for the quantity orderd for all three papers by an account for that date.</li>
        <li>occured_at_date - date of placing the order by the account.</li>
        <li>occured at time - time when the order was placed by the account.</li></ul>
    <li><b>region</b> (the region the sales rep belongs to.)</li>
    <ul><li>id - unique identifier for the region.</li>
        <li>name - the region from where the the sales rep operates from.</li></ul>
    <li><b>sales_rep</b> (details of the 50 unique sales representatives)</li>
    <ul><li>id - unique identifier for the sales rep.</li>
        <li>name - name of the sales representative.</li>
        <li>region_id - region where the sales rep operates from.</li></ul>
    <li><b>web_events</b> (advertisement details the accounts responded to)</li>
    <ul><li>id - unique identifier for the record.</li>
        <li>account_id - unique identifier of the account that responded to a particular advertisement.</li>
        <li>channel - the channel on which the account responded to when the advertisement was posted.</li>
        <li>occured_at_date - date of occurance of the account responding to the advertisement.</li>
        <li>occured_at_time - time of occurance of the account responding to the advertisement.</li></ul></ol>

<i><b>Note:</b> The occured_at has been bifurcated into date and time to improve the analysis further.</i>

<i>In the SQL files, most of the functions have been used i.e. from basic to advanced, given different scenarios of the analysis.</i>

## Approach:
<ol><li>import the excel/csv files into MySQL workbench.</li>
    <li>Clean the datasets.</li>
    <li>Bifurcate the date (occured_at) to represent the date and time separately to leverage both informations. Change the formate to date or time or datetime in a single column.</li></ol>
    
import all csv files and update the name for the ID column

get the data from [data](https://github.com/akshayreddykotha/sql-data-exploration-project/tree/master/data)


