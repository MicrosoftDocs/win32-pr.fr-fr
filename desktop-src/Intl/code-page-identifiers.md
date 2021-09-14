---
description: Le tableau suivant définit les identificateurs de page de codes disponibles.
ms.assetid: 5d6fc86a-f205-4d14-bb7c-ecd71682e0fe
title: Identificateurs de page de codes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35fb0482247313e8d61d61d7d3178906536ab9e0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127240419"
---
# <a name="code-page-identifiers"></a>Identificateurs de page de codes

Le tableau suivant définit les identificateurs de page de codes disponibles.

> [!Note]  
> Les pages de codes ANSI peuvent être différentes sur des ordinateurs différents ou peuvent être modifiées pour un seul ordinateur, ce qui entraîne une altération des données. Pour obtenir les résultats les plus cohérents, les applications doivent utiliser Unicode, par exemple UTF-8 ou UTF-16, au lieu d’une page de codes spécifique.

 



| Identificateur | Nom .NET               | Informations supplémentaires                                                                              |
|------------|-------------------------|-----------------------------------------------------------------------------------------------------|
| 037        | IBM037                  | US-Canada IBM EBCDIC                                                                                |
| 437        | IBM437                  | États-Unis OEM                                                                                   |
| 500        | IBM500                  | IBM EBCDIC international                                                                            |
| 708        | ASMO-708                | Arabe (ASMO 708)                                                                                   |
| 709        |                         | Arabe (ASMO-449 +, BCON v4)                                                                         |
| 710        |                         | Arabe-arabe transparent                                                                         |
| 720        | DOS-720                 | Arabe (ASMO transparent); Arabe (DOS)                                                             |
| 737        | ibm737                  | OEM grec (anciennement 437G); Grec (DOS)                                                              |
| 775        | ibm775                  | Baltique OEM ; Balte (DOS)                                                                            |
| 850        | ibm850                  | OEM multilingue latin 1 ; Europe occidentale (DOS)                                                    |
| 852        | ibm852                  | OEM Latin 2 ; Europe centrale (DOS)                                                                 |
| 855        | IBM855                  | OEM cyrillique (principalement russe)                                                                    |
| 857        | ibm857                  | Turc OEM ; Turc (DOS)                                                                          |
| 858        | IBM00858                | OEM multilingue latin 1 + symbole euro                                                              |
| 860        | IBM860                  | OEM Portugais ; Portugais (DOS)                                                                    |
| 861        | ibm861                  | OEM islandais ; Islandais (DOS)                                                                      |
| 862        | DOS-862                 | OEM-Hébreu ; Hébreu (DOS)                                                                            |
| 863        | IBM863                  | OEM français canadien ; Français canadien (DOS)                                                          |
| 864        | IBM864                  | Arabe OEM ; Arabe (864)                                                                            |
| 865        | IBM865                  | En Scandinavie OEM ; Nordique (DOS)                                                                            |
| 866        | cp866                   | Russe OEM ; Cyrillique (DOS)                                                                         |
| 869        | ibm869                  | Grec moderne grec ; Grec, moderne (DOS)                                                               |
| 870        | IBM870                  | IBM EBCDIC multilingue/ROECE (latin 2); IBM EBCDIC multilingue Latin 2                            |
| 874        | Windows-874             | Thaï (Windows)                                                         |
| 875        | cp875                   | IBM EBCDIC grec moderne                                                                             |
| 932        | MAJ \_ JIS              | Japonais ANSI/OEM ; Japonais (Shift-JIS)                                                             |
| 936        | GB2312                  | Chinois simplifié ANSI/OEM (République populaire de Chine, Singapour); Chinois simplifié (GB2312)                           |
| 949        | KS \_ c \_ 5601-1987        | ANSI/OEM coréen (code HANGÛL unifié)                                                               |
| 950        | Big5                    | Chinois traditionnel ANSI/OEM (Taïwan ; Hong Kong SAR, RPC); Chinois traditionnel (Big5)               |
| 1026       | IBM1026                 | IBM EBCDIC turc (latin 5)                                                                        |
| 1047       | IBM01047                | IBM EBCDIC Latin 1/système ouvert                                                                      |
| 1140       | IBM01140                | IBM EBCDIC US-Canada (037 + symbole euro); IBM EBCDIC (États-Unis-Canada-Europe)                               |
| 1141       | IBM01141                | IBM EBCDIC Allemagne (20273 + symbole euro); IBM EBCDIC (Allemagne-Europe)                                 |
| 1142       | IBM01142                | IBM EBCDIC Denmark-Norway (20277 + symbole euro); IBM EBCDIC (Danemark-Norvège-euro)                   |
| 1143       | IBM01143                | IBM EBCDIC Finland-Sweden (20278 + symbole euro); IBM EBCDIC (Finlande-Suède-Europe)                   |
| 1144       | IBM01144                | IBM EBCDIC italien (20280 + symbole euro); IBM EBCDIC (Italie-Europe)                                     |
| 1145       | IBM01145                | IBM EBCDIC Latin America-Spain (20284 + symbole euro); IBM EBCDIC (Espagne-Europe)                       |
| 1146       | IBM01146                | IBM EBCDIC-Royaume-Uni (20285 + symbole euro); IBM EBCDIC (Royaume-Uni-Europe)                               |
| 1147       | IBM01147                | IBM EBCDIC France (20297 + symbole euro); IBM EBCDIC (France-Europe)                                   |
| 1148       | IBM01148                | IBM EBCDIC international (500 + symbole euro); IBM EBCDIC (International-Europe)                       |
| 1149       | IBM01149                | IBM EBCDIC islandais (20871 + symbole euro); IBM EBCDIC (islandais-euro)                             |
| 1200       | UTF-16                  | Unicode UTF-16, Little endian, ordre d’octet (BMP de ISO 10646); disponible uniquement pour les applications managées |
| 1201       | unicodeFFFE             | Unicode UTF-16, primauté des octets de poids fort (Big endian); disponible uniquement pour les applications managées                       |
| 1250       | Windows-1250            | ANSI-Europe centrale ; Europe centrale (Windows)                                                   |
| 1251       | Windows-1251            | Cyrillique ANSI ; Cyrillique (Windows)                                                                   |
| 1252       | Windows-1252            | Latin ANSI 1 ; Europe occidentale (Windows)                                                            |
| 1253       | Windows-1253            | Grec ANSI ; Grec (Windows)                                                                         |
| 1254       | Windows-1254            | Turc ANSI ; Turc (Windows)                                                                     |
| 1 255       | Windows-1255            | Hébreu ANSI ; Hébreu (Windows)                                                                       |
| 1256       | Windows-1256            | Arabe ANSI ; Arabe (Windows)                                                                       |
| 1257       | Windows-1257            | Balte ANSI ; Balte (Windows)                                                                       |
| 1258       | Windows-1258            | ANSI/OEM vietnamien ; Vietnamien (Windows)                                                           |
| 1361       | Johab                   | Coréen (Johab)                                                                                      |
| 10000      | ordinateurs               | MAC roman ; Europe occidentale (Mac)                                                                   |
| 10001      | x-Mac-japonais          | Japonais (Mac)                                                                                      |
| 10002      | x-Mac-chinesetrad       | Chinois traditionnel MAC (Big5); Chinois traditionnel (Mac)                                           |
| 10003      | x-Mac-coréen            | Coréen (Mac)                                                                                        |
| 10004      | x-Mac-arabe            | Arabe (Mac)                                                                                        |
| 10005      | x-Mac-Hébreu            | Hébreu (Mac)                                                                                        |
| 10006      | x-Mac-grec             | Grec (Mac)                                                                                         |
| 10007      | x-Mac-cyrillique          | Cyrillique (Mac)                                                                                      |
| 10008      | x-Mac-chinesesimp       | Chinois simplifié chinois (GB 2312); Chinois simplifié (Mac)                                          |
| 10010      | x-Mac-roumain          | Roumain (Mac)                                                                                      |
| 10017      | x-Mac-ukrainien         | Ukrainien (Mac)                                                                                     |
| 10021      | x-Mac-thaï              | Thaï (Mac)                                                                                          |
| 10029      | x-Mac-ce                | MAC Latin 2 ; Europe centrale (Mac)                                                                 |
| 10079      | x-Mac-islandais         | Islandais (Mac)                                                                                     |
| 10081      | x-Mac-turc           | Turc (Mac)                                                                                       |
| 10082      | x-Mac-croate          | Croate (Mac)                                                                                      |
| 12 000      | UTF-32                  | Unicode UTF-32, primauté des octets de poids faible ; disponible uniquement pour les applications managées                    |
| 12001      | UTF-32BE                | Unicode UTF-32, primauté des octets de poids fort (Big endian) disponible uniquement pour les applications managées                       |
| 20000      | CNS x-chinois \_          | CNS Taïwan ; Chinois traditionnel (CNS)                                                               |
| 20001      | x-cp20001               | TCA Taïwan                                                                                          |
| 20002      | \_chinois eTEN         | ETEN Taïwan ; Chinois traditionnel (eten)                                                             |
| 20003      | x-cp20003               | IBM5550 Taïwan                                                                                      |
| 20004      | x-cp20004               | Teletext Taïwan                                                                                     |
| 20005      | x-cp20005               | Taïwan Wang                                                                                         |
| 20105      | x-IA5                   | IA5 (IRV international alphabet no. 5, 7 bits); Europe occidentale (IA5)                               |
| 20106      | x-IA5-allemand            | IA5 allemand (7 bits)                                                                                  |
| 20107      | x-IA5-suédois           | IA5 suédois (7 bits)                                                                                 |
| 20108      | x-IA5-norvégien         | IA5 norvégien (7 bits)                                                                               |
| 20127      | US-ASCII                | US-ASCII (7 bits)                                                                                    |
| 20261      | x-cp20261               | T. 61                                                                                                |
| 20269      | x-cp20269               | ISO 6937 accent sans espace                                                                         |
| 20273      | IBM273                  | IBM EBCDIC Allemagne                                                                                  |
| 20277      | IBM277                  | Denmark-Norway IBM EBCDIC                                                                           |
| 20278      | IBM278                  | Finland-Sweden IBM EBCDIC                                                                           |
| 20280      | IBM280                  | IBM EBCDIC italien                                                                                    |
| 20284      | IBM284                  | IBM EBCDIC Latin America-Spain                                                                      |
| 20285      | IBM285                  | IBM EBCDIC-Royaume-Uni                                                                           |
| 20290      | IBM290                  | IBM EBCDIC japonais katakana étendu                                                               |
| 20297      | IBM297                  | IBM EBCDIC France                                                                                   |
| 20420      | IBM420                  | IBM EBCDIC arabe                                                                                   |
| 20423      | IBM423                  | IBM EBCDIC grec                                                                                    |
| 20424      | IBM424                  | IBM EBCDIC Hébreu                                                                                   |
| 20833      | x-EBCDIC-KoreanExtended | IBM EBCDIC coréen étendu                                                                          |
| 20838      | IBM-thaï                | IBM EBCDIC thaï                                                                                     |
| 20866      | koi8-r                  | Russe (KOI8-R); Cyrillique (KOI8-R)                                                                 |
| 20871      | IBM871                  | IBM EBCDIC islandais                                                                                |
| 20880      | IBM880                  | IBM EBCDIC cyrillique russe                                                                         |
| 20905      | IBM905                  | IBM EBCDIC turc                                                                                  |
| 20924      | IBM00924                | IBM EBCDIC Latin 1/système ouvert (1047 + symbole euro)                                                 |
| 20932      | EUC-JP                  | Japonais (JIS 0208-1990 et 0212-1990)                                                              |
| 20936      | x-cp20936               | Chinois simplifié (GB2312); Chinois simplifié (GB2312-80)                                         |
| 20949      | x-cp20949               | Wansung coréen                                                                                      |
| 21025      | cp1025                  | IBM EBCDIC cyrillique Serbian-Bulgarian                                                               |
| 21027      |                         | déconseillé                                                                                        |
| 21866      | KOI8-u                  | Ukrainien (KOI8-U); Cyrillique (KOI8-U)                                                               |
| 28591      | ISO-8859-1              | ISO 8859-1 latin 1 ; Europe occidentale (ISO)                                                          |
| 28592      | ISO-8859-2              | ISO 8859-2-Europe centrale ; Europe centrale (ISO)                                                 |
| 28593      | ISO-8859-3              | ISO 8859-3 latin 3                                                                                  |
| 28594      | ISO-8859-4              | ISO 8859-4 Baltique                                                                                   |
| 28595      | ISO-8859-5              | ISO 8859-5 cyrillique                                                                                 |
| 28596      | ISO-8859-6              | ISO 8859-6 arabe                                                                                   |
| 28597      | ISO-8859-7              | ISO 8859-7 grec                                                                                    |
| 28598      | ISO-8859-8              | ISO 8859-8 Hébreu ; Hébreu (ISO-Visual)                                                              |
| 28599      | ISO-8859-9              | ISO 8859-9 turc                                                                                  |
| 28603      | ISO-8859-13             | ISO 8859-13 estonien                                                                                |
| 28605      | ISO-8859-15             | ISO 8859-15 latin 9                                                                                 |
| 29001      | x-Europa                | Europa 3                                                                                            |
| 38598      | ISO-8859-8-i            | ISO 8859-8 Hébreu ; Hébreu (ISO-Logical)                                                             |
| 50220      | ISO-2022-JP             | ISO 2022 japonais sans katakana demi-chasse ; Japonais (JIS)                                        |
| 50221      | csISO2022JP             | ISO 2022 japonais avec katakana demi-chasse ; Japanese (JIS-autoriser les caractères Kana de 1 octet)                         |
| 50222      | ISO-2022-JP             | ISO 2022 japonais JIS X 0201-1989 ; Japanese (JIS-autoriser les caractères Kana à 1 octet-SO/SI)                         |
| 50225      | ISO-2022-KR             | ISO 2022 coréen                                                                                     |
| 50227      | x-cp50227               | ISO 2022 chinois simplifié ; Chinois simplifié (ISO 2022)                                          |
| 50229      |                         | ISO 2022 chinois traditionnel                                                                        |
| 50930      |                         | Japonais EBCDIC (Katakana) étendu                                                                 |
| 50931      |                         | US-Canada EBCDIC et japonais                                                                       |
| 50933      |                         | EBCDIC coréen étendu et coréen                                                                   |
| 50935      |                         | Chinois simplifié EBCDIC étendu et chinois simplifié                                           |
| 50936      |                         | Chinois simplifié (EBCDIC)                                                                           |
| 50937      |                         | US-Canada EBCDIC et chinois traditionnel                                                            |
| 50939      |                         | Japonais EBCDIC (latin) étendu et japonais                                                       |
| 51932      | EUC-JP                  | Japonais EUC                                                                                        |
| 51936      | EUC-CN                  | Chinois simplifié EUC ; Chinois simplifié (EUC)                                                    |
| 51949      | EUC-KR                  | Coréen (coréen)                                                                                          |
| 51950      |                         | Chinois traditionnel EUC                                                                             |
| 52936      | Hz-GB-2312              | HZ-chinois simplifié GB2312 ; Chinois simplifié (HZ)                                               |
| 54936      | GB18030                 | **Windows XP et versions ultérieures :** GB18030 chinois simplifié (4 octets); Chinois simplifié (GB18030)         |
| 57002      | x-ISCII-de              | ISCII DÉVANÂGARÎ                                                                                    |
| 57003      | x-ISCII-est              | Bangla ISCII                                                                                        |
| 57004      | x-ISCII-ta              | Tamoul ISCII                                                                                         |
| 57005      | x-ISCII-te              | Telugu ISCII                                                                                        |
| 57006      | x-ISCII-As              | ISCII assamais                                                                                      |
| 57007      | x-ISCII-or              | ISCII Odia                                                                                          |
| 57008      | x-ISCII-ka              | Kannada ISCII                                                                                       |
| 57009      | x-ISCII-ma              | Malayalam ISCII                                                                                     |
| 57010      | x-ISCII-Gu              | Gujarati ISCII                                                                                      |
| 57011      | x-ISCII-PA              | Pendjabi ISCII                                                                                       |
| 65 000      | UTF-7                   | Unicode (UTF-7)                                                                                     |
| 65 001      | utf-8                   | Unicode (UTF-8)                                                                                     |



 

 

 



