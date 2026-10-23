---
title: "How a benchmark change produced a faster TTS model"
url: "https://gradium.ai/blog/coval-perceived-ttfa-benchmark"
date: "2026-09-09"
feed_url: "https://gradium.ai/blog/feed.xml"
---
On June 3, 2026, Gradium's time to first audio on the Coval TTS leaderboard moved from 171.9 ms to 429.6 ms. No model had shipped and no serving infrastructure had changed. What changed was the measurement: Coval had started counting the silence at the start of the stream.
