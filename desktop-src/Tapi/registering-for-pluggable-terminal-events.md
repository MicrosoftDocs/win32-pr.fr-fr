---
description: Le processus d’inscription des événements a lieu lorsque le terminal est sélectionné par un flux.
ms.assetid: 03854b38-4dba-480e-b931-34299d04c551
title: Inscription pour les événements de terminal enfichables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c71993d597cbcba7c634068813eb14939539dc7e7d43cda0105e8cf9ee615a1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060457"
---
# <a name="registering-for-pluggable-terminal-events"></a>Inscription pour les événements de terminal enfichables

Le processus d’inscription des événements a lieu lorsque le terminal est sélectionné par un flux. Dans l’implémentation de la méthode [**SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal) de l’application Terminal, nous pouvons utiliser l’interface [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) du terminal attaché au flux, puis appeler **QueryInterface** pour trouver [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration).

``` syntax
HRESULT hr = E_FAIL;
ITPluggableTerminalEventSinkRegistration* pEventRegistration = NULL;
hr = pTerminal->QueryInterface( 
    IID_ITPluggableTerminalEventSinkRegistration,
    (void**)& pEventRegistration
);
```

Si l’appel **QueryInterface** se déroule correctement, nous pouvons appeler la méthode [**RegisterSink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-registersink) . À cet effet, nous devons créer un objet qui implémente l’interface [**ITPluggableTerminalEventSink**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink) . Nous transmettons cette interface en tant que paramètre de la méthode **RegisterSink** .

``` syntax
ITPluggableTerminalEventSink*    pEventSink;

HRESULT hr = CreateEventSink( &pEventSink);
// If (hr != S_OK) process the error here. 

hr = pEventRegistration->RegisterSink( pEventSink );
// If (hr != S_OK) process the error here. 
```

Le terminal qui implémente l’appel [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration) stocke l’interface. Le pointeur sera utilisé lorsque le terminal déclenchera un événement.

Le récepteur d’événements peut être désinscrit à l’aide de [**UnregisterSink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-unregistersink).

``` syntax
hr = pEventRegistration->UnregisterSink();
// If (hr != S_OK) process the error here.
```

 

 
