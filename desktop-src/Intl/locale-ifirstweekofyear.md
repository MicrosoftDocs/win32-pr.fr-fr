---
description: paramètres régionaux \_ IFIRSTWEEKOFYEAR
ms.assetid: 866a28b7-e0b8-4b99-96df-345791a24833
title: LOCALE_IFIRSTWEEKOFYEAR
ms.topic: article
ms.date: 03/04/2020
ms.openlocfilehash: da0d8697e8a02bb6943f4a4154a1ea89c4e01cbaed7576631e3a61d161e80503
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147422"
---
# <a name="locale_ifirstweekofyear"></a>paramètres régionaux \_ IFIRSTWEEKOFYEAR

Première semaine de l’année.



| Valeur | Signification                                                                                                                          |
|-------|----------------------------------------------------------------------------------------------------------------------------------|
| 0     | La semaine contenant 1/1 est la première semaine de l’année. Notez qu’il peut s’agir d’une seule journée, si 1/1 tombe le dernier jour de la semaine. |
| 1     | La première semaine complète suivante 1/1 est la première semaine de l’année.                                                                     |
| 2     | La première semaine contenant au moins quatre jours est la première semaine de l’année. Compatible ISO 8601.                                     |

Si LOCALE_IFIRSTWEEKOFYEAR a la valeur 2, LOCALE_IFIRSTDAYOFWEEK a la valeur 0 (lundi) et LOCALE_ICALENDARTYPE est grégorien, la première semaine suit la définition ISO 8601, où la première semaine est la semaine avec le premier jeudi de l’année grégorienne.


 

 

 



