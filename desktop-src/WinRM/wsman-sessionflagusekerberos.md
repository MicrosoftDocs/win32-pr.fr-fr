---
title: Méthode WSMan. SessionFlagUseKerberos (WSManDisp. h)
description: Retourne la valeur de l’indicateur d’authentification WSManFlagUseKerberos à utiliser dans le paramètre flags de WSMan. CreateSession.
ms.assetid: be005312-1e87-4371-9791-709a9be46f7c
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode SessionFlagUseKerberos
- méthode SessionFlagUseKerberos Windows Remote Management, objet WSMan
- objet WSMan Windows Remote Management, méthode SessionFlagUseKerberos
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseKerberos
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 468d6096343e3c0fe67369abe3927870f2e1eaf89a2d12b9c73e3560d436859e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997201"
---
# <a name="wsmansessionflagusekerberos-method"></a>Méthode WSMan. SessionFlagUseKerberos

La méthode **WSMan. SessionFlagUseKerberos** retourne la valeur de l’indicateur d’authentification **WSManFlagUseKerberos** pour une utilisation dans le paramètre *Flags* de [**WSMan. CreateSession**](wsman-createsession.md). Cette méthode fournit une syntaxe plus efficace pour l’utilisation de la constante afin que les scripts ne soient pas requis pour définir une valeur de constante. Pour plus d’informations sur l’appel de cette méthode, consultez [sessions, constantes](session-constants.md).

**WSManFlagUseKerberos** est une constante dans l’énumération **\_ \_ WSManSessionFlags** . Pour plus d’informations, consultez [constantes d’authentification](authentication-constants.md).

## <a name="syntax"></a>Syntaxe


```VB
WSMan.SessionFlagUseKerberos( _
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

 

 





