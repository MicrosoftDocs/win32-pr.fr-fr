---
description: La méthode SWbemRefreshableItem. Remove supprime l’objet SWbemRefreshableItem de l’objet SWbemRefresher parent. Objet SWbemRefreshableItem de l’objet SWbemRefresher parent.
ms.assetid: 8d3f5e22-c343-4191-a20a-6bca2ec9b01a
ms.tgt_platform: multiple
title: SWbemRefreshableItem. Remove, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.Remove
- ISWbemRefreshableItem.Remove
- ISWbemRefreshableItem.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 028bff202108481ce498be02c6014141313f27cc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010380"
---
# <a name="swbemrefreshableitemremove-method"></a>SWbemRefreshableItem. Remove, méthode

La méthode **SWbemRefreshableItem. Remove** supprime l’objet [**SWbemRefreshableItem**](swbemrefreshableitem.md) de l’objet [**SWbemRefresher**](swbemrefresher.md) parent.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
SWbemRefreshableItem.Remove( _
  [ ByVal lFlags ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lFlags* \[ dans, facultatif\]
</dt> <dd>

Ce paramètre doit avoir la valeur 0 (zéro).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

**Codes d’erreur** Si l’actualisateur n’a pas d’élément avec l’index spécifié, **wbemErrNotFound** est généré.

## <a name="requirements"></a>Spécifications



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

[**SWbemRefresher**](swbemrefresher.md)
</dt> </dl>

 

 




