# View host history

When you've found specific host (following [Search host from name](search_host_from_name.md)), you could access to his alert history.  
To do that, you must clic on host name in list (as example RGM_HOST) and you'll access to new page such as :

![host_detail](../screenshots/host_details.png)

In top left of page, you'll find an area __Host Information__ :

![host_detail_information_area](../screenshots/host_details_information_area.png)

In this area, you'll find a link __View Alert History For This Host__ :

![host_detail_alert_history](../screenshots/host_detail_alert_history.png)

If you click on this link you'll arrive on page with host alerts history list :

![host_alert_history_list](../screenshots/host_alert_history_list.png)

## Navigate in host history

Now you've acceded to host alert history, you could navigate into full knowed history of this host.  
__For performances concerns, we recommand to not exceed one month on alert displaying.__

To navigate accross time, you have two options :

- Click on _"Previous Day"_ to backward to previous day history
- Select time range by clicking on _calendar_ icons and select dates and hours

## Alert history detail

For each line of alerts, you could find all needed informations.  
If we take example of this line :

```text
[2020-01-27 15:21:23] SERVICE ALERT: <hostname>;interfaces;WARNING;HARD;4;(null)
```

We could detail with :

- `2020-01-27 15:21:23` : Correspond to event time
- `SERVICE ALERT` : Correspond to event type. Here is an alert on host service
- `<hostname>` : Is the name of host configured in monitoring platform
- `interfaces` : Is the name of service which as generated alert. Here the service name is simply _interfaces_
- `WARNING` : Correspond to the status of service or host status for the alert.
- `HARD` : Type of alert. You could find two states for an alert, _SOFT_ and _HARD_. The difference is than only HARD state trigger the notification process. It could be assimiled to a confirmation state
- `4` : Is the number of checks effectued in this state
- `(null)` : Correspond to check output. In this case, the check as returned no output and the monitoring platform insert a null value as output.
