---
title: Méthode WSMan. SessionFlagCredUsernamePassword (WSManDisp. h)
description: Retourne la valeur de l’indicateur d’authentification WSManFlagCredUsernamePassword à utiliser dans le paramètre flags de la méthode WSMan. CreateSession.
ms.assetid: 70d12df4-f0ac-499a-8b2f-6ba83b77869e
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode SessionFlagCredUsernamePassword
- Méthode SessionFlagCredUsernamePassword Windows Remote Management, objet WSMan
- Objet WSMan Windows Remote Management, méthode SessionFlagCredUsernamePassword
topic_type:
- apiref
api_name:
- WSMan.SessionFlagCredUsernamePassword
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84827f342f70b13f1a2f0192289b34e347f26045
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033029"
---
# <a name="wsmansessionflagcredusernamepassword-method"></a>Méthode WSMan. SessionFlagCredUsernamePassword

La méthode **WSMan. SessionFlagCredUsernamePassword** retourne la valeur de l’indicateur d’authentification **WSManFlagCredUsernamePassword** à utiliser dans le paramètre *Flags* de la méthode [**WSMan. CreateSession**](wsman-createsession.md) . Cette méthode fournit une syntaxe plus efficace pour l’utilisation de la constante afin que les scripts ne soient pas requis pour définir une valeur de constante. Pour plus d’informations sur l’appel de cette méthode, consultez [sessions, constantes](session-constants.md).

**WSManFlagCredUsernamePassword** est une constante dans l’énumération **\_ \_ WSManSessionFlags** . Pour plus d’informations, consultez [constantes d’authentification](authentication-constants.md).

## <a name="syntax"></a>Syntaxe


```VB
WSMan.SessionFlagCredUsernamePassword( _
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

 

 





