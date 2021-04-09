---
description: Gestion des notifications d’événements DVD
ms.assetid: 7a12aa36-f709-4ee2-aac6-45ab273ad3f9
title: Gestion des notifications d’événements DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8212f3eb9f868c494aa008602713c1750a6c6dc9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103950315"
---
# <a name="handling-dvd-event-notifications"></a>Gestion des notifications d’événements DVD

Le navigateur DVD envoie des notifications à une fenêtre spécifiée par l’application lorsque certains événements se produisent, par exemple lorsque le domaine du DVD change, lorsqu’un nouveau niveau de gestion parental est rencontré et lorsque le navigateur DVD est sur le point d’entrer dans un bloc d’angle. Les paramètres d’événement peuvent contenir des informations supplémentaires relatives à l’événement. Les messages d’erreur et les avertissements sont également envoyés de cette façon. L’application spécifie la fenêtre qui gérera les notifications d’événements à l’aide du pointeur [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) pour appeler [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow), comme suit :


```C++
const DWORD WM_DVD_EVENT = WM_USER + 100;
hr = m_pIME->SetNotifyWindow(reinterpret_cast<OAHWND>(m_hWnd), WM_DVD_EVENT, 0);
```



Dans l’exemple précédent, m \_ HWND est le HWND de la fenêtre qui reçoit les messages et l' \_ événement de DVD WM \_ est le message défini par l’application (supérieur à l' \_ utilisateur WM) qui signale qu’un événement DVD a eu lieu. L’événement lui-même est récupéré par l’application via un appel à [**IMediaEvent :: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent). Étant donné que plusieurs événements peuvent se trouver dans la file d’attente d’événements à un moment donné, l’application doit appeler **GetEvent** dans une boucle qui se répète jusqu’à ce que tous les événements en file d’attente aient été récupérés, comme illustré dans l’exemple de code suivant.


```C++
while (SUCCEEDED(m_pIME->GetEvent(&lEvent, &lParam1, &lParam2, lTimeOut)))
{
    HRESULT hr;
    switch (lEvent)
    {

    case EC_DVD_CURRENT_HMSF_TIME:
        {
            DVD_HMSF_TIMECODE *pTC = reinterpret_cast<DVD_HMSF_TIMECODE *>(&lParam1);
            m_CurTime = *pTC;
            ...
        }
        break;
        ...
    } // switch
}
```



Les événements DVD peuvent contenir des informations supplémentaires dans les paramètres *lParam1* ou *lParam2* , comme illustré ci-dessus, où l’heure actuelle est contenue dans *lParam1*. L’exemple de code précédent provient de l’exemple d’application de DVD dans Dvdcore. cpp. Pour obtenir la liste complète de tous les événements DVD et de leurs paramètres, consultez [codes de notification d’événement DVD](dvd-notification-codes.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Applications DVD](dvd-applications.md)
</dt> </dl>

 

 



