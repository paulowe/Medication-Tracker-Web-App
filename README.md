# Medication Tracker Web App

This is used so users can login and know when they need to take their medication.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### PHP Config File

Replace the lines below in the [config](https://github.com/ChrisLubin/Medication-Tracker-Web-App/tree/master/App/php/config.php) file with your credentials.

```php
$dbname = ''; // FAU username
$dbuser = ''; // FAU username
$dbpass = ''; // FAU LAMP password
```

### SQL Statements

Run the following SQL statements before using the application.

```sql
CREATE TABLE Users (email varchar(40) NOT NULL, password varchar(60), firstName varchar(20), lastName varchar(20), phone int(15), isDoc bool, PRIMARY KEY(email));
CREATE TABLE Calendar (id varchar(36) NOT NULL, email varchar(40), start int(15), duration int(2), title varchar(40), content varchar(40), category varchar(20), PRIMARY KEY(id), FOREIGN KEY(email) REFERENCES Users(email));
CREATE TABLE Prescription (prescription varchar(40), instruction varchar(255), dosage varchar(20), patient varchar(40), patientFname varchar(40), patientLname varchar(40), doctor varchar(40), doctorLname varchar(40), FOREIGN KEY (patient) REFERENCES Users(email), FOREIGN KEY (patientFname) REFERENCES Users(firstName), FOREIGN KEY (patientLname) REFERENCES Users(lastName), FOREIGN KEY (doctor) REFERENCES Users(email), FOREIGN KEY (doctorLname) REFERENCES Users(lastName), PRIMARY KEY (prescription, patient, doctor));
```

## Screenshots

<table>
    <tr>
        <td>
            <img alt="Screenshot 1" src="App/images/Demo/screenshot1.png">
        </td>
        <td>
            <img alt="Screenshot 2" src="App/images/Demo/screenshot2.png">
        </td>
        <td>
            <img alt="Screenshot 3" src="App/images/Demo/screenshot3.png">
        </td>
    </tr>
    <tr>
        <td>
            <img alt="Screenshot 4" src="App/images/Demo/screenshot4.png">
        </td>
        <td>
            <img alt="Screenshot 5" src="App/images/Demo/screenshot5.png">
        </td>
        <td>
            <img alt="Screenshot 6" src="App/images/Demo/screenshot6.png">
        </td>
    </tr>
    <tr>
        <td>
            <img alt="Screenshot 7" src="App/images/Demo/screenshot7.png">
        </td>
        <td>
            <img alt="Screenshot 8" src="App/images/Demo/screenshot8.png">
        </td>
        <td>
            <img alt="Screenshot 9" src="App/images/Demo/screenshot9.png">
        </td>
        </td>
    </tr>
    <tr>
        <td>
            <img alt="Screenshot 10" src="App/images/Demo/screenshot10.png">
        </td>
        <td>
            <img alt="Screenshot 11" src="App/images/Demo/screenshot11.png">
        </td>
    </tr>
</table>

## Authors

- **Alexander Alonso** - _Front End_ - [AlexXXV](https://github.com/AlexXXV)
- **Christopher Lubin** - _Front End/Back End_ - [ChrisLubin](https://github.com/ChrisLubin)
- **Dylan Taylor** - _Back End_ - [coldshock](https://github.com/coldshock)
- **Jordan Morant** - _Front End_ - [jmorant2016](https://github.com/jmorant2016)
- **Kelsey Joseph** - _Front End_ - [KelJ27](https://github.com/KelJ27)
- **Natacha Barcala** - _Front End_ - [nabarcala](https://github.com/nabarcala)

## Special Thanks

Special thanks to [ArrobeFr](https://github.com/ArrobeFr) for providing the source code for the calendar.

## License

This project is licensed under the MIT License - see the [LICENSE.md](https://github.com/ChrisLubin/Medication-Tracker-Web-App/blob/master/LICENSE) file for details.