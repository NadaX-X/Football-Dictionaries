SQUADS_DATA = [ 
 [ 
 "5", 
 "DF", 
 "Marquinhos", 
 "(1994-05-14)14 May 1994 (aged 29)", 
 "68", 
 "Paris Saint-Germain", 
 "Brazil", 
 "France", 
 "2013" 
 ], 
 [ 
 "7", 
 "FW", 
 "Neymar", 
 "(1992-02-05)5 February 1992 (aged 31)", 
 "121", 
 "Paris Saint-Germain", 
 "Brazil", 
 "France", 
 "2010" 
 ], 
 [ 
 "8", 
 "MF", 
 "Arthur Melo", 
 "(1996-08-12)12 August 1996 (aged 27)", 
 "22", 
 "Juventus", 
 "Brazil", 
 "Italy", 
 "2018" 
 ], 
 [ 
 "9", 
 "FW", 
 "Gabriel Jesus", 
 "(1997-04-03)3 April 1997 (aged 26)", 
 "56", 
 "Arsenal", 
 "Brazil", 
 "England", 
 "2016" 
 ], 
 [ 
 "16", 
 "FW", 
 "Lionel Messi", 
 "(1987-06-24)24 June 1987 (aged 36)", 
 "173", 
 "Paris Saint-Germain", 
 "Argentina", 
 "France", 
 "2004" 
 ], 
 [ 
 "21", 
 "DF", 
 "Thiago Silva", 
 "(1984-09-22)22 September 1984 (aged 38)", 
 "108", 
 "Chelsea", 
 "Brazil", 
 "England", 
 "2008" 
 ], 
 [ 
 "22", 
 "MF", 
 "Casemiro", 
 "(1992-02-23)23 February 1992 (aged 31)", 
 "63", 
 "Manchester United", 
 "Brazil", 
 "England", 
 "2011" 
 ], 
 [ 
 "23", 
 "FW", 
 "VinÃcius JÃºnior", 
 "(2000-07-12)12 July 2000 (aged 23)", 
 "26", 
 "Real Madrid", 
 "Brazil", 
 "Spain", 
 "2018" 
 ], 
 [ 
 "24", 
 "DF", 
 "Ãder MilitÃ£o", 
 "(1998-01-18)18 January 1998 (aged 25)", 
 "30", 
 "Real Madrid", 
 "Brazil", 
 "Spain", 
 "2019" 
 ], 
 [ 
 "26", 
 "FW", 
 "Richarlison", 
 "(1997-05-10)10 May 1997 (aged 26)", 
 "40", 
 "Tottenham Hotspur", 
 "Brazil", 
 "England", 
 "2018" 
 ], 
 [ 
 "1", 
 "GK", 
 "Juan Botasso", 
 "(1908-10-23)23 October 1908 (aged 21)", 
 "", 
 "Quilmes", 
 "Argentina", 
 "Argentina", 
 "1930" 
 ], 
 [ 
 "9", 
 "FW", 
 "Roberto Cherro", 
 "(1907-02-23)23 February 1907 (aged 23)", 
 "", 
 "Boca Juniors", 
 "Argentina", 
 "Argentina", 
 "1930" 
 ] 
]
def meth(SQUADS_DATA): 
    player_list = [] # for storing player data 
    for player_data in SQUADS_DATA: # walk through the players in the list 
        player = { # create a dictionary for each player 
            "Number": player_data[0], # first index 
            "Position": player_data[1], 
            "Name": player_data[2], 
            "Date of Birth": player_data[3], 
            "Caps": player_data[4], 
            "Club": player_data[5], 
            "Country": player_data[6],  
            "Club Country": player_data[7], 
            "Year": player_data[8] 
        } 
        player_list.append(player) # add the player to the list 
    return player_list 
 
def meth2(player_list): 
    position_dict = {"GK": [], "DF": [], "MF": [], "FW": []} 
    for player in player_list: 
        position_dict[player["Position"]].append(player) 
    return position_dict 
 
def meth3(position_dict): 
    country_dict = {} 
    for players in position_dict.values(): # walk through the players 
    #ِ All the values that exist in "GK" key 
    # [{'Number': '1', 'Position': 'GK', 'Name': 'Juan Botasso', 'Date of Birth': 
    # '(1908-10-23)23 October 1908 (aged 21)', 'Caps': '', 'Club': 'Quilmes', 'Country': 'Argentina', 'Club Country': 'Argentina', 'Year': '1930'}] 
 
        for player in players: # walk through the information of each player 
 
    # [{'Number': '1', 'Position': 'GK', 'Name': 'Juan Botasso', 'Date of Birth': 
    # '(1908-10-23)23 October 1908 (aged 21)', 'Caps': '', 'Club': 'Quilmes', 'Country': 'Argentina', 'Club Country': 'Argentina', 'Year': '1930'}] 
    # Player : walking through each player in each position(“GK”) ⇒ position 
            country = player["Country"] 
            # Check if the country is already in the dictionary 
            if country not in country_dict: 
                country_dict[country] = { 
                    "GK": [], 
                    "DF": [], 
                    "MF": [], 
                    "FW": [] 
                } 
            # Append the player to the corresponding position list 
            position = player["Position"] 
            country_dict[country][position].append(player) 
    return country_dict 
 
player_list = meth(SQUADS_DATA) 
position_dict = meth2(player_list) 
country_dict = meth3(position_dict) 

for i in country_dict['Brazil']["FW"]:
   print(i)

















