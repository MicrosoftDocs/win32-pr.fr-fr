---
title: Session. identify, méthode (WSManDisp. h)
description: Interroge un ordinateur distant pour déterminer s’il prend en charge le protocole WS-Management.
ms.assetid: b86ec9b8-8fc4-4c3e-aca7-2f7d039749df
ms.tgt_platform: multiple
keywords:
- identifiez la méthode Windows Remote Management
- identifier la méthode Windows Remote Management, objet Session
- Windows Remote Management d’objet de Session, méthode d’identification
topic_type:
- apiref
api_name:
- Session.Identify
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9e897a82644fec7bf206e99ea87ae2df82793a9717259b76fd9ca9d264c74f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642549"
---
# <a name="sessionidentify-method"></a>Session. identify, méthode

La méthode **session. identify** interroge un ordinateur distant pour déterminer s’il prend en charge le protocole WS-Management. Pour plus d’informations, consultez [détection de la prise en charge de WS-Management protocole par un ordinateur distant](detecting-whether-a-remote-computer-supports-ws-management-protocol.md).

## <a name="syntax"></a>Syntaxe


```VB
Session.Identify( _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*indicateurs* \[ dans, facultatif\]
</dt> <dd>

Pour envoyer la demande en mode authentifié, utilisez la constante Authentication à partir de l’énumération **WSManSessionFlags** . Pour envoyer en mode non authentifié, utilisez **WSManFlagUseNoAuthentication**. Pour plus d’informations, consultez [**constantes d’authentification**](authentication-constants.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Chaîne XML qui spécifie la version du protocole WS-Management, le fournisseur du système d’exploitation et, si la demande a été envoyée, la version du système d’exploitation.

## <a name="remarks"></a>Remarques

**Session. identifier** est basé sur l’opération [protocole WS-Management](ws-management-protocol.md) définie en tant que wsmanIdentity. Cela est spécifié dans le paquet SOAP comme suit :


```XML
xmlns:wsmid="https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity"
```



## <a name="examples"></a>Exemples

L’exemple VBScript suivant envoie une demande d’identification non authentifiée à l’ordinateur distant nommé Remote dans le même domaine.


```VB
set WSMan = CreateObject("Wsman.Automation")
set Session = WSMan.CreateSession("Remote", _
  WSMan.SessionFlagUseNoAuthentication)
WScript.Echo Session.Identify
```



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

[**Session**](session.md)
</dt> <dt>

[**IWSManSession :: identifier**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify)
</dt> <dt>

[Protocole Gestion des services web](ws-management-protocol.md)
</dt> </dl>

 

 





