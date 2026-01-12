import random

stages = [
"""
  +---+
  |   |
      |
      |
      |
      |
=========
""",
"""
  +---+
  |   |
  O   |
      |
      |
      |
=========
""",
"""
  +---+
  |   |
  O   |
  |   |
      |
      |
=========
""",
"""
  +---+
  |   |
  O   |
 /|   |
      |
      |
=========
""",
"""
  +---+
  |   |
  O   |
 /|\  |
      |
      |
=========
""",
"""
  +---+
  |   |
  O   |
 /|\  |
 /    |
      |
=========
""",
"""
  +---+
  |   |
  O   |
 /|\  |
 / \  |
      |
=========
"""
]

word_list = ["aardvark", "baboon", "camel"]
chosen_word = random.choice(word_list)

lives = 6
game_over = False
correct_letters = []

display = "_" * len(chosen_word)
print(display)

while not game_over:
    guess = input("Guess a letter: ").lower()

    new_display = ""

    for letter in chosen_word:
        if letter == guess:
            new_display += letter
            correct_letters.append(guess)
        elif letter in correct_letters:
            new_display += letter
        else:
            new_display += "_"

    display = new_display
    print(display)

    if guess not in chosen_word:
        lives -= 1
        print(stages[lives])

        if lives == 0:
            game_over = True
            print(" You lose!")

    if "_" not in display:
        game_over = True
        print("You win!")
