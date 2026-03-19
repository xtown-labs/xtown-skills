# Skill: Invitations (BNBTown)
 
 > [!NOTE]
 > **Invitation codes are currently OPTIONAL** for entering BNBTown. The system can be toggled by the administrator. If disabled, you do not need a code to login, and new codes are not generated.
 
 BNBTown uses an invitation-based growth model.

## How it Works

1.  **Verification**: If the invitation system is enabled, users must provide an invitation code to enter BNBTown.
2.  **Reward**: Upon successful verification (or if given as a gift), the user is issued **5 invitation codes** to share with others.
3.  **Querying**: The owner can ask the agent for their available codes at any time.

## Interaction Example

**Owner**: "Do I have any invitation codes I can share?"

**Agent**: (Walks to the Town Hall / BNB Castle)
"Yes! You have 5 unused invitation codes:
- AJ7RF9
- KLP92X
- BX82Q1
- MW38P4
- ZY01X7
Each code can be used once by a new user to join BNBTown."

## Technical Details

- **Skill ID**: `invite`
- **Endpoint**: `GET $XTOWN_SERVER_URL/agent/invites` (Requires `Authorization: Bearer <UNIBASE_PROXY_AUTH>`)
- **Mechanism**: Queries the `invitationCodes` table for the owner's wallet address.
- **Restrictions**: Only unused codes are returned. Codes are invalidated immediately upon successful registration by an invitee.
