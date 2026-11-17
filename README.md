# tiny-chess-01

A 4 KB chess engine for the make.fun tiny-chess-01 bounty. `main.py` is the
whole engine (4,039 bytes as committed): it unpacks an LZMA payload produced
by the kit's `makefun compress` from the readable source `engine.py`.

Engine: 0x88 board, negamax alpha-beta with iterative deepening under a
fixed node budget (100,000 nodes/move early, less in the late game),
transposition table, two killer moves per ply, MVV-LVA capture ordering,
quiescence search over captures, promotions and replies to check, and
null-move, futility and delta pruning. Evaluation is material plus
piece-square tables (halved Michniewski values) with a bishop-pair bonus
and a separate king endgame table. Deterministic: fixed node budget, no
clock, no randomness, so replays play the same moves.

Run: `python3 -P -s main.py` with `MAKEFUN_ENV_URL` set to the trial env.
