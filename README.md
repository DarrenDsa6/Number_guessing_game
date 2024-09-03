# Number_guessing_game
This file consists of the sh and sql code for the number guessing game exercise under relational database course of free code camp.
Follow the below steps to complete the project:
Here are the commands you’ve used:
1. **Create databases:**
   ```sql
   CREATE DATABASE numbrt_guess;
   CREATE DATABASE number_guess;
   ```

2. **Drop a database:**
   ```sql
   DROP DATABASE numbrt_guess;
   ```

3. **Connect to a database:**
   ```sql
   \c number_guess
   ```

4. **Create tables:**
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

5. **Alter tables to add primary and foreign keys:**
   ```sql
   ALTER TABLE users ADD PRIMARY KEY(user_id);
   ALTER TABLE games ADD PRIMARY KEY(game_id);
   ALTER TABLE games ADD FOREIGN KEY(user_id) REFERENCES users(user_id);
   ```

6. **Dump the database schema and data:**
   ```bash
   pg_dump -cC --inserts -U freecodecamp number_guess > number_guess.sql
   ```

7. **Create a new directory and initialize a Git repository:**
   ```bash
   mkdir number_guessing_game
   cd number_guessing_game
   git init
   ```

8. **Create a new Git branch:**
   ```bash
   git checkout -b main
   ```

9. **Create a file and commit it:**
   ```bash
   touch number_guess.sh
   git add number_guess.sh
   git commit -m "Initial commit"
   ```

10. **Change file permissions and commit:**
    ```bash
    chmod +x number_guess.sh
    git add number_guess.sh
    git commit -m "refactor: Give executable permissions to number_guess.sh"
    ```

11. **Add a shebang and commit:**
    ```bash
    git add number_guess.sh
    git commit -m "feat: added shebang"
    ```

12. **Commit changes to the file:**
    ```bash
    git add number_guess.sh
    git commit -m "feat: Completed bash code"
    git commit -m "feat: Completed bash code 2"
    git commit -m "feat: Completed bash code 3"
    ```

