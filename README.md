# Tiny Chess — 4 KB Python chess engine

A from-scratch chess engine in a single packed `main.py` (3,292 bytes).

- 0x88 board, legal move generation (castling, en passant, promotion)
- Alpha-beta with iterative deepening, PVS, LMR, null-move pruning,
  check extensions
- Quiescence search (captures, all evasions when in check)
- Transposition table, MVV-LVA + killer + history move ordering
- Evaluation: material + piece-square tables (middlegame/endgame king),
  bishop-pair bonus, tempo, king pawn-shield, passed-pawn bonus
- Fixed 60,000-node budget per move: fully deterministic, no clock,
  no randomness, no model calls — about 2 s a move on one CPU

`src.py` is the readable source; `main.py` is packed from it with the
kit's `makefun compress` (`src.py` need not be committed). Practice
trial-0 (kit level 7): see the entry notes. License: MIT.
