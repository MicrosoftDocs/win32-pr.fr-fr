---
title: Décalage du Registre source
description: Soustraire 0,5 de tous les composants.
ms.assetid: 6e1e96b0-e265-4b43-a9cb-8435e1fe891c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5c564dad0d4caf859ae00155dfd9619d90276cf1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940335"
---
# <a name="source-register-bias"></a>Décalage du Registre source

Soustraire 0,5 de tous les composants.

## <a name="registers"></a>Registres

Registre source. Pour plus d’informations sur les types de registres, consultez les [registres PS 1 \_ \_ 1 \_ \_ PS 1 \_ \_ 2 \_ \_ \_ \_ \_ \_ \_ \_ ](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)PS 1 3 PS 1 4.

## <a name="remarks"></a>Notes

Le contenu du Registre n’est pas modifié. Le modificateur est appliqué uniquement aux données lues à partir du Registre. Le biais est appliqué aux quatre canaux de couleurs (RVBA) comme suit :


```
output = (input - 0.5)
```



L’effet est de modifier les données comprises dans la plage de 0 à 1 pour qu’elles se trouvent dans la plage comprise entre-0,5 et 0,5. L’application d’un décalage aux données en dehors de cette plage peut produire des résultats indéfinis.

> [!Note]  
> Ce modificateur s’exclut mutuellement avec le [Registre source inversé](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md), donc il ne peut pas être appliqué au même registre.

 

Ce modificateur est destiné à être utilisé avec les instructions arithmétiques.

## <a name="example"></a>Exemple

Cet exemple effectue la même opération que D3DTOP \_ ADDSIGNED dans DirectX 6,0 et 7,0 syntaxe de texture multiple.


```
add r0, r0, t0_bias; Shift down by 0.5.
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modificateurs de Registre source du nuanceur de pixels](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




