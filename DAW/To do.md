 ### Board
1. create() - Create Board
	1. Given I use Class Board
	2. When I create a new board
	3. Then I validate that the board has been created
2. haveShip(position: Position) -> BoardShips
3. canPlaceShip(ship: Ship) -> BoardShips
4. placeShip(ship: Ship) -> BoardShips
5. getShip() -> BoardShips
6. allShipsDestroyed() -> BoardShips #DAW-Review 
7. 6. makeShot(position: Position) -> BoardShots
8. haveShot(position: Position) -> BoardShots

## BoardShip
1. create() - Create BoardShip: 
	1. Given I use Class BoardShip
	2. When I "create_a_new_boardShip"
	3. Then I "validate_that_the_boardShip_has_been_created"
2. haveShip(position: Position):
	-  Pre-Conditions:
		- Create new boardShips
		- Place at least on ship on a specific position
	1. Given I use Class BoardShip
	2. When I "request_for_ships_on_empty_position"
	3. Then I "validate_that_the_board_has_no_ships_on_requested_position"
	4. And I "request_for_ships_on_used_position"
	5. Then I "validate_that_the_board_has_one_ship_on_requested_position"
3. canPlaceShip(ship: Ship):
	1.  Validate placeShip by position availability
		-  Pre-Conditions:
			- Create new boardShips
			- Place at least on ship on a specific position
		2. Given I use Class BoardShip
		3. When I "request_to_place_new_ship_on_used_position"
		4. Then I "validate_that_it_is_not_possible_to_place_ship_on_used_position"
		5. When I "request_to_place_new_ship_on_empty_position"
		6. Then I "validate_that_it_is_possible_to_place_ship_on_empty_position"
	2. Validate placeShip by type of ship 
		-  Pre-Conditions:
			- Create new boardShips
		2. Given I use Class BoardShip
		3. When I "request_to_place_new_invalid_type_ship_on_empty_position"
		4. Then I "validate_that_it_is_not_possible_to_place_invalid_type_ship"
		5. When I "request_to_place_duplicateship_on_empty_position"
		6. Then I "validate_that_it_is_not_possible_to_place_duplicate_ship"
4. placeShip(ship: Ship):
	-  Pre-Conditions:
		- Create new boardShips
		- Place at least on ship on a specific position
	1. Given I use Class BoardShip
	2. When I "request_to_place_new_ship_on_empty_position"
	5. Then I "validate_that_it_is_possible_to_place_ship_on_empty_position"
5. getCell(position: Position):
	-  Pre-Conditions:
		- Create new boardShips
		- Place at least on ship on a specific position
	1. Given I use Class BoardShip
	2. When I "request_ship_by_position"
	5. Then I "validate_that_the_respones_is_a_valid_ship"
6. allShipsDestroyed() -> BoardShips #DAW-Review Should be implemented on Board
	- Pre-Conditions:
		- Create new boardShips
		- Create new BoardShots
		- Add every possible ship to the board. 
		- Add shots to this ships until theres only one single shot to do on one ship
	1.  Given I use Class Board
	2. When I "request_BoardShips_if_all_ships_are_destroyed"
	3. Then I "validate_all_ships_are_not_destroyed"
	4. When I "request_BoardShots_to_shot_the_last_ship"
	5. And I "request_BoardShips_if_all_ships_are_destroyed"
	6. Then I "validate_all_ships_are_destroyed"


## BoardShots
1. create() - Create BoardShot:
	1. Given I use Class BoardShot
	2. When I "create_a_new_boardShot"
	3. Then I "validate_that_the_boardShot_has_been_created"
1. makeShot(position: Position):
	1. Validate makeShot by position availability
		-  Pre-Conditions:
			- Create new boardShots
			- Shot at least one cell at a specific position
		2. Given I use Class BoardShot
		3. When I "request_to_shoot_one_cell_empty_position"
		4. Then I "validate_shot_has_been_registered"
	2. Validate makeShot by position out of bounds
		-  Pre-Conditions:
			- Create new boardShots
		2. Given I use Class BoardShot
		3. When I "request_to_shoot_one_cell_out_of_bounds_position"
		4. Then I "validate_shot_has_not_been_registered"
2. haveShot(position: Position) -> BoardShots
	-  Pre-Conditions:
		- Create new boardShots
		- Shot at least one cell at a specific position
	1. Given I use Class BoardShot
	2. When I "request_if_cell_has_been_shooted_empty_position"
	3. Then I "validate_there_is_no_shoot_on_that_position"
	4. When I "request_to_shoot_one_cell_used_position"
	5. And I "request_if_cell_has_been_shooted_used_position"
	6. Then I "validate_there_is_a_shoot_on_that_position"

### GameLogic


## Improvment points:

### Database:
	- Partilha de keys entre tables (current game) em vez da query

### Service:
	- Arquitectura to dominio (Board) 
		- BoardShips 
	- Add information about ship state when its shooted