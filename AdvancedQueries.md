>Get all head coach first names, the city where they are located, and their role. Sort the result by first name in ascending order.

SELECT coaches.first_name, teams.city, coaches.role FROM coaches
INNER JOIN teams
ON coaches.team_id = teams.id
ORDER BY coaches.first_name ASC;

>Get all fans named John who support the slammers team (the team name is slammers) and whose id is greater than 100.

SELECT fans.name FROM fans
INNER JOIN teams
ON fans.team_id = teams.fan_id
WHERE fans.name = 'John' AND team.name = slammers AND fans.id > 100

>Display all players first names, last names, and positions who play in Chicago and sort the result by position in descending order.

SELECT players.first_name, players.last_name, players.position FROM players
INNER JOIN teams
ON players.team_id = teams.id
WHERE teams.city = 'chicago'
ORDER BY players.position_name DESC;
