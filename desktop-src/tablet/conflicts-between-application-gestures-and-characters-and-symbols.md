---
description: Description des conflits entre les gestes d’application et les caractères et symboles.
ms.assetid: c9b8c284-7c31-4fb0-8cc4-ff09c9c4f228
title: Conflits entre les gestes d’application et les caractères et symboles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5819bfd7013bc39ecb622b09a1ae42816bb969ec63bf062d19597575bb958279
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009019"
---
# <a name="conflicts-between-application-gestures-and-characters-and-symbols"></a>Conflits entre les gestes d’application et les caractères et symboles

Certains mouvements d’application peuvent entrer en conflit avec des caractères, des combinaisons de caractères, des symboles, des combinaisons de caractères et de symboles ou des mots entiers écrits en un seul trait. La plupart de ces conflits sont évités en ayant une compréhension détaillée du contexte dans lequel le mouvement de l’application est effectué.

Par exemple, pour faire la distinction entre un mouvement droit et un tiret (-) ou un trait de soulignement ( \_ ), une application peut filtrer la manière dont le mouvement est fermé en caractères voisins, la taille relative par rapport aux caractères, ou d’autres informations contenues dans un paquet. La synchronisation du mouvement de l’application peut également être un facteur déterminant dans le choix entre les gestes et les caractères. Il peut y avoir plus de pause avant l’application d’un mouvement d’application que pour l’entrée de caractères. À moins qu’un utilisateur effectue une série de mouvements d’annulation ou de retour arrière, il peut également y avoir plus de pause après un mouvement qu’un caractère.

Les rubriques suivantes détaillent ces conflits :

-   [Conflits avec caractères latins et symboles](conflicts-with-latin-characters-and-symbols.md)
-   [Conflits avec des caractères de East-Asian](conflicts-with-east-asian-characters.md)

 

 



