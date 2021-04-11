---
description: Le placage de relief est une forme spéciale de mappage d’environnement spéculaire ou diffus qui simule les réflexions des objets fractionnés de manière fine sans nécessiter des nombres de polygones extrêmement élevés.
ms.assetid: 3e195e4f-3fa9-43c4-b2e5-42a6b3aaccf2
title: Placage de relief (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9dba4621568f595eae965941168ad6930e183f7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111274"
---
# <a name="bump-mapping-direct3d-9"></a>Placage de relief (Direct3D 9)

Le placage de relief est une forme spéciale de mappage d’environnement spéculaire ou diffus qui simule les réflexions des objets fractionnés de manière fine sans nécessiter des nombres de polygones extrêmement élevés. Le mappage de relief implémenté par Direct3D peut être décrit avec précision en cas de perturbation de la coordonnée de texture par pixel des cartes d’environnement spéculaires ou diffuses, car vous fournissez des informations sur le contour de la carte de relief en termes de valeurs Delta, que le système applique aux coordonnées de texture vous et v d’une carte d’environnement lors de la prochaine étape de texture. Les valeurs Delta sont encodées au format de pixel de la surface de la carte de relief (voir formats de pixel de la [carte de relief](bump-map-pixel-formats.md)).

Le placage de relief repose sur la fusion de plusieurs textures. Cela signifie que l’appareil doit prendre en charge au moins deux phases de fusion ; une pour la carte de relief et une autre pour une carte d’environnement. Au moins trois étapes de fusion de texture sont requises pour appliquer une carte de texture de base supplémentaire, ce qui est le cas le plus courant. Le diagramme suivant montre les relations entre la texture de base, la carte de relief et la carte d’environnement dans la texture de fusion en cascade.

![diagramme de la fusion en cascade de la texture](images/bumpmap-tcascade.png)

Vous devez préparer les étapes de texture de manière appropriée pour activer le mappage de relief. Les rubriques suivantes présentent un placage de relief et fournissent des détails sur la façon dont vous pouvez l’utiliser dans vos applications :

-   [Formats de pixel de la carte de relief](bump-map-pixel-formats.md)
-   [Formules de mappage de relief](bump-mapping-formulas.md)
-   [Utilisation du mappage de relief](using-bump-mapping.md)

Direct3D ne prend pas en charge en mode natif les mappages de hauteur ; Il s’agit simplement d’un format pratique dans lequel stocker et visualiser les données de contour. Votre application peut stocker des informations de contour dans n’importe quel format, voire générer une carte de relief des procédures.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Pipeline de pixels](pixel-pipeline.md)
</dt> </dl>

 

 



