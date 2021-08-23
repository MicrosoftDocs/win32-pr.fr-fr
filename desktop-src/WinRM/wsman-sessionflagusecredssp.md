---
title: Méthode WSMan. SessionFlagUseCredSsp (WSManDisp. h)
description: Retourne la valeur de l’indicateur d’authentification WSManFlagUseCredSsp à utiliser dans le paramètre flags de la méthode WSMan. CreateSession.
ms.assetid: bb167445-91d6-4e06-a976-bf869320784a
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode SessionFlagUseCredSsp
- méthode SessionFlagUseCredSsp Windows Remote Management, objet WSMan
- objet WSMan Windows Remote Management, méthode SessionFlagUseCredSsp
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseCredSsp
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27eb96f1de72bbcceafd40c0ccbcfdd3b990ed2134739195bd29e130dbac5a64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642229"
---
# <a name="wsmansessionflagusecredssp-method"></a>Méthode WSMan. SessionFlagUseCredSsp

Retourne la valeur de l’indicateur d’authentification **WSManFlagUseCredSsp** à utiliser dans le paramètre *Flags* de la méthode [**WSMan. CreateSession**](wsman-createsession.md) . Cette méthode fournit une syntaxe plus efficace pour l’utilisation de la constante afin que les scripts ne soient pas requis pour définir une valeur de constante. Pour plus d’informations sur l’appel de cette méthode, consultez [sessions, constantes](session-constants.md).

**WSManFlagUseCredSsp** est une constante dans l’énumération **\_ \_ WSManSessionFlags** . Pour plus d’informations, consultez [constantes d’authentification](authentication-constants.md).

## <a name="syntax"></a>Syntaxe


```VB
WSMan.SessionFlagUseCredSsp( _
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
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7<br/>                                                                                                        |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                                                           |
| Composant redistribuable<br/>          | Windows Management Framework sur Windows Server 2008 avec sp2, Windows vista avec SP1 et Windows vista avec sp2<br/> |
| En-tête<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>                                      |
| MIDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl>                                    |
| Bibliothèque<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl>                                    |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>                                      |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**WSMan**](wsman.md)
</dt> <dt>

[**Session**](session.md)
</dt> </dl>

 

 





