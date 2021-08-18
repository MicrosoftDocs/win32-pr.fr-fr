---
title: ErrorItem. condition
description: La propriété condition récupère une valeur indiquant la condition de l’erreur.
ms.assetid: efb54b48-cfaa-479f-9ee6-ce6724dca24c
keywords:
- ErrorItem. condition Lecteur Windows Media
topic_type:
- apiref
api_name:
- ErrorItem.condition
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5f4bfe2c4b2b517b0fd300a0c6465ae9f10147518937822212b621d808f0ded
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996639"
---
# <a name="erroritemcondition"></a>ErrorItem. condition

La propriété **condition** récupère une valeur indiquant la condition de l’erreur.

``` syntax
player.error.item(
        index
        ).condition
      
```

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture seule (**long**) qui représente le code de condition.

## <a name="remarks"></a>Remarques

Le code de condition est une valeur utilisée par Microsoft pour fournir des informations supplémentaires au personnel du support technique.

**Lecteur Windows Media 10 Mobile :** Cette propriété retourne toujours 0.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet ErrorItem**](erroritem-object.md)
</dt> </dl>

 

 





