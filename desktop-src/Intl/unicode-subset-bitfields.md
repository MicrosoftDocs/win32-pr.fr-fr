---
description: Les USBss de sous-ensemble Unicode sont utilisés dans les structures FONTSIGNATURE et LOCALESIGNATURE.
ms.assetid: f897dfc7-3e78-48dc-8d3d-6929e2f4ec4d
title: Champs de décodage Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f0fa4791e62f397e62a99a78d41dbcdc67c55299a650b1bc78bea685205399
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787989"
---
# <a name="unicode-subset-bitfields"></a>Champs de décodage Unicode

Les USBss de sous-ensemble Unicode sont utilisés dans les structures [**fontSignature**](/windows/win32/api/wingdi/ns-wingdi-fontsignature) et [**LOCALESIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-localesignature) .



<table>
<thead>
<tr class="header">
<th>bit</th>
<th>Sous-plage Unicode</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>0000 - 007F</td>
<td>Latin de base</td>
</tr>
<tr class="even">
<td>1</td>
<td>0080 - 00FF</td>
<td>Supplément latin-1</td>
</tr>
<tr class="odd">
<td>2</td>
<td>0100 - 017F</td>
<td>Latin étendu-A</td>
</tr>
<tr class="even">
<td>3</td>
<td>0180 - 024F</td>
<td>Latin étendu-B</td>
</tr>
<tr class="odd">
<td rowspan="3">4 $ {REMOVE} $<br />
</td>
<td>0250 - 02AF</td>
<td>Extensions de la Loi</td>
</tr>
<tr class="even">
<td>1D00 - 1D7F</td>
<td>Extensions phonétiques</td>

</tr>
<tr class="odd">
<td>1D80 - 1DBF</td>
<td>Supplément phonétique des extensions</td>

</tr>
<tr class="even">
<td rowspan="2">5 $ {REMOVE} $<br />
</td>
<td>02B0 - 02FF</td>
<td>Lettres du modificateur d’espacement</td>
</tr>
<tr class="odd">
<td>A700 - A71F</td>
<td>Lettres de ton modificateur</td>

</tr>
<tr class="even">
<td rowspan="2">6 $ {REMOVE} $<br />
</td>
<td>0300 - 036F</td>
<td>Combinaison de marques diacritiques</td>
</tr>
<tr class="odd">
<td>1DC0 - 1DFF</td>
<td>Supplément de marques diacritiques de combinaison</td>

</tr>
<tr class="even">
<td>7</td>
<td>0370 - 03FF</td>
<td>Grec et copte</td>
</tr>
<tr class="odd">
<td>8</td>
<td>2C80 - 2CFF</td>
<td>Copte</td>
</tr>
<tr class="even">
<td rowspan="4">9 $ {REMOVE} $<br />
</td>
<td>0400 - 04FF</td>
<td>Cyrillique</td>
</tr>
<tr class="odd">
<td>0500 - 052F</td>
<td>Supplément cyrillique</td>

</tr>
<tr class="even">
<td>2DE0 - 2DFF</td>
<td>Cyrillique étendu-A</td>

</tr>
<tr class="odd">
<td>A640 - A69F</td>
<td>Cyrillique étendu-B</td>

</tr>
<tr class="even">
<td>10</td>
<td>0530 - 058F</td>
<td>Arménien</td>
</tr>
<tr class="odd">
<td>11</td>
<td>0590 - 05FF</td>
<td>Hébreu</td>
</tr>
<tr class="even">
<td>12</td>
<td>A500 - A63F</td>
<td>Vaï</td>
</tr>
<tr class="odd">
<td rowspan="2">13 $ {REMOVE} $<br />
</td>
<td>0600 - 06FF</td>
<td>Arabe</td>
</tr>
<tr class="even">
<td>0750-077F</td>
<td>Supplément arabe</td>

</tr>
<tr class="odd">
<td>14</td>
<td>07C0 - 07FF</td>
<td>GBA</td>
</tr>
<tr class="even">
<td>15</td>
<td>0900 - 097F</td>
<td>Dévanâgarî</td>
</tr>
<tr class="odd">
<td>16</td>
<td>0980 - 09FF</td>
<td>Bangla</td>
</tr>
<tr class="even">
<td>17</td>
<td>0A00 - 0A7F</td>
<td>Gurmukhi</td>
</tr>
<tr class="odd">
<td>18</td>
<td>0A80 - 0AFF</td>
<td>Goudjrati</td>
</tr>
<tr class="even">
<td>19</td>
<td>0B00 - 0B7F</td>
<td>Odia</td>
</tr>
<tr class="odd">
<td>20</td>
<td>0B80 - 0BFF</td>
<td>Tamoul</td>
</tr>
<tr class="even">
<td>21</td>
<td>0C00 - 0C7F</td>
<td>Télougou</td>
</tr>
<tr class="odd">
<td>22</td>
<td>0C80 - 0CFF</td>
<td>Kannada</td>
</tr>
<tr class="even">
<td>23</td>
<td>0D00 - 0D7F</td>
<td>Malayalam</td>
</tr>
<tr class="odd">
<td>24</td>
<td>0E00 - 0E7F</td>
<td>Thaï</td>
</tr>
<tr class="even">
<td>25</td>
<td>0E80 - 0EFF</td>
<td>Lao</td>
</tr>
<tr class="odd">
<td rowspan="2">26 $ {REMOVE} $<br />
</td>
<td>10A0 - 10FF</td>
<td>Géorgien</td>
</tr>
<tr class="even">
<td>2D00 - 2D2F</td>
<td>Supplément géorgien</td>

</tr>
<tr class="odd">
<td>27</td>
<td>1B00 - 1B7F</td>
<td>Balinais</td>
</tr>
<tr class="even">
<td>28</td>
<td>1100 - 11FF</td>
<td>Hangul Jamos</td>
</tr>
<tr class="odd">
<td rowspan="3">29 $ {REMOVE} $<br />
</td>
<td>1E00 - 1EFF</td>
<td>Latin étendu additionnel</td>
</tr>
<tr class="even">
<td>2C60 - 2C7F</td>
<td>Latin étendu-C</td>

</tr>
<tr class="odd">
<td>A720 - A7FF</td>
<td>Latin étendu-D</td>

</tr>
<tr class="even">
<td>30</td>
<td>1F00 - 1FFF</td>
<td>Grec étendu</td>
</tr>
<tr class="odd">
<td rowspan="2">31 $ {REMOVE} $<br />
</td>
<td>2000 - 206F</td>
<td>Ponctuation générale</td>
</tr>
<tr class="even">
<td>2E00 - 2E7F</td>
<td>Ponctuation supplémentaire</td>

</tr>
<tr class="odd">
<td>32</td>
<td>2070 - 209F</td>
<td>Exposants et indices</td>
</tr>
<tr class="even">
<td>33</td>
<td>20A0 - 20CF</td>
<td>Symboles monétaires</td>
</tr>
<tr class="odd">
<td>34</td>
<td>20D0 - 20FF</td>
<td>Combinaison de signes diacritiques pour les symboles</td>
</tr>
<tr class="even">
<td>35</td>
<td>2100 - 214F</td>
<td>Symboles type lettre</td>
</tr>
<tr class="odd">
<td>36</td>
<td>2150 - 218F</td>
<td>Formats de nombres</td>
</tr>
<tr class="even">
<td rowspan="4">37 $ {REMOVE} $<br />
</td>
<td>2190 - 21FF</td>
<td>Flèches</td>
</tr>
<tr class="odd">
<td>27F0 - 27FF</td>
<td>Flèches supplémentaires-A</td>

</tr>
<tr class="even">
<td>2900 - 297F</td>
<td>Flèches supplémentaires-B</td>

</tr>
<tr class="odd">
<td>2B00 - 2BFF</td>
<td>Symboles et flèches divers</td>

</tr>
<tr class="even">
<td rowspan="4">38 $ {REMOVE} $<br />
</td>
<td>2200 - 22FF</td>
<td>Opérateurs mathématiques</td>
</tr>
<tr class="odd">
<td>27C0 - 27EF</td>
<td>Symboles mathématiques divers-A</td>

</tr>
<tr class="even">
<td>2980 - 29FF</td>
<td>Divers symboles mathématiques-B</td>

</tr>
<tr class="odd">
<td>2A00 - 2AFF</td>
<td>Opérateurs mathématiques supplémentaires</td>

</tr>
<tr class="even">
<td>39</td>
<td>2300 - 23FF</td>
<td>Autres techniques</td>
</tr>
<tr class="odd">
<td>40</td>
<td>2400 - 243F</td>
<td>Images de contrôle</td>
</tr>
<tr class="even">
<td>41</td>
<td>2440 - 245F</td>
<td>Reconnaissance optique de caractères</td>
</tr>
<tr class="odd">
<td>42</td>
<td>2460 - 24FF</td>
<td>Alphanumériques encadrés</td>
</tr>
<tr class="even">
<td>43</td>
<td>2500 - 257F</td>
<td>Dessin Box</td>
</tr>
<tr class="odd">
<td>44</td>
<td>2580 - 259F</td>
<td>Éléments de bloc</td>
</tr>
<tr class="even">
<td>45</td>
<td>25A0 - 25FF</td>
<td>Formes géométriques</td>
</tr>
<tr class="odd">
<td>46</td>
<td>2600 - 26FF</td>
<td>Symboles divers</td>
</tr>
<tr class="even">
<td>47</td>
<td>2700 - 27BF</td>
<td>Casseau</td>
</tr>
<tr class="odd">
<td>48</td>
<td>3000 - 303F</td>
<td>Symboles et ponctuation CJC</td>
</tr>
<tr class="even">
<td>49</td>
<td>3040 - 309F</td>
<td>Hiragana</td>
</tr>
<tr class="odd">
<td rowspan="2">50 $ {REMOVE} $<br />
</td>
<td>30A0 - 30FF</td>
<td>Katakana</td>
</tr>
<tr class="even">
<td>31F0 - 31FF</td>
<td>Extensions phonétiques katakana</td>

</tr>
<tr class="odd">
<td rowspan="2">51 $ {REMOVE} $<br />
</td>
<td>3100 - 312F</td>
<td>Bopomofo</td>
</tr>
<tr class="even">
<td>31A0 - 31BF</td>
<td>Bopomofo étendu</td>

</tr>
<tr class="odd">
<td>52</td>
<td>3130 - 318F</td>
<td>Jamos de compatibilité HANGÛL</td>
</tr>
<tr class="even">
<td>53</td>
<td>A840 - A87F</td>
<td>PHAGS-PA</td>
</tr>
<tr class="odd">
<td>54</td>
<td>3200 - 32FF</td>
<td>Lettres et mois CJC entre parenthèses</td>
</tr>
<tr class="even">
<td>55</td>
<td>3300 - 33FF</td>
<td>COMPATIBILITÉ CJC</td>
</tr>
<tr class="odd">
<td>56</td>
<td>AC00 - D7AF</td>
<td>Syllabes Hangul</td>
</tr>
<tr class="even">
<td>57</td>
<td>D800-DFFF</td>
<td>Non-plan 0. Notez que la définition de ce bit implique qu’il existe au moins un point de code supplémentaire au-delà du plan multilingue de base (BMP) pris en charge par cette police. Consultez <a href="surrogates-and-supplementary-characters.md">substituts et caractères supplémentaires</a>.</td>
</tr>
<tr class="odd">
<td>58</td>
<td>10900-1091F</td>
<td>Phéniciennes</td>
</tr>
<tr class="even">
<td rowspan="7">59 $ {REMOVE} $<br />
</td>
<td>2E80 - 2EFF</td>
<td>Complément des radicaux CJC</td>
</tr>
<tr class="odd">
<td>2F00 - 2FDF</td>
<td>Clé chinoise</td>

</tr>
<tr class="even">
<td>2FF0 - 2FFF</td>
<td>Caractères de description IDÉOGRAPHIQUE</td>

</tr>
<tr class="odd">
<td>3190 - 319F</td>
<td>Kanbun</td>

</tr>
<tr class="even">
<td>3400 - 4DBF</td>
<td>Extension de idéogrammes unifiés CJC A</td>

</tr>
<tr class="odd">
<td>4E00 - 9FFF</td>
<td>Idéogrammes unifiés CJC</td>

</tr>
<tr class="even">
<td>20000-2A6DF</td>
<td>Extension B des idéogrammes unifiés CJC</td>

</tr>
<tr class="odd">
<td>60</td>
<td>E000 - F8FF</td>
<td>Zone d’utilisation privée</td>
</tr>
<tr class="even">
<td rowspan="3">61 $ {REMOVE} $<br />
</td>
<td>31C0 - 31EF</td>
<td>Traits CJK</td>
</tr>
<tr class="odd">
<td>F900 - FAFF</td>
<td>Idéogrammes de compatibilité CJC</td>

</tr>
<tr class="even">
<td>2F800 - 2FA1F</td>
<td>Complément idéogrammes de compatibilité CJC</td>

</tr>
<tr class="odd">
<td>62</td>
<td>FB00 - FB4F</td>
<td>Formes de présentation alphabétique</td>
</tr>
<tr class="even">
<td>63</td>
<td>FB50 - FDFF</td>
<td>Formulaires de présentation en arabe-A</td>
</tr>
<tr class="odd">
<td>64</td>
<td>FE20 - FE2F</td>
<td>Combinaison de demi-marques</td>
</tr>
<tr class="even">
<td rowspan="2">65 $ {REMOVE} $<br />
</td>
<td>FE10 - FE1F</td>
<td>Formes verticales</td>
</tr>
<tr class="odd">
<td>FE30 - FE4F</td>
<td>Formulaires de compatibilité CJC</td>

</tr>
<tr class="even">
<td>66</td>
<td>FE50 - FE6F</td>
<td>Petites variantes de forme</td>
</tr>
<tr class="odd">
<td>67</td>
<td>FE70 - FEFF</td>
<td>Formulaires de présentation arabes-B</td>
</tr>
<tr class="even">
<td>68</td>
<td>FF00 - FFEF</td>
<td>Formes demi-chasse et pleine chasse</td>
</tr>
<tr class="odd">
<td>69</td>
<td>FFF0 - FFFF</td>
<td>Offres spéciales</td>
</tr>
<tr class="even">
<td>70</td>
<td>0F00 - 0FFF</td>
<td>Tibétain</td>
</tr>
<tr class="odd">
<td>71</td>
<td>0700 - 074F</td>
<td>Syriaque</td>
</tr>
<tr class="even">
<td>72</td>
<td>0780 - 07BF</td>
<td>Tana</td>
</tr>
<tr class="odd">
<td>73</td>
<td>0D80 - 0DFF</td>
<td>Cingalais</td>
</tr>
<tr class="even">
<td>74</td>
<td>1000 - 109F</td>
<td>Myanmar</td>
</tr>
<tr class="odd">
<td rowspan="3">75 $ {REMOVE} $<br />
</td>
<td>1200 - 137F</td>
<td>Éthiopien</td>
</tr>
<tr class="even">
<td>1380-139F</td>
<td>Supplément éthiopien</td>

</tr>
<tr class="odd">
<td>2D80 - 2DDF</td>
<td>Éthiopien étendu</td>

</tr>
<tr class="even">
<td>76</td>
<td>13A0 - 13FF</td>
<td>Cherokee</td>
</tr>
<tr class="odd">
<td>77</td>
<td>1400 - 167F</td>
<td>SYLLABE autochtones canadienne</td>
</tr>
<tr class="even">
<td>78</td>
<td>1680 - 169F</td>
<td>OGAM</td>
</tr>
<tr class="odd">
<td>79</td>
<td>16A0 - 16FF</td>
<td>Lettre</td>
</tr>
<tr class="even">
<td rowspan="2">80 $ {REMOVE} $<br />
</td>
<td>1780 - 17FF</td>
<td>Khmer</td>
</tr>
<tr class="odd">
<td>19E0 - 19FF</td>
<td>Symboles khmer</td>

</tr>
<tr class="even">
<td>81</td>
<td>1800 - 18AF</td>
<td>Mongol</td>
</tr>
<tr class="odd">
<td>82</td>
<td>2800 - 28FF</td>
<td>Modèles braille</td>
</tr>
<tr class="even">
<td rowspan="2">83 $ {REMOVE} $<br />
</td>
<td>A000 - A48F</td>
<td>Syllabes Yi</td>
</tr>
<tr class="odd">
<td>A490 - A4CF</td>
<td>Radicaux Yi</td>

</tr>
<tr class="even">
<td rowspan="4">84 $ {REMOVE} $<br />
</td>
<td>1700 - 171F</td>
<td>Tagalog</td>
</tr>
<tr class="odd">
<td>1720 - 173F</td>
<td>HANOUNÓO</td>

</tr>
<tr class="even">
<td>1740 - 175F</td>
<td>Bouhid</td>

</tr>
<tr class="odd">
<td>1760 - 177F</td>
<td>Tagbanwa</td>

</tr>
<tr class="even">
<td>85 %</td>
<td>10300-1032F</td>
<td>Ancien italique</td>
</tr>
<tr class="odd">
<td>86</td>
<td>10330-1034F</td>
<td>La</td>
</tr>
<tr class="even">
<td>87</td>
<td>10400-1044F</td>
<td>Deseret</td>
</tr>
<tr class="odd">
<td rowspan="3">88 $ {REMOVE} $<br />
</td>
<td>1D000 - 1D0FF</td>
<td>Symboles musicaux byzantines</td>
</tr>
<tr class="even">
<td>1D100 - 1D1FF</td>
<td>Symboles musicaux</td>

</tr>
<tr class="odd">
<td>1D200 - 1D24F</td>
<td>Vieilles notation musicale grecque</td>

</tr>
<tr class="even">
<td>89</td>
<td>1D400 - 1D7FF</td>
<td>Symboles alphanumériques mathématiques</td>
</tr>
<tr class="odd">
<td rowspan="2">90 $ {REMOVE} $<br />
</td>
<td>FF000 - FFFFD</td>
<td>Utilisation privée (plan 15)</td>
</tr>
<tr class="even">
<td>100000-10FFFD</td>
<td>Utilisation privée (plan 16)</td>

</tr>
<tr class="odd">
<td rowspan="2">91 $ {REMOVE} $<br />
</td>
<td>FE00 - FE0F</td>
<td>Sélecteurs de variante</td>
</tr>
<tr class="even">
<td>E0100 - E01EF</td>
<td>Complément sélecteurs de variante</td>

</tr>
<tr class="odd">
<td>92</td>
<td>E0000 - E007F</td>
<td>Balises</td>
</tr>
<tr class="even">
<td>93</td>
<td>1900 - 194F</td>
<td>Limbu</td>
</tr>
<tr class="odd">
<td>94</td>
<td>1950 - 197F</td>
<td>LETTRE TAÏ le</td>
</tr>
<tr class="even">
<td>95</td>
<td>1980-19DF</td>
<td>Nouveau taï lü</td>
</tr>
<tr class="odd">
<td>96</td>
<td>1A00-1A1F</td>
<td>Bugi</td>
</tr>
<tr class="even">
<td>97</td>
<td>2C00 - 2C5F</td>
<td>Lettre</td>
</tr>
<tr class="odd">
<td>98</td>
<td>2D30 - 2D7F</td>
<td>Tifinagh</td>
</tr>
<tr class="even">
<td>99</td>
<td>4DC0 - 4DFF</td>
<td>Symboles de hexagramme hexagrammes</td>
</tr>
<tr class="odd">
<td>100</td>
<td>A800 - A82F</td>
<td>SYLOTÎ NÂGRÎ</td>
</tr>
<tr class="even">
<td rowspan="3">101 $ {REMOVE} $<br />
</td>
<td>10000-1007F</td>
<td>SYLLABE B linéaire B</td>
</tr>
<tr class="odd">
<td>10080-100FF</td>
<td>Idéogrammes linéaire B</td>

</tr>
<tr class="even">
<td>10100-1013F</td>
<td>Chiffres des mer</td>

</tr>
<tr class="odd">
<td>102</td>
<td>10140-1018F</td>
<td>Anciens nombres grecs</td>
</tr>
<tr class="even">
<td>103</td>
<td>10380-1039F</td>
<td>Ougaritique</td>
</tr>
<tr class="odd">
<td>104</td>
<td>103A0 - 103DF</td>
<td>Ancien persan</td>
</tr>
<tr class="even">
<td>105</td>
<td>10450-1047F</td>
<td>Copeaux</td>
</tr>
<tr class="odd">
<td>106</td>
<td>10480-104AF</td>
<td>Osmanya</td>
</tr>
<tr class="even">
<td>107</td>
<td>10800-1083F</td>
<td>SYLLABE Cypriot</td>
</tr>
<tr class="odd">
<td>108</td>
<td>10A00 - 10A5F</td>
<td>Kharoshthi</td>
</tr>
<tr class="even">
<td>109</td>
<td>1D300 - 1D35F</td>
<td>Symboles Taï Xuan Jing</td>
</tr>
<tr class="odd">
<td rowspan="2">110 $ {REMOVE} $<br />
</td>
<td>12000-123FF</td>
<td>Cuneiform</td>
</tr>
<tr class="even">
<td>12400-1247F</td>
<td>Nombres Cuneiform et ponctuation</td>

</tr>
<tr class="odd">
<td>111</td>
<td>1D360 - 1D37F</td>
<td>Comptage des chiffres de la baguette</td>
</tr>
<tr class="even">
<td>112</td>
<td>1B80 - 1BBF</td>
<td>Soundanais</td>
</tr>
<tr class="odd">
<td>113</td>
<td>1C00 - 1C4F</td>
<td>Lepcha</td>
</tr>
<tr class="even">
<td>114</td>
<td>1C50 - 1C7F</td>
<td>Ol tchiki</td>
</tr>
<tr class="odd">
<td>115</td>
<td>A880 - A8DF</td>
<td>Saurashtra</td>
</tr>
<tr class="even">
<td>116</td>
<td>A900 - A92F</td>
<td>Kayah Li</td>
</tr>
<tr class="odd">
<td>117</td>
<td>A930 - A95F</td>
<td>Rejang</td>
</tr>
<tr class="even">
<td>118</td>
<td>AA00 - AA5F</td>
<td>Cham</td>
</tr>
<tr class="odd">
<td>119</td>
<td>10190-101CF</td>
<td>Anciens symboles</td>
</tr>
<tr class="even">
<td>120</td>
<td>101D0 - 101FF</td>
<td>Disque Phaistos</td>
</tr>
<tr class="odd">
<td rowspan="3">121 $ {REMOVE} $<br />
</td>
<td>10280-1029F</td>
<td>Lycien</td>
</tr>
<tr class="even">
<td>102A0 - 102DF</td>
<td>Carien</td>

</tr>
<tr class="odd">
<td>10920-1093F</td>
<td>Lydien</td>

</tr>
<tr class="even">
<td rowspan="2">122 $ {REMOVE} $<br />
</td>
<td>1F000 - 1F02F</td>
<td>Vignettes de Mahjong</td>
</tr>
<tr class="odd">
<td>1F030 - 1F09F</td>
<td>Vignettes Domino</td>

</tr>
<tr class="even">
<td>123</td>

<td><strong>Windows 2000 et versions ultérieures :</strong> Disposition en cours, horizontal de droite à gauche</td>
</tr>
<tr class="odd">
<td>124</td>

<td><strong>Windows 2000 et versions ultérieures :</strong> Mise en page en cours, vertical avant horizontal</td>
</tr>
<tr class="even">
<td>125</td>

<td><strong>Windows 2000 et versions ultérieures :</strong> Progression de la mise en page, de bas en haut</td>
</tr>
<tr class="odd">
<td>126-127</td>

<td>Réservé pour le processus-utilisation interne</td>
</tr>
</tbody>
</table>



 

 

 



