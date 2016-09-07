# Assignment 1: Evaluate name entity linking

#### Remko Boschker s1282603

This assignment compares the quality of named entity linking using [Open Calais](http://www.opencalais.com/opencalais-demo/) and [DBPedia Spotlight](http://dbpedia-spotlight.github.io/demo/) for two fragments of English text (the Open Calais demonstrator does not support Dutch).

## First text fragment
[Unesco about the Silkroad](http://en.unesco.org/silkroad/about-silk-road)
Indeed, the man who is often credited with founding the Silk Roads by opening up the first route from China to the West in the 2nd century BC, General Zhang Qian, was on a diplomatic mission rather than a trading expedition. Sent to the West in 139 BC by the Han Emperor Wudi to ensure alliances against the Xiongnu, the hereditary enemies of the Chinese, Zhang Qian was captured and imprisoned by them. Thirteen years later he escaped and made his way back to China. Pleased with the wealth of detail and accuracy of his reports, the emperor sent Zhang Qian on another mission in 119 BC to visit several neighbouring peoples, establishing early routes from China to Central Asia.

### Open Calais

Indeed, the man who is often credited with founding the Silk Roads by opening up the first route from <span id="CLFH100007.0" class="CLFCountryCLFHighlight CLFAnyTermHighlight">China</span> to the West in the 2nd century <span id="CLFH100002.0" class="CLFProvinceOrStateCLFHighlight CLFAnyTermHighlight">BC</span>, <span id="CLFH100010.0" class="CLFPersonCareerCLFHighlight CLFAnyEventHighlight"><span id="CLFH100001.0" class="CLFPositionCLFHighlight CLFAnyTermHighlight">General</span> <span id="CLFH100011.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight">Zhang Qian</span></span>, was on a diplomatic mission rather than a trading expedition. Sent to the West in 139 <span id="CLFH100003.0" class="CLFProvinceOrStateCLFHighlight CLFAnyTermHighlight">BC</span> by the Han <span id="CLFH100019.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight"><span id="CLFH100004.0" class="CLFPersonCareerCLFHighlight CLFAnyEventHighlight"><span id="CLFH100017.0" class="CLFPositionCLFHighlight CLFAnyTermHighlight">Emperor</span> Wudi</span></span> to ensure alliances against the Xiongnu, the hereditary enemies of the Chinese, <span id="CLFH100012.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight">Zhang Qian</span> was captured and imprisoned by them. Thirteen years later <span id="CLFH100013.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight">he</span> escaped and made <span id="CLFH100014.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight">his</span> way back to <span id="CLFH100008.0" class="CLFCountryCLFHighlight CLFAnyTermHighlight">China</span>. Pleased with the wealth of detail and accuracy of <span id="CLFH100015.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight">his</span> reports, <span id="CLFH100018.0" class="CLFPositionCLFHighlight CLFAnyTermHighlight">the emperor</span> sent <span id="CLFH100016.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight">Zhang Qian</span> on another mission in 119 BC to visit several neighbouring peoples, establishing early routes from <span id="CLFH100009.0" class="CLFCountryCLFHighlight CLFAnyTermHighlight">China</span> to <span id="CLFH100006.0" class="CLFRegionCLFHighlight CLFAnyTermHighlight"><span id="CLFH100005.0" class="CLFRegionCLFHighlight CLFAnyTermHighlight">Central Asia</span></span>


### DBpedia Spotlight

Indeed, the man who is often credited with founding the [Silk Roads](http://dbpedia.org/resource/Silk_Road) by opening up the first route from [China](http://dbpedia.org/resource/China) to the West in the 2nd century BC, General [Zhang Qian](http://dbpedia.org/resource/Zhang_Qian), was on a [diplomatic mission](http://dbpedia.org/resource/Diplomatic_mission) rather than a trading expedition. Sent to the West in 139 BC by the Han [Emperor Wudi](http://dbpedia.org/resource/Emperor_Wu_of_Han) to ensure alliances against the [Xiongnu](http://dbpedia.org/resource/Xiongnu), the hereditary enemies of the Chinese, [Zhang Qian](http://dbpedia.org/resource/Zhang_Qian) was captured and imprisoned by them. Thirteen years later he escaped and made his way back to [China](http://dbpedia.org/resource/China). Pleased with the wealth of detail and accuracy of his reports, the emperor sent [Zhang Qian](http://dbpedia.org/resource/Zhang_Qian) on another mission in [119 BC](http://dbpedia.org/resource/119_BC) to visit several neighbouring peoples, establishing early routes from [China](http://dbpedia.org/resource/China) to [Central Asia](http://dbpedia.org/resource/Tarim_Basin).


### Additional annotations

## Second text fragment
[the Guardian about a new series of the Cold Feet tv series](https://www.theguardian.com/media/2016/sep/06/cold-feet-gets-warm-welcome-as-6m-tune-in-for-new-series)
It was 13 years since Cold Feet last aired new episodes, but the sitcom’s fans proved as loyal as ever with more than 6 million tuning in to its return on Monday night.

The return of the comedy, which stars James Nesbitt, Hermione Morris, John Thomson and Robert Bathurst, drew an average audience of 6.1 million and a 29% share of all TV viewing between 9pm and 10pm.

The show, which tells the tale of three thirtysomething couples in Manchester, originally ran for five series between 1998 and 2003.

It was one of ITV’s biggest showsat the time, described by some as the UK’s answer to Friends or Thirtysomething, with almost 11 million viewers tuning into its tear-stained finale.

ITV will be pleased with the popularity of the first episode of the eight-part series even if Kevin Lygo, the broadcaster’s new director of television, told an audience at the Edinburgh TV festival that he was not completely sure he would have commissioned its revival.

The show easily won the 9pm slot on Monday night, albeit not against the strongest of competition with BBC1 airing Crimewatch, BBC2 Ripper Street and Channel 4 999: What’s Your Emergency?

### Open Calais
It was 13 years since Cold Feet last aired new episodes, but the sitcom’s fans proved as loyal as ever with more than 6 million tuning in to its return on Monday night.

The return of the comedy, which stars <span id="CLFH100017.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight">James Nesbitt</span>, <span id="CLFH100006.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight">Hermione Morris</span>, <span id="CLFH100007.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight">John Thomson</span> and <span id="CLFH100013.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight">Robert Bathurst</span>, drew an average audience of 6.1 million and a 29% share of all TV viewing between 9pm and 10pm.

The show, which tells the tale of three thirtysomething couples in <span id="CLFH100001.0" class="CLFCityCLFHighlight CLFAnyTermHighlight">Manchester</span>, originally ran for five series between 1998 and 2003.

It was one of <span id="CLFH100003.0" class="CLFCompanyCLFHighlight CLFAnyTermHighlight">ITV</span>’s biggest showsat the time, described by some as the <span id="CLFH100014.0" class="CLFCountryCLFHighlight CLFAnyTermHighlight">UK</span>’s answer to Friends or Thirtysomething, with almost 11 million viewers tuning into its tear-stained finale.

<span id="CLFH100012.0" class="CLFQuotationCLFHighlight CLFAnyEventHighlight"><span id="CLFH100004.0" class="CLFCompanyCLFHighlight CLFAnyTermHighlight">ITV</span> will be pleased with the popularity of the first episode of the eight-part series even if <span id="CLFH100011.0" class="CLFPersonCareerCLFHighlight CLFAnyEventHighlight"><span id="CLFH100008.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight">Kevin Lygo</span>, the broadcaster’s new <span id="CLFH100016.0" class="CLFPositionCLFHighlight CLFAnyTermHighlight">director</span></span><span id="CLFH100016.1" class="CLFPositionCLFHighlight CLFAnyTermHighlight"> of television</span>, told <span id="CLFH100005.0" class="CLFPersonLocationCLFHighlight CLFAnyEventHighlight">an audience at <span id="CLFH100002.0" class="CLFEntertainmentAwardEventCLFHighlight CLFAnyTermHighlight">the <span id="CLFH100015.0" class="CLFCityCLFHighlight CLFAnyTermHighlight">Edinburgh</span></span></span><span id="CLFH100002.1" class="CLFEntertainmentAwardEventCLFHighlight CLFAnyTermHighlight"> TV festival</span> that <span id="CLFH100009.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight">he</span> was not completely sure <span id="CLFH100010.0" class="CLFPersonCLFHighlight CLFAnyTermHighlight">he</span> would have commissioned its revival.</span>

The show easily won the 9pm slot on Monday night, albeit not against the strongest of competition with BBC1 airing Crimewatch, BBC2 Ripper Street and Channel 4 999: What’s Your Emergency?

### DBpedia Spotlight

It was 13 years since [Cold Feet](http://dbpedia.org/resource/Pilot_(Cold_Feet)) last aired new episodes, but the [sitcom](http://dbpedia.org/resource/Sitcom)'s fans proved as loyal as ever with more than 6 million [tuning](http://dbpedia.org/resource/Tuner_(radio)) in to its return on Monday night.

The return of the comedy, which stars [James Nesbitt](http://dbpedia.org/resource/James_Nesbitt), [Hermione](http://dbpedia.org/resource/Hermione_Granger) Morris, [John Thomson](http://dbpedia.org/resource/John_Thomson_(comedian)) and [Robert Bathurst](http://dbpedia.org/resource/Robert_Bathurst), drew an average audience of 6.1 million and a 29% share of all TV viewing between 9pm and 10pm.

The show, which tells the tale of three [thirtysomething](http://dbpedia.org/resource/Thirtysomething_(TV_series)) couples in [Manchester](http://dbpedia.org/resource/Manchester), originally ran for five series between 1998 and 2003.

It was one of [ITV](http://dbpedia.org/resource/ITV_(TV_network))'s biggest showsat the time, described by some as the [UK](http://dbpedia.org/resource/United_Kingdom)'s answer to Friends or [Thirtysomething](http://dbpedia.org/resource/Thirtysomething_(TV_series)), with almost 11 million viewers [tuning](http://dbpedia.org/resource/Tuner_(radio)) into its tear-stained finale.

[ITV](http://dbpedia.org/resource/ITV_(TV_network)) will be pleased with the popularity of the first episode of the eight-part series even if [Kevin Lygo](http://dbpedia.org/resource/Kevin_Lygo), the broadcaster's new director of television, told an audience at the [Edinburgh TV festival](http://dbpedia.org/resource/Edinburgh_International_Television_Festival) that he was not completely sure he would have [commissioned](http://dbpedia.org/resource/Green-light) its revival.

The show easily won the 9pm slot on Monday night, albeit not against the strongest of competition with [BBC1](http://dbpedia.org/resource/BBC_One) airing [Crimewatch](http://dbpedia.org/resource/Crimewatch), [BBC2](http://dbpedia.org/resource/BBC_Two) [Ripper Street](http://dbpedia.org/resource/Ripper_Street) and [Channel 4](http://dbpedia.org/resource/Channel_4) 999: What's Your Emergency?

### Additional annotations

## Counts and discussion
