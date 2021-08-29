---
title: Méthode WSMan. SessionFlagEnableSPNServerPort (WSManDisp. h)
description: Retourne la valeur de l’indicateur d’authentification WSManFlagEnableSPNServerPort à utiliser dans le paramètre flags de la méthode WSMan. CreateSession.
ms.assetid: a18a87e6-dcee-4e9f-8e8c-262fef36ab1a
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode SessionFlagEnableSPNServerPort
- méthode SessionFlagEnableSPNServerPort Windows Remote Management, objet WSMan
- objet WSMan Windows Remote Management, méthode SessionFlagEnableSPNServerPort
topic_type:
- apiref
api_name:
- WSMan.SessionFlagEnableSPNServerPort
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5eb309f8fd9d6351ff34201ec409256bad5160ef2cd0224f5cdbf5263ae05214
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758929"
---
# <a name="wsmansessionflagenablespnserverport-method"></a>Méthode WSMan. SessionFlagEnableSPNServerPort

La méthode **WSMan. SessionFlagEnableSPNServerPort** retourne la valeur de l’indicateur d’authentification **WSManFlagEnableSPNServerPort** à utiliser dans le paramètre *Flags* de la méthode [**WSMan. CreateSession**](wsman-createsession.md) . Cette méthode fournit une syntaxe plus efficace pour l’utilisation de la constante afin que les scripts ne soient pas requis pour définir une valeur de constante. Pour plus d’informations sur l’appel de cette méthode, consultez [sessions, constantes](session-constants.md).

**WSManFlagEnableSPNServerPort** est une constante dans l’énumération **\_ \_ WSManSessionFlags** . Pour plus d’informations, consultez [**autres constantes de session**](other-session-constants.md).

## <a name="syntax"></a>Syntaxe


```VB
WSMan.SessionFlagEnableSPNServerPort( _
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

 

 





