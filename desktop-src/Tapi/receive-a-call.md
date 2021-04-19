---
description: L’exemple de code suivant illustre la gestion des nouvelles notifications d’appel, telles que la recherche ou la création de terminaux appropriés pour le rendu du média.
ms.assetid: 77f6e1b5-b60e-4e8d-b747-7eceae8b0611
title: Recevoir un appel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6a78ebf5b77569f8468a8b2c0a30217f4f7430e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521948"
---
# <a name="receive-a-call"></a>Recevoir un appel

L’exemple de code suivant illustre la gestion des nouvelles notifications d’appel, telles que la recherche ou la création de terminaux appropriés pour le rendu du média. Cet exemple est une partie de l’instruction switch qu’une application doit implémenter pour la gestion des événements. Le code lui-même peut être contenu dans l’implémentation de [**ITTAPIEventNotification :: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event), ou la méthode d' **événement** peut poster un message vers un thread de travail qui contient le commutateur.

Avant d’utiliser cet exemple de code, vous devez effectuer les opérations dans [initialiser l’interface TAPI](initialize-tapi.md), [Sélectionner une adresse](select-an-address.md)et [inscrire des événements](register-events.md).

En outre, vous devez effectuer les opérations illustrées dans [Sélectionner un terminal](select-a-terminal.md) en suivant la récupération des pointeurs d’interface [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) et [**ITAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress) .

> [!Note]  
> Cet exemple ne dispose pas de la vérification des erreurs et des versions appropriées pour le code de production.

 

``` syntax
// pEvent is an IDispatch pointer for the ITCallNotificationEvent interface of the
// call object created by TAPI, and is passed into the event handler by TAPI. 

case TE_CALLNOTIFICATION:
{
    // Get the ITCallNotification interface.
    ITCallNotificationEvent * pNotify;
    hr = pEvent->QueryInterface( 
            IID_ITCallNotificationEvent, 
            (void **)&pNotify 
            );
    // If ( hr != S_OK ) process the error here. 
    
    // Get the ITCallInfo interface.
    ITCallInfo * pCallInfo;
    hr = pNotify->get_Call( &pCallInfo);
    // If ( hr != S_OK ) process the error here. 

    // Get the ITBasicCallControl interface.
    ITBasicCallControl * pBasicCall;
    hr = pCallInfo->QueryInterface(
            IID_ITBasicCallControl,
            (void**)&pBasicCall
            );
    // If ( hr != S_OK ) process the error here. 

    // Get the ITAddress interface.
    ITAddress * pAddress;
    hr = pCallInfo->get_Address( &pAddress );
    // If ( hr != S_OK ) process the error here. 

    // Create the required terminals for this call.
    {
        // See the Select a Terminal code example.
    }
    // Complete incoming call processing.
    hr = pBasicCall->Answer();
    // If ( hr != S_OK ) process the error here. 
}
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Événements](events.md)
</dt> <dt>

[**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification)
</dt> <dt>

[**ITTAPI::RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications)
</dt> <dt>

[**ITCallNotificationEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent)
</dt> <dt>

[**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)
</dt> </dl>

 

 
