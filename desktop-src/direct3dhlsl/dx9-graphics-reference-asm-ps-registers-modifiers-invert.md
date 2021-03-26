---
title: Registre source inversé
description: Effectue un calcul (1 valeur) pour chaque canal du Registre spécifié.
ms.assetid: 387e409f-d76d-4d70-be0f-fb563f542482
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce65960474816a91eb64ece7b754b97090903d46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104971455"
---
# <a name="source-register-invert"></a>Registre source inversé

Effectue un calcul (1 valeur) pour chaque canal du Registre spécifié.

## <a name="syntax"></a>Syntaxe


```
1 - register
```



## <a name="registers"></a>Registres

Registre source. Pour plus d’informations sur les types de registres, consultez les [registres PS 1 \_ \_ 1 \_ \_ PS 1 \_ \_ 2 \_ \_ \_ \_ \_ \_ \_ \_ ](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)PS 1 3 PS 1 4.

## <a name="remarks"></a>Notes

Le contenu du Registre n’est pas modifié. Le modificateur est appliqué uniquement aux données lues à partir du Registre. L’opération inversée est appliquée aux quatre canaux de couleurs (RVBA).

Ce modificateur ne peut être utilisé qu’avec des instructions arithmétiques. En outre, ce modificateur ne peut pas être combiné avec l’autre [masque d’écriture de registre de destination](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).

## <a name="example"></a>Exemple

Cet exemple utilise inversion pour générer le complément du Registre R1.


```
mul r0, r0, 1-r1;
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modificateurs de Registre source du nuanceur de pixels](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




