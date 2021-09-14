---
title: DP3-PS
description: Calcule le produit scalaire à trois composants des registres sources. | DP3-PS
ms.assetid: a365acd1-89c0-4340-8f51-8e478f84ddc0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 09e4178f6aedbfb5242f4c545d624f1d07796008
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127232488"
---
# <a name="dp3---ps"></a>DP3-PS

Calcule le produit scalaire à trois composants des registres sources.

## <a name="syntax"></a>Syntaxe



| DP3 DST, src0, src1 |
|---------------------|



 

where

-   l’heure d’été est le registre de destination.
-   src0 est un registre source.
-   src1 est un registre source.

## <a name="remarks"></a>Notes



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dp3                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

L’extrait de code suivant montre les opérations effectuées :


```
dest.x = dest.y = dest.z = dest.w = 
  (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
```



Cette instruction s’exécute dans le pipeline vectoriel, en écrivant toujours sur les canaux de couleurs. Pour la version 1 \_ 4, cette instruction utilise toujours le pipeline vectoriel, mais peut écrire dans n’importe quel canal.

Une instruction avec un masque d’écriture de destination. RGB (. xyz) peut être co-émise avec DP3, comme indiqué ci-dessous.


```
dp3 r0.rgb, t0, v0            // Copy scalar result to color components
+mov r2.a, t0                 // Copy alpha component from t0 in parallel 
```



L’instruction dp3 peut être modifiée à l’aide du modificateur d’argument d’entrée de [mise à l’échelle signée du Registre source](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) ( \_ BX2) appliqué à ses arguments d’entrée s’ils ne sont pas déjà développés dans une plage dynamique signée. Dans le cas d’un nuanceur d’éclairage, le modificateur d’instruction saturé ( \_ SAT) est souvent utilisé pour fixer les valeurs négatives au noir, comme illustré dans l’exemple suivant.


```
dp3_sat r0, t0_bx2, v0_bx2    // t0 is a bump map, v0 contains the light direction
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




