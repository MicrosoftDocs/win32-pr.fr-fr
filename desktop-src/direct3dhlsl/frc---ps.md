---
title: FRC-PS
description: Retourne la partie fractionnaire de chaque composant d’entrée. | FRC-PS
ms.assetid: 378bc516-c81e-4538-8d6f-987536b19467
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a16dd518333efa1dce878c1418547bc0527d1d64
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127526381"
---
# <a name="frc---ps"></a>FRC-PS

Retourne la partie fractionnaire de chaque composant d’entrée.

## <a name="syntax"></a>Syntax



| FRC DST, SRC |
|--------------|



 

where

-   l’heure d’été est le registre de destination.
-   SRC est un registre source.

## <a name="remarks"></a>Remarques



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| frc                   |      |      |      |      | x    | x    | x     | x    | x     |



 

L’extrait de code suivant montre le fonctionnement conceptuel de l’instruction.


```
dest.x = src.x - (float)floor(src.x);
dest.y = src.y - (float)floor(src.y);
dest.z = src.z - (float)floor(src.z);
dest.w = src.w - (float)floor(src.w);
```



La fonction Floor convertit l’argument passé dans le plus grand entier qui est inférieur ou égal à l’argument. Elle est convertie en valeur float, puis soustraite de la valeur d’origine. La valeur fractionnaire qui en résulte est comprise entre 0,0 et 1,0.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




