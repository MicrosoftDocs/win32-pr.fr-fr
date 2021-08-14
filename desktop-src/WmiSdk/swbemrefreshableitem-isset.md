---
description: La propriété SWbemRefreshableItem. IsSet est une valeur booléenne qui indique si l’objet SWbemRefreshableItem représente un objet unique ou un jeu d’objets. L’objet SWbemRefreshableItem représente un objet unique ou un jeu d’objets.
ms.assetid: 4be5d27c-9020-4150-84ce-f9efc55be947
ms.tgt_platform: multiple
title: SWbemRefreshableItem. IsSet, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.IsSet
- ISWbemRefreshableItem.IsSet
- ISWbemRefreshableItem.get_IsSet
- ISWbemRefreshableItem.put_IsSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 055c776c1beffe1550033d61b54256d7b2e983ca70ac13f1b9fc899920910d4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312918"
---
# <a name="swbemrefreshableitemisset-property"></a>SWbemRefreshableItem. IsSet, propriété

La propriété **SWbemRefreshableItem. isset** est une valeur booléenne qui indique si l’objet [**SWbemRefreshableItem**](swbemrefreshableitem.md) représente un objet unique ou un jeu d’objets.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
SWbemRefreshableItem.IsSet As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Remarques

Si **SWbemRefreshableItem. isset** a la **valeur true**, l’élément représente un objet [**SWbemObjectSet**](swbemobjectset.md) et la propriété de l' [**objet**](swbemrefreshableitem-object.md) est **null**. Si la **valeur est false**, l’élément représente un objet [**SWbemObject**](swbemobject.md) et la propriété de l' **objet** est **null**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemRefreshableItem<br/>                                                  |
| IID<br/>                      | IID \_ ISWbemRefreshableItem<br/>                                                   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SWbemRefreshableItem**](swbemrefreshableitem.md)
</dt> <dt>

[**SWbemRefreshableItem**](swbemrefresher.md)
</dt> </dl>

 

 




