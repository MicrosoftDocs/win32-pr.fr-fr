---
description: L’exemple de code suivant illustre la création d’un appel de conférence simple. Pour plus d’informations sur la vidéoconférence multidiffusion multimédia IP, consultez à propos de la Conférence de téléphonie IP Rendezvous.
ms.assetid: fb55853d-b882-41c8-99e6-bfa897b2dabf
title: Créer une conférence simple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aa0bfd8fede9fa61aedb6b630a2451803e2257d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518780"
---
# <a name="create-a-simple-conference"></a>Créer une conférence simple

L’exemple de code suivant illustre la création d’un appel de conférence simple. Pour plus d’informations sur la vidéoconférence multidiffusion multimédia IP, consultez [à propos de la Conférence de téléphonie IP Rendezvous](about-rendezvous-ip-telephony-conferencing.md).

Avant d’utiliser cet exemple de code, un appel doit être en cours et vous devez effectuer les opérations dans [effectuer un appel](make-a-call.md) ou [recevoir un appel](receive-a-call.md) .

> [!Note]  
> Cet exemple ne dispose pas de la vérification des erreurs et des versions appropriées pour le code de production.

 

``` syntax
// From elsewhere in your code, you have obtained pBasicCall and pCallInfo, 
// which are pointers to the ITBasicCallControl and ITCallInfo interfaces
// of a call currently in progress. pAddress is an ITAddress pointer.

// Create a consultation call for the conference.
ITBasicCallControl *pConsultCall;
HRESULT hr = pAddress->CreateCall(
        bstrAddressToCall,
        dwAddressType,
        &pConsultCall
        );
// If ( hr != S_OK ) process the error here. 

// Move the consultation call into your conference.
// Note: If a CallHub object does not already exist, TAPI will create it.
hr = pBasicCall->Conference(
               pConsultCall,
               VARIANT_TRUE
               );
// If ( hr != S_OK ) process the error here. 

// Finish the creation of the conference.
hr = pConsultCall->Finish(FM_ASCONFERENCE);
// If ( hr != S_OK ) process the error here. 

// Assuming the Finish method succeeds, the consultation call (pConsultCall)
// may transition to the CS_DISCONNECTED state or may remain connected, 
// depending on the service provider.
//
// Get the ITCallHub interface pointer.
ITCallHub *pCallHub;
hr = pCallInfo->get_CallHub( pCallHub );
// If ( hr != S_OK ) process the error here. 

// You can use the ITCallHub interface to obtain additional information on
// the conference. Specific capabilities depend on the TSP/MSP being used.
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[**ITCallHub**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub)
</dt> </dl>

 

 



