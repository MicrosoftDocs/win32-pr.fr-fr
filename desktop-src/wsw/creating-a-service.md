---
title: Création d'un service
description: La création d’un service Web est considérablement simplifiée dans WWSAPI par l’API de modèle de service et l’outil de WsUtil.exe.
ms.assetid: 3536d1c6-6179-4f69-9cc8-27fe6ae30826
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4700324a84962047f403ca7ad090adc3e9f4e99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840781"
---
# <a name="creating-a-service"></a><span data-ttu-id="b544c-103">Création d'un service</span><span class="sxs-lookup"><span data-stu-id="b544c-103">Creating a Service</span></span>

<span data-ttu-id="b544c-104">La création d’un service Web est considérablement simplifiée dans WWSAPI par l’API de [modèle de service](service-model-layer-overview.md) et l’outil de [WsUtil.exe](wsutil-compiler-tool.md) .</span><span class="sxs-lookup"><span data-stu-id="b544c-104">Creating a Web service is greatly simplified in WWSAPI by the [Service Model](service-model-layer-overview.md) API and the [WsUtil.exe](wsutil-compiler-tool.md) tool.</span></span> <span data-ttu-id="b544c-105">Le modèle de service fournit une API qui permet au service et au client d’envoyer et de recevoir des [messages](message.md) sur un [canal](channel.md) en tant qu’appels de méthode C.</span><span class="sxs-lookup"><span data-stu-id="b544c-105">The Service Model provides an API that enables the service and client to send and receive [messages](message.md) over a [channel](channel.md) as C method calls.</span></span> <span data-ttu-id="b544c-106">L’outil WsUtil génère des stubs et des en-têtes pour l’implémentation du service.</span><span class="sxs-lookup"><span data-stu-id="b544c-106">The WsUtil tool generates stubs and headers for implementing the service.</span></span>

## <a name="implementing-a-calculator-service-using-wwsapi"></a><span data-ttu-id="b544c-107">Implémentation d’un service de calculatrice à l’aide de WWSAPI</span><span class="sxs-lookup"><span data-stu-id="b544c-107">Implementing a Calculator Service using WWSAPI</span></span>

<span data-ttu-id="b544c-108">À l’aide des sources générées à partir de l’outil [Wsutil.exe](wsutil-compiler-tool.md) , implémentez le service en procédant comme suit.</span><span class="sxs-lookup"><span data-stu-id="b544c-108">Using the generated sources from the [Wsutil.exe](wsutil-compiler-tool.md) tool, implement the service by the following steps.</span></span>

<span data-ttu-id="b544c-109">Incluez les en-têtes dans la source de votre application.</span><span class="sxs-lookup"><span data-stu-id="b544c-109">Include the headers in your application source.</span></span>

``` syntax
#include "CalculatorProxyStub.h"
```

<span data-ttu-id="b544c-110">Implémentez les opérations de service.</span><span class="sxs-lookup"><span data-stu-id="b544c-110">Implement the service operations.</span></span> <span data-ttu-id="b544c-111">Dans cet exemple, les opérations de service sont les fonctions d’ajout et de soustraction du service de calculatrice.</span><span class="sxs-lookup"><span data-stu-id="b544c-111">In this example, the service operations are the Add and Subtract functions of the calculator service.</span></span>

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

<span data-ttu-id="b544c-112">Définissez le contrat de service en définissant les champs d’une structure de [**\_ \_ contrat de service WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) .</span><span class="sxs-lookup"><span data-stu-id="b544c-112">Define the service contract by setting the fields of a [**WS\_SERVICE\_CONTRACT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) structure.</span></span>

``` syntax
static const DefaultBinding_ICalculatorFunctionTable calculatorFunctions = {Add, Subtract};
static const WS_SERVICE_CONTRACT calculatorContract = 
{
    &DefaultBinding_ICalculatorContractDesc, // comes from the generated header.
    NULL, // for not specifying the default contract
    &calculatorFunctions // specified by the user
};
```

<span data-ttu-id="b544c-113">À présent, créez un hôte de service et ouvrez-le pour la communication.</span><span class="sxs-lookup"><span data-stu-id="b544c-113">Now, create a service host and open it for communication.</span></span>

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

<span data-ttu-id="b544c-114">Reportez-vous à l’exemple de code sur [HttpCalculatorServiceExample](httpcalculatorserviceexample.md) pour une implémentation complète du service de calculatrice.</span><span class="sxs-lookup"><span data-stu-id="b544c-114">Please refer to the code example at [HttpCalculatorServiceExample](httpcalculatorserviceexample.md) for a full implementation of the calculator service.</span></span>

 

 




