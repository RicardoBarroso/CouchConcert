# Acceptance Criteria

The spectator should be able to:
- see the price of a concert, in EUR, before deciding to pay
- pay for a concert with MB WAY, from the moment it is scheduled until its broadcast ends
- start watching the concert as soon as the payment is confirmed
- watch a free concert (price zero) without any payment step
- try again if the MB WAY request expires or is refused

The system should:
- require the spectator to be logged in to buy; otherwise ask them to log in first
- grant access only to the concert that was paid for, and not to other paid concerts
- not ask a spectator who already paid for a concert to pay for it again
- keep the payment as pending, with no access, until MB WAY confirms it
- show a clear message and keep no access when the payment is refused or expires
- reject a purchase after the concert broadcast has ended
- allow only one device at a time per paid ticket
- charge the spectator exactly the price set by the artist
- record a 17.5% platform commission, deducted from the artist's revenue, for each paid concert
- not generate any automatic refund
