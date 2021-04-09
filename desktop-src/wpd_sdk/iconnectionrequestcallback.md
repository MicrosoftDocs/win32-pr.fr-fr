---
description: Définit une méthode de rappel unique.
ms.assetid: 579f7a29-cd98-4d97-9f8e-9b786897df1c
title: Interface IConnectionRequestCallback (Devpkey. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IConnectionRequestCallback
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: aca827de068ce221f013f03b35f88fd76a030dd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953096"
---
# <a name="iconnectionrequestcallback-interface"></a>Interface IConnectionRequestCallback

L’interface **IConnectionRequestCallback** définit une méthode de rappel unique. Une application Windows Mobile Devices (WPD) implémente cette interface COM (Component Object Model) facultative pour recevoir des notifications sur les demandes terminées et pour annuler les demandes en attente. Les demandes sont envoyées à l’aide des méthodes [**IPortableDeviceConnector :: Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) et [**IPortableDeviceConnector ::D éconnecter**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) .

## <a name="members"></a>Membres

L’interface **IConnectionRequestCallback** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IConnectionRequestCallback** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IConnectionRequestCallback** possède ces méthodes.



| Méthode                                                      | Description                                                                           |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**OnComplete**](iconnectionrequestcallback-oncomplete.md) | Avertit une application qu’une demande précédemment planifiée est terminée.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                                                                                             |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                                                                              |
| En-tête<br/>                   | <dl> <dt>Devpkey. h ; </dt> <dt>PortableDeviceConnectApi. h</dt> </dl> |
| MIDL<br/>                      | <dl> <dt>PortableDeviceConnectApi. idl</dt> </dl>                                                                |
| Bibliothèque<br/>                  | <dl> <dt>PortableDeviceGuids. lib</dt> </dl>                                                                     |



 

