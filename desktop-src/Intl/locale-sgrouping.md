---
description: paramètres régionaux \_ SGROUPING
ms.assetid: 3f07ecae-38f4-477b-8b23-a9cd87613c24
title: LOCALE_SGROUPING
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db7242f7d515ce17872376b9a067a7b41831a331
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953255"
---
# <a name="locale_sgrouping"></a>paramètres régionaux \_ SGROUPING

Tailles pour chaque groupe de chiffres à gauche du séparateur décimal. Le nombre maximal de caractères autorisés pour cette chaîne est dix, y compris un caractère null de fin. Une taille explicite est nécessaire pour chaque groupe, et les tailles sont séparées par des points-virgules. Si la dernière valeur est égale à 0, la valeur précédente est répétée. Par exemple, pour regrouper des milliers, spécifiez 3 ; 0. Les paramètres régionaux indo-aryens groupent les premiers mille, puis regroupent par centaines. Par exemple, 12, 34, 56789 est représenté par 3 ; 2 ; 0.

Autres exemples :



| Caractéristique | Chaîne résultante   |
|---------------|--------------------|
| 3 ; 0           | 3 000 000 000 000  |
| 3 ; 2 ; 0         | 30, 00, 00, 00, 00000 |
| 3             | 3 000 000 000 000     |
| 3 ; 2           | 30000000, 00000    |



 

 

 



