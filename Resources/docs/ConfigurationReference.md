# Configuration Reference

```yaml
gos_web_socket:
    client:
        session_handler: ~ # Example: @session.handler.pdo
        firewall: ws_firewall # Example: secured_area, you must replace it by your firewall
        storage:
            driver: @gos_web_socket.server.in_memory.client_storage.driver
            decorator: ~
    shared_config: true
    server:
        port: ~ # Required, Example 1337
        host: ~ # Required, Example 127.0.0.1
        origin_check:         false
        router:
            resources:
                - @AcmeBundle/Resources/config/pubsub/routing.yml
            context:
                tokenSeparator: "/"
    rpc:                  []
    topics:               []
    periodic:             []
    servers:              []
    origins:              []
```
