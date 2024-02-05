## Formål
Hovedformålet for annoteringsarbeidet er at vi skal lage et datasett der vi dokumenterer sentimentet mot entiteter som forekommer i et dokumentent.

## Detaljgrad for annoteringene
- For hver entitet skal du angi hvilket sentiment dokumentet som helhet formidler mot denne entiteten.
- Vi skiller mellom 2 nivåer i intensitet for hvert sentiment target. "Slight" brukes når sentimentet er svakt, men også når det er vagt eller usikkert, men ikke nøytralt.
- "Neutral" brukes for alle entiteter som bare er nevnt i teksten, uten at teksten formidler noe spesielt sentiment mot entiteten.
- Faktaopplysninger uten videre uttrykt sentiment skal ikke tolkes som sentimentbærende.
- Annoteringa skal ikke ta utenomkunnskap om entiteten i hensyn.
- Ironi og sarkasme skal ikke tas hensyn til. Hvis vi leser teksten som negativ, annoterer vi den som negativ.

## Sentimentbærende relasjoner
- Der entiteten omtales anaforisk skal sentimentet også tas med.
- Der en entitet i teksten er medlem av en større entitet, som en gruppe eller organisasjon, kan sentiment mot medlemmet påvirke sentimentet mot den større entiteten.
- Sentiment rettet mot ting skapt av entiteten vi annoterer for kan også påvirke sentimentet mot hovedentiteten.



## Eksempel
Følgende er et utdrag fra et eksempel på annotering av sentiment mot entitetene "Thirty Seconds To Mars" og "Jared Leto". Dette er fra en konsertameldelse. Jared Leto er forgrunnsfiguren av bandet Thirty Seconds To Mars. Alle annotasjonene er ikke nevnt i notatene under. Først kommer den relevante linja fra teksten, så en kommentar på utledet sentiment.

### Entitet "Thirty Seconds To Mars" (Bandet):
```
10: Alt det andre artister og band sparer til forestillingens siste halvtime , brenner Jared Leto og hans Thirty Seconds To Mars av i løpet av den første .
>> Tolkes som negative-slight for "Thirty Seconds To Mars".

26: Men han har nå en gang bygd seg dette absurde rocksirkuset , sammen med den ett år eldre broren Shannon ( trommer ) og gitaristen Tomo Milicevic , og er fast bestemt på å ha det gøy i det .
>> Bandet nevnes anaforisk her med "rocksirkuset". Bandet er først og fremst beskrevet som absurd, og tolkes derfor som negative-slight.

28: Musikken de lager er komplett ubetydelig , en saus av « emo » , industriell rock , « nu metal » og god , gammeldags arenarock , dandert med latterlige tekstklisjeer .
>> Sentimentet i setningen har "musikken" som direkte target, som smitter over på de som lager den, som her blir bandet. Dette tolkes som negaitve-standard.

31: « Night Of The Hunter » og « Search And Destroy » er begge ganske effektive , og « Kings And Queens » - med bandets aller beste « oh oh oh » -refreng , melkes for alt den er verdt .
>> Igjen er det snakk om noe bandet har laget. Her tolkes det som positive-slight.

42: En sjarmerende klønete versjon av Rihannas « Stay » , fremført sammen med resten av bandet , redder stumpene .
>> Positive-slight for anaforen "bandet".

47: Leto og bandet hans liker å gi inntrykk av at de snakker om vektige , viktige saker .
>> Negative-standard for anaforen "bandet".

54: Thirty Seconds To Mars er en hobby , et eksperiment i autoritær kitsch .
>> Kan tolkes som et "slight" sentiment, men grenser mot å være nøytralt. 
```
Sammenlagt lander vi på negative-standard for entiteten "Thirty Seconds To Mars".

### Entitet "Jared Leto"
```
05: Om nøyaktig én uke kan Jared Leto ( 42 ) vinne Oscar for noe langt mer betydningsfullt enn det riktignok festlige og fargerike tullballet han bedrev på scenen i Oslo søndag kveld .
>> Selv om det fargerike tullballet er det som anmeldes i teksten, annoterer vi nå med hensyn til entiteten "Jared Leto". Det positive sentimentet tilknyttet Oscar veier derfor sterkere mot ham i denne setningen og vi utleder et positive-standard-sentiment mot "Jared Leto".

12: Han befaler oss å « jump , jump ! » og « make some noise » ustanselig .
>> Ordet "ustanselig" markerer noe negativt. Derfor tolker vi et negative-standard-sentiment mot anaforen "Han".

23: Leto er kledd i sin vanlige tunika , og vifter med en baseballkølle på sin vei ut på scenen .
>> Dette er en faktaopplysning uten videre sentiment. Dermed tolker vi det som neutral mot "Leto".

31: « Night Of The Hunter » og « Search And Destroy » er begge ganske effektive , og « Kings And Queens » - med bandets aller beste « oh oh oh » -refreng , melkes for alt den er verdt .
>> Ikke direkte nok kobling mot Jared Leto til å markere noe sentiment.

41: Det er forskjell på å pleie publikum og å oppføre seg som en klovn i et barneselskap .
>> Her er det ikke noe direkte mottaker av sentimentet, men vi forstår at det retter seg mot Jared Leto, så vi tolker dette som et negative-standard-sentiment.

48: Tekstene hans er fulle av hul eksistensiell angst , konspirasjonsteoriparanoia , « oss mot dem » -retorikk og generell fremmedgjorthet .
>> "Tekstene" er skrevet av Jared Leto, og sentimentet mot dem, og dermed ham, er negative-standard.
```
Sammenlagt lander vi på negative-slight for entiteten "Jared Leto".