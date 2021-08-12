---
title: texdepth-PS
description: Calculez les valeurs de profondeur à utiliser dans le test de comparaison de mémoire tampon de profondeur pour ce pixel.
ms.assetid: f7128dbb-a5f3-4e95-b53b-7432439ae0c4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f39135c34c07a9a20f03c9ebc979647733884b37680ef07b9bc666b882052690
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118284173"
---
# <a name="texdepth---ps"></a>texdepth-PS

Calculez les valeurs de profondeur à utiliser dans le test de comparaison de mémoire tampon de profondeur pour ce pixel.

## <a name="syntax"></a>Syntaxe



| texdepth DST |
|--------------|



 

where

-   l’heure d’été est le registre de destination.

## <a name="remarks"></a>Notes



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texdepth              |      |      |      | x    |      |      |       |      |       |



 

Cette instruction utilise R5. r/R5. g dans le test de comparaison de la mémoire tampon de profondeur pour ce pixel. Les données des canaux bleu et alpha sont ignorées. Si R5. g = 0, le résultat de R5. r/R5. g = 1,0.

Le registre temporaire R5 est le seul registre que cette instruction peut utiliser.

Après l’exécution de cette instruction, le registre temporaire R5 n’est pas disponible pour une utilisation supplémentaire dans le nuanceur.

Lors de l’échantillonnage multiple, l’utilisation de cette instruction élimine la plupart des avantages de la mémoire tampon de profondeur supérieure. Étant donné que le nuanceur de pixels s’exécute une fois par pixel, la valeur de profondeur unique générée par [texm3x2depth-PS](texm3x2depth---ps.md) ou texdepth sera utilisée pour chacun des tests de comparaison de profondeur de sous-pixel.

## <a name="examples"></a>Exemples

Voici un exemple d’utilisation de texdepth.


```
ps_1_4              
texld  r0, t0        // Sample texture from texture stage 0 (dest 
                     //   register number) into r0
                     // Use texture coordinate data from t0
texcrd r1.rgb, t1    // Load a second set of texture coordinate data into r1
add    r5.rg, r0, r1 // Add the two sets of texture coordinate data
phase                // Phase marker, required when using texdepth instruction
texdepth  r5         // Calculate pixel depth as r5.r / r5.g
                     // Do other color calculations with shader output r0
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




