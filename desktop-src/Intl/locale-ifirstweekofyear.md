---
description: paramètres régionaux \_ IFIRSTWEEKOFYEAR
ms.assetid: 866a28b7-e0b8-4b99-96df-345791a24833
title: LOCALE_IFIRSTWEEKOFYEAR
ms.topic: article
ms.date: 03/04/2020
ms.openlocfilehash: 7f391fb167a9362fc8770bbcc5a495170148b489
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "106523091"
---
# <a name="locale_ifirstweekofyear"></a>paramètres régionaux \_ IFIRSTWEEKOFYEAR

Première semaine de l’année.



| Valeur | Signification                                                                                                                          |
|-------|----------------------------------------------------------------------------------------------------------------------------------|
| 0     | La semaine contenant 1/1 est la première semaine de l’année. Notez qu’il peut s’agir d’une seule journée, si 1/1 tombe le dernier jour de la semaine. |
| 1     | La première semaine complète suivante 1/1 est la première semaine de l’année.                                                                     |
| 2     | La première semaine contenant au moins quatre jours est la première semaine de l’année. Compatible ISO 8601.                                     |

Si LOCALE_IFIRSTWEEKOFYEAR a la valeur 2, LOCALE_IFIRSTDAYOFWEEK a la valeur 0 (lundi) et LOCALE_ICALENDARTYPE est grégorien, la première semaine suit la définition ISO 8601, où la première semaine est la semaine avec le premier jeudi de l’année grégorienne.


 

 

 



