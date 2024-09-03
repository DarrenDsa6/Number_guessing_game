# Number_guessing_game
This file consists of the sh and sql code for the number guessing game exercise under relational database course of free code camp.
Follow the below steps to complete the project:
Here are the commands you’ve used:
It looks like you've already laid out the commands for setting up your database and initializing your Git repository. Here’s a concise list of the commands based on your instructions:

1. **Create the database:**
   ```sql
   CREATE DATABASE number_guess;
   ```

2. **Connect to the database:**
   ```sql
   \c number_guess
   ```

3. **Create tables:**
   ```sql
   CREATE TABLE users(
       user_id SERIAL NOT NULL,
       username VARCHAR(22) UNIQUE NOT NULL,
       frequent_games INT DEFAULT 0 NOT NULL
   );
   CREATE TABLE games(
       game_id SERIAL NOT NULL,
       user_id INT NOT NULL,
       best_guess INT DEFAULT 0 NOT NULL
   );
   ```

4. **Alter tables to add primary and foreign keys:**
   ```sql
   ALTER TABLE users ADD PRIMARY KEY(user_id);
   ALTER TABLE games ADD PRIMARY KEY(game_id);
   ALTER TABLE games ADD FOREIGN KEY(user_id) REFERENCES users(user_id);
   ```

5. **Dump the database schema and data:**
   ```bash
   pg_dump -cC --inserts -U freecodecamp number_guess > number_guess.sql
   ```

6. **Create a new directory and initialize a Git repository:**
   ```bash
   mkdir number_guessing_game
   cd number_guessing_game
   git init
   ```

7. **Create a new Git branch:**
   ```bash
   git checkout -b main
   ```

8. **Create a file and commit it:**
   ```bash
   touch number_guess.sh
   git add number_guess.sh
   git commit -m "Initial commit"
   ```

9. **Change file permissions and commit:**
   ```bash
   chmod +x number_guess.sh
   git add number_guess.sh
   git commit -m "refactor: Give executable permissions to number_guess.sh"
   ```

10. **Add a shebang and commit:**
    ```bash
    git add number_guess.sh
    git commit -m "feat: added shebang"
    ```

11. **Commit changes to the file:**
    ```bash
    git add number_guess.sh
    git commit -m "feat: Completed bash code"
    git commit -m "feat: Completed bash code 2"
    git commit -m "feat: Completed bash code 3"
    ```
