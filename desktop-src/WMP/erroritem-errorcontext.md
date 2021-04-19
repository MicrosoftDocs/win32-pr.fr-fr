---
title: ErrorItem.errorContext
description: La propriété errorContext récupère une valeur indiquant le contexte de l’erreur.
ms.assetid: 700d2bf0-dd3b-4211-99ea-58f952cf24b0
keywords:
- Lecteur Windows Media ErrorItem. errorContext
topic_type:
- apiref
api_name:
- ErrorItem.errorContext
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9b9ed91d34645f08e7d3d28860ced9ca51420dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532517"
---
# <a name="erroritemerrorcontext"></a>ErrorItem.errorContext

La propriété **errorContext** récupère une valeur indiquant le contexte de l’erreur.

``` syntax
player.error.item(
        index
        ).errorContext
```

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **chaîne** en lecture seule qui représente le code de contexte d’erreur.

## <a name="remarks"></a>Notes

Le contexte d’erreur est une information utilisée par Microsoft pour fournir des informations supplémentaires au personnel du support technique.

**Lecteur Windows Media 10 Mobile :** Cette propriété retourne toujours une chaîne vide.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/>                               |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet ErrorItem**](erroritem-object.md)
</dt> </dl>

 

 





