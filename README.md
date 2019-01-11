# NLP - Bi-LSTM for Hashtag Segmentation
Using Keras to implement a bidirectional LSTM for Twitter hashtag segmentation.
The task is to take a hashtag and segment it into the phrase it corresponds to. This task may seem trivial, but a single hashtag can be segmented in many different ways:
> `#wordsoftheday` => “word soft he day" or “words of the day"<br>
`#statefarmisthere` => “state far mist here" or “state farm is here"<br>
`#brainstorm` => “bra in storm" or “brain strom"<br>
`#doubledown` => “do u bled own" or “double down"<br>
`#votedems` => “voted ems" or “vote dems"<br>

The approach to solving this problem is to assume each timestep is a character and assign a binary label: 1 if a character should be followed by a space and 0 otherwise.
>`#nlprocks`<br>
input: [n, l, p, r, o, c, k, s]<br>
label: [0, 0, 1, 0, 0, 0, 0, 0]

## F1 Score: 0.754

## Dataset
~700,000 segmented hashtags from Twitter
