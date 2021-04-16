---
description: Cet article explique comment répondre aux événements qui se produisent dans un graphique de filtre.
ms.assetid: 1c09149b-7f34-4296-bd32-dbbae5e1d62b
title: Réponse aux événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a51481371501c05733e5f637885a71001c1f996
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521399"
---
# <a name="responding-to-events"></a>Réponse aux événements

Cet article explique comment répondre aux événements qui se produisent dans un graphique de filtre.

## <a name="how-event-notification-works"></a>Fonctionnement de la notification d’événement

Pendant l’exécution d’une application DirectShow, les événements peuvent se produire dans le graphique de filtre. Par exemple, un filtre peut rencontrer une erreur de diffusion en continu. Les filtres alertent le gestionnaire du graphique de filtre en envoyant des événements, qui consistent en un code d’événement et deux paramètres d’événement. Le code d’événement indique le type d’événement et les paramètres d’événement fournissent des informations supplémentaires. La signification des paramètres dépend du code de l’événement. Pour obtenir la liste complète des codes d’événement, consultez [codes de notification d’événement](event-notification-codes.md).

Certains événements sont gérés en mode silencieux par le gestionnaire de graphique de filtre, sans que l’application soit notifiée. D’autres événements sont placés dans une file d’attente pour l’application. Selon l’application, vous devrez peut-être gérer différents événements. Cet article se concentre sur trois événements très courants :

-   L’événement [**EC \_ Complete**](ec-complete.md) indique que la lecture s’est terminée normalement.
-   L’événement [**EC \_ USERABORT**](ec-userabort.md) indique que l’utilisateur a interrompu la lecture. Les convertisseurs vidéo envoient cet événement si l’utilisateur ferme la fenêtre vidéo.
-   L’événement [**EC \_ ERRORABORT**](ec-errorabort.md) indique qu’une erreur a provoqué l’arrêt de la lecture.

## <a name="using-event-notification"></a>Utilisation de la notification d’événement

Une application peut demander au gestionnaire de graphique de filtre d’envoyer un message Windows à une fenêtre désignée à chaque fois qu’un nouvel événement se produit. Cela permet à l’application de répondre à l’intérieur de la boucle de message de la fenêtre. Tout d’abord, définissez le message qui sera envoyé à la fenêtre d’application. Les applications peuvent utiliser des numéros de message dans la plage de l' \_ application WM via 0xBFFF en tant que messages privés :


```C++
#define WM_GRAPHNOTIFY  WM_APP + 1
```



Ensuite, interrogez le gestionnaire du graphique de filtre pour l’interface [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) et appelez la méthode [**IMediaEventEx :: SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) :


```C++
IMediaEventEx *g_pEvent = NULL;
g_pGraph->QueryInterface(IID_IMediaEventEx, (void **)&g_pEvent);
g_pEvent->SetNotifyWindow((OAHWND)g_hwnd, WM_GRAPHNOTIFY, 0);
```



Cette méthode désigne la fenêtre spécifiée (g \_ HWND) comme destinataire du message. Appelez la méthode après avoir créé le graphique de filtre, mais avant d’exécuter le graphique.

WM \_ GRAPHNOTIFY est un message Windows ordinaire. Chaque fois que le gestionnaire de graphique de filtre place un nouvel événement dans la file d’attente d’événements, il publie un \_ message WM GRAPHNOTIFY dans la fenêtre d’application désignée. Le paramètre *lParam* du message est égal au troisième paramètre dans [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow). Ce paramètre vous permet d’envoyer des données d’instance avec le message. Le paramètre *wParam* du message de fenêtre est toujours égal à zéro.

Dans la fonction **WindowProc** de votre application, ajoutez une instruction case pour le \_ message WM GRAPHNOTIFY :


```C++
case WM_GRAPHNOTIFY:
    HandleGraphEvent();
    break;
```



Dans la fonction de gestionnaire d’événements, appelez la méthode [**IMediaEvent :: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) pour récupérer les événements de la file d’attente :


```C++
void HandleGraphEvent()
{
    // Disregard if we don't have an IMediaEventEx pointer.
    if (g_pEvent == NULL)
    {
        return;
    }
    // Get all the events
    long evCode;
    LONG_PTR param1, param2;
    HRESULT hr;
    while (SUCCEEDED(g_pEvent->GetEvent(&evCode, &param1, &param2, 0)))
    {
        g_pEvent->FreeEventParams(evCode, param1, param2);
        switch (evCode)
        {
        case EC_COMPLETE:  // Fall through.
        case EC_USERABORT: // Fall through.
        case EC_ERRORABORT:
            CleanUp();
            PostQuitMessage(0);
            return;
        }
    } 
}
```



La méthode [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) récupère le code d’événement et les deux paramètres d’événement. Le quatrième paramètre **GetEvent** spécifie la durée d’attente d’un événement, en millisecondes. Étant donné que l’application appelle cette méthode en réponse à un \_ message WM GRAPHNOTIFY, l’événement est déjà mis en file d’attente. Par conséquent, nous définissons la valeur du délai d’attente sur zéro.

La notification d’événement et la boucle de message sont toutes deux asynchrones, donc la file d’attente peut contenir plusieurs événements au moment où votre application répond au message. En outre, le gestionnaire de graphes de filtre peut supprimer certains événements de la file d’attente, s’ils deviennent non valides. Par conséquent, vous devez appeler [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) jusqu’à ce qu’il retourne un code d’échec, indiquant que la file d’attente est vide.

Dans cet exemple, l’application répond à la valeur [**EC \_ Complete**](ec-complete.md), [**EC \_ USERABORT**](ec-userabort.md)et [**EC \_ ERRORABORT**](ec-errorabort.md) en appelant la fonction de nettoyage définie par l’application, ce qui entraîne la fermeture normale de l’application. L’exemple ignore les deux paramètres d’événement. Après avoir récupéré un événement, appelez [**IMediaEvent :: FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) pour accéder à toutes les ressources gratuites associées aux paramètres de l’événement.

Notez qu’un événement [**EC \_ Complete**](ec-complete.md) ne provoque pas l’arrêt du graphique de filtre. L’application peut arrêter ou suspendre le graphique. Si vous arrêtez le graphique, les filtres libèrent toutes les ressources qu’ils détiennent. Si vous suspendez le graphique, les filtres continuent à contenir des ressources. En outre, lorsqu’un convertisseur vidéo est suspendu, il affiche une image statique du frame le plus récent.

Avant de libérer le pointeur [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) , annulez la notification d’événement en appelant [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) avec un handle de fenêtre **null** :


```C++
// Disable event notification before releasing the graph.
g_pEvent->SetNotifyWindow(NULL, 0, 0);
g_pEvent->Release();
g_pEvent = NULL;
```



Dans le \_ Gestionnaire de messages WM GRAPHNOTIFY, vérifiez le pointeur [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) avant d’appeler [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent):


```C++
if (g_pEvent == NULL) return;
```



Cela empêche une erreur possible qui peut se produire si l’application reçoit la notification d’événement après avoir relâché le pointeur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Tâches de base de DirectShow](basic-directshow-tasks.md)
</dt> <dt>

[Notification d’événement dans DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



