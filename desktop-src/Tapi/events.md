---
description: Les événements sont un élément essentiel de la gestion des appels sous TAPI 3. La gestion des événements comprend quatre étapes.
ms.assetid: db43f4e0-f2f5-49b1-a03d-3df3de0e5611
title: Événements (API de téléphonie)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a9a7d994c7bc9f8019224d826d586d698bc605
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529073"
---
# <a name="events-telephony-api"></a>Événements (API de téléphonie)

Les événements sont un élément essentiel de la gestion des appels sous TAPI 3. La gestion des événements comprend quatre étapes.

**Pour s’inscrire et activer la réception d’événements**

1.  Implémentez la méthode [**ITTAPIEventNotification :: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) . (L’interface TAPI appelle cette méthode lorsqu’un événement se produit.) En règle générale, cette implémentation ne fait pas plus que **AddRef** du pointeur d’interface **IDispatch** , puis publie sur la pompe de messages de l’application.
2.  Inscrivez l’interface sortante [**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) à l’aide des interfaces COM [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) et [**IConnectionPoint**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint) , et transmettez à la méthode [**IConnectionPoint :: Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) un pointeur vers [**ITTAPIEventNotification :: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event).
3.  Appelez la méthode [**ITTAPI ::p ut \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) pour indiquer à l’interface TAPI les événements que l’application doit gérer. Le filtre d’événements se compose des membres **ou** Ed de l’énumération des [**\_ événements TAPI**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) .
    > [!Note]  
    > Vous devez appeler la méthode **ITTAPI ::p ut \_ EventFilter** pour définir le masque de filtre d’événement et activer la réception des événements. Si vous n’appelez pas **ITTAPI ::p ut \_ EventFilter**, votre application ne recevra aucun événement.

     

Vous devez également appeler la méthode [**ITTAPI :: RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) pour chaque objet d’adresse sur lequel l’application doit gérer les appels.

Pour obtenir la liste de toutes les interfaces d’événements, consultez [interfaces](./event-interfaces.md) d’événements. Consultez [inscrire des événements](register-events.md) pour obtenir des exemples de code qui illustrent le processus d’inscription et [reçoivent un appel](receive-a-call.md) pour obtenir un exemple de code qui illustre une utilisation d’événements.

 

 
