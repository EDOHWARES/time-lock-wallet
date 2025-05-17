#  Time-Lock Bitcoin Wallet

> "Bitcoin you can’t touch… yet."  
> A wallet that helps you save for the future, automate inheritance, and create trustless agreements all without needing a third party.


##  What's the idea?

Most people rely on banks, lawyers, or institutions when they want to lock money for future use  like a savings plan, inheritance, or an escrow. But in crypto, **we believe in decentralization**, and that means we need ways to lock and release funds without involving anyone else.

**Time-Lock Bitcoin Wallet** lets you do exactly that.

This is a simple wallet that lets you lock your BTC until a specific block height. It uses Bitcoin Script (`OP_CHECKLOCKTIMEVERIFY`) to make sure **nobody, not even you**, can access the funds before the time is right.


##  Problem We're Solving

In traditional finance:
- You need a **bank** to lock your funds in a savings account.
- You need a **lawyer or legal will** to plan inheritance.
- You need a **third-party escrow** when making a conditional deal.

But in Bitcoin:
- You should be able to do all this *yourself*, in a **trustless and programmable** way.

Yet… most people don’t know how to write raw Bitcoin scripts or build P2SH addresses. That’s where this wallet comes in.


##  What the Wallet Does

This wallet lets users:
1. **Choose a future unlock time (block height)**
2. **Get a Bitcoin address** that is only spendable *after* that block
3. **Fund that address with BTC**
4. Sit back and **wait** — knowing the funds are 100% inaccessible until the unlock block
5. **Spend the funds** once the unlock condition is met



##  Real-World Goals & Use Cases

### Trustless Future Savings
> "I want to save 0.01 BTC for my future self, and I don’t want to be tempted to touch it for 2 years."

### Automated Inheritance
> "If something happens to me, my heir can redeem the BTC after 1 year using this redeem script."

### Time-Based Escrow
> "I’ll lock funds in a script address until we finish a deal. If it’s not complete in time, it gets refunded."

### Hackathon Challenge Gimmick
> "If we win this hackathon, our prize unlocks after 100 blocks as proof we stuck around!"


## Summary of User Flow

1. **Pick a future block height** (e.g., "2 years = ~262,800 blocks")
2. The app generates a **custom Bitcoin script** and corresponding address
3. **Send BTC** to that address
4. The funds sit securely on the chain — **untouchable by anyone**
5. Once the set time is reached, **redeem your funds**

We also show current block progress and countdown.


## Technical Breakdown

| Layer      | Stack                                           |
---------|------------------------------------------------|
| Bitcoin Script | `OP_CHECKLOCKTIMEVERIFY` (CLTV), P2SH / Taproot |
| Frontend   | React / Next.js                                |
| Backend    | Node.js or Python, bitcoinjs-lib               |
| Optional   | Lightning integration via LNBits or Alby       |
| Wallet Integration | QR export, redeem script, CLI guidance        |



## Why Add Lightning?

Lightning Network brings *instant* and *low-fee* transactions — but this app takes it further:

- **Convert Lightning to on-chain** + time-lock it for savings
- **Earn BTC via Lightning**, then lock a % as a form of automated budgeting
- **Bridge time-locks** and **micropayments** for new creative financial flows



## Imagine This…

> “I’ve always wanted to save, but I suck at self-control. With this wallet, I locked 0.01 BTC for 2 years. It’s literally unreachable. Now I’ve got a solid savings plan and no one can break it — not even me.”



## Future Add-ons 

- Multi-party time-lock (e.g., unlock early if 2 of 3 people agree)
- Dead-man switch (funds release if no action taken by deadline)
- Redeem from UI (right now it’s CLI-based)
- Proof of lock for DAOs or grant milestones
- Mobile version (for long-term savings goals with reminders)



## Who's It For?

- Bitcoiners who believe in **self-custody**
- Developers who want trustless ways to handle BTC flow
- Regular people who want a **digital piggy bank**
