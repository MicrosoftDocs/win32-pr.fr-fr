---
title: Méthode IRemoteDesktopClientEvents OnNetworkStatusChanged
description: Appelé lorsque l’état du réseau a changé. | Méthode IRemoteDesktopClientEvents OnNetworkStatusChanged
ms.assetid: B68D1AA0-6403-40CA-95C5-BBBF39CEFFD8
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnNetworkStatusChanged
- Méthode OnNetworkStatusChanged Services Bureau à distance, interface IRemoteDesktopClientEvents
- Services Bureau à distance de l’interface IRemoteDesktopClientEvents, méthode OnNetworkStatusChanged
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnNetworkStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96d14519f5da78a0d42b5bd7e52abf790c21406bfe20848235d2639beed2e215
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515109"
---
# <a name="iremotedesktopclienteventsonnetworkstatuschanged-method"></a>IRemoteDesktopClientEvents :: OnNetworkStatusChanged, méthode

Appelé lorsque l’état du réseau a changé.

## <a name="syntax"></a>Syntaxe


```C++
void OnNetworkStatusChanged(
  [in] unsigned long qualityLevel,
  [in] long          bandwidth,
  [in] long          rtt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*qualityLevel* \[ dans\]
</dt> <dd>

Nouveau niveau de qualité de la connexion. Le niveau de qualité est déterminé à partir de la bande passante et des valeurs de temps d’aller-retour (RTT).

Une des valeurs suivantes.



| Valeur                                                                        | Signification                                                     |
|------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Impossible de déterminer le niveau de qualité.<br/>       |
| <dl> <dt>1</dt> </dl> | La qualité de la connexion est médiocre (une barre).<br/>        |
| <dl> <dt>2</dt> </dl> | La qualité de la connexion est équitable (deux barres).<br/>       |
| <dl> <dt>3</dt> </dl> | La qualité de la connexion est bonne (trois barres).<br/>     |
| <dl> <dt>4</dt> </dl> | La qualité de la connexion est excellente (quatre barres).<br/> |



 

</dd> <dt>

*bande passante* \[ dans\]
</dt> <dd>

Spécifie la nouvelle bande passante de connexion, en kilobits par seconde (Kbits/s).

</dd> <dt>

*RTT* \[ dans\]
</dt> <dd>

Spécifie la nouvelle durée de bouclage de la connexion (latence), en millisecondes.

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

 

 





