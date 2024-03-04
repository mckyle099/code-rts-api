Code.RTS() API Reference
========================

**Code.RTS()** is a video game that uses a Python API that players must use to play the game.

Buildings
---------
.. py:function:: buildCamp(position)

   Builds a Camp at specified position. Camps generate population and provide additional population capacity.

   :param position: A value between 1 and 9 that specifies the position to build the building.
   :type position: int
   :return: True on success, False on failure.
   :rtype: bool
   :Population: -5
   :Population Production: 1
   :Population Capacity: 5
   :Health: 10000

.. py:function:: buildLumberCamp(position)

   Builds a Lumber Camp at specified position. Lumber Camps generate wood and provide additional wood capacity.

   :param position: A value between 1 and 9 that specifies the position to build the building.
   :type position: int
   :return: True on success, False on failure.
   :rtype: bool
   :Population: -5
   :Wood Production: 10
   :Wood Capacity: 500
   :Health: 10000

.. py:function:: buildMarket(position)

   Builds a Market at specified position. Markets enable trading (buyPopulation, sellPopulation, buyWood, sellWood).

   :param position: A value between 1 and 9 that specifies the position to build the building.
   :type position: int
   :return: True on success, False on failure.
   :rtype: bool
   :Population: -5
   :Wood: -400
   :Health: 10000
   :Enables: buyPopulation, sellPopulation, buyWood, sellWood

.. py:function:: buildTower(position)

   Builds a Tower at specified position. Towers are defensive buildings that will attack enemies.

   :param position: A value between 1 and 9 that specifies the position to build the building.
   :type position: int
   :return: True on success, False on failure.
   :rtype: bool
   :Population: -5
   :Wood: -400
   :Health: 10000
   :Damage: 10
   :Range: 20
   :Attack Speed: 1

Units
-----
.. py:function:: createArcher()

   Creates an Archer unit. Archers are ranged units that will attack your enemies.

   :return: True on success, False on failure.
   :rtype: bool
   :Population: -1
   :Wood: -2
   :Health: 100
   :Damage: 10
   :Range: 10
   :Attack Speed: 1
   :Movement Speed: 5

Intel
-----
.. py:function:: getCurrentPopulation()

   Gets your current Population value.

   :return: How much Population you currently have.
   :rtype: int

.. py:function:: getPopulationCapacity()

   Gets your Population Capacity value.

   :return: How much Population Capacity you currently have.
   :rtype: int


Trading
-------
.. py:function:: buyPopulation(amount)

   Gets your Population Capacity value.

   :param amount: How much population you want to buy. Each Population costs 11 Gold.
   :type amount: int
   :return: True if the trade succeeded, False otherwise.
   :rtype: bool
   :Requirement: Market
