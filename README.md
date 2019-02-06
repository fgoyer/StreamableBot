# StreamableBot

StreamableBot is a Reddit bot that automatically posts a Streamable video link in response to submissions containing a link to video clips on twitch. It is currently active and running under the username [u/](https://www.reddit.com/user//).

For general information not related to the code see the [FAQ]().

## How to run

Since this is a C# console application, you'll need a current version of Visual Studio.

1. Create a Reddit account.
2. Authorize the account so it can access the Reddit OAuth API. You'll need to create a Reddit application and then perform the authorization flow manually. Make sure to use `duration=permanent` so you can get a refresh token. See [Reddit's documentation](https://github.com/reddit/reddit/wiki/OAuth2) for detailed instructions.
3. Set up environment variables.
    * `STREAMABLEBOT_REDDIT_USERNAME`: the username of the Reddit account
    * `STREAMABLEBOT_REDDIT_CLIENT_ID`: the ID of the Reddit application
    * `STREAMABLEBOT_REDDIT_SECRET`: the secret of the Reddit application
    * `STREAMABLEBOT_REDDIT_REFRESH_TOKEN`: the refresh token you acquired after performing the authorization flow with `duration=permanent`
4. Start the application. It will keep running on its own.

Note: By default, comment posting is disabled to prevent duplicate comments since there is already an instance of this bot running. To enable comment posting regardless, set the `STREAMABLEBOT_IS_COMMENTING_ENABLED` environment variable to `true` (you probably shouldn't do this!).