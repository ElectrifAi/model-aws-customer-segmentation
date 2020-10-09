# Input/Output Description

- Input: Data at customer level
    - Format: Input data is assumed to be in csv format and comma separated.
    - Identifiers: Customer's accountID should be the identifier or one of the identifiers. 
    - High Importance Columns:
    
    - account_income  Account Income
    - active_1m   Was the customer active in the previous month?
    - age Average  Age of Customers on the Account
    - avg_account_tenure  Average tenure of members on the account in months
    - balance_current sum of current balance across customer_id associated with given account_id at scoring date
    - purchase_amt_1_month    Account Revenue in the past 1 month
    - purchase_amt_service1   service 1 charge in last month
    - purchase_amt_service2   service 2 charge in last month
    - purchase_amt_service3   service 3 charge in last month

    - Medium Importance Columns:

    - account_size    Number of customer_ids on the account_id
    - avg_payment_3m  average payment amount within 3  month2 to scoring date
    - avg_purchased_services  average number of services purchased across members in an account
    - avg_service_tenure  average tenure of services that the account used
    - avg_tenure_service_1    average tenure of service 1 across members of an account
    - avg_tenure_service_2    average tenure of service 2 across members of an account
    - avg_tenure_service_3    average tenure of service 3 across members of an account
    - balance_1m  balance on last  bill
    - days_last_subscription  days since last change in subscription 
    - deactivate_1y   Did this account deactivate in the last year?
    - late_pay_3m_ind indicate of late pay in recent 3 months
    - LATITUDE    LATITUDE
    - LONGITUDE   LONGITUDE
    - num_autopay number of auto payments in recent 3 months
    - num_current_services    number of services that the account is using
    - num_latepay number of late payments in recent 3 months
    - num_months_remaining    Number of months until account subscription ends
    - num_new_members_1m  Number of new members added to account in last 1 month
    - num_new_members_2m  Number of new members added to account in last 2 months
    - num_new_members_3m  Number of new members added to account in last 3 months
    - num_payment number of payments in recent 3 months
    - num_purchased_services  number of services purchased in an account
    - num_subscriptions_closed    Number of times subscription ended in account
    - num_unique_services number of unique services purchased in an account
    - purchase_amt_2_months   Account Revenue in the past 2 months
    - purchase_amt_3_months   Account  Revenue in the past 3 months
    - service1_usage_1m   count of usage of service 1 with 1 month of scoring date across an account
    - service1_usage_2m   usage of service 1 with 2 month of scoring date
    - service1_usage_3m   usage of service 1 with 3 month of scoring date
    - service2_usage_1m   similar to service 1
    - service2_usage_2m   similar to service 1
    - service2_usage_3m   similar to service 1
    - service3_usage_1m   similar to service 1
    - service3_usage_2m   similar to service 1
    - service3_usage_3m   similar to service 1
t   - otal_mrc_amt   total monthly recurring charges (mrc) in the account

    - Low Importance Columns:
               
    - purchase_amt_1_year Account Revenue in the past 1 years
    - purchase_amt_2_years    Account Revenue in the past 2 years
    - purchase_amt_3_years    Account Revenue in the past 3 years
    - purchase_amt_6_months   Account Revenue in the past 6 months
    - rate_plan_is_group  Indicator whether rate plan is a group plan

    - Derived Columns

    - auto_pay_ratio  num_auto_pay/num_payment
    - late_pay_ratio  num_late_pay/num_payment
    - purchase_percent_service1   purchase_amt_service1/purchase_amt_1_month
    - purchase_percent_service2   purchase_amt_service2/purchase_amt_1_month
    - purchase_percent_service3   purchase_amt_service3/purchase_amt_1_month

- Output: a comma separated csv file with original order, and one more column added named 'cluster' which contains model's prediction of the cluster/segment for the record.

