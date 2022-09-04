letters = ["A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M", "N", "O", "P", "Q", "R", "S", "T", "U", "V", "W", "X", "Y", "Z"]
points = [1, 3, 3, 2, 1, 4, 2, 4, 1, 8, 5, 1, 3, 4, 1, 3, 10, 1, 1, 1, 1, 4, 4, 8, 4, 10]

# to handle lowercase inputs as well
letters += [letter.lower() for letter in letters]
points += points
# print(letters)
# print(points)

# dictionary called letter_to_points that has the elements of letters as the keys and the elements of points as the values.
letter_to_points = {key: value for key, value in zip(letters, points)}
letter_to_points[" "] = 0 # to account for blank tiles
#print(letter_to_points)

#  function that will take in a word and return how many points that word is worth
def score_word(word):
  point_total = 0
  #  for loop that goes through the letters in word and adds the point value of each letter to point_total.
  for letter in word: 
    point_total += letter_to_points.get(letter, 0)
  return point_total

brownie_points = score_word("BROWNIE")
print(brownie_points)

# dictionary that maps players to a list of the words they have played
player_to_words = {"player1": ["BLUE", "TENNIS", "EXIT"], "wordNerd": ["EARTH", "EYES", "MACHINE"], "Lexi Con": ["ERASER", "BELLY", "HUSKY"], "Prof Reader": ["ZAP", "COMA", "PERIOD"]}

player_to_points = {}

def update_points_total():
  for player, words in player_to_words.items():
    player_points = 0
    for word in words:
      player_points += score_word(word)
    player_to_points[player] = player_points

update_points_total()
print(player_to_points)

# function that would take in a player and a word, and add that word to the list of words they’ve played
def play_word(player, word):
  player_to_words[player].append(word)
  update_point_totals()
