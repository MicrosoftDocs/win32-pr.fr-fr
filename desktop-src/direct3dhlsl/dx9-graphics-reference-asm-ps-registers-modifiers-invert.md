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
ms.openlocfilehash: a391219f085c18a4c8bf2925a248800b6a26838cc6e2b8556551eb98b5335241
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562769"
---
# <a name="source-register-invert"></a>Registre source inversé

Effectue un calcul (1 valeur) pour chaque canal du Registre spécifié.

## <a name="syntax"></a>Syntaxe


```
1 - register
```



## <a name="registers"></a>Registres

Registre source. Pour plus d’informations sur les types de registres, consultez les [registres PS 1 \_ \_ 1 \_ \_ PS 1 \_ \_ 2 \_ \_ \_ \_ \_ \_ \_ \_ ](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)PS 1 3 PS 1 4.

## <a name="remarks"></a>Remarques

Le contenu du Registre n’est pas modifié. Le modificateur est appliqué uniquement aux données lues à partir du Registre. L’opération inversée est appliquée aux quatre canaux de couleurs (RVBA).

Ce modificateur ne peut être utilisé qu’avec des instructions arithmétiques. En outre, ce modificateur ne peut pas être combiné avec l’autre [masque d’écriture de registre de destination](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).

## <a name="example"></a>Exemples

Cet exemple utilise inversion pour générer le complément du Registre R1.


```
mul r0, r0, 1-r1;
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modificateurs de Registre source du nuanceur de pixels](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




