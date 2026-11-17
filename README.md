# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/anggiatlandoo/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/anggiatlandoo/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A 4 KB chess engine for the make.fun tiny-chess-01 bounty. main.py is the whole engine (4,015 bytes as committed): it unpacks an LZMA payload produced by the kit's makefun compress from the readable source engine.py. Engine: 0x88 board, negamax alpha-beta with iterative deepening under a fixed node budget (100,000 nodes/move early, less in the late game), transposition table, two killer moves per ply, MVV-LVA capture ordering, quiescence search over captures, promotions and replies to check, and null-move, futility and delta pruning. Evaluation is material plus piece-square tables with a bishop-pair bonus and a separate king endgame table. Deterministic: fixed node budget, no clock, no randomness, so replays play the same moves.

## Run it

```sh
python3 -P -s main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=4gqgrk6n&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
