# Ramp_assignment


WITH DailyTotals AS (
    SELECT transaction_time AS transaction_date,
        SUM(transaction_amount) AS total_amount
    FROM
        transactions
    GROUP BY
        DATE(transaction_time)
)

SELECt avg(total_amount)
from DailyTotals
