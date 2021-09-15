---
title: Création d'un service
description: La création d’un service Web est considérablement simplifiée dans WWSAPI par l’API de modèle de service et l’outil de WsUtil.exe.
ms.assetid: 3536d1c6-6179-4f69-9cc8-27fe6ae30826
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4700324a84962047f403ca7ad090adc3e9f4e99
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520961"
---
# <a name="creating-a-service"></a>Création d'un service

La création d’un service Web est considérablement simplifiée dans WWSAPI par l’API de [modèle de service](service-model-layer-overview.md) et l’outil de [WsUtil.exe](wsutil-compiler-tool.md) . Le modèle de service fournit une API qui permet au service et au client d’envoyer et de recevoir des [messages](message.md) sur un [canal](channel.md) en tant qu’appels de méthode C. L’outil WsUtil génère des stubs et des en-têtes pour l’implémentation du service.

## <a name="implementing-a-calculator-service-using-wwsapi"></a>Implémentation d’un service de calculatrice à l’aide de WWSAPI

À l’aide des sources générées à partir de l’outil [Wsutil.exe](wsutil-compiler-tool.md) , implémentez le service en procédant comme suit.

Incluez les en-têtes dans la source de votre application.

``` syntax
#include "CalculatorProxyStub.h"
```

Implémentez les opérations de service. Dans cet exemple, les opérations de service sont les fonctions d’ajout et de soustraction du service de calculatrice.

``` syntax
HRESULT CALLBACK Add (const WS_OPERATION_CONTEXT* context, 
                  int a, int b, int* result, 
                  const WS_ASYNC_CONTEXT* asyncContext, 
                  WS_ERROR* error)
{
    *result = a + b;
    printf ("%d + %d = %d\n", a, b, *result);
    return NOERROR;
}

HRESULT CALLBACK Subtract (const WS_OPERATION_CONTEXT* context, 
                  int a, int b, int* result, 
                  const WS_ASYNC_CONTEXT* asyncContext, 
                  WS_ERROR* error)
{
    *result = a - b;
    printf ("%d - %d = %d\n", a, b, *result);
    return NOERROR;
}
```

Définissez le contrat de service en définissant les champs d’une structure de [**\_ \_ contrat de service WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) .

``` syntax
static const DefaultBinding_ICalculatorFunctionTable calculatorFunctions = {Add, Subtract};
static const WS_SERVICE_CONTRACT calculatorContract = 
{
    &DefaultBinding_ICalculatorContractDesc, // comes from the generated header.
    NULL, // for not specifying the default contract
    &calculatorFunctions // specified by the user
};
```

À présent, créez un hôte de service et ouvrez-le pour la communication.

``` syntax
WS_SERVICE_ENDPOINT serviceEndpoint = {0};
serviceEndpoint.uri.chars = L"https://+:80/example"; // address given as uri
serviceEndpoint.binding.channelBinding =  WS_HTTP_CHANNEL_BINDING; // channel binding for the endpoint
serviceEndpoint.channelType = WS_CHANNEL_TYPE_REPLY; // the channel type
serviceEndpoint.uri.length = (ULONG)wcslen(serviceEndpoint.uri.chars);
serviceEndpoint.contract = (WS_SERVICE_CONTRACT*)&calculatorContract;  // the contract
serviceEndpoint.properties = serviceProperties;
serviceEndpoint.propertyCount = WsCountOf(serviceProperties);

if (FAILED (hr = WsCreateServiceHost (&serviceEndpoint, 1, NULL, 0, &host, error)))
    goto Error;

// WsOpenServiceHost  to start the listeners in the service host 
if (FAILED (hr = WsOpenServiceHost (host, NULL, error)))
    goto Error;
```

Reportez-vous à l’exemple de code sur [HttpCalculatorServiceExample](httpcalculatorserviceexample.md) pour une implémentation complète du service de calculatrice.

 

 




