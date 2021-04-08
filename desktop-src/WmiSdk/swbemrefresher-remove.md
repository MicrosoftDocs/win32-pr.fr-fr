---
description: La méthode SWbemRefresher. Remove supprime l’objet SWbemRefreshableItem avec l’index spécifié de l’actualisateur.
ms.assetid: db5ac740-e2b3-4667-b511-d750cb092e0f
ms.tgt_platform: multiple
title: SWbemRefresher. Remove, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Remove
- ISWbemRefresher.Remove
- ISWbemRefresher.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9504b81ce83a91695765e75e74de374437c188d4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103953428"
---
# <a name="swbemrefresherremove-method"></a>SWbemRefresher. Remove, méthode

La méthode **SWbemRefresher. Remove** supprime l’objet [**SWbemRefreshableItem**](swbemrefreshableitem.md) avec l’index spécifié de l’actualisateur. L’objet **SWbemRefreshableItem** peut représenter soit un objet unique, soit un jeu d’objets.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
objRefresher = .Remove( _
  ByVal LIndex, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedvalueSet ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*LIndex* 
</dt> <dd>

Index de l’élément dans l’objet [**SWbemRefresher**](swbemrefresher.md) .

</dd> <dt>

*IFlags* \[ facultatif\]
</dt> <dd>

Les indicateurs doivent être définis à T0 (zéro).

</dd> <dt>

*objWbemNamedvalueSet* \[ facultatif\]
</dt> <dd>

Null.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode n’a pas de valeur de retour.

## <a name="remarks"></a>Notes

**Codes d’erreur** Si l’actualisateur n’a pas d’élément avec l’index spécifié, **wbemErrNotFound** est généré.

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

 

 




