---
title: Assemblage des chaînes de requête
description: Dans Active Directory, l’utilisation de critères de filtrage spécifiques permet d’améliorer les performances de recherche. Cela est dû au fait que Active Directory évalue tous les prédicats, identifie les index, puis sélectionne un index susceptible de générer le plus petit ensemble de valeurs retournées.
ms.assetid: 4139eedb-1383-4654-9b40-5e294a71be24
ms.tgt_platform: multiple
keywords:
- Assemblage des chaînes de requête ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 610ba78d6536d9cfe12f296fcbfa46d04cd572ae05cdb7d3bb8b0e1e7b5d32a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962194"
---
# <a name="assembling-query-strings"></a>Assemblage des chaînes de requête

Dans Active Directory, l’utilisation de critères de filtrage spécifiques permet d’améliorer les performances de recherche. Cela est dû au fait que Active Directory évalue tous les prédicats, identifie les index, puis sélectionne un index susceptible de générer le plus petit ensemble de valeurs retournées.

Évitez de rechercher du texte au milieu ou à la fin d’une chaîne, par exemple, « CN = \* Hill \* » ou « CN = \* larouse ».

Lorsque cela est possible, recherchez des attributs indexés. Les attributs indexés sont stockés sur tous les contrôleurs de domaine, de sorte que la requête sera plus rapide que la recherche d’un attribut non indexé.

 

 




