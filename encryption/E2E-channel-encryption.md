# E2EE for server messages

## Status
Not implemented.

## Strategy Mock

This is a base scenario.

- Finwe sends server invite to Alex, Doru & Putzi. (Finwe also creates random AES-GCM key).
- Doru & Putzi are online (connected to websockets) & Alex is not online.
- Doru & Putzi click join server, they send a request to Finwe (through WS) to get the key.
- Doru & Putzi receive the key and can now decrypt the contents of the server.
- Finwe goes offline.
- Alex comes back online, but can't join the server until Finwe (server inviter) is also online.
- Finwe comes online, Alex requests invite and gets it (through websockets).
- Alex is now able to decrypt server messages.
