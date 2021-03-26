---
title: Masque d’écriture du registre de destination
description: Un masque d’écriture contrôle les composants d’un registre de destination qui sont écrits après l’achèvement d’une instruction.
ms.assetid: 376a28c8-8a88-4807-a8ab-f59448d965e8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 80f649770b84174dbb716967e9d941034c3966f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940333"
---
# <a name="destination-register-write-mask"></a>Masque d’écriture du registre de destination

Un masque d’écriture contrôle les composants d’un registre de destination qui sont écrits après l’achèvement d’une instruction. Un masque d’écriture de sortie est autorisé tant que les composants sont dans l’ordre de. RVBA ou. XYZW. Autrement dit,. RBA et. XW sont des masques valides. Les registres de texture ont un ensemble de règles et les registres de non-texture ont un autre ensemble de règles.

## <a name="syntax"></a>Syntaxe



| DST. writemask |
|---------------|



 

where

-   l’heure d’été est un registre de destination.
-   writemask est une séquence de masques de l’un ou l’autre des jeux : (x, y, z, w) ou (rouge, vert, bleu, alpha).

## <a name="remarks"></a>Notes

Les masques d’écriture de destination suivants sont disponibles.



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| . XYZW (par défaut)       | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| . xyz                  | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| . w                    | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| masque arbitraire        |      |      |      | x    | x    | x    | x     | x    | x     |



 

Le masque arbitraire permet de combiner tout ensemble de canaux pour produire un masque. Les canaux doivent être listés dans l’ordre r, g, b, a, par exemple, Register. RBA, qui met à jour les canaux rouge, bleu et alpha de la destination. Le masque arbitraire est disponible dans la version 1 \_ 4 ou une version ultérieure.

Si aucun masque d’écriture de destination n’est spécifié, le masque d’écriture de destination est défini par défaut sur le cas RVBA. En d’autres termes, tous les canaux du registre de destination sont mis à jour.

Pour les versions 1 \_ 0 à 1 \_ 3, l’instruction arithmétique [DP3-PS](dp3---ps.md) DP3 peut utiliser uniquement les masques d’écriture de sortie. RGB ou. RVBA.

Les masques d’écriture de registre de destination sont pris en charge uniquement pour les opérations arithmétiques. Ils ne peuvent pas être utilisés sur les instructions d’adressage de texture, à l’exception des instructions de la version 1 \_ 4, [texcrd-PS](texcrd---ps.md) et [texld-PS \_ 2 \_ 0 et up](texld---ps-2-0.md).

La valeur par défaut consiste à écrire les quatre canaux de couleurs.


```
// All four color channels can be written by explicitly listing them.
mul r0.rgba, t0, v0

// Or, the default mask can be used to write all four channels.
mul r0, t0, v0
```



Le masque d’écriture alpha est également appelé masque d’écriture scalaire, car il utilise le pipeline scalaire.


```
add r0.a, t1, v1
```



Par conséquent, cette instruction place efficacement la somme du composant alpha de T1 et le composant alpha de V1 dans R0. a.

Le masque d’écriture de couleur est utilisé pour contrôler l’écriture des canaux de couleurs.


```
// The color write mask is also referred to as the vector write mask, 
//   because it uses the vector pipeline.
mul r0.rgb, t0, v0
```



Pour la version 1 \_ 4, les masques d’écriture de destination peuvent être utilisés dans n’importe quelle combinaison, à condition que les masques soient triés r, g, b, a.


```
// This example updates the red, blue, and alpha channels.
mov r0.rba, r1
```



Une instruction co-émises permet d’émettre simultanément deux instructions potentiellement différentes. Pour ce faire, vous devez exécuter les instructions dans le pipeline alpha et le pipeline RGB.


```
  mul r0.rgb, t0, v0
+ add r1.a,   t1, c1
```



L’avantage des instructions de couplage de cette façon est qu’il permet d’effectuer différentes opérations dans le pipeline Vector et le pipeline scalaire en parallèle.

Ces registres de sortie du nuanceur de sommets sont limités aux masques d’écriture suivants :



| Type de Registre | Masque d’écriture requis                                              |
|---------------|------------------------------------------------------------------|
| oFog          | aucun masque d’écriture explicite n’est autorisé sur ce registre scalaire        |
| Décide          | aucun masque d’écriture explicite n’est autorisé sur ce registre scalaire        |
| oPos          | . XYZW (qui est la valeur par défaut)                                      |
| oT\#          | Mask combiné :. x \| . XY. \| xyz \| . XYZW (qui est la valeur par défaut) |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modificateurs de registre de nuanceur de pixels](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




