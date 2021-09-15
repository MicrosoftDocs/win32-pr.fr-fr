---
description: Interfaces de connexion MTP/Bluetooth
ms.assetid: 7bbd5fe3-85f1-4f0a-9d3e-22746bd23aae
title: Interfaces de connexion MTP/Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97e5194b8a6ababc05c36590ef30ae19ab185efe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522969"
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

 

 



