# CronJob

## metadata

The metdata field is constructed in the same way as it is with `kubernetes`.
Under normal usage minimaly need a `name` and a `namespace` (enviroment).
If no `namespace` is set we default to `default`.

## Scheduler

A job is defined by a list of parameters that define the job behaviour.

| Keyword  | Required | Description                                               |
|----------|----------|-----------------------------------------------------------|
| provider | yes      | The Provider specifies a docker image with all components |

### Predefined schedules

> https://godoc.org/github.com/robfig/cron

You may use one of several pre-defined schedules in place of a cron expression.

Entry                  | Description                                | Equivalent To
-----                  | -----------                                | -------------
@yearly (or @annually) | Run once a year, midnight, Jan. 1st        | 0 0 0 1 1 *
@monthly               | Run once a month, midnight, first of month | 0 0 0 1 * *
@weekly                | Run once a week, midnight between Sat/Sun  | 0 0 0 * * 0
@daily (or @midnight)  | Run once a day, midnight                   | 0 0 0 * * *
@hourly                | Run once an hour, beginning of hour        | 0 0 * * * *

### Complex schedules