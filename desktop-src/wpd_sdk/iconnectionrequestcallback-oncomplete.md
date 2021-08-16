---
description: notifie une application qu’une demande de Connecter ou de déconnexion précédemment planifiée à l’appareil MTP/Bluetooth s’est terminée.
ms.assetid: 1588d0ec-0d6a-4379-bfdc-4ba5fdaa4665
title: 'IConnectionRequestCallback :: OnComplete, méthode (Devpkey. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IConnectionRequestCallback.OnComplete
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: b21248cde95d4b58accb7e629efedfc7c05eef7b08f411e240314a6a07690b3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843187"
---
# <a name="iconnectionrequestcallbackoncomplete-method"></a>IConnectionRequestCallback :: OnComplete, méthode

la méthode **OnComplete** notifie une application qu’une demande de Connecter ou de déconnexion précédemment planifiée à l’appareil MTP/Bluetooth est terminée

## <a name="syntax"></a>Syntaxe


```C++
HRESULT OnComplete(
  [in] HRESULT hrStatus
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hrStatus* \[ dans\]
</dt> <dd>

État de la demande de connexion ou de déconnexion d’un appareil donné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Remarques

Une application implémente l’interface [**IConnectionRequestCallback**](iconnectionrequestcallback.md) pour recevoir des notifications sur les demandes terminées et annuler les demandes en attente.

Windows Les appareils mobiles (WPD) appellent cette méthode pour avertir une application qu’une demande précédemment planifiée est terminée. Chaque demande peut être suivie et annulée par son rappel fourni par l’application. par conséquent, si l’application doit envoyer plusieurs demandes en même temps à l’aide du même objet [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) , chaque demande doit recevoir un objet [**IConnectionRequestCallback**](iconnectionrequestcallback.md) unique comme paramètre d’entrée des méthodes [**IPortableDeviceConnector :: Connecter**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) et [**IPortableDeviceConnector ::D éconnecter**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                                                                                             |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                                                                              |
| En-tête<br/>                   | <dl> <dt>Devpkey. h ; </dt> <dt>PortableDeviceConnectApi. h</dt> </dl> |
| MIDL<br/>                      | <dl> <dt>PortableDeviceConnectApi. idl</dt> </dl>                                                                |
| Bibliothèque<br/>                  | <dl> <dt>PortableDeviceGuids. lib</dt> </dl>                                                                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IConnectionRequestCallback**](iconnectionrequestcallback.md)
</dt> </dl>

 

 




