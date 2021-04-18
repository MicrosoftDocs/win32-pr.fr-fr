---
title: Session. identify, méthode (WSManDisp. h)
description: Interroge un ordinateur distant pour déterminer s’il prend en charge le protocole WS-Management.
ms.assetid: b86ec9b8-8fc4-4c3e-aca7-2f7d039749df
ms.tgt_platform: multiple
keywords:
- Identifiez la méthode Windows Remote Management
- Identifier la méthode Windows Remote Management, objet session
- Windows Remote Management d’objet de session, méthode d’identification
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
ms.openlocfilehash: 24f1caa5b1e44e4ca65082e33bca4d045e487c96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509355"
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

## <a name="remarks"></a>Notes

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

[**session**](session.md)
</dt> <dt>

[**IWSManSession :: identifier**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify)
</dt> <dt>

[Protocole Gestion des services web](ws-management-protocol.md)
</dt> </dl>

 

 





