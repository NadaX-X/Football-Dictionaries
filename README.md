'''Football Dictionaries
This project involves converting a list of football players into dictionaries, and then organizing the players by 
their positions and countries. The goal is to work with complex data structures and practice data manipulation skills.'''
data = {
    "Argentina": {
        "GK": [
            {
                "Number": "1",
                "Position": "GK",
                "Name": "Sergio Romero",
                "Date of Birth": "(1987-02-22)22 February 1987 (aged 37)",
                "Caps": "96",
                "Club": "Manchester United",
                "Club Country": "England",
                "Year": "2023"
            },
            {
                "Number": "12",                 
                "Position": "GK",
                "Name": "Emiliano Martínez",
                "Date of Birth": "(1992-09-02)2 September 1992 (aged 31)",
                "Caps": "26",
                "Club": "Aston Villa",
                "Club Country": "England",
                "Year": "2023"
            }
        ],
        "DF": [
            {
                "Number": "2",
                "Position": "DF",
                "Name": "Nahuel Molina",
                "Date of Birth": "(1998-04-06)6 April 1998 (aged 25)",
                "Caps": "24",
                "Club": "Atlético Madrid",
                "Club Country": "Spain",
                "Year": "2023"
            },
            {
                "Number": "3",
                "Position": "DF",
                "Name": "Nicolás Otamendi",
                "Date of Birth": "(1988-02-12)12 February 1988 (aged 35)",
                "Caps": "75",
                "Club": "Benfica",
                "Club Country": "Portugal",
                "Year": "2023"
            },
            {
                "Number": "13",
                "Position": "DF",
                "Name": "Germán Pezzella",
                "Date of Birth": "(1991-06-27)27 June 1991 (aged 32)",
                "Caps": "29",
                "Club": "Betis",
                "Club Country": "Spain",
                "Year": "2023"
            }
        ],
        "MF": [
            {
                "Number": "5",
                "Position": "MF",
                "Name": "Leandro Paredes",
                "Date of Birth": "(1994-06-29)29 June 1994 (aged 29)",
                "Caps": "44",
                "Club": "Juventus",
                "Club Country": "Italy",
                "Year": "2023"
            },
            {
                "Number": "7",
                "Position": "MF",
                "Name": "Rodrigo De Paul",
                "Date of Birth": "(1994-05-24)24 May 1994 (aged 29)",
                "Caps": "43",
                "Club": "Atlético Madrid",
                "Club Country": "Spain",
                "Year": "2023"
            },
            {
                "Number": "20",
                "Position": "MF",
                "Name": "Alexis Mac Allister",
                "Date of Birth": "(1998-12-24)24 December 1998 (aged 24)",
                "Caps": "15",
                "Club": "Brighton & Hove Albion",
                "Club Country": "England",
                "Year": "2023"
            }
        ],
        "FW": [
            {
                "Number": "10",
                "Position": "FW",
                "Name": "Lionel Messi",
                "Date of Birth": "(1987-06-24)24 June 1987 (aged 36)",
                "Caps": "172",
                "Club": "Paris Saint-Germain",
                "Club Country": "France",
                "Year": "2023"
            },
            {
                "Number": "9",
                "Position": "FW",
                "Name": "Lautaro Martínez",
                "Date of Birth": "(1997-08-22)22 August 1997 (aged 26)",
                "Caps": "40",
                "Club": "Inter Milan",
                "Club Country": "Italy",
                "Year": "2023"
            },
            {
                "Number": "22",
                "Position": "FW",
                "Name": "Julián Álvarez",
                "Date of Birth": "(2000-01-31)31 January 2000 (aged 23)",
                "Caps": "12",
                "Club": "Manchester City",
                "Club Country": "England",
                "Year": "2023"
            }
        ]
    },
    "Brazil": {
        "GK": [{
            "Number": "1",
            "Position": "GK",
            "Name": "Alisson",
            "Date of Birth": "(1992-10-02)2 October 1992 (aged 30)",
            "Caps": "55",
            "Club": "Liverpool",
            "Club Country": "England",
            "Year": "2023"
        },
        {
            "Number": "12",
            "Position": "GK",
            "Name": "Edouard Mendy",
            "Date of Birth": "(1992-03-01)1 March 1992 (aged 31)",
            "Caps": "16",
            "Club": "Chelsea",
            "Club Country": "England",
            "Year": "2023"
        }
    ],
    "DF": [
        {
            "Number": "2",
            "Position": "DF",
            "Name": "Dani Alves",
            "Date of Birth": "(1983-05-06)6 May 1983 (aged 40)",
            "Caps": "125",
            "Club": "Pumas UNAM",
            "Club Country": "Mexico",
            "Year": "2023"
        },
        {
            "Number": "4",
            "Position": "DF",
            "Name": "Marquinhos",
            "Date of Birth": "(1994-05-14)14 May 1994 (aged 29)",
            "Caps": "68",
            "Club": "Paris Saint-Germain",
            "Club Country": "France",
            "Year": "2023"
        },
        {
            "Number": "3",
            "Position": "DF",
            "Name": "Thiago Silva",
            "Date of Birth": "(1984-09-22)22 September 1984 (aged 38)",
            "Caps": "109",
            "Club": "Chelsea",
            "Club Country": "England",
            "Year": "2023"
        }
    ],
    "MF": [
        {
            "Number": "5",
            "Position": "MF",
            "Name": "Casemiro",
            "Date of Birth": "(1992-02-23)23 February 1992 (aged 31)",
            "Caps": "63",
            "Club": "Manchester United",
            "Club Country": "England",
            "Year": "2023"
        },
        {
            "Number": "8",
            "Position": "MF",
            "Name": "Fred",
            "Date of Birth": "(1993-03-05)5 March 1993 (aged 30)",
            "Caps": "28",
            "Club": "Manchester United",
            "Club Country": "England",
            "Year": "2023"
        },
        {
            "Number": "10",
            "Position": "MF",
            "Name": "Neymar",
            "Date of Birth": "(1992-02-05)5 February 1992 (aged 31)",
            "Caps": "124",
            "Club": "Paris Saint-Germain",
            "Club Country": "France",
            "Year": "2023"
        }
    ],
    "FW": [
        {
            "Number": "9",
            "Position": "FW",
            "Name": "Richarlison",
            "Date of Birth": "(1997-05-10)10 May 1997 (aged 26)",
            "Caps": "39",
            "Club": "Tottenham Hotspur",
            "Club Country": "England",
            "Year": "2023"
        },
        {
            "Number": "20",
            "Position": "FW",
            "Name": "Vinicius Junior",
            "Date of Birth": "(2000-07-12)12 July 2000 (aged 23)",
            "Caps": "22",
            "Club": "Real Madrid",
            "Club Country": "Spain",
            "Year": "2023"
        },
        {
            "Number": "7",
            "Position": "FW",
            "Name": "Raphinha",
            "Date of Birth": "(1996-12-14)14 December 1996 (aged 26)",
            "Caps": "17",
            "Club": "Barcelona",
            "Club Country": "Spain",
            "Year": "2023"
        }
    ]
}
}

for i in data['Argentina']['GK']:
  print(i)
