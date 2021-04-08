---
description: Interfaces clientes
ms.assetid: fbe53f17-940a-485e-82b2-c11ae39b3300
title: Interfaces clientes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5d7c85ec5cb9b35e30d68b1d784cdebf230fdaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866525"
---
# <a name="client-interfaces"></a>Interfaces clientes

Les applications utilisent les méthodes prises en charge par les interfaces suivantes pour effectuer des opérations sur les périphériques portables. Ces opérations incluent l’ouverture d’une connexion à un appareil, la récupération de données à partir d’un appareil, l’écriture de données sur un appareil, etc.



| Interface                                                                              | Description                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)                   | Énumère les objets sur un appareil mobile.                                                                                                                                                                                        |
| [**IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)                                             | Fournit un accès de bas niveau à un appareil mobile.                                                                                                                                                                                     |
| [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                     | Récupère une variété de fonctionnalités d’appareil, notamment les formats, les commandes et les objets fonctionnels pris en charge.                                                                                                                          |
| [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                               | Fournit des méthodes pour créer, énumérer et supprimer du contenu sur un appareil.                                                                                                                                                              |
| [**IPortableDeviceDataStream**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream)                         | Expose des méthodes supplémentaires sur un **IStream** utilisé pour les transferts de données.                                                                                                                                                               |
| [**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)                   | Implémenté par l’application pour recevoir des rappels asynchrones.                                                                                                                                                                   |
| [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager)                               | Énumère les appareils connectés à l’ordinateur et fournit un moyen simple de demander des informations d’installation pour l’appareil (notamment le fabricant, le nom convivial et la description).                                       |
| [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                         | Propriétés en lecture et en écriture pour un objet sur l’appareil.                                                                                                                                                                              |
| [**IPortableDevicePropertiesBulk**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)                 | Lit et écrit plusieurs propriétés sur plusieurs objets sur un appareil, de manière asynchrone.                                                                                                                                               |
| [**IPortableDevicePropertiesBulkCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulkcallback) | Implémenté par l’application pour suivre la progression d’une opération asynchrone démarrée à l’aide de l’interface **IPortableDevicePropertiesBulk** .                                                                          |
| [**IPortableDeviceResources**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources)                           | Fournit l’accès aux données d’un objet.                                                                                                                                                                                                |
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                               | Windows 7 uniquement. Fournit un accès de bas niveau à un service d’appareil mobile.                                                                                                                                                             |
| [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)              | Windows 7 uniquement. Récupère diverses fonctionnalités de service, notamment les formats, les commandes, les méthodes et les profils de rendu pris en charge.                                                                                                |
| [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)                 | Windows 7 uniquement. Appelle des méthodes de façon synchrone et asynchrone sur un service.                                                                                                                                                      |
| [**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback)   | Windows 7 uniquement. Implémenté par l’application pour effectuer le suivi de la fin d’une opération de méthode de service asynchrone commencée par l’appel de [ **IPortableDeviceServiceMethods :: InvokeAsync**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync) |
| [**IPortableDeviceServiceManager**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager)                 | Windows 7 uniquement. Énumère les services pris en charge par un appareil et récupère l’appareil associé à un service.                                                                                                             |



 

Le diagramme suivant montre comment une application obtient la plupart des interfaces dont elle a besoin. Toutes les méthodes de toutes les interfaces ou interfaces implémentées par l’application ne sont pas affichées.

![Diagramme montrant la création et la récupération de la plupart des interfaces clientes requises](images/wpd-sdk-interface-diagram.gif)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de référence de programmation**](programming-reference.md)
</dt> </dl>

 

 



