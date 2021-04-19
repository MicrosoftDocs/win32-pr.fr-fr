---
description: Les champs de la page de codes sont utilisés dans les structures FONTSIGNATURE et LOCALESIGNATURE. Remarque tous les paramètres régionaux ne prennent pas en charge les pages de codes.
ms.assetid: 830b1a88-cb0c-4719-b857-4cc2cd67dd5d
title: Champs de page de codes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08f9df44ac14d935a026a10ab1e71eb7378840de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543545"
---
# <a name="code-page-bitfields"></a>Champs de page de codes

Les champs de la page de codes sont utilisés dans les structures [**fontSignature**](/windows/win32/api/wingdi/ns-wingdi-fontsignature) et [**LOCALESIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-localesignature) .

> [!Note]  
> Tous les paramètres régionaux ne prennent pas en charge les pages de codes. Les champs de paramètres binaires décrits dans cette rubrique ne s’appliquent pas aux paramètres régionaux Unicode. Pour déterminer les scripts pris en charge pour les paramètres régionaux, votre application peut utiliser les paramètres régionaux constants de l’identificateur de paramètres régionaux [ \_ SSCRIPTS](locale-sscripts.md) avec [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex).

 

> [!Note]  
> La présence d’un bit dans un champ de bits de page de codes ne signifie pas nécessairement que toutes les chaînes pour des paramètres régionaux peuvent être encodées dans cette page de codes sans perte. Pour conserver les données sans perte, il est recommandé d’utiliser Unicode UTF-8 ou UTF-16.

 



| bit          | Page de codes | Description                                           |
|--------------|-----------|-------------------------------------------------------|
| ANSI         |           |                                                       |
| 0            | 1252      | Latin 1                                               |
| 1            | 1250      | Latin 2 : Europe centrale                               |
| 2            | 1251      | Cyrillique                                              |
| 3            | 1253      | Grec                                                 |
| 4            | 1254      | Turc                                               |
| 5            | 1 255      | Hébreu                                                |
| 6            | 1256      | Arabe                                                |
| 7            | 1257      | Balte                                                |
| 8            | 1258      | Vietnamien                                            |
| 9 - 15       |           | Réservé pour ANSI                                     |
| ANSI et OEM |           |                                                       |
| 16           | 874       | Thaï                                                  |
| 17           | 932       | Japonais, Shift-JIS                                   |
| 18           | 936       | Chinois simplifié (République populaire de Chine, Singapour)                   |
| 19           | 949       | Code Hangul unifié coréen (code Hangul TongHabHyung) |
| 20           | 950       | Chinois traditionnel (Taïwan) Hong Kong (R.A.S.), RPC ()      |
| 21           | 1361      | Coréen (Johab)                                        |
| 22 - 29      |           | Réservé pour les autres ANSI et OEM                   |
| 30 - 31      |           | Réservé par le système.                                   |
| OEM          |           |                                                       |
| 32-46      |           | Réservé pour OEM                                      |
| 47           | 1258      | Vietnamien                                            |
| 48           | 869       | Grec moderne                                          |
| 49           | 866       | Russe                                               |
| 50           | 865       | Nordique                                                |
| 51           | 864       | Arabe                                                |
| 52           | 863       | Français (Canada)                                       |
| 53           | 862       |                                                       |
| 54           | 861       | Islandais                                             |
| 55           | 860       | Portugais                                            |
| 56           | 857       | Turc                                               |
| 57           | 855       | Bé principalement en russe                           |
| 58           | 852       | Latin 2                                               |
| 59           | 775       | Balte                                                |
| 60           | 737       | Grèce anciennement 437G                                  |
| 61           | 708 ; 720  | Arabe ASMO 708                                      |
| 62           | 850       | Latin multilingue 1                                  |
| 63           | 437       | US                                                    |



 

 

 



