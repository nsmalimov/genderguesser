Gender Guesser

Gender Guesser is a simple REST API that guesses the gender of a first name, based on 90 years of data from the Social Security Administration.

TODO:

* Determine table structure names_by_year - id (auto-increment), year (from filename), name sex total (from file contents) - add an index on the name field
* Write SQL importer
    * For each file, get year, for each line, insert into table
* Generate table - names: id, name, sex, total (group by name and sex)
* Generate table - name_sex: id, name, sex_guess, total_humans, total_guess, certainty (total guess/(total_humans)),
* API: name, gender, certainty