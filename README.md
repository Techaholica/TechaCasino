# TechaCasino
A Casino bot for Twitch.tv

I created a casino in the chat room. Everyone that comes to my channel gets an allowance to gamble with. Use !inventory to see what you currently have. Use !bet to see what your current bet is or !bet [BET AMOUNT] to increase your bet. Use !play [blackjack|slots] to play blackjack or slots. Use !hit, !stand, and !doubledown when playing blackjack. You can also !buy [DRINK] from the bar and !drink [DRINK] when you want to drink it. Use !look to look around or !look [OBJECT] to look at something. I will periodically play bets for you to bet on. Use !placebet [BET NUMBER] [BETTING ON] ([WAGER) to place your bets. For example, use !placebet 1 over 20, to place a bet on bet 1 betting that it will go over and you will bet $20 on that bet. If you are feeling generous, use !give [OBJECT] to [USERNAME] to give away drinks to a user. And of course you could always just !dance if you feel like it. Remeber that this is all fake money! Have fun!

For Admins
- Modify TechaCasino.config to customize your casino
- Load TechaCasino.ini
- When a user enters the room, a profile is created in the users directory (if one didn't already exist)
- You can add more objects to the objects directory if you want to add more drinks or other items users can interact with.
- As an admin you will create bets and give them an ID or [BET NUMBER] this number can be any ID. It can even be text, but it needs to be unique across all bets. This is how you will reference your bets. I typically just use bets 1, 2, 3, and so on.
- Use !setbet [BET NUMBER] [PAYOUT] [DESCRIPTION] to create a new bet. This will output to two files. bets.ini is the file which the script uses to payout users, track bets, and all that. bets.txt is a reader friendly version of this file so that you can display it in OBS or whatever broadcast software you are using. 
- Use !closebet [BET NUMBER] to close out a bet so that users can no longer bet against it. 
- Use !endbet [BET NUMBER] [OUTCOME] to give a bet an outcome. This will also payout all users who have bet that outcome for that bet. This is a text matching system, so keep your bets easy to record. Use Yes/No or Over/Under bets. The script looks for this text (not case sensitive) to see if a user won the bet. After you use this bet, the bet is cleared from all user profiles, but the bet outcome stays on the bets.ini and bets.txt files so that you can still display the outcome.
- Use !clearbet [BET NUMBER] to clear out the bet from the bets.ini and bets.txt files.
