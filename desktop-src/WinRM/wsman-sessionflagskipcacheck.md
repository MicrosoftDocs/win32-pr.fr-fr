---
title: Méthode WSMan. SessionFlagSkipCACheck (WSManDisp. h)
description: Retourne la valeur de l’indicateur d’authentification WSManFlagSkipCACheck à utiliser dans le paramètre flags de WSMan. CreateSession.
ms.assetid: a67cadb3-c20a-4a58-a13b-5bbd23c547d1
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode SessionFlagSkipCACheck
- Méthode SessionFlagSkipCACheck Windows Remote Management, objet WSMan
- Objet WSMan Windows Remote Management, méthode SessionFlagSkipCACheck
topic_type:
- apiref
api_name:
- WSMan.SessionFlagSkipCACheck
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e536112b16ad8cbab3cebb2de582a2e0ea8aec0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032368"
---
# <a name="wsmansessionflagskipcacheck-method"></a>Méthode WSMan. SessionFlagSkipCACheck

La méthode **WSMan. SessionFlagSkipCACheck** retourne la valeur de l’indicateur d’authentification **WSManFlagSkipCACheck** pour une utilisation dans le paramètre *Flags* de [**WSMan. CreateSession**](wsman-createsession.md). Cette méthode fournit une syntaxe plus efficace pour l’utilisation de la constante afin que les scripts ne soient pas requis pour définir une valeur de constante. Pour plus d’informations sur l’appel de cette méthode et des exemples de code, consultez [sessions, constantes](session-constants.md).

**WSManFlagSkipCACheck** est une constante dans l’énumération **\_ \_ WSManSessionFlags** . Pour plus d’informations, consultez [**constantes d’authentification**](authentication-constants.md).

## <a name="syntax"></a>Syntaxe


```VB
WSMan.SessionFlagSkipCACheck( _
  ByRef flags _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*indicateurs* \[ à\]
</dt> <dd>

Valeur de la constante.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**WSMan**](wsman.md)
</dt> <dt>

[**session**](session.md)
</dt> </dl>

 

 





