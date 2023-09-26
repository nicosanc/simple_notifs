# Introduction

This library was built for making simple, shortened human readable versions of time deltas. 
This was specifically made for notifications on applications where a user wants to see how long it has been
since the notification was made. For example, instead of a time delta such as "1 hour ago" or "20 minutes ago", the resulting time delta would be
"1h" and "20mi", respectively.
The method will convert your datetime object to an Arrow object, then convert that arrow object to UTC. Thus, there is no need to worry about any type conversions
when using the method. We handle that for you.

## Access
From simple_notifs.simple_notifs import utc_to_human

## Arguments

- Mandatory, a datetime object must be passed as input to the function. 
- By default, days_and_above is set to False. If True, the built in method will only display time deltas starting at "1d". This means any deltas
in seconds, minutes, or hours that are less than a full day, will be truncated to "1d".
