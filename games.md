---
layout: page
title: Games
permalink: /games/
---

A few small browser games I've built. All run peer-to-peer in your browser — no accounts, no backend. The host shares an invite link with friends.

<style>
  .game-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 1.25rem;
    margin: 2rem 0;
  }
  @media (max-width: 600px) {
    .game-grid { grid-template-columns: 1fr; }
  }
  .game-tile {
    position: relative;
    display: block;
    padding: 1.5rem 1.5rem 1.25rem;
    border-radius: 14px;
    text-decoration: none !important;
    color: #1a1a1a;
    background: #fff;
    border: 1px solid rgba(0,0,0,0.08);
    box-shadow: 0 1px 2px rgba(0,0,0,0.04);
    overflow: hidden;
    transition: transform 0.18s ease, box-shadow 0.18s ease, border-color 0.18s ease;
  }
  .game-tile:hover {
    transform: translateY(-3px);
    box-shadow: 0 10px 24px rgba(0,0,0,0.10);
    border-color: rgba(0,0,0,0.12);
    text-decoration: none !important;
  }
  .game-tile::before {
    content: "";
    position: absolute;
    left: 0; top: 0; bottom: 0;
    width: 5px;
    background: var(--accent, #888);
  }
  .game-tile .icon {
    font-size: 2.25rem;
    line-height: 1;
    margin-bottom: 0.6rem;
  }
  .game-tile .title {
    font-size: 1.15rem;
    font-weight: 600;
    margin: 0 0 0.35rem;
    color: #111;
  }
  .game-tile .desc {
    font-size: 0.92rem;
    line-height: 1.45;
    color: #444;
    margin: 0 0 0.85rem;
  }
  .game-tile .players {
    display: inline-block;
    font-size: 0.78rem;
    font-weight: 600;
    letter-spacing: 0.02em;
    padding: 0.25rem 0.6rem;
    border-radius: 999px;
    background: var(--accent-soft, #f0f0f0);
    color: var(--accent-ink, #333);
  }
  .tile-connect4    { --accent: #e63946; --accent-soft: #fde6e8; --accent-ink: #a31621; }
  .tile-checkers    { --accent: #6a4c93; --accent-soft: #ece4f5; --accent-ink: #4b3470; }
  .tile-pictionary  { --accent: #1d9bf0; --accent-soft: #e1f0fb; --accent-ink: #0a5a91; }
  .tile-jigsaw      { --accent: #2a9d8f; --accent-soft: #def0ec; --accent-ink: #1c6e64; }
</style>

<div class="game-grid">
  <a class="game-tile tile-connect4" href="https://bosemessi.github.io/connect4-personal/">
    <div class="icon">🔴🟡</div>
    <div class="title">Connect 4</div>
    <p class="desc">Classic two-player tile-drop. Line up four in a row to win.</p>
    <span class="players">2 players</span>
  </a>

  <a class="game-tile tile-checkers" href="https://bosemessi.github.io/chinese-checkers-personal/">
    <div class="icon">⭐</div>
    <div class="title">Chinese Checkers</div>
    <p class="desc">Race your pieces across the star-shaped board to the opposite corner.</p>
    <span class="players">2–6 players</span>
  </a>

  <a class="game-tile tile-pictionary" href="https://bosemessi.github.io/pictionary_personal/">
    <div class="icon">🎨</div>
    <div class="title">Pictionary</div>
    <p class="desc">Draw the prompt, guess what others draw, score points.</p>
    <span class="players">2–8 players</span>
  </a>

  <a class="game-tile tile-jigsaw" href="https://bosemessi.github.io/puzzle_personal/">
    <div class="icon">🧩</div>
    <div class="title">Collaborative Jigsaw</div>
    <p class="desc">Solve a jigsaw puzzle together in real time.</p>
    <span class="players">1–8 players</span>
  </a>
</div>
