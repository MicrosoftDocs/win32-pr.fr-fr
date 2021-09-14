---
description: Accès aux propriétés de l’objet de service
ms.assetid: 66d9802b-ad28-47a4-8151-9df7aff07d61
title: Accès aux propriétés de l’objet de service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 028ffc178f29f21aa60295b137b48c0fa2357a28
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234515"
---
# <a name="accessing-service-object-properties"></a>Accès aux propriétés de l’objet de service

Une application peut lire et écrire des propriétés pour un objet unique sur un service, pour plusieurs objets identifiés par des identificateurs d’objets, ou pour plusieurs objets du même type. La rubrique [récupération des propriétés](retrieving-content-object-properties.md) de l’objet décrit la lecture des propriétés d’un seul objet sur un service. La rubrique relative à l' [écriture des propriétés](writing-content-object-properties.md) de l’objet décrit l’écriture des propriétés d’un objet unique sur un service.

Reportez-vous à la section [tâches avancées](advanced-tasks.md) pour obtenir une description de la récupération de propriétés pour plusieurs objets.

## <a name="when-to-use-service-property-definitions"></a>Quand utiliser les définitions de propriété de service

Les appels de l’API WPD utilisés pour la récupération et la définition des propriétés d’un service sont les mêmes que ceux des appels pour la récupération des propriétés d’un appareil (par exemple, « récupération des propriétés d’un objet unique »). La principale différence réside dans le fait qu’un autre jeu d’PROPERTYKEYs est utilisé pour interroger les propriétés de l’objet. Pour WpdServiceApiSample, le service de l’appareil PROPERTYKEYs est utilisé (par exemple, le **\_ \_ nom** du type d’GenericObj); pour le WpdApiSample, les PropertyKeys PropertyKeys sont utilisées (telles que le nom de l' **\_ \_ objet wpd**).

Le service d’appareil PROPERTYKEYs est défini dans BridgeDeviceServices. h (inclus par chaque fichier d’en-tête de service) et représente l’ensemble commun de PROPERTYKEYS employés par les applications de services d’appareils et l’implémentation du microprogramme sur l’appareil. Cela permet un ensemble cohérent de définitions dans la pile d’appareils avec une traduction minimale, des groupes PROPERTYKEYs basés sur le service et permet de définir de nouveaux services plus facilement sans avoir à mettre à jour le schéma WPD.

L’ensemble des PROPERTYKEYs utilisés dépend des besoins de votre application :

-   Si votre application communique avec l’appareil en appelant [**IPortableDevice :: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open), utilisez la fonction PROPERTYKEYs définie dans PortableDevice. h. WpdApiSample est un exemple d’une telle application.
-   Si votre application communique avec les services d’appareil en appelant [**IPortableDeviceService :: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open), utilisez la fonction PROPERTYKEYS définie dans BridgeDeviceServices. h. WpdServicesApiSample est un exemple d’une telle application.
-   Si vous écrivez une application complexe qui doit prendre en charge un hybride des services d’appareils et de l’appareil (cela signifie que votre application appelle à la fois **IPortableDevice :: Open** et **IPortableDeviceService :: Open**), vous devez utiliser l’interface wpd PropertyKeys quand vous utilisez IPortableDevice et ses interfaces dérivées, et le service d’appareil PropertyKeys quand vous utilisez [IPortableDeviceService](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) et ses interfaces dérivées.

La plupart des applications WPD doivent appartenir à la première ou à la deuxième catégorie.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[Récupération des propriétés de l’objet](retrieving-content-object-properties.md)
</dt> <dt>

[Écriture de propriétés d’objet](writing-content-object-properties.md)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



