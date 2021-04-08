---
title: Méthode WSMan. SessionFlagUTF8 (WSManDisp. h)
description: Retourne la valeur de l’indicateur d’authentification WSManFlagUTF8 à utiliser dans le paramètre flags de WSMan. CreateSession.
ms.assetid: a79e292a-364b-4bf3-ae66-6a15ad51524f
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode SessionFlagUTF8
- Méthode SessionFlagUTF8 Windows Remote Management, objet WSMan
- Objet WSMan Windows Remote Management, méthode SessionFlagUTF8
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUTF8
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 985763131c2f3d4227f1a24af612ea3141237832
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743213"
---
# <a name="wsmansessionflagutf8-method"></a>Méthode WSMan. SessionFlagUTF8

La méthode **WSMan. SessionFlagUTF8** retourne la valeur de l’indicateur d’authentification **WSManFlagUTF8** pour une utilisation dans le paramètre *Flags* de [**WSMan. CreateSession**](wsman-createsession.md). Cette méthode fournit une syntaxe plus efficace pour l’utilisation de la constante afin que les scripts ne soient pas requis pour définir une valeur de constante. Pour plus d’informations sur l’appel de cette méthode, consultez [sessions, constantes](session-constants.md).

**WSManFlagUTF8** est une constante dans l’énumération **\_ \_ WSManSessionFlags** . Pour plus d’informations, consultez [autres constantes de session](other-session-constants.md).

## <a name="syntax"></a>Syntaxe


```VB
WSMan.SessionFlagUTF8( _
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

 

 





