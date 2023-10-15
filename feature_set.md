# FEATURES SET 

We will present our feature set organized by type of linguistic information used in the development of the rules applied in this work. 

## TimeML Annotation
  - `event-class:` event class annotated in the corpus
  - `event-closest-to-event-class:` annotated class of the event closest to the event in the temporal relation under classification
  - `event-closest-to-event-equal-class:` checks if the event's class value in the temporal relation under classification is equal to the class of the nearest event in the text
  - `event-intervening-preceding-class:` event class mentioned between the temporal expression and the event, in this textual order, in the temporal relation under classification, and closest to the temporal expression. For example, `TIMEX --- event2.class ------------ EVENT`
  - `event-polarity:` event polarity
  - `timex3-temporalfunction:` `temporalFunction` of the temporal expression annotated in the corpus
  - `timex3-type:` type of the temporal expression

## Knowledge About the World
  - `event-temporal-direction:` records the temporal direction of the event. It represents the expected temporal relation between the event and its complement.
  - `event-closest-to-event-temporal-direction:` value of the temporal direction for the event closest to the event in the temporal relation under classification.

## Contextual
  - `event-between-order:` if there is another event between the event and the temporal expression in the relation under classification.
  - `event-conjunction-closest-follow:` closest conjunction after the processed event in the relation.
  - `event-conjunction-closest-precede:` closest conjunction before the processed event in the relation.
  - `event-first-order:` does the event textually precede the temporal expression?
  - `event-has-modal-verb-precede:` checks if the event has modal verbs preceding it.
  - `event-modal-verb:` modal verb text before the event.
  - `event-preposition-precede:` has the value of the preposition that precedes the event in the text.
  - `event-timex3-distance:` distance between the event and the temporal expression.
  - `event-timex3-no-between-order:` checks if there is no event or temporal expression between the event and the temporal expression in the relation under classification.
  - `timex3-between-order:` if there is another temporal expression between the event and the temporal expression in the relation under classification.
  - `timex3-preposition-precede:` has the value of the preposition that precedes the temporal expression in the text.

## Lexical Information
  - `timex3-relevant-lemmas:` the lemma value of the temporal expression if it is in a list of lemmas that have some temporal content and are frequently seen in temporal expressions.

##  Morphological Information
  - `event-closest-to-event-equal-pos:` checks if the grammatical class of the event in the temporal relation under classification is equal to the grammatical class of the event mentioned in the text closest to it.
  - `event-closest-to-event-equal-tense:` checks if the tense of the event in the temporal relation under classification is equal to the tense of the event closest to it in the text.
  - `event-closest-to-event-pos:` grammatical class of the event closest to the event in the temporal relation under classification.
  - `event-closest-to-event-tense:` tense of the event closest to the event in the temporal relation under classification.
  - `event-closest-to-timex3-equal-pos:` checks if the grammatical class of the event in the relation under classification is equal to the grammatical class of the event closest to the temporal expression in the relation under classification.
  - `event-closest-to-timex3-pos:` grammatical class of the event closest to the temporal expression in the temporal relation under classification.
  
  - `event-gov-verb-aspect:` verbal aspect of the verb governing the event. If the event is a verb, the value of this feature is the verbal aspect of the event itself.
  - `event-gov-verb-tense:` tense of the verb governing the event. If the event is a verb, the value of this feature is the tense of the event itself.
  
  - `event-head-pos:` grammatical class of the parent node of the event in the dependency tree.
  - `event-intervening-following-tense:` tense of the event mentioned between the event and the temporal expression, in this textual order, in the temporal relation under classification, and closest to the temporal expression. For example, `EVENT ------------ event2.tense --- TIMEX`.
  - `event-pos:` grammatical class of the event.
  
  - `event-pos-token-1-follow:` grammatical class of the 1st token after the event.
  - `event-pos-token-2-follow:` grammatical class of the 2nd token after the event.
  - `event-pos-token-3-follow:` grammatical class of the 3rd token after the event.
  
  - `event-pos-token-1-precede:` grammatical class of the 1st token before the event.
  - `event-pos-token-2-precede:` grammatical class of the 2nd token before the event.
  - `event-pos-token-3-precede:` grammatical class of the 3rd token before the event.
  
  - `timex3-pos-token-1-follow:` grammatical class of the 1st token after the temporal expression.
  - `timex3-pos-token-2-follow:` grammatical class of the 2nd token after the temporal expression.
  - `timex3-pos-token-3-follow:` grammatical class of the 3rd token after the temporal expression.
  
  - `timex3-pos-token-1-precede:` grammatical class of the 1st token before the temporal expression.
  - `timex3-pos-token-2-precede:` grammatical class of the 2nd token before the temporal expression.
  - `timex3-pos-token-3-precede:` grammatical class of the 3rd token before the temporal expression.
  
  - `timex3-gov-verb-tense:` tense of the verb governing the temporal expression.
  - `timex3-head-pos:` grammatical class of the parent node of the temporal expression.
  - `timex3-pos:` grammatical class of the temporal expression.



## Syntactic Information
  - `event-dep:` the dependency relation that the event has with its parent.
  - `event-head-is-root:` does the event directly modify the root?  
    (e.g., is the event a direct child of the root in the dependency tree?)
  - `event-is-ancestor-timex3:` is the event the governing entity in the relation?
  - `event-preposition-gov:` syntactically governing preposition of the event.
  - `event-root:` is the event the root of the syntactic dependency tree?
  - `event-timex3-dep:` dependency relation between the event and the temporal expression or between the temporal expression and the event.
  - `reichenbach-direct-modification:` does the temporal expression directly modify the event?  
    (Is the expression on the same dependency path as the event?)
  - `reichenbach-temporal-mod-function:` temporal modification function, is there an `nmod` relation in the dependency path from the event to the temporal expression?
  - `timex3-dep:` syntactic dependency relation of the temporal expression with its governor (parent node).
  - `timex3-head-is-root:` does the temporal expression directly modify the root?  
    (e.g., is the temporal expression a direct child of the root in the dependency tree?)
  - `timex3-is-ancestor-event:` is the temporal expression the governing entity in the relation?
  - `timex3-preposition-gov:` syntactically governing preposition of the temporal expression.


## Reichenbachian Tenses
  - `reichenbach-tense:` Reichenbach's tense: assumes one of the values "anterior" (anterior), "simples" (simple), or "posterior" (posterior).
  
  
## Temporal Signals
  Temporal signals consist of conjunctions and temporal adverbs.
  
  - `signal-precede-event-child-event:` is the signal preceding the event syntactically governed by this event?
  - `signal-precede-timex3-child-timex3:` is the signal preceding the temporal expression syntactically governed by this expression?
  
  - `signal-precede-event-dep-if-child-event:` if the signal preceding the event is governed by this event, what is the type of syntactic dependency relation?
  - `signal-precede-timex3-dep-if-child-timex3:` if the signal preceding the temporal expression is governed by this expression, what is the type of syntactic dependency relation?
  
  - `signal-precede-event-distance-event:` distance between the signal preceding the event and this event.
  - `signal-precede-timex3-distance-timex3:` distance between the signal preceding the temporal expression and this expression.
  
  - `signal-precede-event-pos:` grammatical class of the signal preceding the event.
  - `signal-precede-timex3-pos:` grammatical class of the signal preceding the temporal expression.
  
  - `signal-precede-event-text:` text of the signal preceding the event.
  - `signal-precede-timex3-text:` text of the signal preceding the temporal expression.

  **Note:** If there is no signal preceding the event or temporal expression under consideration, the values for all features related to this signal will be null.
  