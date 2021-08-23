---
title: Méthode IRemoteDesktopClientEvents OnAdminMessageReceived
description: Appelé lorsque le contrôle client reçoit un message d’administration.
ms.assetid: CD580207-CEC1-493B-989E-7C1D4FA71228
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnAdminMessageReceived
- Méthode OnAdminMessageReceived Services Bureau à distance, interface IRemoteDesktopClientEvents
- Services Bureau à distance de l’interface IRemoteDesktopClientEvents, méthode OnAdminMessageReceived
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnAdminMessageReceived
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6c50b4b3f26564cc93f1e41653e856f2984559234de92dd2ed2ab02bee20cd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511889"
---
# <a name="iremotedesktopclienteventsonadminmessagereceived-method"></a>IRemoteDesktopClientEvents :: OnAdminMessageReceived, méthode

Appelé lorsque le contrôle client reçoit un message d’administration.

## <a name="syntax"></a>Syntaxe


```C++
void OnAdminMessageReceived(
  [in] BSTR adminMessage
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*adminMessage* \[ dans\]
</dt> <dd>

Message.

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

 

 





