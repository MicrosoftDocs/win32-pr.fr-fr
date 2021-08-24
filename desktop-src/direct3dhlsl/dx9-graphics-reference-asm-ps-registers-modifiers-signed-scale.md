---
title: Mise à l’échelle signée du Registre source
description: Soustrait 0,5 de chaque canal et met à l’échelle le résultat de 2,0. Le nom BX2 provient de Bias et Scale-Times-2, qui est l’opération qu’il effectue.
ms.assetid: ad94145a-2687-4c20-b3ed-70270a0c53bf
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 161cacbf9f10a36e65f37816970aea5d5d804096151a4ae1ce3f814be918ae08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854599"
---
# <a name="source-register-signed-scaling"></a>Mise à l’échelle signée du Registre source

Soustrait 0,5 de chaque canal et met à l’échelle le résultat de 2,0. Le nom BX2 provient de Bias et Scale-Times-2, qui est l’opération qu’il effectue.

## <a name="syntax"></a>Syntaxe


```
source register_bx2
```



## <a name="register"></a>S’inscrire

Registre source. Pour plus d’informations sur les types de registres, consultez les [registres PS 1 \_ \_ 1 \_ \_ PS 1 \_ \_ 2 \_ \_ \_ \_ \_ \_ \_ \_ ](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)PS 1 3 PS 1 4.

## <a name="remarks"></a>Remarques

Cette opération est couramment utilisée pour étendre \[ 1,0 les données de 0,0 à 1,0 à \] \[ 1,0 \] . Ce modificateur est conçu pour être utilisé avec les instructions arithmétiques. Ce modificateur est couramment utilisé sur les entrées de l’instruction du produit scalaire ([DP3-PS](dp3---ps.md)). L’utilisation \_ de BX2 sur des données situées en dehors de la plage de 0 à 1 peut produire des résultats indéfinis.

L’opération de mise à l’échelle signée est appliquée aux données lues à partir du Registre avant l’exécution de l’instruction suivante. L’opération est appliquée aux quatre canaux de couleurs (RVBA) comme suit :


```
y = 2(x - 0.5)
```



Le contenu du Registre n’est pas modifié. Le modificateur est appliqué uniquement aux données lues à partir du Registre.

Ce modificateur s’exclut mutuellement avec le [Registre source inversé](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) , de sorte qu’il ne peut pas être appliqué au même registre.

Informations sur la version :

-   Pour PS \_ 1 \_ 0 et PS \_ 1 \_ 1, vous pouvez utiliser \_ BX2 sur n’importe quel Registre source pour les instructions de texture de la forme texm3x2 \* et texm3x3 \* . \_BX2 ne peut pas être utilisé sur une autre instruction de texture telle que [texreg2ar-PS](texreg2ar---ps.md) ou [texreg2gb-PS](texreg2gb---ps.md).
-   Pour PS \_ 1 \_ 2 et PS \_ 1 \_ 3, vous pouvez utiliser \_ BX2 sur n’importe quel Registre source pour toute instruction Tex, \* à l’exception de : [texreg2ar-PS](texreg2ar---ps.md), [texreg2gb-PS](texreg2gb---ps.md), [texbem-PS](texbem---ps.md) ou [texbeml-PS](texbeml---ps.md).

## <a name="example"></a>Exemple

Cet exemple échantillonne une texture, convertit les données dans la plage comprise entre-1 et + 1, puis calcule un produit scalaire.


```
tex t0                        ; Read a texture color.
dp3_sat r0, t0_bx2, v0_bx2    ; Calculate a dot product.
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modificateurs de Registre source du nuanceur de pixels](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




