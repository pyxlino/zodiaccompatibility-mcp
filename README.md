# Zodiac Compatibility MCP app

Compare zodiac signs and read birth charts.

Ask how two signs match, what your Sun, Moon, Venus or rising sign is, or what today's horoscope says. The app answers with the same calculations as zodiaccompatibility.org and shows each reading with its sign symbols and the website's own wording.

- Website: https://zodiaccompatibility.org
- Documentation: https://zodiaccompatibility.org/app
- Privacy: https://zodiaccompatibility.org/privacy
- Terms: https://zodiaccompatibility.org/terms

This repository documents the hosted connector. It does not contain the
website or its code.

## Connect

- Endpoint: `https://zodiaccompatibility.org/api/mcp`
- Transport: Streamable HTTP
- Authentication: none (no account, sign-in or API key)

```json
{ "mcpServers": { "zodiac-compatibility": { "url": "https://zodiaccompatibility.org/api/mcp" } } }
```

In ChatGPT, add it as a custom MCP server with no authentication. In
Claude, open Customize, then Connectors, choose Add custom connector and enter the URL.

## Tools

All tools are read-only.

| Tool | What it does |
|---|---|
| `check_sign_compatibility` | Returns how two zodiac signs match: a verdict label, the wheel aspect and its angle, the elements and modalities, and one line each for love, friendship and work. |
| `get_sign_profile` | Returns a zodiac sign's dates, element, modality, ruler and polarity, its traits, how it behaves in love, friendship and work, and its compatibility verdict with all twelve signs, with the strongest matches named. |
| `find_sun_sign` | Returns the tropical Sun sign for a birth date. |
| `find_moon_sign` | Returns the Moon's tropical zodiac sign for a birth date, with its degree when a birth time is given. |
| `find_rising_sign` | Returns the rising sign (Ascendant) with its degree, and the Descendant, Midheaven and Imum Coeli signs, for a birth date, time and place. |
| `find_venus_sign` | Returns the sign Venus was in on a birth date, with its degree and whether it was retrograde. |
| `get_birth_chart` | Returns a tropical birth chart with whole-sign houses: the Sun, Moon and rising signs, each planet's sign, degree and house, the Ascendant and Midheaven, and up to ten of the tightest major aspects. |
| `get_synastry` | Returns up to ten of the tightest major aspects between two people's birth charts, each with a short meaning, and a reading for one relationship setting built from the planets that setting weighs. |
| `get_daily_horoscope` | Returns a sign's reading for a UTC date, built from that day's real planet positions: the day's reading with the transits it uses, a one-line preview of the next day, and a line for each of the following seven days. |

## Try asking

- "Are Aries and Leo compatible?"
- "What is my rising sign? I was born on 15 May 1990 at 10:30 in London."
- "What is my horoscope today? I am a Gemini."

## Report an issue

Open an issue in this repository or email support@zodiaccompatibility.org.

## License

The documentation files in this repository are MIT licensed (see
[LICENSE](LICENSE)). The Zodiac Compatibility website, its content, data and brand are
not covered by this license.
