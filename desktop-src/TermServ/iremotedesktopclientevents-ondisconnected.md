---
title: Méthode IRemoteDesktopClientEvents OnDisconnected
description: Appelé lorsque le contrôle client a été déconnecté d’une session à distance.
ms.assetid: EA26B530-0AA8-49D6-8E3C-E53179FC5104
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnDisconnected
- Méthode OnDisconnected Services Bureau à distance, interface IRemoteDesktopClientEvents
- Services Bureau à distance de l’interface IRemoteDesktopClientEvents, méthode OnDisconnected
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnDisconnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bd59b03fe9cb23309d53773289291c8a791935a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742381"
---
# <a name="iremotedesktopclienteventsondisconnected-method"></a>IRemoteDesktopClientEvents :: OnDisconnected, méthode

Appelé lorsque le contrôle client a été déconnecté d’une session à distance.

## <a name="syntax"></a>Syntaxe


```C++
void OnDisconnected(
  [in] long disconnectReason,
  [in] long ExtendedDisconnectReason,
  [in] BSTR disconnectErrorMessage
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*disconnectReason* \[ dans\]
</dt> <dd>

Raison de l’événement de déconnexion.

</dd> <dt>

*ExtendedDisconnectReason* \[ dans\]
</dt> <dd>

Informations étendues pour l’événement de déconnexion.

</dd> <dt>

*disconnectErrorMessage* \[ dans\]
</dt> <dd>

Message d’erreur pour l’événement de déconnexion.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                           |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                 |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | DIID \_ IRemoteDesktopClientEvents est défini comme 079863B7-6D47-4105-8BFE-0CDCB360E67D<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IRemoteDesktopClientEvents**](iremotedesktopclientevents.md)
</dt> </dl>

 

 





