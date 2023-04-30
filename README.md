Download Link: https://assignmentchef.com/product/solved-ece175-final-project-a-game-of-31
<br>
Your task is to develop a program that plays a game of 31. In particular, your program should satisfy thefollowing requirements:1. Playing cards are represented as variables of the following type:typedef struct card s {char suit[9];int value;struct card s *pt;} card;You are allowed to add attributes to this definition, but not to remove any.2. The game is played using two decks of cards.3. The deck is represented as a dynamic list of cards. The cards drawn from the deck are deleted fromthe list.4. The player’s hand is represented as a dynamic list of cards. The list is populated with the cards drawnby the player.5. The dealer’s hand is represented as a dynamic list of cards. The list is populated with the cards drawnby the dealer.6. Before the game starts, the two decks of cards should be shuffled.7. The player starts the game with $1,000. The game terminates if the player loses all his money.8. The minimum bet is $20 and the maximum bet is $200. The system shall not allow the player to betmore than he has available.9. The game rules are as follows:(a) The game proceeds in rounds.(b) Face cards (Kings, Queens, and Jacks) count as 10 points.(c) Aces count as 1 point or 11 points.(d) The player places his/her bet at the beginning of every round and before any cards are dealt.(e) Initially, the dealer and the player are dealt one card each, in the following order: player-dealer.(f) The card of the dealer is dealt face up.(g) After the two cards are dealt, the player goes first. The player has the option of “hit” (being dealtadditional an card) or “stand” (terminate his turn). The player’s objective is to bring his/her handas close to 31 points as possible. The player’s turn terminates when the player stands, hits 31, or theplayer goes “bust” (goes over 31).(h) If the player hits 14, he is given the option to “stand”. The dealer has to hit 31 to win a hand for which a player has chosen to stand at 14.(i) The dealer takes hits until his hand totals 27 or more points. The dealer cannot take a hit beyond 27.(j) In case the player has hit 14, the dealer continues to draw cards until he hits 31 or goes bust.(k) If the player does not go bust and his hand total is higher than the dealer’s total or the dealer goes “bust”, he/she wins the bet. If the dealer and the player have the same hand total, the bet is “pushed” (no win or loss). If the dealer has a higher hand than the player’s hand, the player loses the bet.(l) Exceptions are made if 14 is hit by one of the players. If player hits 14 and dealer hits 31, the dealer wins. If dealer hits 14, he wins. If dealer hits 14, while the player has also hit 14, the dealer has to continuously draw to hit 31, in order to win.(m) The deck is shu&#x270f;ed when less than 30 cards are left. The dealer’s and the player’s lists are deletedat the end of each round (memory is freed back to the system).

CriterionMaximum Points Exemplary (100%) Proficient (75%) Marginal (25%) Unacceptable (0%)Requirements1 Deck shuffling /10Deck is implemented as alinked list. Deck is shuffledwhen less than 30 cards areleft. The shuffling functionproduces a new sequence ofcards per round and everytime the program is restartedDeck is shuffled but cardsequences are not sufficientlyuniqueDeck is not shuffled whenfewer than 30 cards are leftDeck is not implemented as alinked list and/or the deck isnot shuffled2 Card Dealing /10Cards are dealt in the properorder. Dealer’s first cardappears face upThe right number of cards isdealt, but not in a properorderCards are not dealt correctly Card dealing is notimplemented3 Bet handling /5Bets are tallied correctly. Minand max bet are enforcedBets are tallied correctly, butlimits are not enforcedBets are tallied incorrectly Betting is not implemented4 Dealer’s hand /10Dealer’s hand is impementedas a linked list. Memory isdynamically allocated andfreed between game roundsDealer’s hand is implementedas a dynamic list, butmemory is not properlyhandledDealer’s hand is notimplemented as a dynamiclistDealer’s hand is notimplemented5 Player’s hand /10Player’s hand is impementedas a linked list. Memory isdynamically allocated andfreed between game roundsPlayer’s hand is implementedas a dynamic list, butmemory is not properlyhandledPlayer’s hand is notimplemented as a dynamiclistPlayer’s hand is notimplemented6 Game rules /15 All game rules are followed Most game rules are followed Most game rules are notfollowedGame is not functional7 Game Interface /10The interface is inuitive. Theuser is able to play the gamewith minimal isntructions.Transitions from round toround are clearThe interface is intuitive forthe most part. Somedifficulty in understandingthe game navigation.The interface is counterintuitive.Navigation optionsare not clearly stated.Interface limitations preventproper game functionalityThe interface is very basicand does not allowtransitions between gamerounds.Program Design8 Code modularity /10The code is logically dividedto several functions thatimplement importantfunctionality (deck shuffling,dealer hand, player hand,hand tallying, list creation,list deletion, etc.)The code is modular butfurther simplification couldhave been attemptedThe code only has a fewfunctions. Most functionalitiesare integrated within themain functionCode is not modular