---
description: Récupération des événements
ms.assetid: 18c5892d-7e33-497c-ab7d-d17fea5df17e
title: Récupération des événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78d23cf4f8060c15db564e718ba3a2fa4a660022
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385504"
---
# <a name="retrieving-events"></a>Récupération des événements

Le gestionnaire de graphique de filtre expose trois interfaces qui prennent en charge la notification d’événements.

-   [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) contient la méthode pour les filtres pour la publication des événements.
-   [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) contient des méthodes permettant aux applications de récupérer des événements.
-   [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) hérite de et étend l’interface [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) .

Les filtres publient les notifications d’événements en appelant la méthode [**IMediaEventSink :: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) sur le gestionnaire de graphique de filtre. Une notification d’événement se compose d’un code d’événement qui définit le type d’événement, et de deux paramètres qui fournissent des informations supplémentaires. En fonction du code d’événement, les paramètres peuvent contenir des pointeurs, des codes de retour, des temps de référence ou d’autres informations. Pour obtenir la liste complète des codes et paramètres d’événement, consultez [codes de notification d’événement](event-notification-codes.md).

Pour récupérer un événement à partir de la file d’attente, l’application appelle la méthode [**IMediaEvent :: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) sur le gestionnaire de graphique de filtre. Cette méthode bloque jusqu’à ce qu’il y ait un événement à retourner ou jusqu’à ce qu’un délai spécifié se soit écoulé. En supposant qu’il existe un événement de mise en file d’attente, la méthode retourne avec le code d’événement et les deux paramètres d’événement. Après l’appel de **GetEvent**, une application doit toujours appeler la méthode [**IMediaEvent :: FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) pour libérer toutes les ressources associées aux paramètres de l’événement. Par exemple, un paramètre peut être une valeur **BSTR** qui a été allouée par le graphique de filtre.

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



Pour remplacer la gestion par défaut du gestionnaire de graphique de filtre pour un événement, appelez la méthode [**IMediaEvent :: CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) avec le code d’événement en tant que paramètre. Vous pouvez rétablir la gestion par défaut en appelant la méthode [**IMediaEvent :: RestoreDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-restoredefaulthandling) . Si le graphique de filtre n’effectue aucune gestion par défaut pour le code d’événement spécifié, l’appel de ces méthodes n’a aucun effet.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Notification d’événement dans DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



