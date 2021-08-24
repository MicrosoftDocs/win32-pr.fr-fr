---
description: Un effet (qui est souvent stocké dans un fichier avec une extension de fichier. FX) déclare l’état du pipeline défini par un effet.
ms.assetid: 75b76d65-be97-41c2-8c45-4369fcfd69ce
title: Format d’effet (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c9511304a3c24784381092017659fb1a6c593808253383443c8e9f6917c2be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852823"
---
# <a name="effect-format-direct3d-10"></a>Format d’effet (Direct3D 10)

Un effet (qui est souvent stocké dans un fichier avec une extension de fichier. FX) déclare l’état du pipeline défini par un effet. L’état de l’effet peut être divisé en trois catégories :

-   [Variables](d3d10-effect-variable-syntax.md), qui sont généralement déclarées en haut d’un effet.
-   Les [fonctions](d3d10-effect-function-syntax.md), qui implémentent le code du nuanceur, ou sont utilisées comme fonctions d’assistance par d’autres fonctions.
-   [Technique](d3d10-effect-technique-syntax.md), qui implémente des séquences de rendu à l’aide d’une ou de plusieurs passes d’effet. Chaque passe définit un ou plusieurs [groupes d’États](d3d10-effect-states.md) et appelle des fonctions de nuanceur.

![diagramme des catégories d’état d’effet](images/d3d10-effect-intro.png)

Le diagramme précédent montre les catégories d’état d’effet.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence d’effet](d3d10-graphics-reference-effect.md)
</dt> </dl>

 

 



