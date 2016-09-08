# Assignment 1: Evaluate name entity linking

#### Remko Boschker s1282603

This assignment compares the quality of named entity linking using [Open Calais](http://www.opencalais.com/opencalais-demo/) and [DBPedia Spotlight](http://dbpedia-spotlight.github.io/demo/) for two fragments of English text (the Open Calais demonstrator does not support Dutch).

Sometimes recognizing amounts, dates, distances etc. is considered part of this task. It is not included here.

## First text fragment
[Unesco about the Silkroad](http://en.unesco.org/silkroad/about-silk-road)
Indeed, the man who is often credited with founding the Silk Roads by opening up the first route from China to the West in the 2nd century BC, General Zhang Qian, was on a diplomatic mission rather than a trading expedition. Sent to the West in 139 BC by the Han Emperor Wudi to ensure alliances against the Xiongnu, the hereditary enemies of the Chinese, Zhang Qian was captured and imprisoned by them. Thirteen years later he escaped and made his way back to China. Pleased with the wealth of detail and accuracy of his reports, the emperor sent Zhang Qian on another mission in 119 BC to visit several neighbouring peoples, establishing early routes from China to Central Asia.

### Open Calais

Indeed, the man who is often credited with founding the Silk Roads by opening up the first route from <span id="CLFH100007.0" class="CLFCountryCLFHighlight CLFAnyTermHighlight">China [country]</span> to the West in the 2nd century <span id="CLFH100002.0" class="CLFProvinceOrStateCLFHighlight CLFAnyTermHighlight">BC [province or state]</span>, <span id="CLFH100010.0" class="CLFPersonCareerCLFHighlight CLFAnyEventHighlight"><span id="CLFH100001.0" class="CLFPositionCLFHighlight CLFAnyTermHighlight">General [postion]</span> <span id="CLFH100011.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight">Zhang Qian [person]</span></span>, was on a diplomatic mission rather than a trading expedition. Sent to the West in 139 <span id="CLFH100003.0" class="CLFProvinceOrStateCLFHighlight CLFAnyTermHighlight">BC [province or state]</span> by the Han <span id="CLFH100019.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight"><span id="CLFH100004.0" class="CLFPersonCareerCLFHighlight CLFAnyEventHighlight"><span id="CLFH100017.0" class="CLFPositionCLFHighlight CLFAnyTermHighlight">Emperor [position]</span> Wudi [person]</span></span> to ensure alliances against the Xiongnu, the hereditary enemies of the Chinese, <span id="CLFH100012.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight">Zhang Qian [person]</span> was captured and imprisoned by them. Thirteen years later <span id="CLFH100013.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight">he [person]</span> escaped and made <span id="CLFH100014.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight">his [person]</span> way back to <span id="CLFH100008.0" class="CLFCountryCLFHighlight CLFAnyTermHighlight">China [country]</span>. Pleased with the wealth of detail and accuracy of <span id="CLFH100015.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight">his [person]</span> reports, <span id="CLFH100018.0" class="CLFPositionCLFHighlight CLFAnyTermHighlight">the emperor [position]</span> sent <span id="CLFH100016.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight">Zhang Qian [person]</span> on another mission in 119 BC to visit several neighbouring peoples, establishing early routes from <span id="CLFH100009.0" class="CLFCountryCLFHighlight CLFAnyTermHighlight">China [country]</span> to <span id="CLFH100006.0" class="CLFRegionCLFHighlight CLFAnyTermHighlight"><span id="CLFH100005.0" class="CLFRegionCLFHighlight CLFAnyTermHighlight">Central Asia [region]</span></span>


### DBpedia Spotlight

Indeed, the man who is often credited with founding the [Silk Roads](http://dbpedia.org/resource/Silk_Road) by opening up the first route from [China](http://dbpedia.org/resource/China) to the West in the 2nd century BC, General [Zhang Qian](http://dbpedia.org/resource/Zhang_Qian), was on a [diplomatic mission](http://dbpedia.org/resource/Diplomatic_mission) rather than a trading expedition. Sent to the West in 139 BC by the Han [Emperor Wudi](http://dbpedia.org/resource/Emperor_Wu_of_Han) to ensure alliances against the [Xiongnu](http://dbpedia.org/resource/Xiongnu), the hereditary enemies of the Chinese, [Zhang Qian](http://dbpedia.org/resource/Zhang_Qian) was captured and imprisoned by them. Thirteen years later he escaped and made his way back to [China](http://dbpedia.org/resource/China). Pleased with the wealth of detail and accuracy of his reports, the emperor sent [Zhang Qian](http://dbpedia.org/resource/Zhang_Qian) on another mission in [119 BC](http://dbpedia.org/resource/119_BC) to visit several neighbouring peoples, establishing early routes from [China](http://dbpedia.org/resource/China) to [Central Asia](http://dbpedia.org/resource/Tarim_Basin).

### Manual Annotation

Indeed, the man who is often credited with founding the Silk Roads __[geographical feature]__ by opening up the first route from China __[country]__ to the West __[region]__ in the 2nd century BC, General __[position]__ Zhang Qian __[person]__, was on a diplomatic mission rather than a trading expedition. Sent to the West __[region]__ in 139 BC by the Han __[people]__ Emperor __[position]__ Wudi __[person]__ to ensure alliances against the Xiongnu __[people]__, the hereditary enemies of the Chinese __[people]__, Zhang Qian __[person]__ was captured and imprisoned by them. Thirteen years later he escaped and made his way back to China __[country]__. Pleased with the wealth of detail and accuracy of his reports, the emperor sent Zhang Qian __[person]__ on another mission in 119 BC to visit several neighbouring peoples, establishing early routes from China __[country]__ to Central Asia __[region]__.

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

<span id="CLFH100012.0" class="CLFQuotationCLFHighlight CLFAnyEventHighlight"><span id="CLFH100004.0" class="CLFCompanyCLFHighlight CLFAnyTermHighlight">ITV [organization]</span> will be pleased with the popularity of the first episode of the eight-part series even if <span id="CLFH100011.0" class="CLFPersonCareerCLFHighlight CLFAnyEventHighlight"><span id="CLFH100008.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight">Kevin Lygo [person]</span>, the broadcaster’s new <span id="CLFH100016.0" class="CLFPositionCLFHighlight CLFAnyTermHighlight">director</span></span><span id="CLFH100016.1" class="CLFPositionCLFHighlight CLFAnyTermHighlight"> of television [position]</span>, told <span id="CLFH100005.0" class="CLFPersonLocationCLFHighlight CLFAnyEventHighlight">an audience at <span id="CLFH100002.0" class="CLFEntertainmentAwardEventCLFHighlight CLFAnyTermHighlight">the <span id="CLFH100015.0" class="CLFCityCLFHighlight CLFAnyTermHighlight">Edinburgh</span></span></span><span id="CLFH100002.1" class="CLFEntertainmentAwardEventCLFHighlight CLFAnyTermHighlight"> TV festival [entertainment award event]</span> that <span id="CLFH100009.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight">he [person]</span> was not completely sure <span id="CLFH100010.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight">he [person]</span> would have commissioned its revival.</span>

The show easily won the 9pm slot on Monday night, albeit not against the strongest of competition with BBC1 airing Crimewatch, BBC2 Ripper Street and Channel 4 999: What’s Your Emergency?

### DBpedia Spotlight

It was 13 years since [Cold Feet](http://dbpedia.org/resource/Pilot_(Cold_Feet)) last aired new episodes, but the [sitcom](http://dbpedia.org/resource/Sitcom)'s fans proved as loyal as ever with more than 6 million [tuning](http://dbpedia.org/resource/Tuner_(radio)) in to its return on Monday night.

The return of the comedy, which stars [James Nesbitt](http://dbpedia.org/resource/James_Nesbitt), [Hermione](http://dbpedia.org/resource/Hermione_Granger) Morris, [John Thomson](http://dbpedia.org/resource/John_Thomson_(comedian)) and [Robert Bathurst](http://dbpedia.org/resource/Robert_Bathurst), drew an average audience of 6.1 million and a 29% share of all TV viewing between 9pm and 10pm.

The show, which tells the tale of three [thirtysomething](http://dbpedia.org/resource/Thirtysomething_(TV_series)) couples in [Manchester](http://dbpedia.org/resource/Manchester), originally ran for five series between 1998 and 2003.

It was one of [ITV](http://dbpedia.org/resource/ITV_(TV_network))'s biggest shows at the time, described by some as the [UK](http://dbpedia.org/resource/United_Kingdom)'s answer to Friends or [Thirtysomething](http://dbpedia.org/resource/Thirtysomething_(TV_series)), with almost 11 million viewers [tuning](http://dbpedia.org/resource/Tuner_(radio)) into its tear-stained finale.

[ITV](http://dbpedia.org/resource/ITV_(TV_network)) will be pleased with the popularity of the first episode of the eight-part series even if [Kevin Lygo](http://dbpedia.org/resource/Kevin_Lygo), the broadcaster's new director of television, told an audience at the [Edinburgh TV festival](http://dbpedia.org/resource/Edinburgh_International_Television_Festival) that he was not completely sure he would have [commissioned](http://dbpedia.org/resource/Green-light) its revival.

The show easily won the 9pm slot on Monday night, albeit not against the strongest of competition with [BBC1](http://dbpedia.org/resource/BBC_One) airing [Crimewatch](http://dbpedia.org/resource/Crimewatch), [BBC2](http://dbpedia.org/resource/BBC_Two) [Ripper Street](http://dbpedia.org/resource/Ripper_Street) and [Channel 4](http://dbpedia.org/resource/Channel_4) 999: What's Your Emergency?

### Manual Annotation

It was 13 years since Cold Feet __[product]__ last aired new episodes, but the sitcom’s fans proved as loyal as ever with more than 6 million tuning in to its return on Monday night.

The return of the comedy, which stars James Nesbitt __[person]__, Hermione Morris __[person]__, John Thomson __[person]__ and Robert Bathurst __[person]__, drew an average audience of 6.1 million and a 29% share of all TV viewing between 9pm and 10pm.

The show, which tells the tale of three thirtysomething couples in Manchester __[city]__, originally ran for five series between 1998 and 2003.

It was one of ITV’s __[organisation]__ biggest shows at the time, described by some as the UK’s __[country]__ answer to Friends __[product]__ or Thirtysomething __[product]__, with almost 11 million viewers tuning into its tear-stained finale.

ITV __[organisation]__ will be pleased with the popularity of the first episode of the eight-part series even if Kevin Lygo __[person]__, the broadcaster’s new director of television __[postion]__, told an audience at the Edinburgh TV festival __[event]__ that he was not completely sure he would have commissioned its revival.

The show easily won the 9pm slot on Monday night, albeit not against the strongest of competition with BBC1 __[product]__ airing Crimewatch __[product]__, BBC2 __[product]__ Ripper Street __[product]__ and Channel 4 __[product]__ 999: What’s Your Emergency __[product]__?

## Counts and discussion

DBpedia Spotlight does not categorize the named entities found. If the entity found refers to the correct DBpedia page it is counted as correct. Open Calais also does pronoun resolution. It works correctly and is not taken into account.

In the table below the annotations are counted. Values are presented in a table cell as | correct / wrong |.

type correct | text1 manual | text1 Open Calais | text1 DBpedia Spotlight  | text2 Open Calais | text2 DBpedia Spotlight | text2 manual |
---| :-:| :-:|:-:| :-: |:-:|:-:
person | 4/0 | 4/0 | 4/0 |
people | 3/0 | 0/0 | 1/0
city | 0/0 | 0/0 | 0/0 |
region | 3/0 | 1/0 | 0/1 |
province or state | 0/0 | 0/2 | 0/0 |
country | 3/0 | 3/0 | 3/0 |
geographical feature | 1/0 | 0/0 | 1/0
event | 0/0 | 0/0 | 0/0 |
position | 2/0 | 2/1 | 0/0 |
organization | 0/0 | 0/0 | 0/0 |
product | 0/0 | 0/0 | 0/0 |
no named entity | 0 | 0 | 2 |

### Open Calais text 1

Should position be considered a named entity?

the emperor vs Emperor Wu
BC British Colombia in stead of before Christ.
The Chinese and the West are not.

### DBpedia

[diplomatic mission] and [113 BC] are recognized. The Chinese and the West are not.
