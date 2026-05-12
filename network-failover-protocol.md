# Network Failover & Offline Mode Protocol (Toast POS)

**Scenario:** Primary ISP (Internet) goes down during a high-volume service period.
**Goal:** Transition to Offline Mode to ensure order continuity and guest payments without data loss.

## Phase 1: Identification & Immediate Response
1. **Verify Connectivity:** Check the Toast 'Device Status' screen. If "Offline" status appears across all terminals, confirm if the issue is a local router failure or an ISP outage.
2. **Alert Management:** Notify the floor team to avoid restarting tablets, as this can clear the local cache of un-synced orders.

## Phase 2: Enabling Offline Mode
1. **Local Network Continuity:** Ensure the internal LAN (Local Area Network) is still active. Order routing to Kitchen Display Systems (KDS) will continue as long as the local router/switches are powered.
2. **Transaction Protocol:**
   - Toast will automatically enter "Background Sync" mode. 
   - **Constraint:** Do not perform "Full Sync" or log out of the app.
   - **Risk Mitigation:** Remind staff that credit card authorizations are delayed; limit high-value transactions to minimize potential "declined" card risk once the system is back online.

## Phase 3: Restoration
1. **Manual Sync:** Once the ISP light is solid green, monitor the 'Outbox' on the main terminal.
2. **Validation:** Verify that all "Background Total" amounts match the physical receipts before closing the business day.
