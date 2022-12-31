[//]: # (### Terms)

[//]: # (* ``nID`` - Neighbor's ID)

[//]: # (* ``sID`` - Self's ID)

[//]: # (* ``nVal`` - Neighbor's Value)

[//]: # (* ``sVal`` - Self's Value)

[//]: # ()
[//]: # (### Idle)

[//]: # (1. Once per tick, the device will read each of its neighbors)

[//]: # (2. If `nVal == sID`, set `sVal` to `nID`)

[//]: # (3. Change state to Data Exchange with `nID`)

[//]: # ()
[//]: # ()
[//]: # (### Commands)

[//]: # (| ID  | Desc | One Way | Value 1 | Value 2 |)

[//]: # (|-----|------|---------|---------|---------|)

[//]: # (|     |      |         |         |         |)

[//]: # (|     |      |         |         |         |)

[//]: # (|     |      |         |         |         |)


### Rules
1. Receivers will control communication with senders
   * When idle, devices will check neighbors for requests
   * Senders will wait until the receiver acknowledges the request before interacting
2. All devices will discover and remember the ID and port of each of their neighbors
3. Routers will maintain a routing table of known devices
   * This table will contain a list of device IDs that each neighboring device can reach
   * Routers will advertise newly introduced devices to their neighbors
   * Routers will advertise disconnected devices to their neighbors
