# Enterprise-Java-Development-3.02

	author	title	word count	views
	Maria Charlotte	Best Paint Colors	814	14
	Juan Perez	Small Space Decorating Tips	1146	221
	Maria Charlotte	Hot Accessories	986	105
	Maria Charlotte	Mixing Textures	765	22
	Juan Perez	Kitchen Refresh	1242	307
	Maria Charlotte	Homemade Art Hacks	1002	193
	Gemma Alcocer	Refinishing Wood Floors	1571	7542
				
				
id	author	title	word count	views
1	Maria Charlotte	Best Paint Colors	814	14
2	Juan Perez	Small Space Decorating Tips	1146	221
3	Maria Charlotte	Hot Accessories	986	105
4	Maria Charlotte	Mixing Textures	765	22
5	Juan Perez	Kitchen Refresh	1242	307
6	Maria Charlotte	Homemade Art Hacks	1002	193
7	Gemma Alcocer	Refinishing Wood Floors	1571	7542![image](https://user-images.githubusercontent.com/64167338/216847164-1758e19a-1e88-44c3-bc9c-00b5cb47eca9.png)

CREATE TABLE blog (
    id INT NOT NULL AUTO_INCREMENT,
    author VARCHAR(255),
    title VARCHAR(255),
    word_count INT,
    views INT,
    PRIMARY KEY(id)
);

INSERT INTO blog (author, title, word_count, views) VALUES
("Maria Charlotte", "Best Paint Colors", 814, 14),
("Juan Perez", "Small Space Decorating Tips", 1146, 221),
("Maria Charlotte", "Hot Accessories", 986, 105),
("Maria Charlotte", "Mixing Textures", 765, 22),
("Juan Perez", "Kitchen Refresh", 1242, 307),
("Maria Charlotte", "Homemade Art Hacks", 1002, 193),
("Gemma Alcocer", "Refinishing Wood Floors", 1571, 7542)![image](https://user-images.githubusercontent.com/64167338/216847176-0e57392b-9f4b-489c-b20d-42ce31c3a6dc.png)



	Customer Name	Customer Status	Flight Number	Aircraft	Total Aircraft Seats	Flight Mileage	Total Customer Mileage					
	Agustine Riviera	Silver	DL143	Boeing 747	400	135	115235					
	Agustine Riviera	Silver	DL122	Airbus A330	236	4370	115235					
	Alaina Sepulvida	None	DL122	Airbus A330	236	4370	6008					
	Agustine Riviera	Silver	DL143	Boeing 747	400	135	115235					
	Tom Jones	Gold	DL122	Airbus A330	236	4370	205767					
	Tom Jones	Gold	DL53	Boeing 777	264	2078	205767					
	Agustine Riviera	Silver	DL143	Boeing 747	400	135	115235					
	Sam Rio	None	DL143	Boeing 747	400	135	2653					
	Agustine Riviera	Silver	DL143	Boeing 747	400	135	115235					
	Tom Jones	Gold	DL222	Boeing 777	264	1765	205767					
	Jessica James	Silver	DL143	Boeing 747	400	135	127656					
	Sam Rio	None	DL143	Boeing 747	400	135	2653					
	Ana Janco	Silver	DL222	Boeing 777	264	1765	136773					
	Jennifer Cortez	Gold	DL222	Boeing 777	264	1765	300582					
	Jessica James	Silver	DL122	Airbus A330	236	4370	127656					
	Sam Rio	None	DL37	Boeing 747	400	531	2653					
	Christian Janco	Silver	DL222	Boeing 777	264	1765	14642					
												
												
id	Customer Name	Customer Status	Flight Number	Aircraft	Total Aircraft Seats	Flight Mileage	Total Customer Mileage					
1	Agustine Riviera	Silver	DL143	Boeing 747	400	135	115235					
2	Agustine Riviera	Silver	DL122	Airbus A330	236	4370	115235					
3	Alaina Sepulvida	None	DL122	Airbus A330	236	4370	6008					
4	Tom Jones	Gold	DL122	Airbus A330	236	4370	205767					
5	Tom Jones	Gold	DL53	Boeing 777	264	2078	205767					
6	Sam Rio	None	DL143	Boeing 747	400	135	2653					
7	Tom Jones	Gold	DL222	Boeing 777	264	1765	205767					
8	Jessica James	Silver	DL143	Boeing 747	400	135	127656					
9	Ana Janco	Silver	DL222	Boeing 777	264	1765	136773					
10	Jennifer Cortez	Gold	DL222	Boeing 777	264	1765	300582					
11	Jessica James	Silver	DL122	Airbus A330	236	4370	127656					
12	Sam Rio	None	DL37	Boeing 747	400	531	2653					
13	Christian Janco	Silver	DL222	Boeing 777	264	1765	14642					
												
Customers					Flights					Planes		
id	Customer Name	Customer Status	Total Customer Mileage		id	Flight Number	Flight Mileage	Planes id		id	Aircraft	Total Aircraft Seats
1	Agustine Riviera	Silver	115235		1	DL143	135	1		1	Boeing 747	400
2	Alaina Sepulvida	None	6008		2	DL122	4370	2		2	Airbus A330	236
3	Tom Jones	Gold	205767		3	DL53	2078	3		3	Boeing 777	264
4	Sam Rio	None	2653		4	DL222	1765	3		Primary Key		
5	Jessica James	Silver	127656		5	DL37	531	1				
6	Ana Janco	Silver	136773		Primary Key			Foreign Key				
7	Jennifer Cortez	Gold	300582									
8	Christian Janco	Silver	14642									
Primary Key												
												
Summary												
id	Customers id	Flights id										
1	1	1										
2	1	2										
3	2	2										
4	3	2										
5	3	3										
6	3	4										
7	4	1										
8	4	5										
9	5	1										
10	5	2										
11	6	4										
12	7	4										
13	8	4										
Primary Key												![image](https://user-images.githubusercontent.com/64167338/216847195-cc12d95d-2a40-408f-96df-e98c2bf2fffd.png)



-- listar todos los usuarios --
SELECT user, host FROM mysql.user;
-- eliminar usuario en localhost --
DROP USER 'ironhacker'@'localhost';
-- crear usuario en localhost --
CREATE USER 'ironhacker'@'localhost' IDENTIFIED BY '123456';
DROP USER 'ironhacker'@'localhost';
CREATE USER 'ironhacker'@'localhost' IDENTIFIED BY 'Ir0nh4ck3r!';
GRANT ALL PRIVILEGES ON demo.* TO 'ironhacker'@'localhost';
GRANT ALL PRIVILEGES ON demo_test.* TO 'ironhacker'@'localhost';
GRANT ALL PRIVILEGES ON airline.* TO 'ironhacker'@'localhost';




DROP SCHEMA IF EXISTS airline;
CREATE SCHEMA airline;
USE airline;

DROP TABLE IF EXISTS customer;
CREATE TABLE customer (
id INT NOT NULL AUTO_INCREMENT,
    name VARCHAR(60),
    status ENUM('None', 'Silver', 'Gold'),
    mileage INT,
    PRIMARY KEY (id)
);

DROP TABLE IF EXISTS aircraft
CREATE TABLE aircraft (
model VARCHAR(60),
    seats INT,
PRIMARY KEY (model)
);

DROP TABLE IF EXISTS flight_info;
CREATE TABLE flight_info (
flight_number VARCHAR(5),
    mileage INT,
    PRIMARY KEY (flight_number)
);

DROP TABLE IF EXISTS flight;
CREATE TABLE flight (
id INT NOT NULL AUTO_INCREMENT,
customer_id INT NOT NULL,
    aircraft_model VARCHAR(60),
    flight_info_number VARCHAR(5),
    PRIMARY KEY (id),
FOREIGN KEY (customer_id) REFERENCES customer(id),
    FOREIGN KEY (aircraft_model) REFERENCES aircraft(model),
    FOREIGN KEY (flight_info_number) REFERENCES flight_info(flight_number)
);


INSERT INTO customer (name, status, mileage) VALUES
('Agustine Riviera', 'Silver', 115235),
('Alaina Sepulvida', 'None', 6008),
('Tom Jones', 'Gold', 205767),
('Sam Rio', 'None', 2653),
('Jessica James', 'Silver', 127656),
('Ana Janco', 'Silver', 136773),
('Jennifer Cortez', 'Gold', 300582),
('Christian Janco', 'Silver', 14642);

INSERT INTO aircraft (model, seats) VALUES
('Boeing747', 400),
('AirbusA330', 236),
('Boeing777', 264);

INSERT INTO flight_info (flight_number, mileage) VALUES
('DL143', 135),
('DL122', 4370),
('DL53', 2078),
('DL222', 1765),
('DL37', 531);

INSERT INTO flight (customer_id, aircraft_model, flight_info_number) VALUES
(1,'Boeing747','DL143'),
(1,'AirbusA330','DL122'),
(2,'AirbusA330','DL122'),
(3,'AirbusA330','DL122'),
(3,'Boeing777','DL53'),
(4,'Boeing747','DL143'),
(3,'Boeing777','DL222'),
(5,'Boeing747','DL143'),
(6,'Boeing777','DL222'),
(7,'Boeing777','DL222'),
(5,'AirbusA330','DL122'),
(4,'Boeing747','DL37'),
(8,'Boeing777','DL222');


SELECT aircraft_model, COUNT(aircraft_model) AS aircraft_recurrence
FROM flight f
JOIN customer c ON f.customer_id = c.id
WHERE c.status = 'Gold'
GROUP BY aircraft_model
ORDER BY aircraft_recurrence DESC
LIMIT 1;![image](https://user-images.githubusercontent.com/64167338/216847369-7128f774-8822-4435-8901-19e7a7b882c1.png)

