---
title: Méthode IRemoteDesktopClientEvents OnStatusChanged (Locationapi. h)
description: Appelé lorsque le contrôle client a mis à jour son état.
ms.assetid: AAFBDC9E-C8B5-4924-AA69-82EF09996AF7
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnStatusChanged
- Méthode OnStatusChanged Services Bureau à distance, interface IRemoteDesktopClientEvents
- Services Bureau à distance de l’interface IRemoteDesktopClientEvents, méthode OnStatusChanged
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d08b15eb2b8112afcef6c98a841a249672df2ae3fbb7f36ceea513d53a5b0478
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118351621"
---
# <a name="iremotedesktopclienteventsonstatuschanged-method"></a>IRemoteDesktopClientEvents :: OnStatusChanged, méthode

Appelé lorsque le contrôle client a mis à jour son état.

## <a name="syntax"></a>Syntaxe


```C++
void OnStatusChanged(
   long statusCode,
   BSTR statusMessage
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*statusCode* 
</dt> <dd>

Nouveau code d’État.

</dd> <dt>

*statusMessage* 
</dt> <dd>

Texte du message d’État.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                           |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>Locationapi. h</dt> </dl>       |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | DIID \_ IRemoteDesktopClientEvents est défini comme 079863B7-6D47-4105-8BFE-0CDCB360E67D<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IRemoteDesktopClientEvents**](iremotedesktopclientevents.md)
</dt> </dl>

 

 





