---
title: ABS-PS
description: Calcule la valeur absolue. | ABS-PS
ms.assetid: e97db550-2a03-421a-86f4-a6fc5f8e0bca
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e3e7af7b2d30e9d9f2092cb6671610f008ec781d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994876"
---
# <a name="abs---ps"></a>ABS-PS

Calcule la valeur absolue.

## <a name="syntax"></a>Syntax



|              |
|--------------|
| ABS DST, SRC |



 

where

-   l’heure d’été est le registre de destination.
-   SRC est un registre source.

## <a name="remarks"></a>Remarques



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| abs                   |      |      |      |      | x    | x    | x     | x    | x     |



 

Cette instruction fonctionne comme indiqué ici.


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="instruction-information"></a>Informations sur les instructions



|                          |            |
|--------------------------|------------|
| Système d’exploitation minimal | Windows 98 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




