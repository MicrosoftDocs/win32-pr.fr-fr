---
title: texm3x2depth-PS
description: Calculez la valeur de profondeur à utiliser pour le test de profondeur pour ce pixel.
ms.assetid: bacdd471-a6ee-4998-badd-93ffd4fd61d4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 17d3f04cd722664992911759ae1f5f6a4bd5947e0b46e37dc61b62b999ac8d47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892529"
---
# <a name="texm3x2depth---ps"></a>texm3x2depth-PS

Calculez la valeur de profondeur à utiliser pour le test de profondeur pour ce pixel.

## <a name="syntax"></a>Syntaxe



| texm3x2depth DST, SRC |
|-----------------------|



 

where

-   l’heure d’été est le registre de destination.
-   SRC est un registre source.

## <a name="remarks"></a>Remarques



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x2depth          |      |      | x    |      |      |      |       |      |       |



 

Cette instruction doit être utilisée avec l’instruction [texm3x2pad-PS](texm3x2pad---ps.md) .

Lors de l’utilisation de ces deux instructions, les registres de texture doivent utiliser la séquence suivante.


```
 
tex t(n)                     // Define tn as a standard 3-vector.(tn must be 
                             // defined in some way before it is used
texm3x2pad   t(m),   t(n)    // Where m > n
                             // Calculate z value
texm3x2depth t(m+1), t(n)    // Calculate w value; use both z and w to
                             // find depth
```



Le calcul de la profondeur s’effectue après l’utilisation d’une opération de point pour rechercher z et w. Voici plus de détails sur la façon dont le calcul de la profondeur est réalisé.

L’instruction texm3x2pad calcule z.

z = TextureCoordinates (étape m)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

L’instruction texm3x2depth calcule w.

w = TextureCoordinates (étape m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

Calculez la profondeur et stockez le résultat dans t (m + 1).


```
 
if (w == 0)
  t(m+1) = 1.0
else
  t(m+1) = z/w
```



La profondeur calculée est marquée pour être utilisée dans le test de profondeur pour le pixel, remplaçant la valeur de test de profondeur existante pour le pixel.

Veillez à fixer le z/w à la plage de (0-1). Si z/w est en dehors de cette plage, le résultat stocké dans la mémoire tampon de profondeur n’est pas défini.

Après l’exécution de texm3x2depth, l’inscription t (m + 1) n’est plus disponible pour une utilisation dans le nuanceur.

Lors de l’échantillonnage multiple, l’utilisation de cette instruction élimine la plupart des avantages de la mémoire tampon de profondeur supérieure. Étant donné que le nuanceur de pixels s’exécute une fois par pixel, la valeur de profondeur unique générée par texm3x2depth ou [texdepth-PS](texdepth---ps.md) sera utilisée pour chacun des tests de comparaison de profondeur de sous-pixel.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




