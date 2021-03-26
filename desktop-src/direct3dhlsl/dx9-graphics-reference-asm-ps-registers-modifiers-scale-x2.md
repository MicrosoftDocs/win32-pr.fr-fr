---
title: Mise à l’échelle du Registre source x 2
description: Multipliez la valeur par deux avant de l’utiliser dans l’instruction.
ms.assetid: a02c9572-e03d-410b-8b65-7ea1a0bfaa0f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7e88127e4027767d23a2ab576e94802019068dc3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104971454"
---
# <a name="source-register-scale-x-2"></a>Mise à l’échelle du Registre source x 2

Multipliez la valeur par deux avant de l’utiliser dans l’instruction.

## <a name="syntax"></a>Syntaxe


```
register_x2
```



## <a name="register"></a>S’inscrire

Registre source. Pour plus d’informations sur les types de registres, consultez les [registres PS 1 \_ \_ 1 \_ \_ PS 1 \_ \_ 2 \_ \_ \_ \_ \_ \_ \_ \_ ](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)PS 1 3 PS 1 4.

## <a name="remarks"></a>Notes

Le contenu du Registre n’est pas modifié. Le modificateur est appliqué uniquement aux données lues à partir du Registre.

Ce modificateur s’exclut mutuellement avec le [Registre source inversé](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md), donc il ne peut pas être appliqué au même registre.

Ce modificateur est uniquement disponible pour les instructions arithmétiques dans la version 1 \_ 4.

## <a name="example"></a>Exemple

Cet exemple échantillonne une texture, convertit les données dans la plage comprise entre-1 et + 1, puis calcule un produit scalaire.


```
mul r0, r0, r1_x2;
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modificateurs de Registre source du nuanceur de pixels](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




