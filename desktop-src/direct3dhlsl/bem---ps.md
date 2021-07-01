---
title: Bem-PS
description: Appliquez une transformation de mappage d’environnement factice.
ms.assetid: b41009d4-a2bb-4397-ad23-c95ef2620a66
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1adae07e3e2ebbca085981ca03a3b6449e2ffd9d
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129928"
---
# <a name="bem---ps"></a>Bem-PS

Appliquez une transformation de mappage d’environnement factice.

## <a name="syntax"></a>Syntaxe



| Bem DST. RG, src0, src1 |
|------------------------|



 

where

-   DST. RG DST est le registre de destination. Le masque d’écriture du composant rouge et vert doit être utilisé.
-   src0 est un registre source.
-   src1 est un registre source.

## <a name="remarks"></a>Remarques



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| bem                   |      |      |      | x    |      |      |       |      |       |



 

Cette instruction effectue le calcul suivant.


```
(Given n == dest register #)
dest.r = src0.r + D3DTSS_BUMPENVMAT00(stage n) * src1.r 
                + D3DTSS_BUMPENVMAT10(stage n) * src1.g

dest.g = src0.g + D3DTSS_BUMPENVMAT01(stage n) * src1.r
                + D3DTSS_BUMPENVMAT11(stage n) * src1.g
```



Règles d’utilisation de BEM :

1.  Bem doit apparaître dans la première phase d’un nuanceur (c’est-à-dire avant un marqueur de phase).
2.  Bem consomme deux emplacements d’instructions arithmétiques.
3.  Une seule utilisation de cette instruction est autorisée par nuanceur.
4.  Le writemask de destination doit être. RG/.XY.
5.  Cette instruction ne peut pas être co-émise.
6.  Hormis la restriction selon laquelle le masque d’écriture de destination est. RG, les modificateurs sur la source src0, src1 et les modificateurs d’instruction ne sont pas restreints.

## <a name="instruction-information"></a>Informations sur les instructions



| Condition requise                         | Value           |
|--------------------------|------------|
| Système d’exploitation minimal | Windows 98 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




