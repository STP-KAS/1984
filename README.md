# Kworld

Kworld is a Testnet-10 village square at [sixpack.wtf/kworld.html](https://sixpack.wtf/kworld.html). It is a basic, adjustable toy. A person walks up to a shop and pays with one of three rails on proof of work. It is not a bank transfer, and it is not a product that replaces one.

The page code lives in [STP-KAS/sixpack.wtf](https://github.com/STP-KAS/sixpack.wtf). This repository is the note: what the square is, and how a visit works.

## What you see

A welcome gate comes up first.

- **New arrival** opens a funded test address that exists only in that browser tab. Close the tab and the address is gone. Leftover tKAS is swept back and is not yours to recover.
- **Returning** uses Kasware, Kastle, a pasted `kaspatest:` address, or a `.kas` name that already resolves. That choice stays on the browser and keeps its history.

The square is click-to-walk. The shops are Nia's Cafe, Orin's Table, Mara's Groceries, Venn's bank, and Pike's Roadster. The car stays on the square. A lap is a turn, not a title.

The top bar shows who is paying, the tKAS balance, the POCencept balance, and the KUSDT balance. The left side opens the shops, the spending rules, and a bench of related work. The right side is where you change who pays. This page never asks for a seed. A mainnet wallet is refused.

A `.kas` name that points at you ties the public spend to you. A plain `kaspatest:` address, or a name that does not identify you, is the preference here. Creating a name is KNS. This page only resolves one.

## How a visit works

GitHub Pages serves the page. The ledger does not run on Pages. It runs with the sixpack server, which the page calls for balances, the live KAS price, a test-tab open, and a shop spend.

Shop prices are toy cents. A tKAS payment is a real Testnet-10 transaction to the reserve shown on the page:

`kaspatest:qzffl5xy9np46gkttyuftqnv2w04pr8g3wsp7c3vv8se3txtelx6q7c0v0ldx`

The sompi amount follows the live KAS/USD quote. The miner fee is extra tKAS. POCencept and KUSDT do not move on the chain. They are tags in the village ledger. The tag does not change when the KAS price moves.

The bank locks tKAS into POCencept or KUSDT at that live quote. Redeem sends tKAS back only for the locked part. The practice purse can be spent at a shop. It cannot be redeemed. A failed redeem puts the toy balance back.

A new arrival is minted on the server. The browser receives the address and a token. It does not receive the key. The key never goes in git. Closing the tab asks the server to sweep the coins home after a short grace, so a refresh does not burn the wallet.

Spending rules sit in the panel: a daily cap, a shop list, a rail list, and a confirm line. Above the confirm line the till waits for a second yes before it spends.

## Covenants

A covenant, in the sense SilverScript and the Kaspero Labs freelancer sheet use the word, is a rule the Kaspa network enforces on the coins. The sheet holds the coins. The studio does not.

Kworld does not compile a SilverScript covenant into the till. The rules panel is the stand-in you can click. The confirm line is the visible version of "wait for a second yes." A real covenant would put that yes in the script.

The bench links the pieces this square is pointing at:

- [kaspanet/silverscript](https://github.com/kaspanet/silverscript)
- [Freelancer sheet](https://silverscriptstudio.com/freelancer.html)
- [Kaspero Labs on the freelancer contract](https://x.com/KasperoLabs/status/2104543100634886578)
- [argent-lang/argent](https://github.com/argent-lang/argent)

## vProgs

vProgs, in the early prototype, is a guest program whose steps can be sequenced and checked. The public tic-tac-toe guest is a game of plies. It is not a payment rail.

Kworld's shop spend is not a ply inside that match. The village ledger is a server file. A later guest could sequence a till the way that tic-tac-toe guest sequences a move. This square does not claim that sequencer is running here. Coffee is not a move in a match.

- [biryukovmaxim/vprog-tictactoe](https://github.com/biryukovmaxim/vprog-tictactoe)
- [kaspanet/vprogs](https://github.com/kaspanet/vprogs)
- [STP-KAS/vprogs-tn-desk-public](https://github.com/STP-KAS/vprogs-tn-desk-public)

## What this square does not copy

The drawing is original. Jagex art, the RuneScape wordmark, a private-server engine, and a soundtrack file are not in the page. The Go topic list for RuneScape is markers, hiscores, and private-server code. None of that was vendored. Tidewater is an MIT fishing island and was not copied either.

KCC-20 is still Draft. There is no spendable layer-1 stable in this till. POCencept is not Tether. KUSDT is a labeled toy so a freeze can be seen. The freeze does not touch POCencept or tKAS.

The three rails, and why each one exists, are in [STP-KAS/kworld-rails](https://github.com/STP-KAS/kworld-rails). The prompts for the builder and the bot are in [STP-KAS/kworld-prompts](https://github.com/STP-KAS/kworld-prompts).
