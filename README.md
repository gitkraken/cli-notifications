# CLI Notifications

## Schema

```typescript
{
    notifications: [{
        id: string,
        title: string,
        trigger: []TriggerOpts
        description?: string,
        timestamp?: UnixTimestamp, // Eg. 1696989209
    }],
    version: int
}
```

The `trigger` attribute will accept any of these:
- `always`: Always display this notification
- `once`: Display this notification once (requires timestamp)
- `trial`: Display for trial users only