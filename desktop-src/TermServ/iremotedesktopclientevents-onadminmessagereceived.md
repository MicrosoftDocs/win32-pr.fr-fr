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
ms.openlocfilehash: 201dd3111dbac0b6395654ef8dfad21318419de3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384976"
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

 

 





