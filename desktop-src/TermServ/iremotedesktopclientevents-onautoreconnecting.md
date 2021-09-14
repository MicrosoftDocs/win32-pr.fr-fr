---
title: Méthode IRemoteDesktopClientEvents OnAutoReconnecting
description: Appelé lorsque le contrôle client tente de rétablir automatiquement une connexion à une session à distance.
ms.assetid: 299408A9-ED14-42F4-B324-AF4C86FEDABE
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnAutoReconnecting
- Méthode OnAutoReconnecting Services Bureau à distance, interface IRemoteDesktopClientEvents
- Services Bureau à distance de l’interface IRemoteDesktopClientEvents, méthode OnAutoReconnecting
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnAutoReconnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d74c37919384727fdf51aad004349478798a3ffd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237191"
---
# <a name="iremotedesktopclienteventsonautoreconnecting-method"></a>IRemoteDesktopClientEvents :: OnAutoReconnecting, méthode

Appelé lorsque le contrôle client tente de rétablir automatiquement une connexion à une session à distance.

## <a name="syntax"></a>Syntaxe


```C++
void OnAutoReconnecting(
  [in] long         disconnectReason,
  [in] long         ExtendedDisconnectReason,
  [in] BSTR         disconnectErrorMessage,
  [in] VARIANT_BOOL networkAvailable,
  [in] long         attemptCount,
  [in] long         maxAttemptCount
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

</dd> <dt>

*networkAvailable* \[ dans\]
</dt> <dd>

Indique si le réseau est disponible.

</dd> <dt>

*attemptCount* \[ dans\]
</dt> <dd>

La tentative est.

</dd> <dt>

*maxAttemptCount* \[ dans\]
</dt> <dd>

Le nombre maximal de tentatives de reconnexion est effectué.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Spécifications



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

 

 





