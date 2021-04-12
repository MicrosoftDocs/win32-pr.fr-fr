---
title: Vue d’ensemble de la couche de modèle de service
description: L’API du modèle de service WWSAPI modélise la communication entre un client et un service en tant qu’appels de méthode, plutôt qu’en tant que messages de données.
ms.assetid: a1ed1e3c-94ae-4383-9251-83caf2e3ebf3
keywords:
- Vue d’ensemble de la couche de modèle de service services Web pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c74861f0e2ed13b35e308d1314aec2a33dc28c31
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2021
ms.locfileid: "104321422"
---
# <a name="service-model-layer-overview"></a><span data-ttu-id="bbd46-106">Vue d’ensemble de la couche de modèle de service</span><span class="sxs-lookup"><span data-stu-id="bbd46-106">Service Model Layer Overview</span></span>

<span data-ttu-id="bbd46-107">L’API du modèle de service WWSAPI modélise la communication entre un client et un service en tant qu’appels de méthode, plutôt qu’en tant que messages de données.</span><span class="sxs-lookup"><span data-stu-id="bbd46-107">The WWSAPI Service Model API models the communication between a client and a service as method calls, rather than as data messages.</span></span> <span data-ttu-id="bbd46-108">Contrairement à la [couche de canal](channel-layer-overview.md), qui prend en charge des échanges de [messages](message.md) plus traditionnels entre le client et le service, le modèle de service gère automatiquement la communication au moyen d’un proxy de service sur le client et d’un hôte de service sur le service.</span><span class="sxs-lookup"><span data-stu-id="bbd46-108">In contrast to the [channel layer](channel-layer-overview.md), which supports more traditional [message](message.md) exchanges between client and service, the Service Model automatically manages communication by means of a service proxy on the client and a service host on the service.</span></span> <span data-ttu-id="bbd46-109">Cela signifie que le client appelle des fonctions générées et que le serveur implémente les rappels.</span><span class="sxs-lookup"><span data-stu-id="bbd46-109">This means that the client calls generated functions and the server implements callbacks.</span></span>


<span data-ttu-id="bbd46-110">Par exemple, imaginez un service de calculatrice qui effectue l’addition et la soustraction sur deux nombres.</span><span class="sxs-lookup"><span data-stu-id="bbd46-110">For example, consider a calculator service which performs addition and subtraction on two numbers.</span></span> <span data-ttu-id="bbd46-111">L’addition et la soustraction sont des opérations naturellement représentées naturellement comme appels de méthode.</span><span class="sxs-lookup"><span data-stu-id="bbd46-111">Addition and subtraction are operations naturally represented as method calls.</span></span>

![Diagramme montrant comment un service de calculatrice communique avec un client à l’aide d’appels de méthode pour l’addition et la soustraction.](images/servicemodelintro.png)

<span data-ttu-id="bbd46-113">Le modèle de service représente la communication entre le client et le service en tant qu’appels de méthode déclarés, et masque donc les détails de communication de la couche de canal sous-jacente de l’application, ce qui rend le service plus facile à implémenter.</span><span class="sxs-lookup"><span data-stu-id="bbd46-113">The service model represents the communication between client and the service as declared method calls, and so conceals the communication details of the underlying channel layer from the application, making the service easier to implement.</span></span>

## <a name="specifying-a-service"></a><span data-ttu-id="bbd46-114">Spécification d’un service</span><span class="sxs-lookup"><span data-stu-id="bbd46-114">Specifying a Service</span></span>

<span data-ttu-id="bbd46-115">Un service doit être spécifié en termes de modèles d’échange de messages, ainsi que sa représentation de données réseau.</span><span class="sxs-lookup"><span data-stu-id="bbd46-115">A service must be specified in terms of its message exchange patterns as well as its network data representation.</span></span> <span data-ttu-id="bbd46-116">Pour les services, cette spécification est généralement fournie sous forme de documents de schéma WSDL et XML.</span><span class="sxs-lookup"><span data-stu-id="bbd46-116">For services, this specification is usually provided as WSDL and XML schema documents.</span></span>

<span data-ttu-id="bbd46-117">Le document WSDL est un document XML qui contient la liaison de canal et les modèles d’échange de messages du service, tandis que le document de schéma XML est un document XML qui définit la représentation des messages individuels.</span><span class="sxs-lookup"><span data-stu-id="bbd46-117">The WSDL document is an XML document which contains the channel binding and the message exchange patterns of the service, whereas the XML schema document is an XML document that defines the data representation of the individual messages.</span></span>

<span data-ttu-id="bbd46-118">Pour le service de calculatrice et ses opérations d’addition et de soustraction, le document WSDL peut se présenter comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="bbd46-118">For the calculator service and its addition and subtraction operations, the WSDL document might look like the following example:</span></span>

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" 
xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd" 
xmlns:soapenc="http://schemas.xmlsoap.org/soap/encoding/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsp="http://schemas.xmlsoap.org/ws/2004/09/policy" 
xmlns:wsap="http://schemas.xmlsoap.org/ws/2004/08/addressing/policy" xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
xmlns:msc="http://schemas.microsoft.com/ws/2005/12/wsdl/contract" xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" 
xmlns:soap12="http://schemas.xmlsoap.org/wsdl/soap12/" xmlns:wsa10="http://www.w3.org/2005/08/addressing" 
xmlns:wsx="http://schemas.xmlsoap.org/ws/2004/09/mex" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:portType name="ICalculator">
  <wsdl:operation name="Add">
   <wsdl:input wsaw:Action="http://Example.org/ICalculator/Add" 
   message="tns:ICalculator_Add_InputMessage" />
   <wsdl:output wsaw:Action="http://Example.org/ICalculator/AddResponse" 
   message="tns:ICalculator_Add_OutputMessage" />
  </wsdl:operation>
 </wsdl:portType>
</wsdl:definitions>
```

<span data-ttu-id="bbd46-119">De même, son schéma XML peut être défini comme suit :</span><span class="sxs-lookup"><span data-stu-id="bbd46-119">Likewise, its XML schema can be defined as follows:</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:element name="Add">
  <xs:complexType>
   <xs:sequence>
    <xs:element minOccurs="0" name="a" type="xs:int" />
    <xs:element minOccurs="0" name="b" type="xs:int" />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
 <xs:element name="AddResponse">
  <xs:complexType>
   <xs:sequence>
    <xs:element minOccurs="0" name="result" type="xs:int" 
    />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
</xs:schema> 
```

## <a name="converting-metadata-to-code"></a><span data-ttu-id="bbd46-120">Conversion de métadonnées en code</span><span class="sxs-lookup"><span data-stu-id="bbd46-120">Converting Metadata to Code</span></span>

<span data-ttu-id="bbd46-121">Le modèle de service fournit le [WsUtil.exe](web-service-compiler-tool.md) en tant qu’outil pour traiter ces documents de métadonnées, en convertissant un fichier WSDL en en-tête C et en fichiers sources.</span><span class="sxs-lookup"><span data-stu-id="bbd46-121">The service model provides the [WsUtil.exe](web-service-compiler-tool.md) as a tool to process these metadata documents, converting a WSDL file into a C header and source files.</span></span>

![Diagramme montrant comment WsUtil.exe convertit un fichier WSDL en en-tête C et en fichiers sources.](images/doctotool.png)

<span data-ttu-id="bbd46-123">Le [WsUtil.exe](web-service-compiler-tool.md) génère l’en-tête et les sources pour l’implémentation de service, ainsi que les opérations de service côté client pour le client.</span><span class="sxs-lookup"><span data-stu-id="bbd46-123">The [WsUtil.exe](web-service-compiler-tool.md) generates header and sources for service implementation as well as client-side service operations for the client .</span></span>

## <a name="calling-the-calculator-service-from-a-client"></a><span data-ttu-id="bbd46-124">Appel du service de calculatrice à partir d’un client</span><span class="sxs-lookup"><span data-stu-id="bbd46-124">Calling the Calculator Service From a Client</span></span>

<span data-ttu-id="bbd46-125">Comme pour l’implémentation du service, le client doit inclure l’en-tête ou les en-têtes générés.</span><span class="sxs-lookup"><span data-stu-id="bbd46-125">As with the service implementation, the client must include the generated header or headers.</span></span>

``` syntax
#include "CalculatorProxyStub.h"
```

<span data-ttu-id="bbd46-126">À présent, l’application cliente peut créer et ouvrir un proxy de service pour commencer à communiquer avec le service de calculatrice.</span><span class="sxs-lookup"><span data-stu-id="bbd46-126">Now, The client application can create and open a service proxy to begin communication with the calculator service.</span></span>

``` syntax
WS_ENDPOINT_ADDRESS address = {0};
WS_STRING uri= WS_STRING_VALUE(L"http://localhost/example");
address.uri = uri;

if (FAILED (hr = WsCreateServiceProxy(WS_CHANNEL_TYPE_REQUEST, WS_HTTP_CHANNEL_BINDING, NULL, NULL, 0, &serviceProxy, error)))
    goto Error;

if (FAILED (hr = WsOpenServiceProxy(serviceProxy, &address, NULL, error)))
    goto Error;
```

<span data-ttu-id="bbd46-127">L’application peut appeler l’opération Add sur le service Calculator avec le code suivant :</span><span class="sxs-lookup"><span data-stu-id="bbd46-127">The application can call the Add operation on the calculator service with the following code:</span></span>

``` syntax
if (FAILED (hr = DefaultBinding_ICalculator_Add(serviceProxy, heap, 1, 2, &result, NULL, 0, NULL, error)))
    goto Error;
```

<span data-ttu-id="bbd46-128">Reportez-vous à l’exemple de code sur [HttpCalculatorClientExample](httpcalculatorclientexample.md) pour une implémentation complète du service de calculatrice.</span><span class="sxs-lookup"><span data-stu-id="bbd46-128">Please refer to the code example at [HttpCalculatorClientExample](httpcalculatorclientexample.md) for full implementation of the calculator service.</span></span>

## <a name="service-model-components"></a><span data-ttu-id="bbd46-129">Composants du modèle de service</span><span class="sxs-lookup"><span data-stu-id="bbd46-129">Service Model Components</span></span>

<span data-ttu-id="bbd46-130">L’interaction des composants individuels du modèle de service WWSAPI dans l’exemple de calculatrice est la suivante :</span><span class="sxs-lookup"><span data-stu-id="bbd46-130">The interaction of the individual WWSAPI Service Model components within the Calculator example is as follows:</span></span>

-   <span data-ttu-id="bbd46-131">Le client crée un [proxy de service](service-proxy.md) et l’ouvre.</span><span class="sxs-lookup"><span data-stu-id="bbd46-131">The client creates a [service proxy](service-proxy.md) and opens it.</span></span>
-   <span data-ttu-id="bbd46-132">Le client appelle la fonction Add du service et passe le proxy de service.</span><span class="sxs-lookup"><span data-stu-id="bbd46-132">The client calls the Add function of the service, and passes in the service proxy.</span></span>
-   <span data-ttu-id="bbd46-133">Le message est sérialisé selon les métadonnées de sérialisation dans l’en-tête et les fichiers sources générés par l’outil de métadonnées ([WsUtil.exe](web-service-compiler-tool.md)).</span><span class="sxs-lookup"><span data-stu-id="bbd46-133">The message is serialized according to the serialization metadata in the header and source files generated by the metadata tool ([WsUtil.exe](web-service-compiler-tool.md)).</span></span>
-   <span data-ttu-id="bbd46-134">Le message est écrit sur le canal et transmis sur le réseau au service.</span><span class="sxs-lookup"><span data-stu-id="bbd46-134">The message is written to the channel and is transmitted over the network to the service.</span></span>
-   <span data-ttu-id="bbd46-135">Côté serveur, le service est hébergé à l’intérieur d’un hôte de service et possède un point de terminaison qui écoute le contrat ICalculator.</span><span class="sxs-lookup"><span data-stu-id="bbd46-135">On the server side, the service is hosted inside a service host, and has an endpoint listening for the ICalculator contract.</span></span>
-   <span data-ttu-id="bbd46-136">À l’aide des métadonnées du modèle de service dans le stub, le service désérialise le message à partir du client et le distribue au stub.</span><span class="sxs-lookup"><span data-stu-id="bbd46-136">Using the Service Model metadata in the stub, the service deserializes the message from the client and dispatches it to the stub.</span></span>
-   <span data-ttu-id="bbd46-137">Le service côté serveur appelle la méthode Add, en lui transmettant le contexte d’opération.</span><span class="sxs-lookup"><span data-stu-id="bbd46-137">The server-side service calls the Add method, passing it the operation context.</span></span> <span data-ttu-id="bbd46-138">Ce contexte d’opération contient la référence au message entrant.</span><span class="sxs-lookup"><span data-stu-id="bbd46-138">This operation context contains the reference to the incoming message.</span></span>

![Diagramme montrant l’interaction des composants individuels du modèle de service WWSAPI.](images/servicemodellayout.png)

<span data-ttu-id="bbd46-140">Composants</span><span class="sxs-lookup"><span data-stu-id="bbd46-140">Components</span></span>

-   <span data-ttu-id="bbd46-141">[Hôte de service](service-host.md): héberge un service.</span><span class="sxs-lookup"><span data-stu-id="bbd46-141">[Service host](service-host.md): Hosts a service.</span></span>
-   <span data-ttu-id="bbd46-142">[Proxy de service](service-proxy.md): définit la manière dont un client communique avec un service.</span><span class="sxs-lookup"><span data-stu-id="bbd46-142">[Service proxy](service-proxy.md): Defines how a client communicates with a service.</span></span>
-   <span data-ttu-id="bbd46-143">[Context](context.md): jeu de propriétés pour rendre les informations spécifiques à l’état disponibles pour une opération de service.</span><span class="sxs-lookup"><span data-stu-id="bbd46-143">[Context](context.md): Property bag for making state-specific information available to a service operation.</span></span>
-   <span data-ttu-id="bbd46-144">[Contrat](contract.md): définition d’interface d’un service.</span><span class="sxs-lookup"><span data-stu-id="bbd46-144">[Contract](contract.md): The interface definition of a service.</span></span> <span data-ttu-id="bbd46-145">Par exemple, ICalculator représente un contrat pour le service Calculator dans notre exemple de code.</span><span class="sxs-lookup"><span data-stu-id="bbd46-145">For example, ICalculator represents a contract for the calculator service in our example code.</span></span>
-   <span data-ttu-id="bbd46-146">[WsUtil.exe](web-service-compiler-tool.md): l’outil de métadonnées de modèle de service pour générer des proxies et des stubs.</span><span class="sxs-lookup"><span data-stu-id="bbd46-146">[WsUtil.exe](web-service-compiler-tool.md): The Service Model metadata tool for generating proxies and stubs.</span></span>

 

 




