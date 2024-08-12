SELECT city, population
FROM north_american_cities
WHERE country="Canada";
---------------------------
SELECT city
FROM north_american_cities
WHERE country="United States"
ORDER BY latitude DESC;
---------------------------
SELECT city
FROM north_american_cities
WHERE longitude < -87.6298
ORDER BY longitude;
---------------------------
SELECT city
FROM north_american_cities
WHERE country="Mexico"
ORDER BY population DESC
LIMIT 2;
---------------------------
SELECT city
FROM north_american_cities
WHERE country="United States"
ORDER BY population DESC
LIMIT 2 OFFSET 2;
---------------------------
SELECT director, COUNT()
FROM movies
GROUP BY director;
---------------------------
SELECT director, SUM(domestic_sales + international_sales)
FROM boxoffice
LEFT JOIN movies
 on id = movie_id
GROUP BY director;
---------------------------
- White hat hacker has sent SQLPD exposed members' details of a shady site connected to various persons of interest. Please submit all members' details.
SELECT *
FROM members;
---------------------------
- A mailing list of an illegal online service was sent to the SQLPD hot-line. Please submit all entries' details.
SELECT *
FROM mailing_list;
---------------------------
- A hacked site subscribers' details have surfaced on a darknet forum. Please submit all subscribers usernames, mailing addresses and number of comments' details.
SELECT username, mailingAddress, Comments
FROM subscribers;
---------------------------
- A mailing list of an illegal online service was sent to the SQLPD hot-line. Please submit all records number of password changes, surnames and join dates' details.
SELECT PasswordChanges, Surname, Joined
FROM mailing_list;
---------------------------
- A hacked site subscribers' details have surfaced on a darknet forum. Please submit all subscribers mailing addresses' details. Please make sure there are no duplicates.
SELECT DISTINCT MailingAddress
FROM subscribers;
---------------------------
- An illegal site's servers were seized in a recent operation. Please submit all users' details sorted by last access times in ascending order.
SELECT *
FROM users
ORDER BY LastAccess;
---------------------------
- A mailing list of an illegal online service was sent to the SQLPD hot-line. Please submit all records' details sorted by emails in descending order.
SELECT *
FROM mailing_list
ORDER BY Email DESC;
---------------------------
- An illegal site's servers were seized in a recent operation. Please submit all users email addresses and first names' details sorted by first names in descending order. Please make sure there are no duplicates.
SELECT DISTINCT EmailAddress, FirstName
FROM users
ORDER BY FirstName DESC;
---------------------------
- A mailing list of an illegal online service was sent to the SQLPD hot-line. Please submit all entries emails and family names' details sorted by emails in descending order and then by family names in ascending order.
SELECT Email, FamilyName
FROM mailing_list
ORDER BY Email DESC, FamilyName;
---------------------------
- White hat hacker has sent SQLPD exposed subscribers' details of a shady site connected to various persons of interest. Please submit the top 3 subscribers' details when sorted by subscribed since dates in ascending order and then by password hashes in descending order.
SELECT *
FROM subscribers
ORDER BY SubscribedSince, PasswordHash DESC
LIMIT 3;
---------------------------
- An illegal site's servers were seized in a recent operation. Please submit the top 10 users surnames, number of downloads and access times' details when sorted by surnames in descending order and then by access times in ascending order. Please make sure there are no duplicates.
SELECT DISTINCT Surname, NumberOfDownloads, AccessTime
FROM users
ORDER BY Surname DESC, AccessTime
LIMIT 10;
---------------------------
