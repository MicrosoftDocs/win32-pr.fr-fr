---
title: Création d’un client
description: La création d’un client pour les services Web est considérablement simplifiée dans WWSAPI par l’API de modèle de service et l’outil WsUtil.exe.
ms.assetid: 09f489e8-958d-4bc5-a232-aa59bd75333a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606a68f574a9ad79d15f3ddd48247f93a5414250
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380376"
---
# <a name="creating-a-client"></a><span data-ttu-id="73978-103">Création d’un client</span><span class="sxs-lookup"><span data-stu-id="73978-103">Creating a Client</span></span>

<span data-ttu-id="73978-104">La création d’un client pour les services Web est considérablement simplifiée dans WWSAPI par l’API de [modèle de service](service-model-layer-overview.md) et l’outil [WsUtil.exe](wsutil-compiler-tool.md) .</span><span class="sxs-lookup"><span data-stu-id="73978-104">Creating a client for Web services is greatly simplified in WWSAPI by the [Service Model](service-model-layer-overview.md) API and the [WsUtil.exe](wsutil-compiler-tool.md) tool.</span></span> <span data-ttu-id="73978-105">Le modèle de service fournit une API qui permet au client d’envoyer et de recevoir des [messages](message.md) sur un [canal](channel.md) en tant qu’appels de méthode C.</span><span class="sxs-lookup"><span data-stu-id="73978-105">The Service Model provides an API that enables the client to send and receive [messages](message.md) over a [channel](channel.md) as C method calls.</span></span> <span data-ttu-id="73978-106">L’outil WsUtil génère des en-têtes et des assistances pour l’implémentation du client.</span><span class="sxs-lookup"><span data-stu-id="73978-106">The WsUtil tool generates headers and helpers for implementing the client.</span></span> <span data-ttu-id="73978-107">Ces en-têtes incluent les types et les prototypes de fonction pour les fonctions C représentant les services offerts par le service Web cible.</span><span class="sxs-lookup"><span data-stu-id="73978-107">These headers include the types and function prototypes for C functions representing the services offered by the target Web service.</span></span> <span data-ttu-id="73978-108">Les applications auxiliaires sont utilisées pour créer le proxy de service, qui contient les informations de liaison et l' [adresse de point de terminaison](endpoint-address.md) pour le service.</span><span class="sxs-lookup"><span data-stu-id="73978-108">The helpers are used to create the service proxy, which contains the binding information and [endpoint address](endpoint-address.md) for the service.</span></span>

## <a name="using-wsutil-to-generate-headers-and-helpers"></a><span data-ttu-id="73978-109">Utilisation de WsUtil pour générer des en-têtes et des assistances</span><span class="sxs-lookup"><span data-stu-id="73978-109">Using WsUtil to Generate Headers and Helpers</span></span>

<span data-ttu-id="73978-110">Pour générer les en-têtes et les aiders, WsUtil ouvre et lit les fichiers de métadonnées du service cible (fichiers WSDL et XSD) et les convertit en en-têtes. par conséquent, il est nécessaire de récupérer les fichiers de métadonnées pour le service cible à l’avance, par exemple à l’aide de SvcUtil, une partie du Windows Communication Foundation.</span><span class="sxs-lookup"><span data-stu-id="73978-110">To generate the headers and helpers, WsUtil opens and reads the metadata files for the target service — wsdl and xsd files— and converts them into headers; therefore, it is necessary to retrieve the metadata files for the target service in advance, for example by using SvcUtil, a part of the Windows Communication Foundation.</span></span> <span data-ttu-id="73978-111">Pour des raisons de sécurité, il est impératif que vos copies de ces fichiers soient dignes de confiance.</span><span class="sxs-lookup"><span data-stu-id="73978-111">For security reasons, it is imperative that your copies of these files are trustworthy.</span></span> <span data-ttu-id="73978-112">(Pour plus d’informations, consultez la section « sécurité » de la rubrique de l' [outil compilateur WsUtil](wsutil-compiler-tool.md) .)</span><span class="sxs-lookup"><span data-stu-id="73978-112">(For more information, see the "Security" section of the [WsUtil Compiler Tool](wsutil-compiler-tool.md) topic.)</span></span>

<span data-ttu-id="73978-113">Pour exécuter WsUtil, utilisez la syntaxe de ligne de commande suivante si les fichiers WSDL et XSD du service se trouvent dans leur propre répertoire : `WsUtil.exe *.wsdl *.xsd` .</span><span class="sxs-lookup"><span data-stu-id="73978-113">To run WsUtil, use the following command-line syntax if the WSDL and XSD files for the service are in their own directory: `WsUtil.exe *.wsdl *.xsd`.</span></span> <span data-ttu-id="73978-114">Vous pouvez également spécifier les fichiers par nom complet.</span><span class="sxs-lookup"><span data-stu-id="73978-114">Alternatively, you can specify the files by full name.</span></span>

<span data-ttu-id="73978-115">WsUtil génère généralement deux fichiers pour chaque fichier de métadonnées : un en-tête et un fichier C.</span><span class="sxs-lookup"><span data-stu-id="73978-115">WsUtil generally generates two files for each metadata file: a header and a C file.</span></span> <span data-ttu-id="73978-116">Ajoutez ces fichiers à votre projet de codage et utilisez les \# instructions include pour les inclure dans le code de votre client.</span><span class="sxs-lookup"><span data-stu-id="73978-116">Add these files to your coding project, and use \#include statements to include them in the code for your client.</span></span> <span data-ttu-id="73978-117">(Les fichiers XSD représentent des types, et les fichiers WSDL représentent des opérations.)</span><span class="sxs-lookup"><span data-stu-id="73978-117">(The XSD files represent types, and the WSDL files represent operations.)</span></span>

## <a name="creating-the-service-proxy"></a><span data-ttu-id="73978-118">Création du proxy de service</span><span class="sxs-lookup"><span data-stu-id="73978-118">Creating the Service Proxy</span></span>

<span data-ttu-id="73978-119">L’en-tête généré par WsUtil contient une routine d’assistance pour la création du proxy de service avec la liaison requise.</span><span class="sxs-lookup"><span data-stu-id="73978-119">The header generated by WsUtil contains a helper routine for creating the service proxy with the required binding.</span></span> <span data-ttu-id="73978-120">Cette routine est incluse dans la section « routines d’assistance de la stratégie » du fichier d’en-tête généré.</span><span class="sxs-lookup"><span data-stu-id="73978-120">This routine is included in the "Policy helper routines" section of the generated header file.</span></span> <span data-ttu-id="73978-121">Par exemple, l’en-tête généré pour le service de calculatrice illustré dans l’exemple [httpcalculatorclientexample](httpcalculatorclientexample.md) contient le prototype de fonction suivant.</span><span class="sxs-lookup"><span data-stu-id="73978-121">For example, the generated header for the calculator service illustrated in the [httpcalculatorclientexample](httpcalculatorclientexample.md) example will contain the following function prototype.</span></span>


```
HRESULT BasicHttpBinding_ICalculator_CreateServiceProxy(
    __in_opt WS_HTTP_BINDING_TEMPLATE* templateValue,
    __in_ecount_opt(proxyPropertyCount) const WS_PROXY_PROPERTY* proxyProperties,
    __in const ULONG proxyPropertyCount,
    __deref_out_opt WS_SERVICE_PROXY** _serviceProxy,
    __in_opt WS_ERROR* error);
```



<span data-ttu-id="73978-122">Incorporez cette application d’assistance dans votre code et transmettez un handle de [ \_ \_ proxy de service Web](ws-service-proxy.md) pour recevoir le descripteur du proxy de service créé.</span><span class="sxs-lookup"><span data-stu-id="73978-122">Incorporate this helper in your code and pass a [WS\_SERVICE\_PROXY](ws-service-proxy.md) handle to receive the handle to the created service proxy.</span></span> <span data-ttu-id="73978-123">Dans le scénario le plus simple, dans lequel seul un handle de proxy de service et un objet d’erreur sont passés à la fonction, l’appel ressemble à ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="73978-123">In the simplest scenario, in which only a service proxy handle and an error object are passed to the function, the call looks like the following.</span></span>


```C++
hr = BasicHttpBinding_ICalculator_CreateServiceProxy(
            NULL,
            NULL,
            0,
            &serviceProxy,
            error);
```



<span data-ttu-id="73978-124">Pour créer la partie adresse du proxy de service, appelez [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) avec un handle vers le proxy de service et un pointeur vers [**une \_ \_ adresse de point de terminaison WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) contenant l’adresse de point de terminaison de service à laquelle vous souhaitez vous connecter.</span><span class="sxs-lookup"><span data-stu-id="73978-124">To create the address portion of the service proxy, call [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) with a handle to the service proxy and a pointer to a [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) containing the service endpoint address to which you wish to connect.</span></span>

## <a name="implementing-the-client-with-function-prototypes"></a><span data-ttu-id="73978-125">Implémentation du client à l’aide de prototypes de fonction</span><span class="sxs-lookup"><span data-stu-id="73978-125">Implementing the Client with Function Prototypes</span></span>

<span data-ttu-id="73978-126">Les en-têtes générés à partir des fichiers WSDL de service contiennent également des prototypes de fonction C représentant les services disponibles à partir du service Web et spécifiques à la liaison requise.</span><span class="sxs-lookup"><span data-stu-id="73978-126">The headers generated from the service WSDL files also contain C function prototypes representing the services available from the Web service and specific to the binding required.</span></span> <span data-ttu-id="73978-127">Par exemple, un en-tête généré pour le service de calculatrice illustré dans HttpCalculatorServiceExample contient le prototype suivant pour l’opération de multiplication de ce service.</span><span class="sxs-lookup"><span data-stu-id="73978-127">For example, a header generated for the calculator service illustrated in HttpCalculatorServiceExample will contain the following prototype for that service's multiplication operation.</span></span>

``` syntax
HRESULT BasicHttpBinding_ICalculator_Multiply(
    __in WS_SERVICE_PROXY* _serviceProxy,
    __in double n1,
    __in double n2,
    __out double* MultiplyResult,
    __in WS_HEAP* _heap,
    __in_ecount_opt(_callPropertyCount) const WS_CALL_PROPERTY* _callProperties,
    __in const ULONG _callPropertyCount,
    __in_opt const WS_ASYNC_CONTEXT* _asyncContext,
    __in_opt WS_ERROR* _error);
```

<span data-ttu-id="73978-128">Vous pouvez copier les prototypes et les utiliser en tant que modèles pour coder les appels de fonction dans votre client, dans chaque cas en passant le handle au proxy de service.</span><span class="sxs-lookup"><span data-stu-id="73978-128">You can copy the prototypes and use them as templates for coding the function calls in your client, in each case passing the handle to service proxy.</span></span> <span data-ttu-id="73978-129">Lorsque vous avez terminé avec le proxy de service, appelez [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy).</span><span class="sxs-lookup"><span data-stu-id="73978-129">When you are finished with the service proxy, call [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy).</span></span>

 

 




