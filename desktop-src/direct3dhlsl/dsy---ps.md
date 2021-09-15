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
ms.openlocfilehash: c5f595d836ed8eb8525175ddb81e743cb7a04811
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127524701"
---
# <a name="dsy---ps"></a>DSY-PS

Calcule le taux de modification de l’axe y de la cible de rendu.

## <a name="syntax"></a>Syntaxe



| DSY DST, SRC |
|--------------|



 

Où :

-   l’heure d’été est un registre de destination.
-   SRC est un registre de source d’entrée.

## <a name="remarks"></a>Notes



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

 

 




