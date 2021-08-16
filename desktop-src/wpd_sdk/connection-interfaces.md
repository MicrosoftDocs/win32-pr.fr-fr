---
description: Interfaces de connexion MTP/Bluetooth
ms.assetid: 7bbd5fe3-85f1-4f0a-9d3e-22746bd23aae
title: Interfaces de connexion MTP/Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c0f32717afe14be05cae6e43d097e67fc9790729e5be4ce9c2dfa6f901a126a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843366"
---
# <a name="mtpbluetooth-connection-interfaces"></a>Interfaces de connexion MTP/Bluetooth

les interfaces suivantes permettent aux applications d’énumérer et de se connecter uniquement aux périphériques qui prennent en charge le protocole mtp (Media Transfer Protocol) sur Bluetooth (mtp/Bluetooth). les interfaces du pilote WPD, du regroupement et du client ne sont pas limitées au protocole MTP/Bluetooth.



| Interface                                                              | Description                                                                                                         |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**IConnectionRequestCallback**](iconnectionrequestcallback.md)       | Définit une méthode de rappel unique que les applications utilisent pour recevoir une notification des demandes terminées et annulées. |
| [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md) | Énumère les interfaces **IPortableDeviceConnector** .                                                                 |
| [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector)           | prend en charge les méthodes que les applications appellent pour établir des connexions aux appareils Bluetooth MTP.                          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de référence de programmation**](programming-reference.md)
</dt> </dl>

 

 



