---
description: La méthode SWbemRefresher. Item retourne le SWbemRefreshableItem spécifié à partir de la collection. SWbemRefreshableItem à partir de la collection.
ms.assetid: 8ae3dea5-0582-422e-9cd8-b6d91b41588a
ms.tgt_platform: multiple
title: SWbemRefresher. Item, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Item
- ISWbemRefresher.Item
- ISWbemRefresher.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1290a395b9fc3f4e485a90822103ccb51b40edcc1b72fdf08433eaed72cdd213
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897569"
---
# <a name="swbemrefresheritem-method"></a>SWbemRefresher. Item, méthode

La méthode **SWbemRefresher. Item** retourne le [**SWbemRefreshableItem**](swbemrefreshableitem.md) spécifié à partir de la collection.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
objItem = .Item( _
  ByVal lIndex _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lIndex* 
</dt> <dd>

Valeur d’index de l’élément dans la collection.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si l’appel réussit, l’objet [**SWbemRefreshableItem**](swbemrefreshableitem.md) spécifié est retourné.

## <a name="error-codes"></a>Codes d’erreur

Si l’actualisateur n’a pas d’élément avec l’index spécifié, **wbemErrNotFound** est généré.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemRefresher<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemRefresher<br/>                                                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SWbemRefresher**](swbemrefresher.md)
</dt> </dl>

 

 




