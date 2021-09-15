---
title: Comment déclencher des événements à partir d’un fournisseur UI Automation
description: Cette rubrique contient un exemple de code qui montre comment un fournisseur UI Automation Microsoft déclenche un événement.
ms.assetid: 43826258-9321-4d44-bd31-6a3b42f00d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417c86771c24cc1a67fd907aaf0628037edce44d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518129"
---
# <a name="how-to-raise-events-from-a-ui-automation-provider"></a>Comment déclencher des événements à partir d’un fournisseur UI Automation

Cette rubrique contient un exemple de code qui montre comment un fournisseur UI Automation Microsoft déclenche un événement.

L’exemple de code suivant montre une méthode d’une application qui implémente un bouton personnalisé. L’application appelle la méthode chaque fois que le bouton personnalisé est appelé. La méthode vérifie si des clients écoutent des événements et, le cas échéant, déclenche l’événement [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md) pour informer les clients que le bouton a été appelé.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Conceptuel**
</dt> <dt>

[Vue d'ensemble des événements UI Automation](uiauto-eventsoverview.md)
</dt> <dt>

[Rubriques de procédures pour les fournisseurs UI Automation](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




