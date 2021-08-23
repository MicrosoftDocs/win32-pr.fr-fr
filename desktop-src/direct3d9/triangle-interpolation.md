---
description: Pendant le rendu, le pipeline interpole les données de vertex sur chaque triangle.
ms.assetid: 6fa05e56-c4cd-4623-abe9-2b1c8bbc644b
title: Interpolation de triangle (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a411f53351ccd5d3407b358b03e705677e9bf5a96a57b162016afe09332bae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746259"
---
# <a name="triangle-interpolation-direct3d-9"></a>Interpolation de triangle (Direct3D 9)

Pendant le rendu, le pipeline interpole les données de vertex sur chaque triangle. Les données de vertex peuvent être une grande variété de données et peuvent inclure (sans s’y limiter) : couleur diffuse, couleur spéculaire, alpha diffuse (opacité du triangle), alpha spéculaire et un facteur de brouillard (issu de l’alpha spéculaire pour le pipeline de la fonction fixe et du registre de brouillard pour le pipeline de vertex programmable). Les données de vertex sont définies par la [déclaration de vertex (Direct3D 9)](vertex-declaration.md).

Pour certaines données de vertex, l’interpolation dépend du mode de trame actuel, comme indiqué dans le tableau suivant.



| Mode d’ombrage | Description                                                                                                                                                                 |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| À deux dimensions         | Seul le facteur de brouillard est interpolé en mode ombré plat. Pour toutes les autres valeurs interpolées, la couleur du premier vertex du triangle est appliquée sur l’ensemble du visage. |
| Gouraud      | L’interpolation linéaire est effectuée entre les trois vertex.                                                                                                               |



 

La couleur diffuse et la couleur spéculaire sont traitées différemment, en fonction du modèle de couleurs. Dans le modèle de couleurs RVB, le système utilise les composants de couleur rouge, vert et bleu dans l’interpolation.

Le composant alpha d’une couleur est traité comme une valeur interpolée distincte, car les pilotes de périphérique peuvent implémenter la transparence de deux manières différentes : à l’aide de la fusion de texture ou à l’aide de stippling.

Utilisez le membre ShadeCaps de la structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) pour déterminer les formes d’interpolation prises en charge par le pilote de périphérique actuel.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Systèmes de coordonnées et géométrie](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



