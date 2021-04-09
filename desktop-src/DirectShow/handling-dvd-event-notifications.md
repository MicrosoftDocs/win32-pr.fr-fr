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
# <a name="handling-dvd-event-notifications"></a><span data-ttu-id="30593-103">Gestion des notifications d’événements DVD</span><span class="sxs-lookup"><span data-stu-id="30593-103">Handling DVD Event Notifications</span></span>

<span data-ttu-id="30593-104">Le navigateur DVD envoie des notifications à une fenêtre spécifiée par l’application lorsque certains événements se produisent, par exemple lorsque le domaine du DVD change, lorsqu’un nouveau niveau de gestion parental est rencontré et lorsque le navigateur DVD est sur le point d’entrer dans un bloc d’angle.</span><span class="sxs-lookup"><span data-stu-id="30593-104">The DVD Navigator sends notifications to an application-specified window when certain events take place, such as when the DVD domain changes, when a new parental management level is encountered, and when the DVD Navigator is about to enter an angle block.</span></span> <span data-ttu-id="30593-105">Les paramètres d’événement peuvent contenir des informations supplémentaires relatives à l’événement.</span><span class="sxs-lookup"><span data-stu-id="30593-105">The event parameters can contain additional information related to the event.</span></span> <span data-ttu-id="30593-106">Les messages d’erreur et les avertissements sont également envoyés de cette façon.</span><span class="sxs-lookup"><span data-stu-id="30593-106">Error messages and warnings are also sent in this way.</span></span> <span data-ttu-id="30593-107">L’application spécifie la fenêtre qui gérera les notifications d’événements à l’aide du pointeur [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) pour appeler [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow), comme suit :</span><span class="sxs-lookup"><span data-stu-id="30593-107">The application specifies the window that will handle the event notifications by using the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) pointer to call [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow), as follows:</span></span>


```C++
const DWORD WM_DVD_EVENT = WM_USER + 100;
hr = m_pIME->SetNotifyWindow(reinterpret_cast<OAHWND>(m_hWnd), WM_DVD_EVENT, 0);
```



<span data-ttu-id="30593-108">Dans l’exemple précédent, m \_ HWND est le HWND de la fenêtre qui reçoit les messages et l' \_ événement de DVD WM \_ est le message défini par l’application (supérieur à l' \_ utilisateur WM) qui signale qu’un événement DVD a eu lieu.</span><span class="sxs-lookup"><span data-stu-id="30593-108">In the preceding example, m\_hWnd is the HWND of the window to receive the messages and WM\_DVD\_EVENT is the application-defined message (greater than WM\_USER) that will signal that a DVD event has taken place.</span></span> <span data-ttu-id="30593-109">L’événement lui-même est récupéré par l’application via un appel à [**IMediaEvent :: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent).</span><span class="sxs-lookup"><span data-stu-id="30593-109">The event itself is retrieved by the application through a call to [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent).</span></span> <span data-ttu-id="30593-110">Étant donné que plusieurs événements peuvent se trouver dans la file d’attente d’événements à un moment donné, l’application doit appeler **GetEvent** dans une boucle qui se répète jusqu’à ce que tous les événements en file d’attente aient été récupérés, comme illustré dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="30593-110">Because more than one event might be in the event queue at any given time, the application must call **GetEvent** within a loop that repeats until all queued events have been retrieved, as shown in the following code example.</span></span>


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



<span data-ttu-id="30593-111">Les événements DVD peuvent contenir des informations supplémentaires dans les paramètres *lParam1* ou *lParam2* , comme illustré ci-dessus, où l’heure actuelle est contenue dans *lParam1*.</span><span class="sxs-lookup"><span data-stu-id="30593-111">DVD events might contain additional information in the *lParam1* or *lParam2* parameters, as illustrated above where the current time is contained in *lParam1*.</span></span> <span data-ttu-id="30593-112">L’exemple de code précédent provient de l’exemple d’application de DVD dans Dvdcore. cpp.</span><span class="sxs-lookup"><span data-stu-id="30593-112">The preceding code example is from the DVD sample application in Dvdcore.cpp.</span></span> <span data-ttu-id="30593-113">Pour obtenir la liste complète de tous les événements DVD et de leurs paramètres, consultez [codes de notification d’événement DVD](dvd-notification-codes.md).</span><span class="sxs-lookup"><span data-stu-id="30593-113">For a complete list of all DVD events and their parameters, see [DVD Event Notification Codes](dvd-notification-codes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="30593-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="30593-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30593-115">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="30593-115">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



