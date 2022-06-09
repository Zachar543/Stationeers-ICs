# Protocol

### Message Data Format
Format:`-CCCCCCCCBBAA`

`A` = Target (2-digits),
`B` = Command (2-digits),
`C` = Data

### Rules
* Requesting device is responsible for clearing `memReq` & `memResp`
* All devices wait for `memReq` = 0 (on request) or `memResp` = 0 (on response) before updating
* Target `00` means all devices that implement the command should respond
* Responses should echo the request's `Target` and `Command`

### Commands
| Command | Description           |
|---------|-----------------------|
| 1       | Request an item       |
| 2       | Request available qty |
| 99      | Request an Id         |
