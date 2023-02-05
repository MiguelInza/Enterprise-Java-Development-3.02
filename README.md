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
