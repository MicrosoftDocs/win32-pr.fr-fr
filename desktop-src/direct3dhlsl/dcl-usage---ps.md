---
title: dcl_semantics (SM3-PS ASM)
description: Déclarez l’association entre la sortie du nuanceur de sommets et l’entrée de nuanceur de pixels.
ms.assetid: 4f4dc6fe-0efa-4d84-aefd-583e90ab9a61
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 944ddd2b581c6179ac4a3fe22f2b687f85aecfdc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101957"
---
# <a name="dcl_semantics-sm3---ps-asm"></a>\_sémantique DCL (SM3-PS ASM)

Déclarez l’association entre la sortie du nuanceur de sommets et l’entrée de nuanceur de pixels.

## <a name="syntax"></a>Syntaxe



|                                                   |
|---------------------------------------------------|
| sémantique DCL Centre d' \_ \[ \_ \] heure d’été \[ \_\] |



 

Où :

-   \_Semantics : identifie l’utilisation des données prévue et peut être l’une des valeurs de [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (sans le \_ préfixe D3DDECLUSAGE). En outre, un index d’entiers peut être ajouté à la sémantique pour distinguer les paramètres qui utilisent une sémantique similaire.
-   \[\_Centre de [gravité](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md) \] est un modificateur d’instruction facultatif. Il est pris en charge sur \_ les instructions d’utilisation de la liste DCL qui déclarent les registres d’entrée et sur les instructions de recherche de texture. Le centre de gravité est ajouté sans espace.
-   DST : Registre de destination. Consultez [ \_ registres PS 3 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-3-0.md).
-   \_masque d’écriture : le même registre de sortie peut être déclaré plusieurs fois, à chaque fois avec un masque d’écriture unique (une sémantique différente peut donc être appliquée à des composants individuels). Toutefois, la même sémantique ne peut pas être utilisée plusieurs fois dans une déclaration. Cela signifie que les vecteurs doivent avoir quatre composants ou moins, et ne peuvent pas traverser les limites d’un registre à quatre composants (registres de sortie individuels). Lorsque la \_ sémantique psize est utilisée, elle doit avoir un masque d’écriture complet, car elle est considérée comme une scalaire. Lorsque la \_ sémantique de position est utilisée, elle doit avoir un masque d’écriture complet, car les quatre composants doivent être écrits.

## <a name="remarks"></a>Notes



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| utilisation de DCL \_            |      |      |      |      |      |      |       | x    | x     |



 

Toutes les \_ instructions d’utilisation de la DCL doivent apparaître avant la première instruction exécutable.

## <a name="declaration-examples"></a>Exemples de déclaration


```
ps_3_0

; Declaring inputs
dcl_normal      v0.xyz
dcl_blendweight v0.w ; Must be same reg# as normal, matching vshader packing
dcl_texcoord1   v1.y ; Mask can be any subset of mask from vshader semantic
dcl_texcoord0   v1.zw; Has to be same reg# as texcoord1, to match vshader

; Declaring samplers
dcl_2d s0
dcl_2d s1

def c0, 0, 0, 0, 0

mov r0.x, v1.y ; texcoord1
mov r0.y, c0
texld r0, r0, s0

texld r1, v1.zw, s1
...
(output regs in ps_3_0 are same as ps_2_0: oC0-oC3, oDepth)
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[Exemple d’anticrénelage](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)
</dt> </dl>

 

 