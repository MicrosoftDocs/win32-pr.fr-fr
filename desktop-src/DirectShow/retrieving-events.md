---
description: Récupération des événements
ms.assetid: 18c5892d-7e33-497c-ab7d-d17fea5df17e
title: Récupération des événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1132b2b0140c86c2be1e7916e8d1de28e231b2eca50596714aaa82346aaf83eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072723"
---
# <a name="retrieving-events"></a>Récupération des événements

le gestionnaire de Graph de filtre expose trois interfaces qui prennent en charge la notification d’événements.

-   [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) contient la méthode pour les filtres pour la publication des événements.
-   [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) contient des méthodes permettant aux applications de récupérer des événements.
-   [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) hérite de et étend l’interface [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) .

les filtres publient les notifications d’événements en appelant la méthode [**IMediaEventSink :: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) sur le gestionnaire de Graph de filtre. Une notification d’événement se compose d’un code d’événement qui définit le type d’événement, et de deux paramètres qui fournissent des informations supplémentaires. En fonction du code d’événement, les paramètres peuvent contenir des pointeurs, des codes de retour, des temps de référence ou d’autres informations. Pour obtenir la liste complète des codes et paramètres d’événement, consultez [codes de notification d’événement](event-notification-codes.md).

pour récupérer un événement à partir de la file d’attente, l’application appelle la méthode [**IMediaEvent :: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) sur le gestionnaire de Graph de filtre. Cette méthode bloque jusqu’à ce qu’il y ait un événement à retourner ou jusqu’à ce qu’un délai spécifié se soit écoulé. En supposant qu’il existe un événement de mise en file d’attente, la méthode retourne avec le code d’événement et les deux paramètres d’événement. Après l’appel de **GetEvent**, une application doit toujours appeler la méthode [**IMediaEvent :: FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) pour libérer toutes les ressources associées aux paramètres de l’événement. Par exemple, un paramètre peut être une valeur **BSTR** qui a été allouée par le graphique de filtre.

L’exemple de code suivant montre comment récupérer des événements de la file d’attente.


```C++
long evCode;
LONG_PTR param1, param2;
HRESULT hr;
while (hr = pEvent->GetEvent(&evCode, &param1, &param2, 0), SUCCEEDED(hr))
{
    switch(evCode) 
    { 
        // Call application-defined functions for each 
        // type of event that you want to handle.
    } 
    hr = pEvent->FreeEventParams(evCode, param1, param2);
}
```



pour remplacer la gestion par défaut du filtre Graph Manager pour un événement, appelez la méthode [**IMediaEvent :: CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) avec le code d’événement en tant que paramètre. Vous pouvez rétablir la gestion par défaut en appelant la méthode [**IMediaEvent :: RestoreDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-restoredefaulthandling) . Si le graphique de filtre n’effectue aucune gestion par défaut pour le code d’événement spécifié, l’appel de ces méthodes n’a aucun effet.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Notification d’événements dans DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



