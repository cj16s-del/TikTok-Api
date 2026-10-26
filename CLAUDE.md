# drako! TikTok marketing memory

This repo is a fork of TikTok-Api. This file is the persistent memory for helping **drako! (@drakoo.wav)** grow their TikTok and music. Read it at the start of every session.

## Who they are
- Underground rapper and producer from Norfolk / Virginia Beach, VA. Makes beats in FL Studio and raps on their own songs.
- Account plan: mostly opinion text posts (photo mode), plus videos they want to post (beats, music).
- Goal: turn views into **profile views, followers and listens to their music**.

## Standing instructions
- Before writing any new post, review the analytics below (and any new screenshots) and say what's working and what's holding them back. Keep the good habits and drop the bad ones.
- When they send new weekly analytics, add them to the tables below, then commit and push to `main`.
- Use the MarketingSkills `social` skill guidance and TikTok-Api where it works (see notes at the bottom).

## Writing rules (their preferences)
- **Photo/text post** = screen text + title (bold line at the bottom) + caption. **Video posts have no title**; the first line of the caption does that job.
- Screen text: a strong line, then a twist in brackets, often with 😭. Vary the twist; repeated "DON'T say" / "NOT ___" lines got stale. The bracket can just be funny; it doesn't always need to invite a response.
- **No made-up details.** Only use facts they gave or that are verifiably true. Production details must come from them.
- **No obvious engagement bait** in captions ("comment below", "full song on my page", "thoughts?"). They delete it.
- Always use the **strongest buzzwords** for the topic in titles and captions.
- Max **5 hashtags** (TikTok limit). No #fyp / #viral.
- Celebrity hot takes: aim the joke at the person who did something, not at anyone's looks.
- Sound: **their own song** by default (their top post used it). Use their beat on posts aimed at artists, with the sound renamed to `prod. drako! 🔥`.
- Location: Norfolk · Virginia Beach.

## Weekly analytics

| Week | Post views | Profile views | Profile view rate | Likes | Comments | Shares | New followers |
|---|---|---|---|---|---|---|---|
| Oct 14–20, 2026 | 12.3K | 219 | 1.8% | 377 | 180 | 14 | ? |
| Oct 18–24, 2026 | 140.6K | 1.2K | 0.85% | 5.3K | 3.6K | 115 | ? |

Targets: profile view rate back above 1.5%. Shares are the weakest metric.

Traffic (Oct 14–20): For You 96.7%, profile 3.0%, search 0.2%, sound 0.1%. Search queries that found them: "iayze funny moments" (26%), "iayze fl preset", "iayze 556", "fl studio".

## Post results

| Post | Type | Views | Likes | Comments | Saves | New followers | Sound |
|---|---|---|---|---|---|---|---|
| Jay-Z "picking HIMSELF" + Nine Vicious/MGK twist | text | 20.9K | 992 | 303 | 53 | ? | Tom Ford (Jay-Z) |
| VST question (NOT Serum/Omnisphere) | text | 11.8K | 399 | 316 | 121 | 1 | Foul Out (own) |
| Samples question (NOT Splice) | text | 7.7K | 170 | 51 | 24 | 2 | Fanta (own) |
| Artists/prods "lock in" (no bracket twist) | text | 1.7K | 35 | 8 | 0 | 1 | own |
| Face + Norfolk map | photos | 1.3K | 81 | 34 | 6 | 24 | — |
| Spider-Man edit | video | 323 | 19 | 0 | 2 | — | Reminiscing (own) |

The user says their top-viewed post overall (a Jay-Z post) used their own song. The Jay-Z reply post (Miley/Metallica) underperformed after the bracket twist moved into the title. The beat-pack post (asking producers for beats) and the first beat video (diamond* x Pz' type beat) underperformed.

## What works / what doesn't
- Works: one clear question or hot take plus a bracket twist on screen; producer knowledge questions (lots of saves); news hot takes (views and comments); replying in comments.
- Doesn't: posts with no question or take; two questions at once; asking people to do something for you; running the same topic many posts in a row.
- Biggest gap: text posts get views but few followers. Posts showing their face or music convert far better. Fixes: pin posts on the profile, a clear bio, video replies on camera, a face/music post every 3–4 posts, series ("part 2").

## Hashtag data (TikTok-Api, Oct 2026, avg views per video)
- Strong: #esdeekid ~35.8k, #fakemink ~14.2k, #producertok ~10k, #vocalmixing ~9.6k, #flstudio ~9.2k.
- Medium: #undergroundrap ~6.5k, #pluggnb ~6k.
- Weak: #rappertok ~5.5k, #homestudio ~4.4k, #undergroundbeats ~3.9k, #undergroundhiphop ~2.9k.
- Only tag artists the beat actually sounds like.

## TikTok-Api notes
- Run from repo root with `PYTHONPATH=.`; launch Chromium with `executable_path="/opt/pw-browsers/chromium"`.
- Without an `ms_token`, TikTok often returns empty responses. Hashtag lookups work intermittently (one session per tag, with pauses). User profile listing fails.
- Video lookups need the full URL (`https://www.tiktok.com/@drakoo.wav/video/<id>`). Resolve short links with `curl -sIL -o /dev/null -w '%{url_effective}'`; photo-post IDs work with `/video/` in the URL.
