# Assignment 1: Evaluate name entity linking

#### Remko Boschker s1282603

This assignment compares the quality of named entity linking using [Open Calais](http://www.opencalais.com/opencalais-demo/) and [DBPedia Spotlight](http://dbpedia-spotlight.github.io/demo/) for two fragments of English text (the Open Calais demonstrator does not support Dutch).

Sometimes recognizing amounts, dates, distances etc. is considered part of this task. It is not included here.

For Open Calais I have added the type of named entity that is encoded in the html in square brackets. Open Calais also does pronoun resolution. It works correctly and is not taken into account. Open Calais has a sophisticated recognition of positions and careers. However I have not included them in the named entity recognition task because they are not proper names or biological kinds or substances.

DBpedia Spotlight does not categorize the named entities found. If the entity found refers to the correct DBpedia page it is counted as correct. I have added the type in square brackets manually.

## First text fragment
[Unesco about the Silkroad](http://en.unesco.org/silkroad/about-silk-road)
Indeed, the man who is often credited with founding the Silk Roads by opening up the first route from China to the West in the 2nd century BC, General Zhang Qian, was on a diplomatic mission rather than a trading expedition. Sent to the West in 139 BC by the Han Emperor Wudi to ensure alliances against the Xiongnu, the hereditary enemies of the Chinese, Zhang Qian was captured and imprisoned by them. Thirteen years later he escaped and made his way back to China. Pleased with the wealth of detail and accuracy of his reports, the emperor sent Zhang Qian on another mission in 119 BC to visit several neighbouring peoples, establishing early routes from China to Central Asia.

### Open Calais

Indeed, the man who is often credited with founding the Silk Roads by opening up the first route from <span id="CLFH100007.0" class="CLFCountryCLFHighlight CLFAnyTermHighlight">China [country]</span> to the West in the 2nd century <span id="CLFH100002.0" class="CLFProvinceOrStateCLFHighlight CLFAnyTermHighlight">BC [province or state]</span>, <span id="CLFH100010.0" class="CLFPersonCareerCLFHighlight CLFAnyEventHighlight"><span id="CLFH100001.0" class="CLFPositionCLFHighlight CLFAnyTermHighlight">General </span> <span id="CLFH100011.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight">Zhang Qian [person]</span></span>, was on a diplomatic mission rather than a trading expedition. Sent to the West in 139 <span id="CLFH100003.0" class="CLFProvinceOrStateCLFHighlight CLFAnyTermHighlight">BC [province or state]</span> by the Han <span id="CLFH100019.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight"><span id="CLFH100004.0" class="CLFPersonCareerCLFHighlight CLFAnyEventHighlight"><span id="CLFH100017.0" class="CLFPositionCLFHighlight CLFAnyTermHighlight">Emperor </span> Wudi [person]</span></span> to ensure alliances against the Xiongnu, the hereditary enemies of the Chinese, <span id="CLFH100012.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight">Zhang Qian [person]</span> was captured and imprisoned by them. Thirteen years later <span id="CLFH100013.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight">he [person]</span> escaped and made <span id="CLFH100014.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight">his [person]</span> way back to <span id="CLFH100008.0" class="CLFCountryCLFHighlight CLFAnyTermHighlight">China [country]</span>. Pleased with the wealth of detail and accuracy of <span id="CLFH100015.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight">his [person]</span> reports, <span id="CLFH100018.0" class="CLFPositionCLFHighlight CLFAnyTermHighlight">the emperor </span> sent <span id="CLFH100016.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight">Zhang Qian [person]</span> on another mission in 119 BC to visit several neighbouring peoples, establishing early routes from <span id="CLFH100009.0" class="CLFCountryCLFHighlight CLFAnyTermHighlight">China [country]</span> to <span id="CLFH100006.0" class="CLFRegionCLFHighlight CLFAnyTermHighlight"><span id="CLFH100005.0" class="CLFRegionCLFHighlight CLFAnyTermHighlight">Central Asia [region]</span></span>


### DBpedia Spotlight

Indeed, the man who is often credited with founding the [Silk Roads](http://dbpedia.org/resource/Silk_Road) __[geographical feature]__ by opening up the first route from [China](http://dbpedia.org/resource/China) __[country]__ to the West in the 2nd century BC, General [Zhang Qian](http://dbpedia.org/resource/Zhang_Qian) __[person]__, was on a [diplomatic mission](http://dbpedia.org/resource/Diplomatic_mission) __[not a named entity]__ rather than a trading expedition. Sent to the West in 139 BC by the Han [Emperor Wudi](http://dbpedia.org/resource/Emperor_Wu_of_Han) __[person]__ to ensure alliances against the [Xiongnu](http://dbpedia.org/resource/Xiongnu) __[people]__, the hereditary enemies of the Chinese, [Zhang Qian](http://dbpedia.org/resource/Zhang_Qian) __[person]__ was captured and imprisoned by them. Thirteen years later he escaped and made his way back to [China](http://dbpedia.org/resource/China) __[country]__. Pleased with the wealth of detail and accuracy of his reports, the emperor sent [Zhang Qian](http://dbpedia.org/resource/Zhang_Qian) __[person]__ on another mission in [119 BC](http://dbpedia.org/resource/119_BC) __[not a named entity]__ to visit several neighbouring peoples, establishing early routes from [China](http://dbpedia.org/resource/China) __[country]__ to [Central Asia](http://dbpedia.org/resource/Tarim_Basin) __[region incorrect]__.

### Manual Annotation

Indeed, the man who is often credited with founding the Silk Roads __[geographical feature]__ by opening up the first route from China __[country]__ to the West __[region]__ in the 2nd century BC, General  Zhang Qian __[person]__, was on a diplomatic mission rather than a trading expedition. Sent to the West __[region]__ in 139 BC by the Han __[people]__ Emperor  Wudi __[person]__ to ensure alliances against the Xiongnu __[people]__, the hereditary enemies of the Chinese __[people]__, Zhang Qian __[person]__ was captured and imprisoned by them. Thirteen years later he escaped and made his way back to China __[country]__. Pleased with the wealth of detail and accuracy of his reports, the emperor sent Zhang Qian __[person]__ on another mission in 119 BC to visit several neighbouring peoples, establishing early routes from China __[country]__ to Central Asia __[region]__.

## Second text fragment
[the Guardian about a new series of the Cold Feet tv series](https://www.theguardian.com/media/2016/sep/06/cold-feet-gets-warm-welcome-as-6m-tune-in-for-new-series)
It was 13 years since Cold Feet last aired new episodes, but the sitcom’s fans proved as loyal as ever with more than 6 million tuning in to its return on Monday night.

The return of the comedy, which stars James Nesbitt, Hermione Morris, John Thomson and Robert Bathurst, drew an average audience of 6.1 million and a 29% share of all TV viewing between 9pm and 10pm.

The show, which tells the tale of three thirtysomething couples in Manchester, originally ran for five series between 1998 and 2003.

It was one of ITV’s biggest shows at the time, described by some as the UK’s answer to Friends or Thirtysomething, with almost 11 million viewers tuning into its tear-stained finale.

ITV will be pleased with the popularity of the first episode of the eight-part series even if Kevin Lygo, the broadcaster’s new director of television, told an audience at the Edinburgh TV festival that he was not completely sure he would have commissioned its revival.

The show easily won the 9pm slot on Monday night, albeit not against the strongest of competition with BBC1 airing Crimewatch, BBC2 Ripper Street and Channel 4 999: What’s Your Emergency?

### Open Calais
It was 13 years since Cold Feet last aired new episodes, but the sitcom’s fans proved as loyal as ever with more than 6 million tuning in to its return on Monday night.

The return of the comedy, which stars <span id="CLFH100017.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight">James Nesbitt [person]</span>, <span id="CLFH100006.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight">Hermione Morris [person]</span>, <span id="CLFH100007.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight">John Thomson [person]</span> and <span id="CLFH100013.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight">Robert Bathurst [person]</span>, drew an average audience of 6.1 million and a 29% share of all TV viewing between 9pm and 10pm.

The show, which tells the tale of three thirtysomething couples in <span id="CLFH100001.0" class="CLFCityCLFHighlight CLFAnyTermHighlight">Manchester [city]</span>, originally ran for five series between 1998 and 2003.

It was one of <span id="CLFH100003.0" class="CLFCompanyCLFHighlight CLFAnyTermHighlight">ITV [organisation]</span>’s biggest shows at the time, described by some as the <span id="CLFH100014.0" class="CLFCountryCLFHighlight CLFAnyTermHighlight">UK [country]</span>’s answer to Friends or Thirtysomething, with almost 11 million viewers tuning into its tear-stained finale.

<span id="CLFH100012.0" class="CLFQuotationCLFHighlight CLFAnyEventHighlight"><span id="CLFH100004.0" class="CLFCompanyCLFHighlight CLFAnyTermHighlight">ITV [organization]</span> will be pleased with the popularity of the first episode of the eight-part series even if <span id="CLFH100011.0" class="CLFPersonCareerCLFHighlight CLFAnyEventHighlight"><span id="CLFH100008.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight">Kevin Lygo [person]</span>, the broadcaster’s new <span id="CLFH100016.0" class="CLFPositionCLFHighlight CLFAnyTermHighlight">director</span></span><span id="CLFH100016.1" class="CLFPositionCLFHighlight CLFAnyTermHighlight"> of television </span>, told <span id="CLFH100005.0" class="CLFPersonLocationCLFHighlight CLFAnyEventHighlight">an audience at <span id="CLFH100002.0" class="CLFEntertainmentAwardEventCLFHighlight CLFAnyTermHighlight">the <span id="CLFH100015.0" class="CLFCityCLFHighlight CLFAnyTermHighlight">Edinburgh</span></span></span><span id="CLFH100002.1" class="CLFEntertainmentAwardEventCLFHighlight CLFAnyTermHighlight"> TV festival [event]</span> that <span id="CLFH100009.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight">he [person]</span> was not completely sure <span id="CLFH100010.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight">he [person]</span> would have commissioned its revival.</span>

The show easily won the 9pm slot on Monday night, albeit not against the strongest of competition with BBC1 airing Crimewatch, BBC2 Ripper Street and Channel 4 999: What’s Your Emergency?

### DBpedia Spotlight

It was 13 years since [Cold Feet](http://dbpedia.org/resource/Pilot_(Cold_Feet)) __[product]__ last aired new episodes, but the [sitcom](http://dbpedia.org/resource/Sitcom) __[not a named entity]__'s fans proved as loyal as ever with more than 6 million [tuning](http://dbpedia.org/resource/Tuner_(radio)) __[not a named entity]__ in to its return on Monday night.

The return of the comedy, which stars [James Nesbitt](http://dbpedia.org/resource/James_Nesbitt) __[person]__, [Hermione](http://dbpedia.org/resource/Hermione_Granger) Morris __[person incorrect]__, [John Thomson](http://dbpedia.org/resource/John_Thomson_(comedian)) __[person]__ and [Robert Bathurst](http://dbpedia.org/resource/Robert_Bathurst) __[person]__, drew an average audience of 6.1 million and a 29% share of all TV viewing between 9pm and 10pm.

The show, which tells the tale of three [thirtysomething](http://dbpedia.org/resource/Thirtysomething_(TV_series)) __[product incorrect]__ couples in [Manchester](http://dbpedia.org/resource/Manchester) __[city]__, originally ran for five series between 1998 and 2003.

It was one of [ITV](http://dbpedia.org/resource/ITV_(TV_network)) __[organisation]__ 's biggest shows at the time, described by some as the [UK](http://dbpedia.org/resource/United_Kingdom) __[country]__'s answer to Friends or [Thirtysomething](http://dbpedia.org/resource/Thirtysomething_(TV_series)) __[product]__, with almost 11 million viewers [tuning](http://dbpedia.org/resource/Tuner_(radio)) __[not a named entity]__ into its tear-stained finale.

[ITV](http://dbpedia.org/resource/ITV_(TV_network)) __[organisation]__ the first episode of the eight-part series even if [Kevin Lygo](http://dbpedia.org/resource/Kevin_Lygo) __[person]__, the broadcaster's new director of television, told an audience at the [Edinburgh TV festival](http://dbpedia.org/resource/Edinburgh_International_Television_Festival) __[event]__ that he was not completely sure he would have [commissioned](http://dbpedia.org/resource/Green-light) __[not a named entity]__ its revival.

The show easily won the 9pm slot on Monday night, albeit not against the strongest of competition with [BBC1](http://dbpedia.org/resource/BBC_One) __[product]__ airing [Crimewatch](http://dbpedia.org/resource/Crimewatch) __[product]__, [BBC2](http://dbpedia.org/resource/BBC_Two) __[product]__ [Ripper Street](http://dbpedia.org/resource/Ripper_Street) __[product]__ and [Channel 4](http://dbpedia.org/resource/Channel_4) __[product]__ 999: What's Your Emergency?

### Manual Annotation

It was 13 years since Cold Feet __[product]__ last aired new episodes, but the sitcom’s fans proved as loyal as ever with more than 6 million tuning in to its return on Monday night.

The return of the comedy, which stars James Nesbitt __[person]__, Hermione Morris __[person]__, John Thomson __[person]__ and Robert Bathurst __[person]__, drew an average audience of 6.1 million and a 29% share of all TV viewing between 9pm and 10pm.

The show, which tells the tale of three thirtysomething couples in Manchester __[city]__, originally ran for five series between 1998 and 2003.

It was one of ITV’s __[organisation]__ biggest shows at the time, described by some as the UK’s __[country]__ answer to Friends __[product]__ or Thirtysomething __[product]__, with almost 11 million viewers tuning into its tear-stained finale.

ITV __[organisation]__ will be pleased with the popularity of the first episode of the eight-part series even if Kevin Lygo __[person]__, the broadcaster’s new director of television ____, told an audience at the Edinburgh TV festival __[event]__ that he was not completely sure he would have commissioned its revival.

The show easily won the 9pm slot on Monday night, albeit not against the strongest of competition with BBC1 __[product]__ airing Crimewatch __[product]__, BBC2 __[product]__ Ripper Street __[product]__ and Channel 4 __[product]__ 999: What’s Your Emergency __[product]__?

## Counts and discussion

In the table below the annotations are counted. Values are presented in a table cell as [ correct/wrong/missed ].

| type | text1 manual | text1 Open Calais | text1 DBpedia Spotlight  | text2 manual | text2 Open Calais | text2 DBpedia Spotlight |
| ---| :-:| :-:|:-:| :-: |:-:|:-: |
| person | 4 | 4/0/0 | 4/0/0 | 5 | 5/0/0 | 4/1/0 |
| people | 3 | 0/0/3 | 1/0/2 | - | - | - |
| city | - | - | - | 1 | 1/0/0 | 1/0/0 |
| region | 3 | 1/0/2 | 0/1/2 | - | - | - |
| province or state | - | 0/2/0 | - | - | - | - |
| country | 3 | 3/0/0 | 3/0/0 | 1 | 1/0/0 | 1/0/0 |
| geographical feature | 1 | 0/0/1 | 1/0/0 | - | - | - |
| event | - | - | - | 1 | 1/0/0 | 1/0/0 |
| organization | - | - | - | 2 | 2/0/0 | 2/0/0 |
| product | - | - | - | 9 | 0/0/9 | 7/1/1 |
| not a named entity | - | 0/0/0 | 0/2/0 | - | 0/0/0 | 0/3/0 |
| __total__ | __14__ | __8/2/6__ | __9/3/4__ | __19__ | __10/0/9__ | __17/5/1__ |


Recognizing people, cities, countries and organizations appears to be working well with almost no errors. However the more abstract _the Chinese_ or _the West_ are missed by both systems.

Open Calais mistakes BC (before Christ) in a date for British Columbia and does not recognize the names of television series or broadcast channels at all.

DPpedia Spotlight appears to sometimes create a reference to a page for a word that is not a named entity, but it does not create a reference for any noun that presumably has a DPpedia entry.
