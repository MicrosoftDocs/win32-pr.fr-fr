---
description: L’exemple de code suivant illustre un transfert d’appel.
ms.assetid: 05862605-2600-4cdf-8390-e24e4e8586f3
title: Transférer un appel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd1d537efd33ea2df4ddb9ad3e9b55b633cca18f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528261"
---
# <a name="transfer-a-call"></a><span data-ttu-id="c8cc8-103">Transférer un appel</span><span class="sxs-lookup"><span data-stu-id="c8cc8-103">Transfer a Call</span></span>

<span data-ttu-id="c8cc8-104">L’exemple de code suivant illustre un transfert d’appel.</span><span class="sxs-lookup"><span data-stu-id="c8cc8-104">The following code example demonstrates a call transfer.</span></span>

<span data-ttu-id="c8cc8-105">Avant d’utiliser cet exemple de code, un appel doit être en cours et vous devez effectuer les opérations dans [effectuer un appel](make-a-call.md) ou [recevoir un appel](receive-a-call.md).</span><span class="sxs-lookup"><span data-stu-id="c8cc8-105">Before using this code example, a call must be in progress, and you must perform the operations in [Make a Call](make-a-call.md) or [Receive a Call](receive-a-call.md).</span></span>

> [!Note]  
> <span data-ttu-id="c8cc8-106">Cet exemple ne dispose pas de la vérification des erreurs et des versions appropriées pour le code de production.</span><span class="sxs-lookup"><span data-stu-id="c8cc8-106">This example does not have the error checking and releases appropriate for production code.</span></span>

 

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

## <a name="related-topics"></a><span data-ttu-id="c8cc8-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c8cc8-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8cc8-108">**ITCallInfo**</span><span class="sxs-lookup"><span data-stu-id="c8cc8-108">**ITCallInfo**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[<span data-ttu-id="c8cc8-109">**ITBasicCallControl**</span><span class="sxs-lookup"><span data-stu-id="c8cc8-109">**ITBasicCallControl**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[<span data-ttu-id="c8cc8-110">**ITCallHub**</span><span class="sxs-lookup"><span data-stu-id="c8cc8-110">**ITCallHub**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub)
</dt> </dl>

 

 



