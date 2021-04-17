---
description: Récupération des propriétés de plusieurs objets par format d’objet
ms.assetid: c3f5edfd-8a6a-4bbd-9787-a4268c38f18f
title: Récupération des propriétés de plusieurs objets par format d’objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a352704b3ce5d063c544a41c467f372554bc901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485457"
---
# <a name="retrieving-properties-for-multiple-objects-by-object-format"></a>Récupération des propriétés de plusieurs objets par format d’objet

En plus d’une récupération en bloc des propriétés d’une collection d’identificateurs d’objet, une application peut également effectuer une récupération en bloc de propriétés pour tous les objets d’un type particulier. Comme dans l’exemple précédent, la récupération en bloc pour un type donné requiert que le pilote de périphérique prenne en charge les récupérations en bloc.

Votre application peut effectuer une récupération en bloc à l’aide des interfaces décrites dans le tableau suivant.



| Interface                                                                                      | Description                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [**Interface IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | Fournit l’accès aux méthodes spécifiques au contenu.                   |
| [**Interface IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)                 | Utilisé pour identifier les propriétés à récupérer.                   |
| [**Interface IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | Utilisé pour déterminer si un pilote donné prend en charge les opérations en bloc. |
| [**Interface IPortableDevicePropertiesBulk**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | Prend en charge l’opération de récupération en bloc.                             |
| [**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Utilisé pour stocker les identificateurs d’objet pour l’opération en bloc.       |



 

La fonction ReadContentPropertiesBulkFilteringFormat dans le module ContentProperties. cpp de l’exemple d’application illustre une opération de récupération en bloc pour les objets d’un type ou d’un format particulier.

Le code trouvé dans la fonction ReadContentPropertiesBulkFilteringFormat est presque identique au code trouvé dans la fonction ReadContentPropertiesBulk. (Pour obtenir une description complète de cette fonction, consultez la rubrique [extraction des propriétés de plusieurs objets](retrieving-properties-for-multiple-objects.md) .)

La principale différence se produit lorsque l’opération est mise en file d’attente. Lors du filtrage par type ou format, la méthode [**IPortableDevicePropertiesBulk :: QueueGetValuesByObjectFormat**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectformat) est appelée à la place de la méthode [**IPortableDevicePropertiesBulk :: QueueGetValuesByObjectList**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectlist) .


```C++
hr = pPropertiesBulk->QueueGetValuesByObjectFormat(WPD_OBJECT_FORMAT_WMA,
                                                   WPD_DEVICE_OBJECT_ID,
                                                   100,
                                                   pPropertiesToRead,
                                                   pCallback,
                                                   &guidContext);
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Interface IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Interface IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)
</dt> <dt>

[**Interface IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**Interface IPortableDevicePropertiesBulk**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Guide de programmation**](programming-guide.md)
</dt> </dl>

 

 



