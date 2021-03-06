# Changelog

## v0.6.0
* `Pigeon.APNS.Notification.new/3` returns `%Pigeon.APNS.Notification{}` struct
* Configure APNS to use SSL port 2197 with `apns_2197: true` in your `config.exs`
* Error feedback symbols converted from `CamelCase` to `snake_case`
* APNS expiration values supported with `expiration` key in `%Pigeon.APNS.Notification{}`

## v0.5.2
* Fixed bug where APNSWorker would hang up if SSL connection failed. Now retries the connection twice more before gracefully shutting down. 

## v0.5.1
* GCM error responses return proper chunk of regstration IDs

## v0.5.0
* `Pigeon.GCM.Notification.new/2` returns `%Pigeon.GCM.Notification{}` struct
* Multiple registration IDs allowed in `Pigeon.GCM.push/2`
* Remove `:gcm_worker`
