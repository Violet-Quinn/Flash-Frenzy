**Flash Frenzy**

**Flash Frenzy** is a bilingual flashcard application built with Python's `tkinter` library. It helps users learn and retain French and English vocabulary in a fun and interactive way. Users can test their language skills by flipping between French and English words, keeping track of learned words, and customizing their vocabulary list. The app saves unlearned words for later practice, ensuring a personalized and focused learning experience.

---

### Features

- **Randomized Vocabulary Practice**: Displays a random French word with its English translation shown after a short delay, encouraging users to guess before revealing the answer.
- **Progress Tracking**: Tracks words you’ve learned by removing them from the practice list and saving the remaining words in a local CSV file.
- **Automatic Flip Timer**: Each card automatically flips after a few seconds, revealing the English translation to enhance memory retention.
- **User-Friendly Interface**: Provides a clear and intuitive UI with buttons to mark words as "known" or "unknown."
- **Customizable Vocabulary List**: Loads from a CSV file, allowing users to add or modify words in their learning list.

---

### Installation

Clone the Repository:

```bash
git clone https://github.com/your-username/flash-frenzy.git
cd flash-frenzy
```

Install Dependencies:

- The project uses `tkinter` (included with Python), `pandas`, and `Pillow`.
- Install `pandas` and `Pillow` by running:

  ```bash
  pip install pandas pillow
  ```

- Place `card_front.png`, `card_back.png`, `right.png`, and `wrong.png` in the `images` folder, and ensure `french_words.csv` is in the `data` folder.

---

### Usage

Run the application by executing:

```bash
python flash_frenzy.py
```

---

### How to Use Flash Frenzy

1. **Start Practicing**: When you launch the app, a French word is displayed.
2. **Guess and Flip**: Try to recall the English translation before the card flips automatically.
3. **Mark as Known or Unknown**:
   - Click the checkmark button if you know the word. This removes it from future practice sessions.
   - Click the cross button if you don’t know the word; it will remain in the practice list.
4. **Automatic Card Rotation**: After marking a word, a new card appears for continued practice.

---

### Data Storage

The vocabulary list is stored in a file named `words_to_learn.csv`. Unlearned words are saved in the following format:

```json
[
    {"French": "mot", "English": "word"},
    {"French": "chien", "English": "dog"}
]
```

---

### Code Overview

- **Constants**: Defines the background color and paths to the image assets.
- **Functions**:
  - `next_card()`: Loads the next random word, displays the French word and initiates a timer for the flip.
  - `flip_card()`: Reveals the English translation of the current word.
  - `is_known()`: Marks the word as known, removes it from the list, and saves the updated list to `words_to_learn.csv`.
- **UI Setup**: Configures the `tkinter` UI with labels, images, and buttons for navigation.

---

### Contributing

Contributions are welcome! Open an issue or submit a pull request if you’d like to improve or add features.
