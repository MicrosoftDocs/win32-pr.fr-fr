---
title: Comment déclencher des événements à partir d’un fournisseur UI Automation
description: Cette rubrique contient un exemple de code qui montre comment un fournisseur UI Automation Microsoft déclenche un événement.
ms.assetid: 43826258-9321-4d44-bd31-6a3b42f00d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417c86771c24cc1a67fd907aaf0628037edce44d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106513486"
---
# <a name="how-to-raise-events-from-a-ui-automation-provider"></a><span data-ttu-id="fd7cb-103">Comment déclencher des événements à partir d’un fournisseur UI Automation</span><span class="sxs-lookup"><span data-stu-id="fd7cb-103">How to Raise Events from a UI Automation Provider</span></span>

<span data-ttu-id="fd7cb-104">Cette rubrique contient un exemple de code qui montre comment un fournisseur UI Automation Microsoft déclenche un événement.</span><span class="sxs-lookup"><span data-stu-id="fd7cb-104">This topic contains example code that shows how a Microsoft UI Automation provider raises an event.</span></span>

<span data-ttu-id="fd7cb-105">L’exemple de code suivant montre une méthode d’une application qui implémente un bouton personnalisé.</span><span class="sxs-lookup"><span data-stu-id="fd7cb-105">The following example code shows a method from an application that implements a custom button.</span></span> <span data-ttu-id="fd7cb-106">L’application appelle la méthode chaque fois que le bouton personnalisé est appelé.</span><span class="sxs-lookup"><span data-stu-id="fd7cb-106">The application calls the method whenever the custom button is invoked.</span></span> <span data-ttu-id="fd7cb-107">La méthode vérifie si des clients écoutent des événements et, le cas échéant, déclenche l’événement [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md) pour informer les clients que le bouton a été appelé.</span><span class="sxs-lookup"><span data-stu-id="fd7cb-107">The method checks whether any clients are listening for events and, if so, raises the [**UIA\_Invoke\_InvokedEventId**](uiauto-event-ids.md) event to notify the clients that the button was invoked.</span></span>


```C++
// Responds to a button click. The source of the click could 
// be the mouse, the keyboard, or a client's call to 
// IUIAutomationInvokePattern::Invoke.
void CustomButton::InvokeButton(HWND hwnd)
{
    // TODO: Perform program actions invoked by the control.

    // Check whether any clients are listening for UI Automation 
    // events.
    if (UiaClientsAreListening())
    {
        // Raise an Invoked event. GetUIAutomationProvider is an
        // application-defined method that returns a pointer to
        // the application's IRawElementProviderSimple interface.
        UiaRaiseAutomationEvent(
            GetUIAutomationProvider(hwnd), UIA_Invoke_InvokedEventId); 
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="fd7cb-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fd7cb-108">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="fd7cb-109">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="fd7cb-109">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fd7cb-110">Vue d'ensemble des événements UI Automation</span><span class="sxs-lookup"><span data-stu-id="fd7cb-110">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> <dt>

[<span data-ttu-id="fd7cb-111">Rubriques de procédures pour les fournisseurs UI Automation</span><span class="sxs-lookup"><span data-stu-id="fd7cb-111">How-To Topics for UI Automation Providers</span></span>](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




