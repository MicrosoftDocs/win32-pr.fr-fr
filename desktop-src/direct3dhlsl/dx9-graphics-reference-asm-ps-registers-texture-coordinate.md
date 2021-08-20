---
title: Registre de coordonnées de texture (référence PS HLSL)
description: Registre d’entrée de nuanceur de pixels contenant des coordonnées de texture.
ms.assetid: 423f249d-fa9f-41f2-adbf-d97ceace06f5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 42ef86bba7ca3c31f6158a6aee8d3228cd696fa500f4066b2ef7492558c307c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118090024"
---
# <a name="texture-coordinate-register-hlsl-ps-reference"></a>Registre de coordonnées de texture (référence PS HLSL)

Registre d’entrée de nuanceur de pixels contenant des coordonnées de texture.



| Versions de nuanceur de pixels       | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ logiciels | 2 \_ x | 3 \_ 0 | 3 \_ logiciels |
|-----------------------------|------|------|------|------|------|-------|------|------|-------|
| Registre de coordonnées de texture |      |      |      |      | x    | x     | x    | x    | x     |



 

Un registre de coordonnées de texture contient des données de coordonnée de texture. Avant d’utiliser un registre de coordonnées de texture, il doit être déclaré par une déclaration de nuanceur de pixels. Pour plus d’informations sur la façon de déclarer un registre de texture, consultez [DCL-(SM2, SM3-PS ASM)](dcl---ps.md).

En outre, Voici d’autres propriétés des registres de coordonnées de texture.

-   Il y a huit registres de coordonnées de texture de nuanceur de pixels, T0 à T7.
-   Il s’agit de registres en lecture seule.
-   Elles contiennent des valeurs RVBA à quatre composants à partir des vertex d’entrée.
-   Elles contiennent des valeurs de données de plage dynamique haute précision interpolées à partir des données de vertex. Les valeurs sont générées avec l’interpolation de perspective correcte. Les données sont de précision à virgule flottante et sont signées.
-   Il n’y a qu’un maximum dans une seule instruction.
-   Plusieurs lectures d’un registre de coordonnées de texture dans un nuanceur doivent utiliser un [masque d’écriture de registre de destination](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)identique.
-   Le modificateur de précision partielle facultatif \[ \_ pp \] s’applique aux lectures dépendantes. Cela est dû au fait que la précision partielle affecte les opérations arithmétiques impliquant le registre de coordonnées de texture. Il n’affecte pas la précision des instructions d’adresse de texture, car il n’affecte pas les itérateurs de coordonnée de texture.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscrit](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




