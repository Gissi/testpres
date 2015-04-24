Developing data products - shiny app presentation
========================================================
author: Gissur JÃ³nasson
date: Fri Apr 24 01:16:41 2015


Idea behind the app.
========================================================
transition: fade

I am a huge football fan makeing it straigh forward to make an app analyzing data for english premier league fantasy game. therefore I choose to make an app about it 


* web scraping the data from [EPL fantasy premierleague](http://http://fantasy.premierleague.com/)
* enrich the data 
* Use it for fun facts and spot players that are outliers when it comes to pricing

What was created
========================================================
transition: rotate

* function - fantasy()
* Takes litle time to load give it a second.




```r
points <- fantasy()
points
```

```
             Player Team Pos Selected Price GW Total
1            Hazard  CHE MID    45.0%    NA 11   211
2           Sánchez  ARS MID    27.3%    NA  0   180
3              Kane  TOT FWD    50.6%    NA  6   174
4            Agüero  MCI FWD    26.1%    NA  6   168
5            Austin  QPR FWD    19.5%    NA  0   163
6          Ivanovic  CHE DEF    30.2%    NA  5   160
7             Silva  MCI MID    22.6%    NA  2   154
8           Eriksen  TOT MID    23.4%    NA  9   153
9          Fàbregas  CHE MID    32.0%    NA  3   152
10         Sterling  LIV MID    32.5%    NA  0   147
11            Terry  CHE DEF    20.9%    NA  6   144
12        Henderson  LIV MID    22.0%    NA  0   144
13          Cazorla  ARS MID    10.8%    NA  0   143
14            Costa  CHE FWD    29.0%    NA  0   142
15          Downing  WHU MID    21.2%    NA  1   142
16            Clyne  SOU DEF    35.7%    NA  0   136
17         Bertrand  SOU DEF    22.7%    NA  1   134
18           Chadli  TOT MID    10.3%    NA 10   134
19            Fonte  SOU DEF    14.7%    NA  3   133
20       Sigurdsson  SWA MID    24.7%    NA  2   128
21         Berahino  WBA FWD    13.1%    NA  2   128
22           Baines  EVE DEF    14.5%    NA  7   126
23         Mignolet  LIV GKP     8.3%    NA  0   126
24            Oscar  CHE MID     5.3%    NA  5   125
25           Rooney  MUN FWD    20.9%    NA  2   125
26        Fabianski  SWA GKP     8.6%    NA  2   125
27         Jagielka  EVE DEF    14.3%    NA  6   124
28           de Gea  MUN GKP    24.8%    NA  2   124
29          Coleman  EVE DEF     5.6%    NA  6   121
30            Pellè  SOU FWD    11.1%    NA  2   121
31           Heaton  BUR GKP     5.2%    NA 11   120
32             Mata  MUN MID    10.1%    NA  2   120
33    Ki Sung-yueng  SWA MID     8.1%    NA  1   119
34          Forster  SOU GKP     7.7%    NA  0   118
35             Ings  BUR FWD     4.8%    NA  2   117
36            Tadic  SOU MID     4.3%    NA  2   117
37          Bolasie  CRY MID     7.4%    NA  1   115
38             Hart  MCI GKP     6.7%    NA  7   115
39       Yaya Touré  MCI MID     5.9%    NA  3   114
40           Adrián  WHU GKP     2.2%    NA  1   114
41      Azpilicueta  CHE DEF     8.0%    NA  8   112
42            Guzan  AVL GKP    12.5%    NA  0   111
43           Lukaku  EVE FWD     6.5%    NA  1   111
44         Coutinho  LIV MID     8.5%    NA  0   111
45           Skrtel  LIV DEF     8.0%    NA  0   111
46          Janmaat  NEW DEF     9.2%    NA  4   111
47        Cresswell  WHU DEF     4.9%    NA  1   111
48           Giroud  ARS FWD    16.5%    NA  0   109
49          Walters  STK MID     3.2%    NA  5   109
50           Cahill  CHE DEF    11.8%    NA  6   106
51         Courtois  CHE GKP     9.3%    NA  7   105
52         Puncheon  CRY MID     5.1%    NA  1   105
53         Williams  SWA DEF     9.7%    NA  1   105
54         Di María  MUN MID     9.8%    NA  1   104
55       van Persie  MUN FWD     1.9%    NA  0   103
56          Lescott  WBA DEF     3.7%    NA  6   103
57          Benteke  AVL FWD     3.1%    NA  0   102
58           Lloris  TOT GKP     9.0%    NA  0   102
59            Brunt  WBA MID     0.5%    NA 11   102
60          Speroni  CRY GKP     3.1%    NA  1   101
61            Diouf  STK FWD     0.6%    NA  8   101
62            Ulloa  LEI FWD     5.7%    NA  7   100
63          Begovic  STK GKP     6.0%    NA  3   100
64             Boyd  BUR MID     6.7%    NA  2    99
65             Mané  SOU MID     2.1%    NA  2    99
66           Foster  WBA GKP     4.4%    NA  0    98
67            Sakho  WHU FWD     2.1%    NA  0    98
68      Mertesacker  ARS DEF     3.9%    NA  0    97
69            Green  QPR GKP     2.8%    NA  0    97
70        Koscielny  ARS DEF     8.0%    NA  0    96
71            Navas  MCI MID     1.2%    NA 11    96
72             Bony  MCI FWD     3.8%    NA  0    96
73          Colback  NEW MID     2.4%    NA  6    96
74           Ramsey  ARS MID    11.1%    NA  0    95
75       Pantilimon  SUN GKP     3.7%    NA  0    95
76         Trippier  BUR DEF     2.1%    NA  2    94
77           Moreno  LIV DEF     6.9%    NA  0    94
78           Taylor  SWA DEF     5.0%    NA  0    94
79          Willian  CHE MID     0.7%    NA  1    93
80           Clichy  MCI DEF     8.6%    NA  0    93
81            Cissé  NEW FWD     0.6%    NA  0    93
82           Crouch  STK FWD     1.5%    NA  1    93
83          Larsson  SUN MID     3.5%    NA  0    93
84       Elmohamady  HUL MID     1.8%    NA  0    92
85            Vardy  LEI FWD     3.4%    NA  2    92
86           O'Shea  SUN DEF     8.4%    NA  0    92
87         Naismith  EVE FWD    11.2%    NA  1    91
88              Fer  QPR MID     0.5%    NA  0    91
89             Özil  ARS MID     3.6%    NA  0    89
90       Agbonlahor  AVL FWD     1.9%    NA  0    89
91          Welbeck  ARS FWD     4.7%    NA  0    88
92             Dann  CRY DEF     2.0%    NA  0    88
93         McGregor  HUL GKP     2.4%    NA  0    88
94          Sissoko  NEW MID     1.7%    NA  0    88
95     Schneiderlin  SOU MID     6.0%    NA 10    88
96          Vergini  SUN DEF     1.0%    NA  0    88
97             Rose  TOT DEF     8.2%    NA  2    87
98         Morrison  WBA MID     0.1%    NA 11    87
99          Gerrard  LIV MID     3.1%    NA  0    86
100        Zabaleta  MCI DEF     5.1%    NA  8    86
101         N'Zonzi  STK MID     0.4%    NA  6    86
102        Valencia  WHU FWD     0.6%    NA  2    85
103         Johnson  SUN MID     2.3%    NA  0    84
104         Gardner  WBA MID     0.1%    NA  7    84
105            Krul  NEW GKP    13.1%    NA  2    83
106         Kouyaté  WHU MID     0.5%    NA  1    83
107       Cambiasso  LEI MID     1.8%    NA  6    82
108          Milner  MCI MID     1.4%    NA  0    82
109    Alderweireld  SOU DEF     2.8%    NA  0    82
110         Monreal  ARS DEF     2.1%    NA  0    81
111         Herrera  MUN MID     3.0%    NA  1    81
112           Ayoze  NEW FWD     1.2%    NA  2    81
113       Routledge  SWA MID     1.0%    NA  2    81
114         Shelvey  SWA MID     3.1%    NA  1    81
115          Dawson  WBA DEF     3.8%    NA  6    81
116            Ward  CRY DEF     3.0%    NA  1    80
117         Arfield  BUR MID     0.4%    NA  1    79
118         Jedinak  CRY MID     2.2%    NA  1    79
119         Jelavic  HUL FWD     1.0%    NA  0    79
120        Smalling  MUN DEF     1.4%    NA  2    79
121          Barnes  BUR FWD     1.0%    NA -2    78
122        Fellaini  MUN MID     1.9%    NA  2    78
123           Nasri  MCI MID     1.8%    NA  1    77
124        Valencia  MUN MID     0.7%    NA  2    77
125       Shawcross  STK DEF     7.1%    NA  2    77
126       Jenkinson  WHU DEF     0.7%    NA  1    77
127            Zaha  CRY MID     1.1%    NA  2    76
128          Ledley  CRY MID     0.1%    NA  1    76
129         Lallana  LIV MID     0.5%    NA  0    76
130           Matic  CHE MID     3.5%    NA  3    75
131       Fernández  SWA DEF     0.2%    NA  1    75
132        Shackell  BUR DEF     0.5%    NA  1    74
133         Schlupp  LEI DEF     1.7%    NA  6    74
134          Mahrez  LEI MID     0.3%    NA  1    74
135         Wanyama  SOU MID     4.1%    NA  0    74
136          Wisdom  WBA DEF    14.3%    NA  1    74
137             Mee  BUR DEF     0.3%    NA  2    73
138          Morgan  LEI DEF     0.9%    NA 11    73
139            Dyer  SWA MID     4.7%    NA  1    73
140           Blind  MUN MID     1.1%    NA  0    72
141           Noble  WHU MID     1.3%    NA  2    72
142        McArthur  CRY MID     0.0%    NA  2    71
143          Howard  EVE GKP     9.3%    NA  6    71
144          Falcao  MUN FWD     1.8%    NA  2    71
145           Davis  SOU MID     1.7%    NA  2    71
146          Lamela  TOT MID     1.4%    NA  4    71
147         Tomkins  WHU DEF     0.4%    NA  0    71
148        Cissokho  AVL DEF     3.3%    NA  0    70
149     Fernandinho  MCI MID     0.7%    NA  1    70
150          Zamora  QPR FWD     3.1%    NA  0    70
151         Yoshida  SOU DEF     2.3%    NA  1    70
152      Vertonghen  TOT DEF     2.0%    NA  1    70
153         Wickham  SUN FWD     0.6%    NA  0    70
154           Gomis  SWA FWD     0.5%    NA  0    70
155         Weimann  AVL FWD     2.2%    NA  0    69
156           Jones  BUR MID     0.7%    NA  2    69
157        Mirallas  EVE MID     1.9%    NA  7    69
158       Livermore  HUL MID     0.5%    NA  0    69
159          Nugent  LEI FWD     0.7%    NA  0    69
160         Mangala  MCI DEF     0.9%    NA  7    69
161       Coloccini  NEW DEF     3.3%    NA  1    69
162     Ward-Prowse  SOU MID     1.3%    NA  1    69
163        Chambers  ARS DEF     6.9%    NA  0    68
164          Hutton  AVL DEF     8.4%    NA  0    68
165            Dier  TOT DEF    11.2%    NA  2    68
166         Pieters  STK DEF     0.9%    NA  2    68
167           Gibbs  ARS DEF     1.8%    NA  0    67
168           Young  MUN MID     1.6%    NA  2    67
169         Caulker  QPR DEF     5.0%    NA  0    67
170        Phillips  QPR MID     0.9%    NA  0    67
171        Fletcher  SUN FWD     0.4%    NA  0    67
172       Sessegnon  WBA MID     0.3%    NA  0    67
173           Gayle  CRY FWD     0.8%    NA  1    66
174        Gouffran  NEW MID     0.5%    NA  1    66
175           Moses  STK MID     0.3%    NA  0    66
176      Demichelis  MCI DEF     1.4%    NA  6    65
177         Cabella  NEW MID     0.8%    NA  1    65
178         Kompany  MCI DEF     8.7%    NA  0    64
179            Isla  QPR DEF     0.4%    NA  0    64
180            Long  SOU FWD     1.4%    NA  1    64
181          Wilson  STK DEF     1.5%    NA  0    64
182        Bardsley  STK DEF     0.6%    NA  0    64
183            Adam  STK MID     0.5%    NA  7    64
184           Mason  TOT MID     0.2%    NA  1    63
185        McCarthy  EVE MID     1.0%    NA  3    62
186         Barkley  EVE MID     3.4%    NA  1    62
187         Jovetic  MCI FWD     2.8%    NA  0    62
188          Ameobi  NEW MID     2.5%    NA  1    62
189         McAuley  WBA DEF     0.4%    NA  5    62
190           Kelly  CRY DEF     0.7%    NA  0    61
191          Stones  EVE DEF     1.1%    NA  9    61
192           Sakho  LIV DEF     0.8%    NA  0    61
193         Lampard  MCI MID     1.2%    NA  3    61
194           Dzeko  MCI FWD     3.8%    NA  1    61
195           Jones  MUN DEF     2.7%    NA  0    61
196          Vargas  QPR FWD     0.1%    NA  0    61
197           Clark  AVL DEF     0.9%    NA  0    60
198          Murray  CRY FWD     5.0%    NA  2    60
199            Reid  WHU DEF     0.7%    NA  1    60
200            Song  WHU MID     0.3%    NA  2    60
201         Chester  HUL DEF     2.3%    NA  0    59
202        Fernando  MCI MID     0.5%    NA  3    59
203           Bojan  STK FWD     2.5%    NA  0    59
204      Arnautovic  STK MID     0.6%    NA  2    59
205           Gómez  SUN MID     0.1%    NA  0    59
206           Ideye  WBA FWD     0.2%    NA  0    59
207           Brown  SUN DEF     0.4%    NA  0    58
208         Carrick  MUN MID     0.2%    NA  0    57
209     van Aanholt  SUN DEF     3.1%    NA  0    57
210          Rangel  SWA DEF     0.5%    NA  1    57
211         Dorrans  WBA MID     0.3%    NA  0    57
212     Chamberlain  ARS MID     1.0%    NA  0    56
213        Bellerín  ARS DEF     4.5%    NA  0    56
214           Barry  EVE MID     1.6%    NA  3    56
215       Konchesky  LEI DEF     0.6%    NA  0    56
216         Carroll  WHU FWD     0.3%    NA  0    56
217           Delph  AVL MID     1.1%    NA  0    55
218     Huddlestone  HUL MID     1.2%    NA  0    55
219             Can  LIV MID     0.3%    NA  0    55
220            Cork  SWA MID     1.7%    NA  2    55
221         Montero  SWA MID     0.1%    NA  1    55
222      Réveillere  SUN DEF     0.2%    NA  0    54
223          Ospina  ARS GKP     2.6%    NA  0    53
224         Delaney  CRY DEF     0.5%    NA  1    53
225          Lennon  EVE MID     1.0%    NA  3    53
226       Hernández  HUL FWD     0.1%    NA  0    53
227          Lovren  LIV DEF     9.6%    NA  0    53
228         Kolarov  MCI DEF     3.1%    NA  6    53
229      Williamson  NEW DEF     0.6%    NA  1    53
230           Nolan  WHU MID     1.1%    NA  1    53
231       Cleverley  AVL MID     0.1%    NA  0    52
232           Evans  MUN DEF     0.3%    NA  0    52
233        Campbell  CRY FWD     1.1%    NA  0    51
234           Allen  LIV MID     0.1%    NA  0    51
235         Flamini  ARS MID     0.2%    NA  0    50
236        N'Zogbia  AVL MID     0.3%    NA  0    50
237            Duff  BUR DEF     6.4%    NA  2    50
238         Rodwell  SUN MID     1.5%    NA  0    50
239      Amalfitano  WHU MID     0.1%    NA  0    50
240         Dummett  NEW DEF     4.8%    NA  0    49
241           Okore  AVL DEF     0.3%    NA  0    48
242            Remy  CHE FWD     3.4%    NA  0    48
243           Diamé  HUL MID     0.8%    NA  0    48
244            King  LEI MID     1.5%    NA 11    48
245        Kranjcar  QPR MID     0.1%    NA  0    48
246      Cattermole  SUN MID     2.5%    NA  0    48
247        Szczesny  ARS GKP     4.7%    NA  0    47
248           Bruce  HUL DEF    11.3%    NA  0    47
249          Davies  HUL DEF     1.7%    NA  0    47
250      Schmeichel  LEI GKP     3.4%    NA  8    47
251            Rojo  MUN DEF     0.8%    NA  0    47
252          Whelan  STK MID     0.0%    NA  2    47
253        Westwood  AVL MID     0.3%    NA  0    46
254       Sturridge  LIV FWD     8.5%    NA  0    46
255           Henry  QPR MID     0.2%    NA  0    46
256         Cameron  STK DEF     3.5%    NA  2    46
257        Anichebe  WBA FWD     0.2%    NA  2    46
258         Ramires  CHE MID     0.4%    NA  1    45
259          Drogba  CHE FWD     1.1%    NA  1    45
260          Meyler  HUL MID     0.1%    NA  0    45
261        Markovic  LIV MID     0.2%    NA  0    45
262         Johnson  LIV DEF     0.7%    NA  0    45
263        Bentaleb  TOT MID     0.9%    NA  1    45
264         Dembélé  TOT MID     0.4%    NA  1    45
265           Vlaar  AVL DEF     8.9%    NA  0    44
266         Sánchez  AVL MID     0.4%    NA  0    44
267         Haidara  NEW DEF     0.5%    NA  0    44
268          Barton  QPR MID     0.2%    NA  0    44
269           James  LEI MID     0.1%    NA  0    43
270      Wasilewski  LEI DEF     4.2%    NA  1    43
271        Townsend  TOT MID     0.4%    NA  0    43
272        Fletcher  WBA MID     0.5%    NA  3    43
273           Osman  EVE MID     0.5%    NA  0    42
274       Robertson  HUL DEF     0.5%    NA  0    42
275         Muniesa  STK DEF     0.2%    NA  0    42
276      Jutkiewicz  BUR FWD     0.2%    NA  1    41
277          Dawson  HUL DEF     1.4%    NA  0    41
278         Ramírez  HUL MID     0.1%    NA  0    41
279           Defoe  SUN FWD     0.8%    NA  0    41
280       Pocognoli  WBA DEF     0.2%    NA  0    41
281         de Laet  LEI DEF     0.3%    NA  1    40
282         McGeady  EVE MID     1.0%    NA  0    39
283           Eto'o  EVE FWD     0.6%    NA  0    39
284           Brady  HUL MID     0.1%    NA  0    39
285        Adebayor  TOT FWD     1.9%    NA  0    39
286         Lambert  LIV FWD     1.8%    NA  0    38
287         Collins  WHU DEF     0.3%    NA -1    38
288          Marney  BUR MID     0.3%    NA  0    37
289           Quinn  HUL MID     0.7%    NA  0    37
290           Zouma  CHE DEF     1.1%    NA  6    36
291       Hangeland  CRY DEF     0.7%    NA  0    36
292         McShane  HUL DEF     2.2%    NA  0    36
293         Rosicky  ARS MID     0.5%    NA  0    35
294          Gardos  SOU DEF     0.1%    NA  0    35
295         Buckley  SUN MID     0.0%    NA  0    35
296        Coquelin  ARS MID     0.2%    NA  0    34
297         Chamakh  CRY FWD     0.4%    NA  0    34
298           Aluko  HUL MID     0.1%    NA  0    34
299           Dunne  QPR DEF     0.1%    NA  0    34
300            Elia  SOU MID     0.9%    NA  0    34
301           Fazio  TOT DEF     0.1%    NA  2    34
302      Richardson  AVL MID     0.2%    NA  0    33
303        Schürrle  CHE MID     2.6%    NA  0    33
304          N'Doye  HUL FWD     0.3%    NA  0    33
305           Lucas  LIV MID     1.1%    NA  0    33
306            Shaw  MUN DEF     2.6%    NA  2    33
307           Keane  BUR DEF     0.1%    NA  0    32
308            Cech  CHE GKP     1.7%    NA  0    32
309            Hill  QPR DEF     0.1%    NA  0    32
310        Naughton  SWA DEF     0.5%    NA  0    32
311          Bacuna  AVL MID     0.1%    NA  0    31
312         Kightly  BUR MID     0.1%    NA  0    31
313           Hamer  LEI GKP     7.0%    NA  0    31
314          McNair  MUN DEF     0.2%    NA  2    31
315         Obertan  NEW MID     0.2%    NA  1    31
316             Yun  QPR DEF     1.7%    NA  0    31
317          Davies  TOT DEF     0.8%    NA  1    31
318         Soldado  TOT FWD     0.8%    NA  0    31
319      Drinkwater  LEI MID     0.1%    NA  1    29
320          Sandro  QPR MID     0.1%    NA  0    29
321         Ireland  STK MID     0.1%    NA  1    29
322         Mannone  SUN GKP     4.5%    NA  0    29
323            Cole  WHU FWD     0.6%    NA  2    29
324     Filipe Luis  CHE DEF     2.2%    NA  0    28
325           Besic  EVE MID     0.3%    NA  1    28
326            Huth  LEI DEF     0.4%    NA  6    28
327       Balotelli  LIV FWD     1.2%    NA  0    28
328         Januzaj  MUN MID     1.1%    NA  1    28
329         Rivière  NEW FWD     0.4%    NA  0    28
330         Hoilett  QPR MID     0.2%    NA  0    28
331          Kaboul  TOT DEF     1.6%    NA  0    28
332           Baker  AVL DEF     0.1%    NA  0    27
333          Zárate  QPR FWD     0.4%    NA  0    27
334          Walker  TOT DEF     0.6%    NA  0    27
335          Robles  EVE GKP     0.1%    NA  0    26
336           Anita  NEW MID     0.1%    NA  2    26
337           Baird  WBA DEF     2.5%    NA  1    26
338        Mariappa  CRY DEF     0.1%    NA  0    25
339         Simpson  LEI DEF     0.2%    NA  0    25
340      Wollscheid  STK DEF     0.4%    NA  2    25
341            Cole  AVL MID     0.1%    NA  0    24
342          Lowton  AVL DEF     0.1%    NA  0    24
343           Mutch  CRY MID     0.6%    NA  0    24
344        Rosenior  HUL DEF     0.3%    NA  0    24
345           Touré  LIV DEF     0.5%    NA  0    24
346   Steven Taylor  NEW DEF     2.9%    NA  0    24
347           Yacob  WBA MID     0.2%    NA  3    24
348         Debuchy  ARS DEF     4.1%    NA  0    23
349         Walcott  ARS MID     0.2%    NA  0    23
350           Mikel  CHE MID     0.4%    NA  1    23
351            Koné  EVE FWD     0.1%    NA  5    23
352           Tioté  NEW MID     1.1%    NA  0    23
353          Capoue  TOT MID     0.1%    NA  0    23
354        Wilshere  ARS MID     2.2%    NA  0    22
355        Senderos  AVL DEF     0.9%    NA  0    22
356       Manquillo  LIV DEF     0.3%    NA  0    22
357           Sagna  MCI DEF     1.3%    NA  0    22
358          Traore  QPR MID     0.3%    NA  0    22
359          Onuoha  QPR DEF     0.1%    NA  0    22
360       Chiriches  TOT DEF     0.1%    NA  0    22
361          Rafael  MUN DEF     0.5%    NA  0    21
362        Bridcutt  SUN MID     0.3%    NA  0    21
363           Jones  SUN DEF     0.1%    NA  0    21
364         Carroll  SWA MID     0.1%    NA  0    21
365         Mulumbu  WBA MID     0.1%    NA  0    21
366        Sinclair  AVL MID     0.3%    NA  0    20
367      Albrighton  LEI MID     1.9%    NA  3    20
368           Abeid  NEW MID     0.0%    NA  1    20
369        Paulinho  TOT MID     1.0%    NA  5    20
370          Arteta  ARS MID     0.7%    NA  0    19
371         Wallace  BUR MID     0.1%    NA  1    19
372          Distin  EVE DEF     1.4%    NA  0    19
373        Kramaric  LEI FWD     0.1%    NA  2    19
374       Schwarzer  LEI GKP     0.1%    NA  0    19
375       Ferdinand  QPR DEF     2.4%    NA  0    19
376            Amat  SWA DEF     0.2%    NA  0    19
377         Pienaar  EVE MID     0.3%    NA  0    18
378         Hammond  LEI MID     0.1%    NA  0    18
379          Borini  LIV FWD     0.2%    NA  0    18
380        Richards  SWA DEF     0.4%    NA  0    18
381           Vokes  BUR FWD     0.0%    NA  1    17
382          Sanogo  CRY FWD     0.7%    NA  1    17
383        Blackett  MUN DEF     0.8%    NA  1    17
384         Davis K  SOU GKP     2.1%    NA  1    17
385           Emnes  SWA FWD     0.0%    NA  1    17
386          Myhill  WBA GKP    13.3%    NA  8    17
387         Álvarez  SUN MID     0.0%    NA  0    16
388        Grealish  AVL MID     0.1%    NA  0    15
389         Alcaraz  EVE DEF     0.1%    NA  0    15
390          Wilson  MUN FWD     0.3%    NA  0    15
391          Varela  WBA MID     0.0%    NA  0    15
392         O'Brien  WHU DEF     0.4%    NA  0    15
393        Martinez  ARS GKP     0.1%    NA  0    14
394          Gibson  EVE MID     0.4%    NA  0    14
395     Ryan Taylor  NEW DEF     0.0%    NA  1    14
396            Reed  SOU MID     0.1%    NA  0    14
397            Vorm  TOT GKP     0.4%    NA  3    14
398            Ward  BUR DEF     0.0%    NA  0    13
399           Moore  LEI DEF     1.4%    NA  0    13
400       Knockaert  LEI MID     0.1%    NA  0    13
401         Assaidi  LIV MID     0.1%    NA  0    13
402        Altidore  SUN FWD     0.2%    NA  0    13
403          Barrow  SWA FWD     0.0%    NA  0    13
404          Jarvis  WHU MID     0.0%    NA  1    13
405      Carles Gil  AVL MID     0.1%    NA  0    12
406          Taylor  BUR MID     0.1%    NA  1    12
407         Sordell  BUR FWD     0.0%    NA  0    12
408          Aarons  NEW MID     0.1%    NA  0    12
409       Armstrong  NEW FWD     0.2%    NA  1    12
410          Graham  SUN FWD     0.0%    NA  0    12
411         Britton  SWA MID     0.1%    NA  0    12
412          Gamboa  WBA DEF     0.1%    NA  0    12
413          Olsson  WBA DEF     0.1%    NA  1    12
414         Gabriel  ARS DEF     0.1%    NA  0    11
415          Harper  HUL GKP     0.1%    NA  0    11
416       Jakupovic  HUL GKP     2.7%    NA  0    11
417            Wood  LEI FWD     0.8%    NA  0    11
418             Ibe  LIV MID     0.5%    NA  0    11
419        Ben Arfa  NEW MID     0.5%    NA  0    11
420         Taarabt  QPR MID     0.1%    NA  0    11
421       Stambouli  TOT MID     0.0%    NA  0    11
422         Sidwell  STK MID     1.2%    NA  1    11
423         Bartley  SWA DEF     1.2%    NA  0    11
424 Nélson Oliveira  SWA FWD     0.0%    NA  2    11
425        Cuadrado  CHE MID     0.1%    NA  0    10
426          Oviedo  EVE DEF     0.0%    NA  0     9
427            Atsu  EVE MID     0.1%    NA  0     9
428            Ince  HUL MID     0.5%    NA  0     9
429    José Enrique  LIV DEF     0.2%    NA  0     9
430     Giaccherini  SUN MID     0.0%    NA  0     8
431          Coates  SUN DEF     0.0%    NA  0     8
432        Podolski  ARS FWD     0.4%    NA  0     7
433            Bent  AVL FWD     0.4%    NA  0     7
434          Bannan  CRY MID     0.0%    NA  0     7
435         Hibbert  EVE DEF     0.1%    NA  0     7
436         Alnwick  NEW GKP     0.7%    NA  0     7
437        Djuricic  SOU MID     0.0%    NA  0     7
438         Targett  SOU DEF     0.5%    NA  0     7
439       McManaman  WBA MID     0.0%    NA  0     7
440           Demel  WHU DEF     0.2%    NA  0     7
441           Akpom  ARS FWD     0.0%    NA  0     6
442       Guédioura  CRY MID     0.0%    NA  0     6
443           Upson  LEI DEF     0.5%    NA  0     6
444          Vaz Te  WHU FWD     1.5%    NA  0     6
445            Reid  BUR MID     0.3%    NA  0     5
446          Souaré  CRY DEF     0.0%    NA  1     5
447       Gutiérrez  NEW MID     0.3%    NA  0     5
448          Elliot  NEW GKP     2.4%    NA  0     5
449          Mayuka  SOU FWD     0.0%    NA  0     5
450         Samaras  WBA FWD     0.0%    NA  0     5
451            Nenê  WHU MID     0.0%    NA  0     5
452        Campbell  ARS FWD     0.4%    NA  0     4
453          Ameobi  CRY FWD     0.0%    NA  0     4
454           Sagbo  HUL FWD     0.0%    NA  0     4
455        Figueroa  HUL DEF     0.4%    NA  0     4
456           Jones  LIV GKP     0.0%    NA  0     4
457            Pozo  MCI FWD     0.0%    NA  0     4
458 Wright-Phillips  QPR MID     0.2%    NA  0     4
459          Fulton  SWA MID     0.0%    NA  0     4
460           Salah  CHE MID     0.2%    NA  0     3
461        Chalobah  CHE MID     0.0%    NA  0     3
462         O'Keefe  CRY MID     0.0%    NA  0     3
463           Doyle  CRY FWD     0.0%    NA  0     3
464         Garbutt  EVE DEF     0.3%    NA  0     3
465        Lawrence  LEI FWD     0.1%    NA  0     3
466       Caballero  MCI GKP     0.1%    NA  0     3
467          Powell  MUN MID     0.0%    NA  0     3
468         de Jong  NEW MID     0.4%    NA  0     3
469         Faurlin  QPR MID     0.1%    NA  0     3
470         Doughty  QPR MID     0.0%    NA  0     3
471      Odemwingie  STK MID     0.3%    NA  0     3
472           Poyet  WHU MID     0.5%    NA  0     3
473        Williams  CRY MID     0.0%    NA  0     2
474        Browning  EVE DEF     0.2%    NA  0     2
475        McCarthy  QPR GKP     0.6%    NA  0     2
476       Grego-Cox  QPR MID     0.0%    NA  0     2
477       Tiendalli  SWA DEF     0.0%    NA  0     2
478         Tremmel  SWA GKP     0.1%    NA  0     2
479          Blanco  WBA MID     0.0%    NA  0     2
480        Davidson  WBA DEF     0.0%    NA  0     2
481    Jääskeläinen  WHU GKP     0.6%    NA  0     2
482  Maitland-Niles  ARS MID     0.0%    NA  0     1
483  Hepburn-Murphy  AVL FWD     0.0%    NA  0     1
484        Lafferty  BUR DEF     0.5%    NA  0     1
485            Long  BUR DEF     0.6%    NA  0     1
486    Loftus-Cheek  CHE MID     0.0%    NA  0     1
487          Thomas  CRY MID     0.0%    NA  0     1
488       Hennessey  CRY GKP     0.2%    NA  0     1
489          Fryers  CRY DEF     0.0%    NA  0     1
490       Snodgrass  HUL MID     0.3%    NA  0     1
491         Maguire  HUL DEF     0.1%    NA  0     1
492 Taylor-Fletcher  LEI MID     0.4%    NA  0     1
493          Boyata  MCI DEF     0.1%    NA  0     1
494          Thorpe  MUN DEF     0.0%    NA  0     1
495        Anderson  MUN MID     0.0%    NA  0     1
496       Hernández  MUN FWD     0.3%    NA  0     1
497         Pereira  MUN MID     0.0%    NA  0     1
498            Nani  MUN MID     0.6%    NA  0     1
499         Lingard  MUN MID     0.1%    NA  0     1
500          Vuckic  NEW MID     0.0%    NA  0     1
501         Furlong  QPR DEF     0.0%    NA  0     1
502         Isgrove  SOU MID     0.5%    NA  0     1
503          Seager  SOU FWD     0.0%    NA  0     1
504            Gape  SOU MID     0.0%    NA  0     1
505         Hesketh  SOU MID     0.0%    NA  0     1
506        McCarthy  SOU DEF     0.1%    NA  0     1
507          Yedlin  TOT DEF     0.0%    NA  0     1
508          Holtby  TOT MID     0.1%    NA  0     1
509        Teixeira  STK DEF     0.0%    NA  0     1
510         Shenton  STK MID     0.0%    NA  0     1
511         Mandron  SUN FWD     0.1%    NA  0     1
512          Grimes  SWA MID     0.0%    NA  0     1
513        Morrison  WHU MID     0.0%    NA  0     1
514       Vermaelen  ARS DEF     0.1%    NA  0     0
515          Hayden  ARS DEF     0.1%    NA  0     0
516         Huddart  ARS GKP     0.0%    NA  0     0
517           Diaby  ARS MID     0.0%    NA  0     0
518           Ajayi  ARS DEF     0.0%    NA  0     0
519        Miyaichi  ARS MID     0.0%    NA  0     0
520         Zelalem  ARS MID     0.0%    NA  0     0
521          Bielik  ARS MID     0.0%    NA  0     0
522           Macey  ARS GKP     0.0%    NA  0     0
523          Gnabry  ARS MID     0.0%    NA  0     0
524            Herd  AVL DEF     0.0%    NA  0     0
525      Carruthers  AVL MID     0.0%    NA  0     0
526            Luna  AVL DEF     0.0%    NA  0     0
527           Tonev  AVL MID     0.0%    NA  0     0
528        Robinson  AVL FWD     0.1%    NA  0     0
529       El Ahmadi  AVL MID     2.0%    NA  0     0
530         Johnson  AVL MID     0.0%    NA  0     0
531        Kinsella  AVL DEF     0.0%    NA  0     0
532           Given  AVL GKP     7.2%    NA  0     0
533        Donacien  AVL DEF     0.2%    NA  0     0
534          Calder  AVL MID     0.0%    NA  0     0
535           Kozák  AVL FWD     0.0%    NA  0     0
536         Gardner  AVL MID     0.1%    NA  0     0
537         Bennett  AVL DEF     0.0%    NA  0     0
538        Dummigan  BUR DEF     0.1%    NA  0     0
539          Hewitt  BUR MID     0.0%    NA  0     0
540           Gilks  BUR GKP     2.9%    NA  0     0
541        Dummigan  BUR DEF     0.1%    NA  0     0
542           Brown  CHE MID     0.0%    NA  0     0
543              Ba  CHE FWD     0.0%    NA  0     0
544         Solanke  CHE FWD     0.0%    NA  0     0
545           Swift  CHE MID     0.0%    NA  0     0
546      van Ginkel  CHE MID     0.0%    NA  0     0
547          Torres  CHE FWD     0.3%    NA  0     0
548           Baker  CHE MID     0.0%    NA  0     0
549             Aké  CHE DEF     0.1%    NA  0     0
550          Piazon  CHE MID     0.0%    NA  0     0
551     Christensen  CHE DEF     0.0%    NA  0     0
552       McEachran  CHE MID     0.0%    NA  0     0
553          Inniss  CRY DEF     0.2%    NA  0     0
554        McCarthy  CRY DEF     0.4%    NA  0     0
555          Garvan  CRY MID     0.0%    NA  0     0
556         Campaña  CRY MID     0.0%    NA  0     0
557            Gray  CRY MID     0.0%    NA  0     0
558          Dobbie  CRY FWD     0.0%    NA  0     0
559            Kébé  CRY MID     0.0%    NA  0     0
560            Hunt  CRY DEF     0.0%    NA  0     0
561 Jerome Williams  CRY DEF     0.0%    NA  0     0
562         Johnson  CRY FWD     0.0%    NA  0     0
563         Boateng  CRY MID     0.3%    NA  0     0
564  Lee Chung-yong  CRY MID     0.0%    NA  0     0
565       Griffiths  EVE GKP     0.0%    NA  0     0
566          Ledson  EVE MID     0.0%    NA  0     0
567         McAleny  EVE FWD     0.1%    NA  0     0
568           Duffy  EVE DEF     0.1%    NA  0     0
569         Dudgeon  HUL DEF     0.0%    NA  0     0
570          Watson  HUL GKP     0.1%    NA  0     0
571      Proschwitz  HUL FWD     0.0%    NA  0     0
572          Hopper  LEI FWD     0.1%    NA  0     0
573           Smith  LEI GKP     0.1%    NA  0     0
574          Barmby  LEI FWD     0.2%    NA  0     0
575        Bakayogo  LEI DEF     0.2%    NA  0     0
576           Smith  LIV DEF     0.0%    NA  0     0
577        Teixeira  LIV MID     0.0%    NA  0     0
578        Flanagan  LIV DEF     0.2%    NA  0     0
579        Williams  LIV DEF     0.0%    NA  0     0
580           Agger  LIV DEF     0.2%    NA  0     0
581           Ilori  LIV DEF     0.1%    NA  0     0
582        Rossiter  LIV MID     0.0%    NA  0     0
583           Reina  LIV GKP     0.0%    NA  0     0
584       Brannagan  LIV MID     0.0%    NA  0     0
585           Aspas  LIV FWD     0.0%    NA  0     0
586           Coady  LIV DEF     0.0%    NA  0     0
587            Ward  LIV GKP     0.1%    NA  0     0
588        Seyi Ojo  LIV MID     0.0%    NA  0     0
589            Suso  LIV MID     0.0%    NA  0     0
590        Zuculini  MCI MID     0.0%    NA  0     0
591        Richards  MCI DEF     0.1%    NA  0     0
592         Ambrose  MCI FWD     0.0%    NA  0     0
593        Nastasic  MCI DEF     0.2%    NA  0     0
594     Javi García  MCI MID     0.1%    NA  0     0
595           Rekik  MCI DEF     0.0%    NA  0     0
596         Negredo  MCI FWD     0.0%    NA  0     0
597        Angelino  MCI DEF     0.0%    NA  0     0
598          Varela  MUN DEF     0.0%    NA  0     0
599           James  MUN DEF     0.1%    NA  0     0
600          Valdés  MUN GKP     0.0%    NA  0     0
601          Varela  MUN DEF     0.0%    NA  0     0
602           Keane  MUN FWD     0.0%    NA  0     0
603      Lindegaard  MUN GKP     0.1%    NA  0     0
604          Valdés  MUN GKP     0.0%    NA  0     0
605            Amos  MUN GKP     0.0%    NA  0     0
606         Vermijl  MUN DEF     0.0%    NA  0     0
607      Bigirimana  NEW MID     0.0%    NA  0     0
608           Kemen  NEW MID     0.0%    NA  0     0
609         Streete  NEW DEF     0.0%    NA  0     0
610        Ferguson  NEW MID     0.0%    NA  0     0
611        Campbell  NEW FWD     0.1%    NA  0     0
612        Marveaux  NEW MID     0.0%    NA  0     0
613           Satka  NEW DEF     0.2%    NA  0     0
614          Sterry  NEW DEF     0.0%    NA  0     0
615        Ferreyra  NEW FWD     0.0%    NA  0     0
616         Woodman  NEW GKP     0.0%    NA  0     0
617     Yanga-Mbiwa  NEW DEF     0.1%    NA  0     0
618          Santon  NEW DEF     0.1%    NA  0     0
619          O'Neil  QPR MID     0.0%    NA  0     0
620          Murphy  QPR GKP     1.6%    NA  0     0
621      Sutherland  QPR MID     0.0%    NA  0     0
622           Jenas  QPR MID     0.2%    NA  0     0
623        Mitchell  QPR MID     0.0%    NA  0     0
624          Comley  QPR MID     0.0%    NA  0     0
625        Stephens  SOU DEF     0.2%    NA  0     0
626           Sharp  SOU FWD     0.0%    NA  0     0
627        Hooiveld  SOU DEF     0.2%    NA  0     0
628           Boruc  SOU GKP     0.2%    NA  0     0
629         McQueen  SOU MID     0.0%    NA  0     0
630       Gallagher  SOU FWD     0.0%    NA  0     0
631       Rodriguez  SOU FWD     0.1%    NA  0     0
632         Osvaldo  SOU FWD     0.0%    NA  0     0
633         McQueen  SOU MID     0.0%    NA  0     0
634       Gazzaniga  SOU GKP     0.1%    NA  0     0
635           Sharp  SOU FWD     0.0%    NA  0     0
636         Friedel  TOT GKP     0.1%    NA  0     0
637          Falque  TOT MID     0.0%    NA  0     0
638           Winks  TOT MID     0.0%    NA  0     0
639            Ball  TOT DEF     0.0%    NA  0     0
640    Assou-Ekotto  TOT DEF     0.2%    NA  0     0
641      Fredericks  TOT DEF     0.1%    NA  0     0
642        Ceballos  TOT MID     0.0%    NA  0     0
643       Pritchard  TOT MID     0.0%    NA  0     0
644       Veljkovic  TOT DEF     0.3%    NA  0     0
645        Palacios  STK MID     0.2%    NA  0     0
646          Jerome  STK FWD     0.1%    NA  0     0
647       Wilkinson  STK DEF     1.9%    NA  0     0
648            Ward  STK MID     0.1%    NA  0     0
649         Butland  STK GKP     0.0%    NA  0     0
650            Ness  STK MID     0.0%    NA  0     0
651         Shotton  STK DEF     0.2%    NA  0     0
652            Shea  STK MID     0.0%    NA  0     0
653        Sørensen  STK GKP     0.2%    NA  0     0
654         Diakité  SUN DEF     0.4%    NA  0     0
655         Mavrias  SUN MID     0.0%    NA  0     0
656          Cabral  SUN MID     0.0%    NA  0     0
657          Robson  SUN DEF     0.0%    NA  0     0
658         Watmore  SUN FWD     0.0%    NA  0     0
659     M. Karlsson  SUN FWD     0.0%    NA  0     0
660           Agnew  SUN MID     0.1%    NA  0     0
661         Roberge  SUN DEF     0.1%    NA  0     0
662         N'Diaye  SUN MID     0.0%    NA  0     0
663     M. Karlsson  SUN FWD     0.0%    NA  0     0
664         Mavrias  SUN MID     0.0%    NA  0     0
665           Michu  SWA MID     0.0%    NA  0     0
666        Kingsley  SWA DEF     0.0%    NA  0     0
667            Tate  SWA DEF     0.1%    NA  0     0
668         Sheehan  SWA MID     0.0%    NA  0     0
669       Hernández  SWA MID     0.0%    NA  0     0
670         Cornell  SWA GKP     0.1%    NA  0     0
671           Lucas  SWA MID     0.1%    NA  0     0
672           Chico  SWA DEF     0.0%    NA  0     0
673            King  SWA MID     0.1%    NA  0     0
674      José Cañas  SWA MID     0.1%    NA  0     0
675        Shephard  SWA DEF     0.0%    NA  0     0
676    Álex Pozuelo  SWA MID     0.0%    NA  0     0
677        Donnelly  SWA FWD     0.0%    NA  0     0
678         Daniels  WBA DEF     0.1%    NA  0     0
679          Thorne  WBA MID     0.0%    NA  0     0
680       Adil Nabi  WBA FWD     0.0%    NA  0     0
681          O'Neil  WBA DEF     0.3%    NA  0     0
682         Daniels  WBA GKP     0.1%    NA  0     0
683            Rose  WBA GKP     0.1%    NA  0     0
684           Roofe  WBA MID     0.0%    NA  0     0
685          Oxford  WHU DEF     0.0%    NA  0     0
686           Potts  WHU DEF     0.3%    NA  0     0
687           Maiga  WHU FWD     0.0%    NA  0     0
688  Manny Onariase  WHU DEF     0.0%    NA  0     0
689        Chambers  WHU DEF     0.7%    NA  0     0
690     Alou Diarra  WHU MID     0.1%    NA  0     0
691          Cullen  WHU MID     0.0%    NA  0     0
692     Alou Diarra  WHU MID     0.1%    NA  0     0
693        Chambers  WHU DEF     0.7%    NA  0     0
694  Manny Onariase  WHU DEF     0.0%    NA  0     0
695             Lee  WHU FWD     0.2%    NA  0     0
```

This was the output for the local shiny app.
======================================================== 


![alt text](original_app.png)


For some reason it did not work to add it to shinyapp.io
======================================================== 
transition: rotate

* therefor created another app based on the old one but with built in data
* url [Shiny app for course project](https://gissi.shinyapps.io/shiny_app1)
* Next time I will try to do more advance things like using googlevis example graph below


```r
library(googleVis)
M <- gvisMotionChart(Fruits, "Fruit", "Year", options = list(width = 400, height = 350))
plot(M)
```

