Date: 20190427 

# Project Spec — Pre-trained Image Classifier to Identify Dog Breeds

## Timing Code

| Criteria | Specification  |
|:--|:--|
| Implement `time()` functions | Call the time functions before the start of main code and after the main logic has been finished. |


## Command Line Arguments

| Criteria | Specification  |
|:--|:--|
| Enable *dir* argument  | Add command line argument for --dir` with `default='pet_images/'`.
 |
| Enable *arch* argument | Add command line argument for --arch` with `default='vgg'` |
| Enable *dogfile* argument | Adds command line argument for `--dogfile` with `default='dognames.txt'` |


## Pet Image Labels


| Criteria | Specification  |
|:--|:--|
| Handle hidden files  | Makes sure files starting with '.' are ignored by checking for `'.'` using a conditional statement. |
| Dictionary returned in the correct format. | Dictionary key and label are in the correct format and retrieves 40 key-value pairs, e.g: `{'Poodle_07956.jpg': ['poodle'], 'fox_squirrel_01.jpg': ['fox squirrel'] ... }` |
| Correct function call | `'in_arg.dir'` is passed as an argument inside `check_images.py` while calling the `get_pet_labels()` function. |


## Classifying Images

| Criteria | Specification  |
|:--|:--|
| Correct function call | Appends `images_dir` to each value before making the function call, `classifier(images_dir+users_key, model)` |
| Format output | Convert the output to lower case and strip any whitespaces |
| Verifies and stores results appropriately. Display output when the function is called. | Appends `1` to correct label, and `0` to falsely classified values. |


## Classifying Labels as Dogs

| Criteria | Specification  |
|:--|:--|
| *Matches* and *non-matches* between `Classifier` and `Pet Image` labels have both labels classified as "dogs" or "not dogs" as appropriate for the labels.  | Check the displayed output and see if all matches and non-matches are appropriately displayed. |

## Results

| Criteria | Specification  |
|:--|:--|
| Accurate overall scores for three models by running `run_models_batch.sh` after writing all the code. | All three models score as expected. |





