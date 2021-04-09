---
description: Notifie une application qu’une demande de connexion ou de déconnexion précédemment planifiée à l’appareil MTP/Bluetooth est terminée.
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
ms.openlocfilehash: 922169b7e17335c47425665bb9a9e54891e68723
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866522"
---
# <a name="iconnectionrequestcallbackoncomplete-method"></a>IConnectionRequestCallback :: OnComplete, méthode

La méthode **OnComplete** notifie une application qu’une demande de connexion ou de déconnexion précédemment planifiée à l’appareil MTP/Bluetooth est terminée

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

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

Une application implémente l’interface [**IConnectionRequestCallback**](iconnectionrequestcallback.md) pour recevoir des notifications sur les demandes terminées et annuler les demandes en attente.

Les appareils mobiles Windows (WPD) appellent cette méthode pour avertir une application qu’une demande précédemment planifiée est terminée. Chaque demande peut être suivie et annulée par son rappel fourni par l’application. Par conséquent, si l’application doit envoyer plusieurs demandes en même temps à l’aide du même objet [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) , chaque demande doit recevoir un objet [**IConnectionRequestCallback**](iconnectionrequestcallback.md) unique comme paramètre d’entrée des méthodes [**IPortableDeviceConnector :: Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) et [**IPortableDeviceConnector ::D éconnecter**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                                                                                             |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                                                                              |
| En-tête<br/>                   | <dl> <dt>Devpkey. h ; </dt> <dt>PortableDeviceConnectApi. h</dt> </dl> |
| MIDL<br/>                      | <dl> <dt>PortableDeviceConnectApi. idl</dt> </dl>                                                                |
| Bibliothèque<br/>                  | <dl> <dt>PortableDeviceGuids. lib</dt> </dl>                                                                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IConnectionRequestCallback**](iconnectionrequestcallback.md)
</dt> </dl>

 

 




