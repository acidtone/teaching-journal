# [OBS Studio - Advanced Mic Settings (Noise Removal, Compressor, Noise Gate)](https://www.youtube.com/watch?v=noqKxopwp74) 
by Gaming Careers
- **Noise suppression**: for removing minor background noise like fans, Hvac, etc.
    1. Click cog next to the sound source -> Filters
    2. Click `+` to add filter
    3. Select `Noise Suppression` -> Custom name -> OK
    4. Tweak Level. Try -20dB?
- **Noise Gate**: turns off mic when you're not talking
    1. Source -> Filters -> `+`
    2. Select `Noise Gate`
    3. Tweak settings:
        - `Close Threshold`: the sound level at which the mic will mute itself.
        - `Open Threshold`: the sound level that will trigger the mic to unmute.
        - `Attack Time`: the time needed for a noise to be active before the mic will become active.
        - `Hold Time`: the amount of time the mic will remain active after you top speaking. If the value is too low, the mic may cut out in between words.
        - `Release Time`: The amount of time the OBS filter takes to actually turn off the mic (how is this different than Hold Time?).
- **Compressor**: Turns down the mic level when you're loud and raises it when you're quiet.
    1. Source -> Filters -> `+`
    2. Select `Compressor`
    3. Tweak settings:
        - `Ratio`: Amount of compression that's applied. Example: `2` will reduce mic level by half.
        - `Threshold`: Threshold at which the compressor will kick in.
        - `Attack`: How quickly the compressor will kick in after the `Threshold` is reached.
        - `Release`: How quickly the compressor will return to normal after the levels drop below `Threshold`.
        - `Output Gain`: Increase of decrease the gain of the mic.
- **Gain**: Increase of decrease the gain of the mic.
    1. Source -> Filters -> `+`
    2. Select `Gain`
    3. Tweak setting.
