---
title: DSY-PS
description: Calcule le taux de modification de l’axe y de la cible de rendu.
ms.assetid: b35862d7-fc43-4cf8-bfe3-3eccbda2a133
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 735b0d3ae75abe76e5075b3d22612ad0d56c7a21bab74f29010f47b54d161324
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950539"
---
# <a name="dsy---ps"></a>DSY-PS

Calcule le taux de modification de l’axe y de la cible de rendu.

## <a name="syntax"></a>Syntaxe



| DSY DST, SRC |
|--------------|



 

Où :

-   l’heure d’été est un registre de destination.
-   SRC est un registre de source d’entrée.

## <a name="remarks"></a>Remarques



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dsy                   |      |      |      |      |      | x    | x     | x    | x     |



 

Le taux de modification calculé à partir du Registre source est une approximation sur le contenu du même registre dans le ou les pixels adjacents qui exécutent le nuanceur de pixels dans l’étape de verrouillage avec le pixel actuel.

Les instructions [DSX](dsx---ps.md) et DSY calculent leur résultat en examinant le contenu actuel du Registre source (par composant) pour les différents pixels de la zone locale s’exécutant dans l’étape de verrouillage. La formule exacte utilisée pour calculer le dégradé varie en fonction du matériel, mais doit être cohérente avec la manière dont le matériel effectue les mêmes opérations dans le cadre du processus de calcul du niveau de détail pour l’échantillonnage de texture.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[texldd-PS](texldd---ps.md)
</dt> </dl>

 

 




