# Frequency

This is my current list of word frequency in Esperanto.

I've calculated this using my own [word list][korpuso.txt],
which attempts to only include words found in La Fundamento,
and the Esperanto works available on [Project Gutenberg][gutendex_eo].

[korpuso.txt]: https://gist.github.com/norwd/2de16364ab4c69fb00c67f3d8964001e
[gutendex_eo]: https://gutendex.com/books/?languages=eo

## Method

Using a sorted and distinct list of allowed words `vortaro.txt`,
which is currently maintained as a gist but may later be included in this repo,
and a directory of text files to use as a corpus `gutenberg/*.txt`,
it is trivial to get the top 100 most used words, as well as their frequencies:

```bash
cat gutenberg/*.txt |
grep --fixed-strings --line-regexp --file vortaro.txt - |
sort |
uniq --count |
sort --numeric-sort --reverse |
head --lines 100 # adjust this value to select more or fewer of the most often used words
```

## Results

So, for a courpus of 1,670,647 words from Project Gutenberg,
excluding the English text in the headings and the like (this is why we match the words to a list of allowed words),
this methods produces the following 100 most used Esperanto words:

| Frequency | Percentage | Word |
| --- | --- | --- |
| 199853 | 11.9626% | la |
| 88177 | 5.27802% | kaj |
| 72772 | 4.35592% | de |
| 66657 | 3.98989% | mi |
| 42862 | 2.56559% | al |
| 42302 | 2.53207% | en |
| 41557 | 2.48748% | ne |
| 41349 | 2.47503% | li |
| 34364 | 2.05693% | estas |
| 34352 | 2.05621% | vi |
| 29135 | 1.74394% | ke |
| 20994 | 1.25664% | por |
| 20379 | 1.21983% | sed |
| 18592 | 1.11286% | estis |
| 15669 | 0.9379% | kun |
| 14635 | 0.876008% | kiu |
| 14457 | 0.865353% | ni |
| 13515 | 0.808968% | ili |
| 13459 | 0.805616% | kiel |
| 13084 | 0.78317% | sur |
| 12879 | 0.770899% | pri |
| 12186 | 0.729418% | tiu |
| 11704 | 0.700567% | per |
| 11559 | 0.691888% | el |
| 11221 | 0.671656% | mia |
| 10731 | 0.642326% | ŝi |
| 10262 | 0.614253% | pli |
| 10024 | 0.600007% | ĉi |
| 9941 | 0.595039% | tio |
| 8951 | 0.53578% | kiam |
| 8850 | 0.529735% | oni |
| 8444 | 0.505433% | nun |
| 8341 | 0.499268% | tiel |
| 8325 | 0.49831% | nur |
| 8306 | 0.497173% | se |
| 7784 | 0.465927% | ĝi |
| 7660 | 0.458505% | lin |
| 7642 | 0.457428% | diris |
| 7539 | 0.451262% | unu |
| 7532 | 0.450843% | da |
| 6714 | 0.40188% | do |
| 6709 | 0.401581% | sin |
| 6548 | 0.391944% | povas |
| 6482 | 0.387993% | jam |
| 6004 | 0.359382% | plej |
| 5978 | 0.357825% | tie |
| 5904 | 0.353396% | ĝin |
| 5817 | 0.348188% | tre |
| 5813 | 0.347949% | aŭ |
| 5780 | 0.345974% | post |
| 5591 | 0.334661% | jes |
| 5586 | 0.334361% | tion |
| 5518 | 0.330291% | sia |
| 5498 | 0.329094% | pro |
| 5239 | 0.313591% | kiuj |
| 5235 | 0.313352% | ankaŭ |
| 5220 | 0.312454% | ĉar |
| 5204 | 0.311496% | via |
| 5113 | 0.306049% | kion |
| 5069 | 0.303415% | ja |
| 5057 | 0.302697% | sian |
| 5033 | 0.301261% | je |
| 4883 | 0.292282% | dum |
| 4877 | 0.291923% | sinjoro |
| 4825 | 0.28881% | tute |
| 4788 | 0.286596% | ol |
| 4685 | 0.28043% | antaŭ |
| 4557 | 0.272769% | ho |
| 4549 | 0.27229% | jen |
| 4307 | 0.257804% | ĉe |
| 4305 | 0.257685% | kiun |
| 4284 | 0.256428% | havas |
| 4255 | 0.254692% | devas |
| 4196 | 0.25116% | ĉiuj |
| 4183 | 0.250382% | for |
| 4181 | 0.250262% | kio |
| 4168 | 0.249484% | mem |
| 4048 | 0.242301% | tamen |
| 3978 | 0.238111% | ĉu |
| 3941 | 0.235897% | tiam |
| 3927 | 0.235059% | bone |
| 3910 | 0.234041% | tiun |
| 3907 | 0.233861% | mian |
| 3901 | 0.233502% | eĉ |
| 3778 | 0.22614% | du |
| 3736 | 0.223626% | ilin |
| 3667 | 0.219496% | ankoraŭ |
| 3666 | 0.219436% | is |
| 3610 | 0.216084% | eble |
| 3553 | 0.212672% | tiuj |
| 3522 | 0.210817% | volas |
| 3348 | 0.200401% | tuj |
| 3213 | 0.192321% | esperanto |
| 3176 | 0.190106% | estus |
| 3144 | 0.188191% | esti |
| 3134 | 0.187592% | nia |
| 3134 | 0.187592% | kie |
| 3123 | 0.186934% | granda |
| 3112 | 0.186275% | iom |
| 3094 | 0.185198% | nu |
