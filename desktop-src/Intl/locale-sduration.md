---
description: paramètres régionaux \_ SDURATION
ms.assetid: 45ffd7ed-f964-4948-8679-cf960b5c1e0e
title: LOCALE_SDURATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00740d2f041794b36e8f0e0d8ad2d25723bc12e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522854"
---
# <a name="locale_sduration"></a>paramètres régionaux \_ SDURATION

**Windows Vista et versions ultérieures :** Format de durée de temps composé des images de format énumérées dans le tableau suivant. Le format est semblable au format des [paramètres régionaux \_ sTimeFormat par](locale-stime-constants.md). Comme pour les paramètres régionaux \_ sTimeFormat par, ce format peut également inclure toute chaîne de caractères placée entre guillemets simples. Les formats peuvent inclure, par exemple, "h :mm : SS" ou "d d’h’h’is'. fff'". En comparaison avec les paramètres régionaux \_ sTimeFormat par, il existe des images de format supplémentaires pour les fractions de seconde. Étant donné que ce format est pour la durée, pas pour l’heure, il ne spécifie pas un système à horloge de 12 ou 24 heures, ou inclut un indicateur AM/PM. Cette constante peut être utilisée, par exemple, pour une application multimédias qui affiche l’heure du fichier ou une application d’événement sportif qui affiche les heures de fin.



| Valeur | Signification                                                                                                                                                                                                                             |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| h     | Heures sans zéros non significatifs pour les heures à un chiffre                                                                                                                                                                                  |
| hh    | Heures avec des zéros non significatifs pour les heures à un chiffre                                                                                                                                                                                     |
| m     | Minutes sans zéros non significatifs pour les minutes à un chiffre                                                                                                                                                                              |
| MM    | Minutes avec zéros non significatifs pour les minutes à un chiffre                                                                                                                                                                                 |
| s     | Secondes sans zéros non significatifs pour les secondes à un chiffre                                                                                                                                                                              |
| ss    | Secondes avec des zéros non significatifs pour les secondes à un chiffre                                                                                                                                                                                 |
| f     | Dixièmes de seconde                                                                                                                                                                                                                  |
| ff    | Centièmes de seconde                                                                                                                                                                                                              |
| fff   | Millièmes de seconde ; le caractère « f » peut se produire jusqu’à neuf fois consécutives (fffffffff), bien que la prise en charge des minuteries de fréquence soit limitée à 100 nanosecondes ; Si neuf caractères sont présents, les deux derniers chiffres sont toujours nuls |



 

 

 



