# 表情包 (stickers)

Put images here, one sub-folder per mood, and the bird will attach one now and then:

    stickers/
      categories.json      <- {"folder name": "when the bird should use it"}
      happy/   a.png b.gif
      cry/     ...

- Only folders listed in categories.json AND containing at least one png/jpg/gif/webp are offered to the model.
- The model ends a reply with `&&happy&&` on its own line; the bot strips the tag and sends a random
  image from that folder (never the same file twice in a row).
- `STICKER_CHANCE` in config.py is the dice roll per reply (default 0.35). Set 0 to turn stickers off.
