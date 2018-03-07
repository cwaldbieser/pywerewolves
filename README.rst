============
PyWerewolves
============

PyWerewolves is a simple, hot-seat, curses based adaption of the party game
of Werewolves (sometimes called Mafia), written in Python.

Players are randomly assinged roles of Villagers or Werewolves.  During the
night, players with certain roles are able to take special actions that
reveal information or change the information in the game.  Three extra cards
are dealt to the table, but no one knows which roles they are.

During the morning, players discuss what happened during the night, but they
are free to bend the truth or outright fib about what they observed.

Then everyone votes to eliminate a player.  If at least one player gets more
than one vote, then the player or players with the most votes are eliminated.
The current roles of each player are revealed, and the players win with the
team their role is affiliated with.

The goal is for villagers is to eliminate at least one werewolf, or if all
the werewolves are on the table, for no one to be eliminated.

The goal for the werewolves is for no werewolf to be eliminated.

Specific roles may have other winning conditions.

-----------
Night Roles
-----------

Certain roles have powers they may use at night.  These powers are always activated
in the same order:

* Werewolf - wins with the werewolves.  During the night, wakes up and sees all
  her fellow werewolves.
* Minion - wins with the werewolves.  Wakes up and can see the werewolves, but
  they cannot see her.  Wins even if eliminated as long as no werewolf players
  are eliminated.  However, if there are no werewolf players (i.e. they are all
  on the table), the minion only wins if a villager other than herself is 
  eliminated.
* Seer - wins with the village.  Can use her powers to reveal cards.
* Robber - wins with the village.  Can steal the role of another player, leaving
  her own role in its place.
* Troublemaker - wins with the village.  Can switch the roles of 2 players.
* Insomniac - wins with the village.  Wakes up and sees if her card changed.

-----------
Other Roles
-----------

* Villager - wins with the village.
* Hunter - wins with the village.  If the hunter is eliminated, the player he
  voted for is also eliminated.
* Tanner - wins only if she is eliminated.  The tanner's job makes her so
  miserable that the sweet kiss of death would be a mercy.  The village can
  win jointly with the Tanner if one or more werewolves are eliminated with the
  Tanner.  The werewolves can never win if the Tanner wins.

----------------
Running the game
----------------

To run the game:

.. code:: shell

    $ ./game.py NUMBER_OF_PLAYERS

For help and command line options:

.. code:: shell

    $ ./game.py -h


