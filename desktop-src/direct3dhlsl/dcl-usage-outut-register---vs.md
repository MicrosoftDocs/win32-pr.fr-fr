---
title: sortie dcl_usage (SM1, SM2, SM3-vs ASM)
description: Les différents types de registres de sortie ont été réduits en douze registres de sortie (deux pour la couleur, huit pour la texture, un pour la position et un pour le brouillard et la taille du point).
ms.assetid: 500ca6b3-0f8a-446e-b1b9-edc51f006ad4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 314c9c9a9a9e62915e9224b3cf165bc54d09a516
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999166"
---
# <a name="dcl_usage-output-sm1-sm2-sm3---vs-asm"></a>sortie d’utilisation de DCL \_ (SM1, SM2, SM3-vs ASM)

Les différents types de registres de sortie ont été réduits en douze registres de sortie (deux pour la couleur, huit pour la texture, un pour la position et un pour le brouillard et la taille du point). Elles peuvent être utilisées pour tout ce que l’utilisateur souhaite interpoler pour le nuanceur de pixels : les coordonnées de la texture, les couleurs, le brouillard, etc.

Les registres de sortie requièrent des déclarations qui incluent une sémantique. Par exemple, les anciens registres de position et de taille de point sont remplacés par la déclaration d’un registre de sortie avec une sémantique de position ou de taille de point.

Parmi les douze registres de sortie, les dix (pas nécessairement o0 à O9) comportent quatre composants (XYZW), un autre doit être déclaré comme position (et doit également inclure les quatre composants) et, éventuellement, une taille de point scalaire.

## <a name="syntax"></a>Syntax

La syntaxe de déclaration des registres de sortie est similaire aux déclarations du registre d’entrée :



|                                  |
|----------------------------------|
| sémantique de DCL \_ o \[ . masque d’écriture \_\] |



 

Où :

-   la \_ sémantique DCL peut utiliser le même ensemble de sémantique que pour la déclaration d’entrée. Les noms sémantiques proviennent de [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (et sont associés à un index, tel que position3). Il doit toujours y avoir un registre de sortie avec la sémantique positiont0 lorsqu’il n’est pas utilisé pour le traitement des vertex. La sémantique positiont0 et la sémantique pointsize0 sont les seules qui ont un sens au-delà de la simple autorisation de la liaison entre vertex et nuanceurs de pixels. Pour les nuanceurs avec contrôle de Flow, on suppose que la sortie de cas le plus défavorable est déclarée. Il n’y a pas de valeurs par défaut si un nuanceur ne génère pas réellement ce qu’il déclare (en raison du contrôle de Flow).
-   o est un registre de sortie. Consultez [ \_ registres de sortie](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).
-   \_le masque d’écriture indique le même registre de sortie qui peut être déclaré plusieurs fois (par conséquent, une sémantique différente peut être appliquée à des composants individuels), à chaque fois avec un masque d’écriture unique. Toutefois, la même sémantique ne peut pas être utilisée plusieurs fois dans une déclaration. Cela signifie que les vecteurs doivent avoir quatre composants ou moins, et ne peuvent pas traverser les limites d’un registre à quatre composants (registres individuels). Lorsque la sémantique de taille de point est utilisée, elle doit avoir un masque d’écriture complet, car elle est considérée comme une valeur scalaire. Lorsque la sémantique de position est utilisée, elle doit avoir un masque d’écriture complet, car les quatre composants doivent être écrits.

## <a name="remarks"></a>Remarques



| Versions de nuanceur vertex | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|-------|
| utilisation de DCL \_             | x    | x     |



 

Toutes les instructions d' [ \_ utilisation](dcl-usage-input-register---vs.md) de la DCL doivent apparaître avant la première instruction exécutable.

## <a name="declaration-examples"></a>Exemples de déclaration


```
vs_3_0
dcl_color4     o3.x    // color4 is a semantic name.
dcl_texcoord3  o3.yz   // Different semantics can be packed into one register.
dcl_fog        o3.w 
dcl_tangent    o4.xyz
dcl_position   o7.xyzw // position must be declared to some unique register 
                       //   in a vertex shader, with all 4 components.

dcl_psize      o6      // Pointsize cannot have a mask 
                       //   (that is, mask is full .xyzw)
                       // This is an implied scalar register. 
                       // No other semantics can be assigned to any components
                       //   of this register.
                       // If pointsize declaration is not used (typical),
                       //   only 11 "out" registers are available, not 12.
                       // Pixel shaders cannot see this value.

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
