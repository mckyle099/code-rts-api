Code.RTS() API Reference
========================

| **Code.RTS()** is a video game that uses a Python API that players must use to play the game.
| Visit `www.code-rts.com <https://www.code-rts.com>`_ for news, manual, and download.

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

.. py:function:: repairBuilding(position, amount)

   Repairs building at specified position. Costs 1 wood per HP.

   :param position: A value between 1 and 9 that specifies the position of the building to repair.
   :type position: int
   :param amount: A integer value for how much HP to repair.
   :type amount: int
   :return: True on success, False on failure.
   :rtype: bool
   :Wood: -amount
   :Health: +amount

.. py:function:: destroyBuilding(position)

   Destroys building at specified position.

   :param position: A value between 1 and 9 that specifies the position of the building to destroy.
   :type position: int
   :return: True on success, False on failure.
   :rtype: bool

Units
-----
.. py:function:: createArcher()

   Creates an Archer. Archers are ranged units that will attack your enemies.

   :return: True on success, False on failure.
   :rtype: bool
   :Population: -1
   :Wood: -2
   :Health: 100
   :Damage: 10
   :Range: 10
   :Attack Speed: 1
   :Movement Speed: 5

.. py:function:: createSpearman()

   Creates a Spearman. Spearmen are melee units that will attack your enemies.

   :return: True on success, False on failure.
   :rtype: bool
   :Population: -1
   :Wood: -2
   :Health: 100
   :Damage: 10
   :Range: 1
   :Attack Speed: 2
   :Movement Speed: 10

Intel
-----
.. py:function:: getCurrentPopulation()

   Gets your current Population value.

   :return: How much Population you currently have.
   :rtype: int

.. py:function:: getMaxPopulation()

   Gets your Maximum Population capacity value.

   :return: How much Maximum Population capacity you currently have.
   :rtype: int

.. py:function:: getCurrentWood()

   Gets your current Population value.

   :return: How much Population you currently have.
   :rtype: int

.. py:function:: getMaxWood()

   Gets your Maximum Wood capacity value.

   :return: How much Maximum Wood capacity you currently have.
   :rtype: int

.. py:function:: getCurrentGold()

   Gets your current Gold value.

   :return: How much Gold you currently have.
   :rtype: int

.. py:function:: getBuildingCurrentHealth(position)

   Gets the Health of the Building at the specified position.

   :param position: A value between 1 and 9 that specifies the position of the building to get current health of.
   :type position: int
   :return: How much health the building currently has.
   :rtype: int

.. py:function:: getBuildingMaxtHealth(position)

   Gets the Maximum Health of the Building at the specified position.

   :param position: A value between 1 and 9 that specifies the position of the building to get maximum health of.
   :type position: int
   :return: How much maximum health the building has.
   :rtype: int

Trading
-------
.. py:function:: buyPopulation(amount)

   Buy Population for Gold.

   :param amount: How much Population you want to buy.
   :type amount: int
   :return: True if the trade succeeded, False otherwise.
   :rtype: bool
   :Requirement: Market
   :Population: 1 * amount
   :Gold: -11 * amount

.. py:function:: sellPopulation(amount)

   Sell Population for Gold.

   :param amount: How much Population you want to sell.
   :type amount: int
   :return: True if the trade succeeded, False otherwise.
   :rtype: bool
   :Requirement: Market
   :Population: -1 * amount
   :Gold: 9 * amount

.. py:function:: buyWood(amount)

   Buy Wood for Gold.

   :param amount: How much Wood you want to buy. Must be a multiple of 10. 10 Wood costs 11 Gold.
   :type amount: int
   :return: True if the trade succeeded, False otherwise.
   :rtype: bool
   :Requirement: Market
   :Wood: 10 * amount
   :Gold: -11 * amount

.. py:function:: sellWood(amount)

   Sell Wood for Gold.

   :param amount: How much Wood you want to sell. Must be a multiple of 10.
   :type amount: int
   :return: True if the trade succeeded, False otherwise.
   :rtype: bool
   :Requirement: Market
   :Wood: -10 * amount
   :Gold: 9 * amount
