# PairWatch
PairWatch lets friends watch a local video in sync—directly in the browser—without uploading to a server. Media flows peer-to-peer over WebRTC; a tiny signaling service and TURN relay exist only to help peers connect through NATs. Sync is driven by a Leader/Follower model using the leader’s media clock as the single source of truth.

## Key features (Phase 1)
- True P2P media: browser-to-browser via WebRTC DataChannels
- Leader/Follower sync: heartbeats, drift control (rate-nudge, snap)
- Instant start: play while downloading using Media Source Extensions (MSE)
- Privacy-first: no media stored server-side (TURN relays are encrypted)
- Works across NATS: minimal signaling + coturn for reliability