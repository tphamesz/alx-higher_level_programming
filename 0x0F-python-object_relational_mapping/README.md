Python - Object-relational mapping

In this project, I learned about how object-relational mapping is used for database scripting. I became familiar with using MySQLdb and SQLAlchemy to query, create, edit, and delete tables in MySQL.

Tasks 📃

Get all states
0-select_states.py: Python script that uses MySQLdb to list all states in the database hbtn_0e_0_usa.

Usage: ./0-select_states.py .

Results are ordered by ascending states.id.

Filter states
1-filter_states.py: Python script that uses MySQLdb to list all states with names starting with N in the database hbtn_0e_0_usa.

Usage: ./1-filter_states.py .

Results are ordered by ascending states.id.

Filter states by user input
2-my_filter_states.py: Python script that uses MySQLdb to display all values matching a given name in the states table of the database hbtn_0e_0_usa.

Usage: ./2-my_filter_states.py .

Results are ordered by ascending states.id.

Uses string formatting to construct the SQL query.

SQL Injection...
3-my_safe_filter_states.py: Python script that uses MySQLdb to display all values matching a given name in the states table of the database hbtn_0e_0_usa.

Usage: ./3-my_safe_filter_states.py .

Results are ordered by ascending states.id.

Safe from SQL injections.

Cities by states
4-cities_by_state.py: Python script that uses MySQLdb to list all cities from the database hbtn_0e_4_usa.

Usage: ./4-cities_by_state.py .

Results are ordered by ascending cities.id.

All cities by state
5-filter_cities.py: Python script that uses MySQLdb to list all cities of a given state in the database hbtn_0e_4_usa.

Usage: ./5-filter_cities.py .

Results are sorted by ascending cities.id.

First state model
model_state.py: Python module defining a class State that inherits from SQLAlchemy Base and links to the MySQL table states.

All states via SQLAlchemy
7-model_state_fetch_all.py: Python script that uses SQLAlchemy to list all State objects from the database hbtn_0e_6_usa.

Usage: ./7-model_state_fetch_all.py .

Results are sorted by ascending states.id.

First state
8-model_state_fetch_first.py: Python script that uses SQLAlchemy to print the first State object from the database hbtn_0e_6_usa, ordered by states.id.

Usage: ./8-model_state_fetch_first.py .

If the states table is empty, prints Nothing.

Contains a
9-model_state_filter_a.py: Python script that uses SQLAlchemy to list all State objects that contain the letter a in the database hbtn_0e_6_usa.

Usage: ./9-model_state_filter_a.py .

Results are ordered by ascending states.id.

Get a state
10-model_state_my_get.py: Python script that uses SQLAlchemy to print the id of the State object with name matching that passed as argument in the database hbtn_0e_6_usa.

Usage: ./10-model_state_my_get.py .

Displays the id of the matched State.

If no match is found, prints Not found.

Add a new state
11-model_state_insert.py: Python script that uses SQLAlchemy to add the State object "Louisiana" to the database hbtn_0e_6_usa.

Usage: ./11-model_state_insert.py .

Prints the id of the new State after creation.

Update a state
12-model_state_update_id_2.py: Python script that uses SQLAlchemy to change the name of the State object with id = 2 in the database hbtn_0e_6_usa to "New Mexico".

Usage: ./12-model_state_update_id_2.py .

Delete states
13-model_state_delete_a.py: Python script that uses SQLAlchemy to delete all State objects with a name containing the letter a from the database hbtn_0e_6_usa.

Usage: ./13-model_state_delete_a.py .

Cities in state
model_city.py: Python module defining a class City that inherits from SQLAlchemy Base and links to the MySQL table cities.

Includes class attribute state_id that is a foreign key to states.id.

14-model_city_fetch_by_state.py: Python script that uses SQLAlchemy to list all City objects in the database hbtn_0e_14_usa.

Usage: ./14-model_city_fetch_by_state.py .

Results are sorted by ascending cities.id.

City relationship
relationship_state.py: Python module defining a class State that inherits from SQLAlchemy Base and links to the MySQL table states.

Identical to the State class defined in model_state.py.

Includes class attribute classes that represents a relationship with the class City. If the State object is deleted, all linked City objects are also deleted. State objects are backreferenced to City objects as state.

relationship_city.py: Python module defining a class City that inherits from SQLAlchemy Base and links to the MySQL table cities.

Identical to the City class defined in model_city.py.

100-relationship_states_cities.py: Python script that uses SQLAlchemy to add the State "California" with City "San Francisco" to the database hbtn_0e_100_usa.

Usage: ./100-relationship_states_cities.py .

Uses the cities relationship for all State objects.

List relationship
101-relationship_states_cities_list.py: Python script that uses SQLAlchemy to list all State and corresponding City objects in the database hbtn_0e_101_usa.

Usage: ./101-relationship_states_cities_list.py .

Uses the cities relationship for all State objects.

Results are sorted by ascending states.id and cities.id.

List city
102-relationship_cities_states_list.py: Python script that uses SQLAlchemy to list all City objects from the database hbtn_0e_101_usa.

Usage: ./102-relationship_cities_states_list.py .

Uses the state relationship to access the State objects linked to City objects.

Results are sorted by ascending cities.id.
