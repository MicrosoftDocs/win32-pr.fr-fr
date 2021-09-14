---
description: Learning Quand un événement se produit
ms.assetid: 4e44089b-676b-4220-9721-54ddf56bf760
title: Learning Quand un événement se produit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19ed537430fd66818687b142f059399292c923e1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999011"
---
# <a name="learning-when-an-event-occurs"></a>Learning Quand un événement se produit

pour traiter les événements de DirectShow, une application a besoin d’un moyen de savoir quand les événements sont en attente dans la file d’attente. le gestionnaire de Graph de filtre propose deux méthodes pour effectuer cette opération :

-   **Notification de fenêtre :** le gestionnaire de Graph de filtre envoie un message de Windows défini par l’utilisateur à une fenêtre d’application chaque fois qu’un nouvel événement se présente.
-   **Signalement des événements :** le gestionnaire de Graph de filtre signale un événement Windows s’il y a DirectShow événements dans la file d’attente et réinitialise l’événement si la file d’attente est vide.

Une application peut utiliser l’une ou l’autre technique. La notification de fenêtre est généralement plus simple.

**Notification de fenêtre**

Pour configurer la notification de fenêtre, appelez la méthode [**IMediaEventEx :: SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) et spécifiez un message privé. Les applications peuvent utiliser des numéros de message dans la plage de l' \_ application WM via 0xBFFF en tant que messages privés. chaque fois que le gestionnaire de Graph de filtre place une nouvelle notification d’événement dans la file d’attente, il publie ce message dans la fenêtre désignée. L’application répond au message dans la boucle de messages de la fenêtre.

L’exemple de code suivant montre comment définir la fenêtre de notification.


```C++
#define WM_GRAPHNOTIFY WM_APP + 1   // Private message.
pEvent->SetNotifyWindow((OAHWND)g_hwnd, WM_GRAPHNOTIFY, 0);
```



le message est un message de Windows ordinaire et est publié séparément de la file d’attente des notifications d’événements DirectShow. L’avantage de cette approche est que la plupart des applications implémentent déjà une boucle de message. par conséquent, vous pouvez incorporer DirectShow gestion des événements sans trop de travail supplémentaire.

L’exemple de code suivant montre comment répondre au message de notification. Pour obtenir un exemple complet, consultez [réponse aux événements](responding-to-events.md).


```C++
LRESULT CALLBACK WindowProc( HWND hwnd, UINT msg, UINT wParam, LONG lParam)
{
    switch (msg)
    {
        case WM_GRAPHNOTIFY:
            HandleEvent();  // Application-defined function.
            break;
        // Handle other Windows messages here too.
    }
    return (DefWindowProc(hwnd, msg, wParam, lParam));
}
```



Étant donné que la notification d’événements et la boucle de message sont toutes deux asynchrones, la file d’attente peut contenir plusieurs événements au moment où votre application répond au message. En outre, les événements peuvent parfois être effacés de la file d’attente s’ils deviennent non valides. Par conséquent, dans votre code de gestion des événements, appelez [**IAMMediaEvent :: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) jusqu’à ce qu’il retourne un code d’échec, ce qui indique que la file d’attente est vide.

Avant de libérer le pointeur [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) , annulez la notification d’événement en appelant [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) avec un pointeur **null** . Dans votre code de traitement des événements, vérifiez si votre pointeur **IMediaEventEx** est valide avant d’appeler [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent). Ces étapes empêchent une erreur possible, dans laquelle l’application reçoit la notification d’événement après la libération du pointeur **IMediaEventEx** .

**Signalisation d’événements**

le gestionnaire de Graph de filtre conserve un événement de réinitialisation manuelle qui reflète l’état de la file d’attente d’événements. si la file d’attente contient des notifications d’événements en attente, le gestionnaire de Graph de filtre signale l’événement de réinitialisation manuelle. Si la file d’attente est vide, un appel à la méthode [**IMediaEvent :: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) réinitialise l’événement. Une application peut utiliser cet événement pour déterminer l’état de la file d’attente.

> [!Note]  
> La terminologie peut prêter à confusion ici. l’événement de réinitialisation manuelle est le type d’événement créé par la Windows fonction [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) ; Il n’a rien à faire avec les événements définis par DirectShow.

 

Appelez la méthode [**IMediaEvent :: GetEventHandle**](/windows/desktop/api/Control/nf-control-imediaevent-geteventhandle) pour obtenir un descripteur de l’événement de réinitialisation manuelle. Attendez que l’événement soit signalé en appelant une fonction telle que [**WaitForMultipleObjects**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjects). une fois que l’événement est signalé, appelez [**IMediaEvent :: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) pour accéder à l’événement DirectShow.

L'exemple de code suivant illustre cette approche. Elle obtient le handle d’événement, puis attend dans les intervalles de 100 millisecondes que l’événement soit signalé. Si l’événement est signalé, il appelle **GetEvent** et imprime le code d’événement et les paramètres d’événement dans la fenêtre de console. La boucle se termine lorsque l’événement [**EC \_ Complete**](ec-complete.md) se produit, indiquant que la lecture est terminée.


```C++
HANDLE  hEvent; 
long    evCode, param1, param2;
BOOLEAN bDone = FALSE;
HRESULT hr = S_OK;
hr = pEvent->GetEventHandle((OAEVENT*)&hEvent);
if (FAILED(hr))
{
    /* Insert failure-handling code here. */
}

while(!bDone) 
{
    if (WAIT_OBJECT_0 == WaitForSingleObject(hEvent, 100))
    { 
        while (S_OK == pEvent->GetEvent(&evCode, &param1, &param2, 0)) 
        {
            printf("Event code: %#04x\n Params: %d, %d\n", evCode, param1, param2);
            pEvent->FreeEventParams(evCode, param1, param2);
            bDone = (EC_COMPLETE == evCode);
        }
    }
} 
```



Étant donné que le graphique de filtre définit ou réinitialise automatiquement l’événement, le cas échéant, votre application ne doit pas le faire. En outre, lorsque vous relâchez le graphique de filtre, le graphique de filtre ferme le descripteur d’événement. n’utilisez donc pas le descripteur d’événement après ce point.

 

 
