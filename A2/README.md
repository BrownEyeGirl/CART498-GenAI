# Assignment 2 <br>
## P+7 (Oulipian language modelling) <br>

## Background <br>
The Oulipo (Ouvroir de Littérature Potentielle, or “Workshop of Potential Literature”) is a French literary group founded in 1960 by writer Raymond Queneau and mathematician François Le Lionnais. The group focuses on using rules and constraints in writing as a way to spark creativity. Rather than seeing constraints as obstacles, Oulipians treat them as tools to inspire new forms of storytelling and poetry. Their work combines mathematics, language, and playfulness, making their approach both unique and influential in modern literature.

One of the most famous Oulipian writers is Georges Perec, who is known for his creative use of constraints. His novel La Disparition (“A Void”) is written entirely without the letter "e," which is especially challenging given how common "e" is in French. Perec’s writing often plays with the structure of language in surprising ways.

![Olipian Photo](https://upload.wikimedia.org/wikipedia/commons/7/76/Myart_georges-perec_1978.jpg)

George Perec

(George Perec, 1978. From Wikidata)

## The N+7 technique <br>
One popular Oulipian technique is N+7, where each noun in a text is replaced by the noun seven entries later in a dictionary. This creates unusual, absurd, and often funny results, encouraging writers to think differently about language and meaning.

The N+7 technique process is straightforward

Start with a text. Choose any text—this could be a poem, a sentence, or a passage.
Use a dictionary. Have a dictionary (or word list) handy.
Replace each noun. For every substantive noun in the original text, replace it with the noun appearing seven nouns away in the dictionary. If the end of the dictionary is reached, you can loop back to the beginning.
Maintain grammar. Ensure the new text maintains grammatical correctness as much as possible, though the results often turn out surreal and nonsensical.
For example, using the N+7 technique with a standard English dictionary for the original sentence:

One must have a mind of winter.

”mind” → 7 nouns after “mind” is “minimum” or “mindset” (depending on the dictionary)
“winter” → 7 nouns after “wishing” or “wipe”
Then, after applying the technique the results are:

Original: “One must have a mind of winter”
Dictionary one: “One must have a minimum of wishing”
Dictionary two: “One must have a mindset of wipe”
Online example

## Assignment and deliverables <br>
For this assignment, you will create a variation of the N+7 technique we will name P+7. Using the GPT-2 language model, you will replace the last word of each line from The Snow Man with the token that has the seventh-highest probability according to the model’s predictions.

By the end of this assignment, submit a link to a GitHub repository named CART498-GenAI containing a folder labelled A02 with the following items:

A version of the text processed with your P+7 technique, saved as a .txt file.
A second version of the text processed with P+x. Choose an x value that produces the funniest, wittiest, or most absurd version of the original text. Save this as a .txt file, and include the x value in the filename (e.g., P+23.txt or P+12.txt).
A Python notebook with the script used to generate your P+7 and P+x transformations using the GPT-2 language model.
A short reflection (250–350 words) explaining how altering the x value impacted the output of your P+x version. Additionally, discuss how you would implement a P+7 technique in which all nouns are replaced with their seventh-highest probability alternatives.
