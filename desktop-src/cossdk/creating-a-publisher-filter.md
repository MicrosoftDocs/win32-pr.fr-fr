---
description: Création d’un filtre d’éditeur
ms.assetid: d91efecc-f02a-41c6-acf7-37b74723e7e8
title: Création d’un filtre d’éditeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 997fe37cf0021bcb2aa153c2dc4b73597e0c43cc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111439"
---
# <a name="creating-a-publisher-filter"></a>Création d’un filtre d’éditeur

Il existe deux méthodes pour établir le filtre de l’éditeur : à l’aide de la propriété MultiPublisherFilterCLSID de la classe d’événements, ou à l’aide de [**IEventControl :: SetPublisherFilter**](/windows/desktop/api/Eventsys/nf-eventsys-ieventcontrol-setpublisherfilter).

-   Étant donné qu’elle vous permet de composer l’objet d’événement avec le service [com+ en file d’attente](com--queued-components.md) , la méthode recommandée consiste à utiliser la propriété MultiPublisherFilterCLSID de la classe d’événements pour définir le filtre de l’éditeur. Cela établit un objet de filtre pour toutes les méthodes des interfaces d’événements pour un objet d’événement. L’objet d’événement active le filtre de l’éditeur lorsque l’objet de classe d’événements est instancié à l’aide de [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).
-   Vous pouvez également utiliser [**SetPublisherFilter**](/windows/desktop/api/Eventsys/nf-eventsys-ieventcontrol-setpublisherfilter). Toutefois, si vous choisissez cette méthode, l’interface n’est pas mise en file d’attente et ne peut donc pas utiliser l’objet d’événement avec le service composants en file d’attente COM+ entre le serveur de publication et l’objet de classe d’événements. Pour plus d’informations sur l’utilisation du service Queued Components avec des événements COM+, consultez [utilisation d’événements com+ avec des composants en file d’attente com+](using-com--events-with-com--queued-components.md).

Un événement peut avoir un ou plusieurs objets de filtre, ou aucun. Les objets de filtre d’éditeur doivent prendre en charge [**IPublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) ou [**IMultiInterfacePublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-imultiinterfacepublisherfilter), selon que vous disposez d’une interface de déclenchement unique ou de plusieurs interfaces de déclenchement sur l’objet de classe d’événements. Les interfaces **IPublisherFilter** et **IMultiInterfacePublisherFilter** spécifient toutes deux une méthode **Initialize** . La méthode Initialize est appelée par l’objet de classe **d'** événements immédiatement après la création de l’objet de filtre.

Les événements COM+ essaient d’appeler deux méthodes sur le filtre. Tout d’abord, elle appelle [**IPublisherFilter ::P reparetofire**](/windows/desktop/api/EventSys/nf-eventsys-ipublisherfilter-preparetofire) et transmet un pointeur d’interface [**IFiringControl**](/windows/desktop/api/EventSys/nn-eventsys-ifiringcontrol) au filtre. Ensuite, il interroge l’objet de filtre pour l’interface d’événement. Si le filtre prend en charge l’interface d’événement, il appelle une méthode sur celui-ci. Cela permet d’accéder aux paramètres du serveur de publication d’un événement. Le filtre peut utiliser ces paramètres pour déterminer les abonnements à activer.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtrage des événements dans COM+](filtering-events-in-com-.md)
</dt> </dl>

 

 
