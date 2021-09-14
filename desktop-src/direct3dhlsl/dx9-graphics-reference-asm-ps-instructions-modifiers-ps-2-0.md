---
title: Modificateurs pour ps_2_0 et versions ultérieures
description: Les modificateurs d’instruction affectent le résultat de l’instruction avant qu’elle ne soit écrite dans le registre de destination. En savoir plus sur les modificateurs pour ps_2_0 et versions ultérieures.
ms.assetid: eb2a8a1f-51bc-4516-b679-a8fb25b0dda0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dc8ed91f8e103ebbab7c43ffe53201f0e1d5dfcf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127232386"
---
# <a name="modifiers-for-ps_2_0-and-above"></a>Modificateurs pour PS \_ 2 \_ 0 et versions ultérieures

Les modificateurs d’instruction affectent le résultat de l’instruction avant qu’elle ne soit écrite dans le registre de destination.

Cette section contient des informations de référence pour les modificateurs d’instruction implémentés par le nuanceur de pixels version 2 \_ 0 et versions ultérieures.



| Nom                                     | Syntaxe     | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------------------------|------------|------|------|-------|------|-------|
| [Centroïde](#centroid)                    | \_centroïde | x    | x    | x     | x    | x     |
| [\_Précision partielle](#partial-precision) | \_p       | x    | x    | x     | x    | x     |
| [Saturer](#saturate)                    | \_sot      | x    | x    | x     | x    | x     |



 

## <a name="centroid"></a>Centroïde

Le modificateur de centre de gravité est un modificateur facultatif qui fixe l’interpolation d’attribut dans la plage de la primitive quand un centre de pixels à plusieurs échantillons n’est pas couvert par la primitive. Cela peut être observé dans l’échantillonnage de centre de [gravité](https://msdn.microsoft.com/library/ee415231(VS.85).aspx).

Vous pouvez appliquer le modificateur de centre de gravité à une instruction d’assembly comme indiqué ici :


```
dcl_texcoord0_centroid v0
```



Vous pouvez également appliquer le modificateur de centre de gravité à une sémantique comme indiqué ici :


```
float4 TexturePointCentroidPS( float4 TexCoord : TEXCOORD0_centroid ) : COLOR0
{
    return tex2D( PointSampler, TexCoord );
}
```



De plus, tout [Registre de couleur d’entrée](dx9-graphics-reference-asm-ps-registers-input-color.md) (v \# ) déclaré avec une sémantique de couleur aura automatiquement le niveau de gravité appliqué. Il n’est pas garanti que les dégradés calculés à partir des attributs de centre de gravité de l’échantillonnage sont exacts.

## <a name="partial-precision"></a>Précision partielle

Le modificateur d’instruction de précision partielle ( \_ pp) indique les zones où la précision partielle est acceptable, à condition que l’implémentation sous-jacente la prenne en charge. Les implémentations sont toujours gratuites pour ignorer le modificateur et effectuer les opérations affectées en toute précision.

Le \_ modificateur pp peut se produire dans deux contextes :

-   Sur une déclaration de coordonnée de texture pour permettre le passage de coordonnées de texture au nuanceur de pixels en forme de précision partielle. Cela permet, par exemple, d’utiliser des coordonnées de texture pour transmettre des données de couleur au nuanceur de pixels, ce qui peut être plus rapide avec une précision partielle qu’avec une précision totale dans certaines implémentations. En l’absence de ce modificateur, les coordonnées de texture doivent être passées en pleine précision.
-   Sur toute instruction, y compris les instructions de chargement de texture. Cela indique que l’implémentation est autorisée à exécuter l’instruction avec une précision partielle et à stocker un résultat de précision partielle. En l’absence d’un modificateur explicite, l’instruction doit être exécutée à la précision totale (quelle que soit la précision d’entrée).

Exemples :


```
dcl_texcoord0_pp t1
cmp_pp r0, r1, r2, r3
```



## <a name="saturate"></a>Saturer :

Le modificateur d’instruction saturé ( \_ SAT) sature (ou bride) le résultat de l’instruction dans la plage \[ 0, 1 \] avant d’écrire dans le registre de destination.

Le \_ modificateur d’instruction SAT peut être utilisé avec n’importe quelle instruction, à l’exception [de FRC-PS](frc---ps.md), [SinCos,-PS](sincos---ps.md)et de toute instruction Tex \* .

Pour PS \_ 2 \_ 0, PS \_ 2 \_ x et PS \_ 2 \_ SW, le \_ modificateur d’instruction SAT ne peut pas être utilisé avec des instructions qui écrivent dans des registres de sortie (registre de[couleur de sortie](dx9-graphics-reference-asm-ps-registers-output-color.md) ou registre de [profondeur de sortie](dx9-graphics-reference-asm-ps-registers-output-depth.md)). Cette restriction ne s’applique pas à PS \_ 3 \_ 0 et versions ultérieures.

Exemple :


```
dp3_sat r0, v0, c1
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




