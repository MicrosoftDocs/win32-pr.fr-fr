---
description: Le processus d’inscription des événements a lieu lorsque le terminal est sélectionné par un flux.
ms.assetid: 03854b38-4dba-480e-b931-34299d04c551
title: Inscription pour les événements de terminal enfichables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d42bf75cfd0d7e6bd4d8a2520335c374cce28c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869197"
---
# <a name="registering-for-pluggable-terminal-events"></a><span data-ttu-id="09966-103">Inscription pour les événements de terminal enfichables</span><span class="sxs-lookup"><span data-stu-id="09966-103">Registering for Pluggable Terminal Events</span></span>

<span data-ttu-id="09966-104">Le processus d’inscription des événements a lieu lorsque le terminal est sélectionné par un flux.</span><span class="sxs-lookup"><span data-stu-id="09966-104">The event registration process take place when the terminal is selected by a stream.</span></span> <span data-ttu-id="09966-105">Dans l’implémentation de la méthode [**SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal) de l’application Terminal, nous pouvons utiliser l’interface [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) du terminal attaché au flux, puis appeler **QueryInterface** pour trouver [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration).</span><span class="sxs-lookup"><span data-stu-id="09966-105">In the terminal application's implementation of the [**SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal) method, we can use the [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interface of the terminal that was attached to the stream, and call **QueryInterface** to find [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration).</span></span>

``` syntax
HRESULT hr = E_FAIL;
ITPluggableTerminalEventSinkRegistration* pEventRegistration = NULL;
hr = pTerminal->QueryInterface( 
    IID_ITPluggableTerminalEventSinkRegistration,
    (void**)& pEventRegistration
);
```

<span data-ttu-id="09966-106">Si l’appel **QueryInterface** se déroule correctement, nous pouvons appeler la méthode [**RegisterSink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-registersink) .</span><span class="sxs-lookup"><span data-stu-id="09966-106">If the **QueryInterface** call succeeds, we can call the [**RegisterSink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-registersink) method.</span></span> <span data-ttu-id="09966-107">À cet effet, nous devons créer un objet qui implémente l’interface [**ITPluggableTerminalEventSink**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink) .</span><span class="sxs-lookup"><span data-stu-id="09966-107">For this purpose, we should create an object that implements the [**ITPluggableTerminalEventSink**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink) interface.</span></span> <span data-ttu-id="09966-108">Nous transmettons cette interface en tant que paramètre de la méthode **RegisterSink** .</span><span class="sxs-lookup"><span data-stu-id="09966-108">We pass this interface as a parameter of the **RegisterSink** method.</span></span>

``` syntax
ITPluggableTerminalEventSink*    pEventSink;

HRESULT hr = CreateEventSink( &pEventSink);
// If (hr != S_OK) process the error here. 

hr = pEventRegistration->RegisterSink( pEventSink );
// If (hr != S_OK) process the error here. 
```

<span data-ttu-id="09966-109">Le terminal qui implémente l’appel [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration) stocke l’interface.</span><span class="sxs-lookup"><span data-stu-id="09966-109">The terminal that implements the [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration) call will store the interface.</span></span> <span data-ttu-id="09966-110">Le pointeur sera utilisé lorsque le terminal déclenchera un événement.</span><span class="sxs-lookup"><span data-stu-id="09966-110">The pointer will be used when the terminal will fire an event.</span></span>

<span data-ttu-id="09966-111">Le récepteur d’événements peut être désinscrit à l’aide de [**UnregisterSink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-unregistersink).</span><span class="sxs-lookup"><span data-stu-id="09966-111">The event sink can be unregistered using [**UnregisterSink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-unregistersink).</span></span>

``` syntax
hr = pEventRegistration->UnregisterSink();
// If (hr != S_OK) process the error here.
```

 

 
