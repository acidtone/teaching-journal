# [How To Show Chat Messages On Stream](https://www.youtube.com/watch?v=OK1V_7CmyfY) ("Featured Chat")
by Gaming Careers
- Initial Setup
    1. Go to [featured.chat](https://featured.chat/);
    2. Login with Twitch account and authorize the app;
    3. Click `Enable Featured Chat`;
    4. Add browser source into OBS (or whatever streaming software):
        1. Copy the "Main" URL;
        2. In OBS add "Browser Source" to a Scene of your choice and paste the URL;
        3. Set the dimensions to match your Canvas Resolution;
        4. Check "Control audio via OBS".
- Test Twitch chat message:
    1. Open Twitch chat;
    2. Type test message of *more than one word*;
    3. Go back to the `featured.chat` website -> `My Dashboard`;
    4. Find test message and click `+` to add it to the queue;
    5. Click Twitch logo next to message to show on stream.
- Customize Styles:
    1. Go back to the `featured.chat` website -> `My Settings`;
    2. Blah, blah, bah
- Highlighting Messages: Auto-adds messages to the queue if a viewer redeems a "Highlight My Message Channel Points" reward.
    1. Enable "Automatically put highlighted messages into the On Deck queue";
    2. Enable and customize the cost of the Highlight My Message reward in the Twitch Channel Point Dashboard.
- Q & A Chat: Allow viewers to prepend a message with custom characters to auto-add questions.
    1. Instruct viewers to ask a question by starting the message with `q:` (or whatever);
    2. In `featured.chat`:
        1. Go to AMA/Q&A tab in the Dashboard;
        2. Click settings cog and enter your prefix;
        3. Start filtering by clicking the `Play` icon.
- Chat Dock: Access chat directly in OBS
    1. Go to `featured.chat` > `My Settings` -> `Other`;
    2. Enable "Broadcaster - Skip Queue";
    3. Copy the "OBS Dock URL";
    4. In OBS go to `View` > `Docks` > `Custom Browser Docks`;
    5. Add new Browser Dock and paste URL;
    6. Arrange the new Dock as desired. You can now feature a message directly from OBS.
- Moderator Permissions
    1. Click "Add Moderators" to add your Twitch mods with one click;
    2. Have mods log into `featured.chat` using their Twitch account;
