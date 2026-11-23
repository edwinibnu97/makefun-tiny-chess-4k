# makefun-tiny-chess-4k

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/edwinibnu97/makefun-tiny-chess-4k/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/edwinibnu97/makefun-tiny-chess-4k/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A compact chess engine in 4,096 bytes of Python for make.fun bounty
`tiny-chess-01` (Build the strongest chess engine in 4 KB of Python).

`main.py` is the engine, packed from the readable source `engine_src.py`
with the kit's `makefun compress` (the source itself is not committed, it
travels with the session bundle). 0x88 board, negamax + alpha-beta,
quiescence search, transposition table, killer moves, null-move pruning,
iterative deepening to a fixed 100,000-node budget (deterministic, no
clock, no unseeded randomness). Evaluation: material + piece-square
tables. Talks to the env at `MAKEFUN_ENV_URL` (POST /game, POST /move),
plays moves in UCI. Perft-verified (startpos 20/400/8902, Kiwipete
48/2039/97862) and mate-in-1 verified.

MIT licensed. Built with an AI coding agent; see TRANSCRIPT.md.

## Run it

```sh
MAKEFUN_ENV_URL=http://localhost:8080 python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=q17yfxs8&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
