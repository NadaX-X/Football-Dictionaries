# Football-Dictionaries
SQUADS_DATA = [ 
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
  ], 
  [ 
    "-", 
    "MF", 
    "Pierre Braine", 
    "(1900-10-26)26 October 1900 (aged 29)", 
    "42", 
    "Royal Beerschot AC", 
    "Belgium", 
    "Belgium", 
    "1930" 
  ], 
  [ 
    "-", 
    "MF", 
    "Alexis Chantraine", 
    "(1901-03-16)16 March 1901 (aged 29)", 
    "0", 
    "Royal FC Liegeois", 
    "Belgium", 
    "Belgium", 
    "1930" 
  ], 
  [ 
    "-", 
    "GK", 
    "Jean De Bie", 
    "(1892-05-09)9 May 1892 (aged 38)", 
    "37", 
    "Royal Racing Club de Bruxelles", 
    "Belgium", 
    "Belgium", 
    "1930" 
  ], 
  [ 
    "-", 
    "MF", 
    "Oscar", 
    "(1991-09-09)9 September 1991 (aged 22)", 
    "29", 
    "Chelsea", 
    "Brazil", 
    "England", 
    "2010" 
  ], 
  [ 
    "-", 
    "MF", 
    "Paulinho", 
    "(1988-07-25)25 July 1988 (aged 25)", 
    "25", 
    "Tottenham Hotspur", 
    "Brazil", 
    "England", 
    "2010" 
  ], 
  [ 
    "-", 
    "MF", 
    "Hernanes", 
    "(1985-05-29)29 May 1985 (aged 29)", 
    "23", 
    "Internazionale", 
    "Brazil", 
    "Italy", 
    "2014" 
  ], 
  [ 
    "-", 
    "MF", 
    "Luiz Gustavo", 
    "(1987-07-23)23 July 1987 (aged 26)", 
    "17", 
    "VfL Wolfsburg", 
    "Brazil", 
    "Germany", 
    "2014" 
  ], 
  [ 
    "-", 
    "MF", 
    "Fernandinho", 
    "(1985-05-04)4 May 1985 (aged 29)", 
    "6", 
    "Manchester City", 
    "Brazil", 
    "England", 
    "2014" 
  ], 
  [ 
    "-", 
    "MF", 
    "Willian", 
    "(1988-08-09)9 August 1988 (aged 25)", 
    "5", 
    "Chelsea", 
    "Brazil", 
    "England", 
    "2014" 
  ], 
  [ 
    "-", 
    "FW", 
    "Lee Keun-Ho", 
    "(1985-04-11)11 April 1985 (aged 29)", 
    "62", 
    "Sangju Sangmu", 
    "South Korea", 
    "South Korea", 
    "2014" 
  ], 
  [ 
    "-", 
    "FW", 
    "Koo Ja-Cheol", 
    "(1989-02-27)27 February 1989 (aged 25)", 
    "35", 
    "Mainz 05", 
    "South Korea", 
    "Germany", 
    "2014" 
  ], 
  [ 
    "-", 
    "FW", 
    "Kim Shin-Wook", 
    "(1988-04-14)14 April 1988 (aged 26)", 
    "26", 
    "Ulsan Hyundai", 
    "South Korea", 
    "South Korea", 
    "2014" 
  ] 
]
def players_as_dictionaries(squads_list): 
    ls = [] 
    for _ in range(len(squads_list)): 
      ls.append({}) 
      for i in range(len(squads_list[0])): 
        if i==0: 
          ls[]['number'] = squads_list[][i] 
        elif i==1: 
          ls[]['position'] = squads_list[][i] 
        elif i==2: 
          ls[]['name'] = squads_list[][i] 
        elif i==3: 
          ls[]['date_of_birth'] = squads_list[][i] 
        elif i==4: 
          ls[]['caps'] = squads_list[][i] 
        elif i==5: 
          ls[]['club'] = squads_list[][i] 
        elif i==6: 
          ls[]['country'] = squads_list[][i] 
        elif i==7: 
          ls[]['club_country'] = squads_list[][i] 
        elif i==8: 
          ls[]['year'] = squads_list[][i] 
    return ls
def players_by_position(squads_list): 
    ln = {"GK":[],"DF":[],"MF":[],"FW":[]} 
    for player in range(len(squads_list)): 
      if squads_list[player]['position'] == "GK": 
        ln["GK"].append([squads_list[player]]) 
      elif squads_list[player]['position'] == "DF": 
        ln["DF"].append([squads_list[player]]) 
      elif squads_list[player]['position'] == "MF": 
        ln["MF"].append([squads_list[player]]) 
      elif squads_list[player]['position'] == "FW": 
        ln["FW"].append([squads_list[player]]) 
    return ln 
def players_by_country_and_position(squads_list): 
    country=[] 
    for _ in range(len(squads_list)): 
      country.append(squads_list[_]['country']) 
    keys=list(set(country)) 
    ln={} 
    for key in keys: 
      ln[key] = {"GK":[],"DF":[],"MF":[],"FW":[]} 
      for player inrange(len(squads_list)): 
        for val in ln[key].keys(): 
          if squads_list[player]['country'] == key and squads_list[player]['position']==val: 
            ln[key][val].append([squads_list[player]]) 
    return ln
SQUADS_DATA=players_as_dictionaries(SQUADS_DATA) 
print(SQUADS_DATA)
print(players_by_position(SQUADS_DATA)["GK"])
print(players_by_country_and_position(SQUADS_DATA))
