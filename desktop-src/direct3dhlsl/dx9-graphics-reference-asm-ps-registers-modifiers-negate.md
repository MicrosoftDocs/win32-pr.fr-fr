---
title: Négation du Registre source
description: Effectue une négation (y-x) sur tous les composants du Registre.
ms.assetid: fe11f7a7-81be-4237-8194-15704f6fe43c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2f6082523926d70e670e0b792c6e7e8f41c7c1a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029100"
---
# <a name="source-register-negate"></a>Négation du Registre source

Effectue une négation (y =-x) sur tous les composants du Registre.

## <a name="syntax"></a>Syntaxe


```
- register
```



## <a name="registers"></a>Registres

Registre source. Pour plus d’informations sur les types de registres, consultez les [registres PS 1 \_ \_ 1 \_ \_ PS 1 \_ \_ 2 \_ \_ \_ \_ \_ \_ \_ \_ ](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)PS 1 3 PS 1 4.

## <a name="remarks"></a>Notes

Le contenu du Registre n’est pas modifié. Le modificateur est appliqué uniquement aux données lues à partir du Registre. L’opération de négation est appliquée aux quatre canaux de couleurs (RVBA).

Cette opération est effectuée après tout autre modificateur présent sur le même argument.

Ce modificateur s’exclut mutuellement avec le [Registre source inversé](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) , de sorte qu’il ne peut pas être appliqué au même registre.

Ce modificateur est destiné à être utilisé uniquement avec des instructions arithmétiques.

## <a name="example"></a>Exemple

L’exemple suivant montre comment utiliser ce modificateur.


```
mul r0, r0, -v1;
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modificateurs de Registre source du nuanceur de pixels](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




