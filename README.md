#RankPoints

RankPoints keeps track of points that are awarded to players using plugins such as VoteReward which allow you to run commands (or on console).  PurePerms ranks are set automatically according to the config.

This plugin ONLY supports PurePerms. Please post questions in the "Thread" section, not "Review".

In-Game Commands:
/rankpoints - displays your own rank points
/rankpoints player - displays rank points for a player

Console or Plugin Commands:
rankpoints player points

where player is a player's IGN, and points is an integer.

Putting the following lines at the end of VoteReward

Commands:
  - "rankpoints {USERNAME} 1"

or running the command "rankpoints awzaw 1" on console, will add 1 point to the player awzaw's current rank points total, then check the config.yml which must be configured in this format, for example:

Ranks:
- Member
- Builder
- Admin
Points:
- 0
- 5
- 50

You MUST have PurePerms installed, and the Ranks in RankPoints config.yml MUST all be existing PurePerms groups.

IMPORTANT:
The first rank MUST be the default PurePerms group, with the points needed set to to zero.  Players with higher ranks, or ranks not in the Ranks config will not be deranked.

Q: Why doesn't it work?

A: You MUST have PurePerms installed, the Ranks in RankPoints config.yml MUST all be existing PurePerms groups. Also the first rank MUST be the default PurePerms group, with points set to to zero. If that doesn't help, check you are using a recent version of PurePerms.

Q: Will players who get rank points ever be deranked when earning points?

A: Players with a rank not listed in the RankPoints config.yml file, or above the target rank (ie who already have a higher rank in the RankPoints config) will not be deranked.

Q: What can I use this plugin for?

A: RankPoints is designed to give players ranks automatically according to the number of votes (with VoteReward), but can be used with any plugin that allows you to run the command "rankpoints {USERNAME} {POINTS}" where {USERNAME} is the players IGN, and {POINTS} is an integer.

TODO:
Permissions, give rank points to all online players, add error checking for missing ranks, bad config etc, Configurable rankpoints help command and "Success" message when players are ranked etc
