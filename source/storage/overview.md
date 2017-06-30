title: Overview
description: 
---

Overall goal is to minimise and ideally eliminate configuration.

Design Paradigms
- Re-use and re-purposing of existing knowledge in other systems
- Self-discovery, self-describing, import and learning
- Convention over configuration
- Semantic configuration with Domain specific languages
- Failure proof
- Progressive truthfulness. Perhaps a better way to build models of physical objects...Start with a model that is fully detailed but only resembles what is wanted. Then, one adjusts one attribute after another, bringing the result ever closer to the mental vision of the new creation, or to the real properties of a real-world object

Multi-Layer Architecture - Users Layers of Knowledge
- App user - no technical knowledge
- App administrator - no technical knowledge
- App deployment & setup - some technical knowledge
- App developer - some technical knowledge
- Component developer - technical knowledge

## Notes from [Semantic UI Author](https://news.ycombinator.com/item?id=14075720)

Semantic is based on the idea that describing physicality (the function of html/css) is a task natural language is acutely optimized for, while describing the implementation of behavior ("cooking recipes", or the vast majority of programming implementation) is best served by programming languages.

Part of how natural language optimizes for transmitting meaning is by reducing ideal forms of concepts to words based on the exact amount of specificity for conveying meaning between humans. I.e. "horse" instead of "quadrupedal mammal that has a heart and has eyes and has a tongue..." etc.
These 'units of optimized human idea transmission' (read words) are then clarified using a system of modifiers that take care of removing just enough ambiguity that the idea is communicated effectively. "The kindly, gentle lion", "The angry, hungry lion".
The modifiers themselves carry no absolute meaning. A "large ant" may be smaller than a "small planet", but we understand them -- in context -- of the nouns.

Language is littered with other interesting features like this that are designed particularly for this task of describing physicality. Most of which are absent from programmatic implementations of 'languages for describing physicality' like HTML/CSS.
Other key examples of useful cognitive optimization: Plurality, "Three large red buttons" vs "Large red button, large red button"; significant word order, "left floated right aligned column" vs "right floated left aligned" column.

I think the main drawback with using a natural language approach is that the implementation has to be bullet proof. Although everyone uses language, we never have to implement systems of interpreting language from phoneme to neuronal pathway. So even though the benefits are clear, the path forward in mapping language to systems of programmatic physicality isn't exactly straightforward.
