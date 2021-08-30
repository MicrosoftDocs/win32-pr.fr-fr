---
description: Calcul des valeurs de paramètre
ms.assetid: cc3c26ed-a007-4350-99be-0ebd94953689
title: Calcul des valeurs de paramètre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad23cb9c50413fed36dde205ef97be0139dd6152f0a301f230793ef2cb131684
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057769"
---
# <a name="calculating-parameter-values"></a>Calcul des valeurs de paramètre

Éventuellement, une mémoire tampon d’entrée peut être très volumineuse. dans l’idéal, lorsque le DMO traite la mémoire tampon, les paramètres suivent exactement leurs courbes dans tout le lot de données. toutefois, un DMO a une certaine liberté dans la manière dont il calcule ces valeurs.

-   L’approche la plus précise consiste à calculer la valeur exacte pour chaque unité atomique de données ; par exemple, chaque exemple audio. Cette approche est la plus coûteuse en termes de calcul.
-   Une autre approche consiste à découper les données en unités plus petites de taille fixe, comme les exemples 100. Cette approche crée un effet « escalier-Stepping ». Pour certains paramètres, cela peut être acceptable. Dans les effets audio, il peut créer des artefacts sonores.
-   Un compromis consiste à utiliser la technique précédente, mais au sein de chaque lot, effectuer une interpolation linéaire de la valeur de paramètre pour chaque exemple.

Ces problèmes sont particulièrement importants pour le traitement audio. Une seconde d’audio peut contenir des échantillons audio 48 000 par canal, ce qui représente un grand nombre de calculs à effectuer, mais l’oreille est sensible aux artefacts tels que les alias.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Paramètres de média](media-parameters.md)
</dt> </dl>

 

 



