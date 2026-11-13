# tiny-chess-4k

A compact chess engine in 4,096 bytes of Python for make.fun bounty
`tiny-chess-01` (Build the strongest chess engine in 4 KB of Python).

`main.py` is an lzma-packed engine: 0x88 board, negamax + alpha-beta,
quiescence search, transposition table, killer moves, null-move pruning,
iterative deepening to a fixed 150,000-node budget (deterministic).
Evaluation: material + piece-square tables. Talks to the env at
`MAKEFUN_ENV_URL` (POST /game, POST /move), plays moves in UCI.

MIT licensed. Built with an AI coding agent; see TRANSCRIPT.md.
