## 2026-11-18

**Scope:**
- In: payment for one individual concert, through one external payment provider, with a single method (MB WAY) and a single currency (EUR).
- In: the artist sets the concert price when scheduling it (price can be zero for a free concert); the platform keeps a 17.5% commission deducted from the artist's revenue, and the spectator pays exactly the price the artist set.
- In: purchase is allowed from the moment the concert is scheduled until the broadcast ends (pre-sale and late entry).
- Out: monthly subscription (separate item), additional payment methods and currencies, recordings or purchase after the concert ends, automatic refunds.

**Users:** a spectator with an account. An account is required to buy, so that access is tied to the spectator. The artist is affected only as the one who sets the price.

**Edge cases:**
- MB WAY requires confirmation in the bank app, so a payment can stay pending. Access is granted only after the payment is confirmed; if the request expires or is refused, the spectator keeps no access and can try again.
- A spectator who already paid for a concert is not asked to pay again.
- Free concerts (price zero) skip the payment step.
- A paid ticket can be used on one device at a time; a second simultaneous session is not allowed.
- No refunds in the MVP, not even for a cancelled concert or a failed broadcast; these cases are handled manually by support.

**Constraints:**
- Commission of 17.5% is deducted from the artist, not added to the spectator's price.
- Currency is EUR only; payment goes through an external provider that supports MB WAY.
- Depends on the artist being able to schedule a concert with a price (0010) and on the spectator being able to watch it (0020).

**Open questions:**
- Which payment provider will be used for MB WAY?
- How and when the artist receives their revenue (payout) is not covered here.
- Behavior when a second device tries to join: block the new session, or end the old one?
- Whether the spectator sees the commission or any fee breakdown (assumed no).
