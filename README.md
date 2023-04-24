# DAML Fundementals Capstone

This shows a generic interface for doing application RPCs over a canton ledger. This is just an example to show moving data around via the canton ledger.

It includes

- RejectRPC - reject the RPC sent by user
- UpdateRPC - update the RPC sent by user
- PushRPC - Push a RPC to be reviewed
- Accpet - Accpet a pushed or updated RPC

## Workflow

An app or user creates an RPC with a command/message and id, this id is sent to the "controller" app that either accepts or rejects the RPC. 

The app that has created the RPC can update it before the RPC is rejected/accepted, after it's rejected/accepted you'll have to send a new RPC out to get the data you actually want
