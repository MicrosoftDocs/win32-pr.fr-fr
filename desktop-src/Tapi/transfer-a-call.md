---
description: L’exemple de code suivant illustre un transfert d’appel.
ms.assetid: 05862605-2600-4cdf-8390-e24e4e8586f3
title: Transférer un appel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e71d6e6fd9dc275a6d4c00e84806132cabf756effcb41e7a704b20929bc46d1a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072829"
---
# <a name="transfer-a-call"></a>Transférer un appel

L’exemple de code suivant illustre un transfert d’appel.

Avant d’utiliser cet exemple de code, un appel doit être en cours et vous devez effectuer les opérations dans [effectuer un appel](make-a-call.md) ou [recevoir un appel](receive-a-call.md).

> [!Note]  
> Cet exemple ne dispose pas de la vérification des erreurs et des versions appropriées pour le code de production.

 

``` syntax
// From elsewhere in your code, you have obtained pAddress and pBasicCall, 
// which are pointers to the ITAddress and ITBasicCallControl interfaces
// of the call in progress that will be transferred.

// Create the call object for transfer. bstrAddressToCall and dwAddressType
// have been retrieved from a UI.
ITBasicCallControl * pConsultCall
HRESULT hr = pAddress->CreateCall(
        bstrAddressToCall,
        dwAddressType,
        &pConsultCall
        );
// If ( hr != S_OK ) process the error here. 

// Start the transfer.
hr = pBasicCall->Transfer(
        pConsultCall,
        VARIANT_TRUE
        );
// If ( hr != S_OK ) process the error here. 

// Depending on the service provider, additional operations may be available
// or required.

// Finish the transfer.
hr = pConsultCall->Finish(FM_ASTRANSFER);
// If ( hr != S_OK ) process the error here. 

// The consultation call transitions to CS_DISCONNECTED.
// The objects associated with pConsultCall and pBasicCall can be released immediately or
// used for information purposes and released later.
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[**ITCallHub**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub)
</dt> </dl>

 

 



