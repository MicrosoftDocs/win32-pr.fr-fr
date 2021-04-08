---
title: Événements
description: Un service hébergé doit implémenter l’interface IUPnPEventSource s’il a des variables d’état d’événement.
ms.assetid: 7558496d-c909-4602-bfaa-d21108392fed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68a6382ee88d2ca5168c94eac20727bbfee4a598
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840154"
---
# <a name="eventing"></a>Événements

Un service hébergé doit implémenter l’interface [**IUPnPEventSource**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsource) s’il a des variables d’état d’événement. Cette interface a deux méthodes : [**Advise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise) et [**Unadvise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise). Cette interface fournit un mécanisme permettant à l’hôte d’appareil de s’abonner aux notifications d’événements générées par le service hébergé. Il n’y aura pas plus d’un récepteur d’événements enregistré à la fois.

Un service hébergé doit implémenter la méthode [**Advise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise) en maintenant une référence à l’interface [**IUPnPEventSink**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsink) , qui a été transmise en tant que paramètre. Si l’interface est trouvée, la méthode **Advise** contient une référence à cette interface jusqu’à ce que [**Unadvise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise) soit appelée, ou jusqu’à ce que l’objet de service hébergé soit supprimé. La méthode **Advise** est appelée une seule fois.

Pour supprimer l’abonnement, l’hôte d’appareil appelle [**Unadvise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise) et passe le pointeur d’objet utilisé quand il a appelé [**Advise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise). Le service hébergé supprime l’abonnement si le pointeur est le même que celui passé à **Advise**.

Quand la valeur d’une variable d’état change, le service hébergé doit signaler qu’un événement s’est produit. Pour ce faire, les services appellent la méthode [**IUPnPEventSink :: OnStateChanged**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsink-onstatechanged) .

Lorsque l’hôte de l’appareil n’a plus besoin de recevoir des notifications du service hébergé, il appelle [**IUPnPEventSource :: Unadvise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise), en passant le même pointeur d’objet que celui qu’il a reçu de la part de l' [**avis**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise). L’hôte d’appareil appelle cette méthode lorsque l’appareil n’est plus sur le réseau.

 

 




