---
description: L’exemple de code suivant montre comment créer un objet d’appel, découvrir les flux associés à l’appel, sélectionner et créer les terminaux appropriés, sélectionner les terminaux sur les flux et terminer la connexion.
ms.assetid: 49815b18-a8ea-46e0-b2a4-3d7a82e727b0
title: Effectuer un appel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc22ebde34e65c9acc8e6c7dd81944b06804935
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544774"
---
# <a name="make-a-call"></a>Effectuer un appel

L’exemple de code suivant montre comment créer un objet d’appel, découvrir les flux associés à l’appel, sélectionner et créer les terminaux appropriés, sélectionner les terminaux sur les flux et terminer la connexion.

Avant d’utiliser cet exemple de code, vous devez effectuer les opérations dans [initialiser TAPI](initialize-tapi.md) et [Sélectionner une adresse](select-an-address.md).

En outre, vous devez effectuer les opérations illustrées dans [Sélectionner un terminal](select-a-terminal.md) après l’appel à [**ITAddress :: createCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall).

> [!Note]  
> Cet exemple ne dispose pas de la vérification des erreurs et des versions appropriées pour le code de production.

 

``` syntax
// Specify the destination address.
//
// szAddressToCall and 
// dwAddressType have been
// retrieved from a user interface.
ITBasicCallControl * pBasicCall
bstrAddressToCall = SysAllocString( szAddressToCall );
// If ( bstrAddressToCall == NULL ) process the error here. 

HRESULT hr = pAddress->CreateCall(
    bstrAddressToCall,
    dwAddressType,
    &pBasicCall
 );
// If ( hr != S_OK ) process the error here. 

SysFreeString(bstrAddressToCall);

// Create the required terminals for this call.
{
    // See the Select a Terminal code example.
}

// Make the connection.
pBasicCall->Connect( TRUE );
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ITAddress::CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall)
</dt> <dt>

[**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[**ITBasicCallControl :: Connect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect)
</dt> </dl>

 

 



