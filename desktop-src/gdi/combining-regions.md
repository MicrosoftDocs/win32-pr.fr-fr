---
description: Une application combine deux régions en appelant la fonction CombineRgn.
ms.assetid: d16f9ca5-33e2-4752-900e-743245838377
title: Combinaison de régions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f51db22daea448acfb02120844ca2859a5ba11e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570784"
---
# <a name="combining-regions"></a>Combinaison de régions

Une application combine deux régions en appelant la fonction [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn) . À l’aide de cette fonction, une application peut combiner les parties qui se croisent de deux régions, toutes les parties à l’exception de celles de deux régions, les deux régions d’origine dans leur intégralité, et ainsi de suite. Vous trouverez ci-dessous cinq valeurs qui définissent les combinaisons de régions.



| Valeur     | Signification                                                                               |
|-----------|---------------------------------------------------------------------------------------|
| RGN \_ et  | Les parties qui se croisent de deux régions d’origine définissent une nouvelle région.                   |
| \_copie RGN | Une copie de la première (des deux régions d’origine) définit une nouvelle région.               |
| \_diff RGN | La partie de la première région qui ne croise pas la seconde définit une nouvelle région. |
| RGN \_ ou   | Les deux régions d’origine définissent une nouvelle région.                                         |
| RGN \_ Xor  | Les parties des deux régions d’origine qui ne se chevauchent pas définissent une nouvelle région.      |



 

L’illustration suivante montre les cinq combinaisons possibles d’un carré et d’une région circulaire résultant d’un appel à [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn).

![illustration illustrant les résultats décrits dans le tableau précédent](images/csrgn-02.png)

 

 



