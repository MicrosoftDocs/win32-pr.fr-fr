---
description: Paramètres régionaux \_ smon \* constantes
ms.assetid: df7f026b-2f2d-420f-8a14-656734409835
title: Constantes LOCALE_SMON *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e932888360cc81e08a1cff1f45082b5fc1b91ead
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516971"
---
# <a name="locale_smon-constants"></a>Paramètres régionaux \_ smon \* constantes

Cette rubrique définit les \_ \* constantes smon de paramètres régionaux utilisées par nls pour représenter des valeurs monétaires.



| Valeur                   | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| paramètres régionaux \_ SMONDECIMALSEP  | Caractère (s) utilisé (s) comme séparateur décimal monétaire. Le nombre maximal de caractères autorisés pour cette chaîne est de quatre, y compris un caractère null de fin. Par exemple, si un montant monétaire est affiché sous la forme « $3,40 », tout comme « trois dollars et 40 centimes » s’affiche dans le États-Unis, le séparateur décimal monétaire est « . ».                                                                                                                                             |
| paramètres régionaux \_ SMONGROUPING    | Tailles pour chaque groupe de chiffres monétaires à gauche du séparateur décimal. Le nombre maximal de caractères autorisés pour cette chaîne est dix, y compris un caractère null de fin. Une taille explicite est nécessaire pour chaque groupe, et les tailles sont séparées par des points-virgules. Si la dernière valeur est égale à 0, la valeur précédente est répétée. Par exemple, pour regrouper des milliers, spécifiez 3 ; 0. Les langues indiennes groupent les premiers mille, puis regroupent par centaines. Par exemple, 12, 34, 56789 est représenté par 3 ; 2 ; 0. |
| paramètres régionaux \_ SMONTHOUSANDSEP | Caractère (s) utilisé (s) comme séparateur monétaire entre des groupes de chiffres à gauche du séparateur décimal. Le nombre maximal de caractères autorisés pour cette chaîne est de quatre, y compris un caractère null de fin. En règle générale, les groupes représentent des milliers. Toutefois, en fonction de la valeur spécifiée pour les paramètres régionaux \_ SMONGROUPING, ils peuvent représenter autre chose.                                                                                                                                 |



 

 

 



