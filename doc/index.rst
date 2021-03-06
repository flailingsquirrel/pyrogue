Contents:
=========

.. toctree::
   :maxdepth: 4

   modules 

Overview
========

This is the pyrogue python-based roguelike game.  It is an 
excellent starting place for learing to code roguelikes.

Quick Grok
==========

- :class:`~pyrogue.pyro.Pyro` has a :class:`~pyrogue.pyro.Game`
- :class:`~pyrogue.pyro.Game` has a 
    - :class:`~pyrogue.player.PlayerCharacter`
    - :class:`~pyrogue.dungeons.Dungeon`
    - :class:`~pyrogue.dungeons.Level`
- Creatures:
    - Inherit off :class:`~pyrogue.creatures.Creature`
    - Have an :class:`~pyrogue.creatures.AI` to guide them
    - Are placed in game by :attr:`~pyrogue.dungeons.Level.AddCreature`
    - Have an :class:`~pyrogue.creatures.Iventory` 
    - Use Astar to calculate paths: :class:`~pyrogue.astar.path` 
- Player Character:
    - Drives game play in method :attr:`~pyrogue.player.PlayerCharacter.Update`
- Dungeon Level: :class:`~pyrogue.dungeons.Level`
    - Has a map stored in :attr:`~pyrogue.dungeons.Level.layout`
    - Stores data with (x,y) keys
        - Has list of items :attr:`~pyrogue.dungeons.Level.items`
        - Has list of creatures :attr:`~pyrogue.dungeons.Level.creatures`
        - Has list of creatures :attr:`~pyrogue.dungeons.Level.mobs` 
    - Calculates field of view with :class:`~pyrogue.fov.FOVMap`
    - Dungeon maps generated in :class:`~pyrogue.dungeon_gen.Level` 

Level Drawing
=============

- Player Update method calls drawing method :attr:`~pyrogue.player.PlayerCharacter.Update`
- Calls self.current_level.Display :attr:`~pyrogue.dungeons.Level.Display`


Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
