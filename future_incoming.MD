# The Future That Comes Upon Us #

The rapid development of Generative AI has introduced numerous new challenges: amplifying biases, erosion of trust, disinformation, lack of accountability, manipulation - to name a few.
When it comes to speech, the focus is often on unauthorized voice cloning. Today, I want to talk about an often-overlooked aspect: the intersection of social manipulation and generative speech.

In the following, I build an argument that speech-enabled LLM provides considerably higher manipulation risks that the text LLM alone. Firstly, I argue that, unlike text, speech has a direct access to our emotional, irrational brain. Secondly, the progress in the speech technology approaches the state where that can be used. Next, I discuss how combining those can provide a large spectrum of possible manipulations. Finally, I touch on how far we are from this sort of dystopia.

### Prelim 0 ###

The first point I want to make is that audio differs significantly from text. I believe that audio has a more direct access to our emotional, non-rational brain.

Written text is a technology and a very recent one: the oldest known written symbols date some 10,000 years back [[1]](#reference-1). Individuals must learn to read, and this skill is acquired at a relatively later age. It takes time to cultivate the skill of visualizing concepts from text and being emotionally moved by it.

In contrast, audio communication predates our own species. Birds, reptiles, insects, and even fish communicate via sounds [[2]](#reference-2). Sound-producing animals existed hundreds of millions of years ago [[3]](#reference-3). Humans produce sounds from the first minutes of their lives,  utilizing their limited repertoire of vocalizations to communicate their needs to their caregivers. The voice of your child can produce emotional response even before one realizes _what_ is being said. Conversely, children already recognize their mother's voice even before they are born. The way babies cry already mimics the patterns of their parent's language [[4]](#reference-4).


Therefore, my hypothesis is that, compared to audio, humans possess a natural defense against being influenced by text. Just as individuals tend to be more rational when communicating in a foreign language than in their native one [[5]](#reference-5), I believe humans exhibit a greater rationality when reading text compared to hearing speech. Conversely, we can say that audio has a more direct access to our brains.


### Prelim 1 ###

Another point is that the quality of speech generation systems has rapidly become alarmingly good. Compare the capabilities from nine years ago [[6]](#reference-6) to those of three years ago [[7]](#reference-6), and then to what is available today [[8]](#reference-8), [[9]](#reference-9). These systems now offer very high audio quality, naturally-sounding prosody and emotions, faster-than-real-time generation, and include realistic non-word vocalizations. They can perform zero-shot voice cloning from just a few seconds of audio [[10]](#reference-10), [[11]](#reference-11), [[12]](#reference-12).

It's highly probable that within just a few years, the average person will find it impossible to distinguish synthesized speech from natural human speech. In fact, it's already difficult to distinguish synthetic speech, particularly over phone calls. At the same time, the voices, prosody, paralinguistic features will be easily configurable.

### Putting it all together ###

While the focus has largely been on challenges posed by textual Large Language Models (LLMs), I believe that it is the combination of speech generation and smart LLMs that presents an even more unsettling array of problems. Imagine an agent as smart as a SoTA reasoning LLM, optimized to manipulate or scam you and now equipped with a direct access to your emotional state. Wouldn't that make manipulation even easier?

There could be different levels of this.

Consider a scenario beginning with a highly empathetic voice answering your call to an airline support line. The voice and what is being said are optimized to reduce the number of refunds. "Yes John, I understand how that makes you feel. We are deeply sorry for the flight being delayed. Would you accept this meal voucher as an apology?" At this stage, it is perhaps not as different as optimizing the shade of the ten blue links to increase the user engagement [[13]](#reference-13).

The next level is still simplistic. For instance, an AI might figure out your socio-demographic situation from your accent and voice. Maybe it can figure out which voices you find attractive. Maybe if can figure out your native language and switch to it, building a connection over typical problems of your diaspora. It can use all that to convince you buying a year's worth of printing paper.


With a few more optimization steps, the bot on the other end of the line could precisely time pauses and emphasize specific words or phrases, in a ways that are extremely tailored for you --- in order to subtly increase your susceptibility to a scam. Now, extrapolate this to millions of simultaneous sessions, operating 24/7 from a distant data center. Large-scale LLMs deployments weaponized to incrementally affect your purchasing decisions or straight scam you.

Or consider a cold call where the AI attempts to mimic your child's voice, based solely on your 'Hello,' to solicit money from you. Ok, this one might be hard, but what success rate would make the numbers work, economically? Still might be considerably more profitable than the current scam schemes.


### Are we there yet? ###

I think we are not there yet, technology-wise. However, we are getting there fast.

Direct, end-to-end speech-to-speech models provide good reactivity and high dialog quality. They can back-channel and do all the paralinguistic stuff. However, the small open ones are dumber than their textual counterparts, even those that were textually pretrained. Perhaps this is less of a problem for the large, closed ones, such as Gemini. Fortunately, sustaining an interactive dialogue for 20 minutes requires reserving significant hardware resources for that duration, and these large models demand substantial computational power. Consequently, such a scenario is likely not economically viable with the current generation of large commercial models.


In turn, cascaded systems, which sandwich a pure textual LLM with a combination of Speech-to-Text (STT) and Text-to-Speech (TTS) models, are smarter but lack dialog reflexes. They have an intrinsically limited expressiveness because two disjoint systems separately generate and synthesize words. Furthermore, the LLM and TTS communicate solely via text, which offers a quite limited bandwidth for transmitting expression and prosody. A further challenge lies in the latency inherent in cascaded systems, arising from the sequential requirement for one model to transcribe, another to formulate a reply, and a third to synthesize that response.

Now I believe the progress is being made and we can see those problems being cracked before our eyes, one-by-one.

For instance, the latency limitation is being relaxed due to streaming STT and TTS becoming workable solutions.
Streaming STT starts feeding tokens into a standard LLM even before the user finishes speaking, allowing the LLM to begin processing immediately and generating a reply the moment it determines the user's turn is complete.
TTS can start synthesizing when the first token comes out of the LLM. The total latency can drop to as little as 0.5s [[14]](#reference-14). As a reference, the recommended round-about latency for VoIP calls is below 0.3s and likely people can easily adjust to 0.5s when chatting over the phone. One can imagine a cascaded system with a lower latency and better prosody if, e.g. TTS is merged on top of the LLM itself.


All in all, as end-to-end systems become smarter and cheaper, and cascaded systems become more interactive, we can see increasingly more scenarios from the previous Section being unlocked.


### What's next? ###
Is there a solution to avoid this dystopia? Unfortunately, I believe the answer is no. The underlying technology is getting there
and the market would be happy to capitalize on that. However, I hope that writing down my thoughts might help to start a discussion.


### References ###


<a id="reference-1">[1]</a> https://en.wikipedia.org/wiki/Jiahu_symbols

<a id="reference-2">[2]</a> https://pmc.ncbi.nlm.nih.gov/articles/PMC6519373/ --- a random paper on the topic, maybe there are better references!

<a id="reference-3">[3]</a> https://www.scientificamerican.com/article/fossils-reveal-when-animals-started-making-noise/

<a id="reference-4">[4]</a> https://www.sciencedirect.com/science/article/pii/S0960982209018247

<a id="reference-5">[5]</a> https://www.sciencedirect.com/science/article/abs/pii/S001002771300228X

<a id="reference-6">[6]</a> https://deepmind.google/discover/blog/wavenet-a-generative-model-for-raw-audio/

<a id="reference-7">[7]</a> https://google-research.github.io/seanet/soundstorm/examples/

<a id="reference-8">[8]</a> https://www.hume.ai/blog/introducing-evi-3

<a id="reference-9">[9]</a> https://elevenlabs.io/voice-library

<a id="reference-10">[10]</a> https://google-research.github.io/seanet/speartts/examples/#prompting

<a id="reference-11">[11]</a> https://elevenlabs.io/voice-cloning

<a id="reference-12">[12]</a> https://www.microsoft.com/en-us/research/project/vall-e-x/

<a id="reference-13">[13]</a> https://www.quora.com/How-much-did-Google-increase-conversions-after-its-41-shades-of-blue-test/answer/Ronny-Kohavi


<a id="reference-14">[14]</a> https://github.com/kyutai-labs/unmute
