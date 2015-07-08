# Blackjack

## Description
Blackjack C# console game


## Objectives

### Learning Objectives

After completing this assignment, you should…

* Use control-flow (having the computer make decisions)
* Create a user interface
* Use data-flow (your deck is a unique set of resources)


### Performance Objectives

After completing this assignment, you be able to effectively use

* Classes
* Arrays
* Console / Terminal




## Details

Code you may want
-----------------

```c#

#... snip
  public enum Suit
        {
            Hearts,
            Clubs,
            Diamonds,
            Spades            
        }

        public enum Rank
        {
            Ace,
            Deuce,
            Three,
            ....
            Queen,
            King
        }
        
        foreach (Rank r in Enum.GetValues(typeof(Rank)))
        {
            foreach (Suit s in Enum.GetValues(typeof(Suit)))
            {
                deck.Add(new Card(s, r));
            }
        }

        //sort the deck. NOTICE that the variable 'deck' is unchanged, but 'randomDeck' is the actual sorted deck.
        var randomDeck = deck.OrderBy(x => Guid.NewGuid()).ToList();

```

### Deliverables

* A gist containing at least:
  * `BlackJack.cs` : your game class
  * `Card.cs` : your Card class
  * `Deck.cs` : your Deck class

To submit your assignment:

* Create a gist, with 1 file per class
* Submit a link to it to this gist as a GitHub Issue here

### Requirements

* You should create classes for your data, and use methods instead of having one big loop


## Normal Mode

0. don't consider Aces as possible 1's ... they are always 11s
0. This is a 2 hand game (dealer and player)
0. no splitting or funny business
0. 1 deck in the game
0. 52 card deck
0. NO WILDS
0. New deck every game
0. deck must be shuffled every game
0. no betting at all
0. must have suits (ace of diamonds)
0. Dealer hits if less than 16, otherwise dealer stays
0. You enter what you play
0. No if you get 5 cards you win funnybusiness
0. get as close to 21 without going over
0. Must beat the dealer
0. you can see 1 of dealers cards, while you are playing
0. If you get blackjack, you win automagically

            
## Hard Mode

1. You win if you have 6 cards and stay under 21
1. Dealer wins blackjack before any player actions

## Nightmare Mode

1. Add the idea of tracking your progress as you play over time.
1. Let the player choose if an Ace is a 1 or an 11
1. Add 7 decks to the game in a "Show", shuffle them all together, deal from the "Shoe"
            


## Notes

This can be fairly challenging, and is the end of our adventure in pure c#
programming.

## Additional Resources

* [Play Blackjack](http://freeblackjackdoc.com/blackjack-game.htm)  
* [Info on Blackjack](https://en.wikipedia.org/wiki/Blackjack)
