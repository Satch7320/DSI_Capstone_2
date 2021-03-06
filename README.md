# DSI Capstone 2
The second of three capstones in the Galvanize Data Science Immersive.


## Proposals

### 1: M:tG Card Generator
Using the API from https://scryfall.com again, the entire library of Magic cards is easily accessible as a JSON file in a single query. My intention with the project would be to create a neural network that could create 'legitimate' Magic cards, i.e. those that could exist under the game's rules. There are many interrelated elements; a card's color, cost, rules text, name, and type all follow guidelines set by the designers and I want to see if I can train a neural network to create cards that obey these rules without explicitly defining the rules.

For example, a blue card is more likely to be an instant than a green card, a creature's cost is usually correlated to its power/toughness, and colors have primary, secondary, and tertiary keyword availabilities, so if the generator created a soldier with 1 power/1 toughness, deathtouch, and a cost of {U}{U}{U}, this would break the design rules. Deathtouch is not a blue keyword, a mana cost of 3 is too high for a 1/1 with a single keyword, and there are 66 Blue soldiers out of 1,590 blue creatures in contrast to the 432 soldiers of the 2,470 creatures in white.

This is compounded by the changes in card text and design over the years, because rulings are updated with the introduction of new mechanics and cards every set alongside some large game-wide changes in certain epochs of the game, like retroactive text changes (so 'exile' instead of 'remove ~ from the game'). This would make for a difficult but interesting unsupervised learning task.

### 2: Handwriting Recognition
Similar in principle to the numeral recognition of our learning material, this dataset (https://www.kaggle.com/landlord/handwriting-recognition) is already broken apart into train/test/validation files spanning over 300,000 images of handwritten names. The intention is to develop a model that accurately classifies a name by identifying its constituent parts (letters). 

The CSV files align the images with their known names from human identification, so building an efficacious model that adequately recognizes handwritten characters ignoring 'noise' like the typed prompts (e.g. 'nom' or 'name') and overhang from cropped fields provides a good opportunity to train a convolutional neural network. There might be some small potential for use in natural language processing, but it is impractical, since a 'name' is not necessarily an exclusive word; Cliff and Heather are both names and objects, for example. 

### 3: EMG Data for Muscle Activation in Climbers
A bit more novel than the other two proposals, my sister has elected to share with me electromyograph data she collected during research trials intended to learn how experience influences muscle activation in rock climbers. Because it was collected for business purposes, I will not link the data in this proposal. To access the data directly, please email jana.r.montgomery@gmail.com. 

The eventual use of the data was to learn which cues would be most helpful to novice climbers, to accelerate learning good muscle activation and form. The study format was of 4 female climbers ranging from 1 to 43 years experience in rock climbing performing 5 types of pre-determined indoor routes and measuring muscle activation across 17 sites during those routes. The greatest differences in muscle activation between experience levels in these controlled environments are expected to indicate which cues should be implemented.

The difficulty with this dataset is the limited amount of data available. While it is highly controlled and thusly very clean, performing cross-validation would be hamstrung by the amount of data and confidence intervals would likely have little meaning. Regardless, this was a professionally done research trial and for this reason means it would be a more strongly guided way to approach fitting data to a linear regression model and identifying the strength of experience as a predictor of muscle activation.
