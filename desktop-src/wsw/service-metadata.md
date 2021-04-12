---
title: Métadonnées du service
description: L’hôte de service WWSAPI prend en charge WS-MetadataExchange pour ses points de terminaison.
ms.assetid: 5a6feb34-7fff-4000-b3be-63112b22905a
keywords:
- Métadonnées de service natives-services Web
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ebf15614ac9e89a4e08fdd19102492d0121e65d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104463947"
---
# <a name="service-metadata"></a><span data-ttu-id="ffcb8-106">Métadonnées du service</span><span class="sxs-lookup"><span data-stu-id="ffcb8-106">Service Metadata</span></span>

<span data-ttu-id="ffcb8-107">L’hôte de service WWSAPI prend en charge WS-MetadataExchange pour ses points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="ffcb8-107">The WWSAPI service host supports WS-MetadataExchange for its endpoints.</span></span> <span data-ttu-id="ffcb8-108">Vous activez ce type d’échange de métadonnées sur l’hôte de service en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="ffcb8-108">You enable such metadata exchange on the service host with the following steps:</span></span>

-   <span data-ttu-id="ffcb8-109">Spécifiez les documents de métadonnées dans la propriété de [**\_ \_ métadonnées WS service**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) sur l' [ \_ \_ hôte WS service](ws-service-host.md).</span><span class="sxs-lookup"><span data-stu-id="ffcb8-109">Specify metadata documents in the [**WS\_SERVICE\_METADATA**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) property on the [WS\_SERVICE\_HOST](ws-service-host.md).</span></span>
-   <span data-ttu-id="ffcb8-110">Spécifiez le nom du service dans la propriété de [**\_ \_ métadonnées WS service**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) sur l' [ \_ \_ hôte du service WS](ws-service-host.md).</span><span class="sxs-lookup"><span data-stu-id="ffcb8-110">Specify the service name in the [**WS\_SERVICE\_METADATA**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) property on the [WS\_SERVICE\_HOST](ws-service-host.md).</span></span>
-   <span data-ttu-id="ffcb8-111">Spécifiez le port pour les points de terminaison individuels à l’aide de la propriété de [**\_ \_ \_ \_ métadonnées de propriété de point**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) de terminaison de service WS sur le point de [**\_ \_ terminaison de service WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span><span class="sxs-lookup"><span data-stu-id="ffcb8-111">Specify the port for individual endpoints by using the [**WS\_SERVICE\_ENDPOINT\_PROPERTY\_METADATA**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) property on the [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span></span>
-   <span data-ttu-id="ffcb8-112">Activez une ou plusieurs structures de [**\_ point de \_ terminaison de service WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) pour traiter les demandes de WS-MetadataExchange.</span><span class="sxs-lookup"><span data-stu-id="ffcb8-112">Enable one or more [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) structures to service the WS-MetadataExchange requests.</span></span>
-   <span data-ttu-id="ffcb8-113">Si vous le souhaitez, spécifiez le **\_ \_ \_ \_ \_ \_ \_ suffixe de l’URL d’échange de métadonnées du point de terminaison WS service** dans l’énumération de l' [**\_ \_ \_ \_ ID de propriété du point de terminaison de service Web**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) pour traiter Ws-MetadataExchange demandes sur une adresse spécifique.</span><span class="sxs-lookup"><span data-stu-id="ffcb8-113">Optionally, specify **WS\_SERVICE\_ENDPOINT\_PROPERTY\_METADATA\_EXCHANGE\_URL\_SUFFIX** in the [**WS\_SERVICE\_ENDPOINT\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) enumeration for servicing Ws-MetadataExchange requests on a specific address.</span></span>


<span data-ttu-id="ffcb8-114">Spécification de documents de métadonnées/nom de service sur l’hôte de service</span><span class="sxs-lookup"><span data-stu-id="ffcb8-114">Specifying Metadata documents / Service name on the Service Host</span></span>

<span data-ttu-id="ffcb8-115">La première étape consiste à spécifier les documents de métadonnées sur l’hôte de service.</span><span class="sxs-lookup"><span data-stu-id="ffcb8-115">The first step is to specify the metadata documents on the service host.</span></span> <span data-ttu-id="ffcb8-116">Pour ce faire, rassemblez les documents individuels sous la forme d’un tableau de la \_ chaîne WS XML \_ \* .</span><span class="sxs-lookup"><span data-stu-id="ffcb8-116">Do this by gathering the individual documents as an array of WS\_XML\_STRING\*'s.</span></span> <span data-ttu-id="ffcb8-117">Ces chaînes peuvent être des documents de schéma XML, WSDL ou WS-Policy.</span><span class="sxs-lookup"><span data-stu-id="ffcb8-117">These strings can be XML Schema, WSDL or WS-Policy document.</span></span> <span data-ttu-id="ffcb8-118">Cela est spécifié par le biais de la propriété de [**\_ \_ \_ métadonnées de propriété de service Web**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) .</span><span class="sxs-lookup"><span data-stu-id="ffcb8-118">This is specified through the [**WS\_SERVICE\_PROPERTY\_METADATA**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) property.</span></span>

<span data-ttu-id="ffcb8-119">Éventuellement, une application peut également spécifier le nom du service et l’espace de noms dans le cadre des [**\_ \_ métadonnées du service WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata).</span><span class="sxs-lookup"><span data-stu-id="ffcb8-119">Optionally, an application can also specify the service name and namespace as part of the [**WS\_SERVICE\_METADATA**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata).</span></span> <span data-ttu-id="ffcb8-120">Si le document de métadonnées ne spécifie pas l’élément de service pour le nom de service donné, le modèle de service génère un élément de service avec les ports WSDL correspondants pour le service.</span><span class="sxs-lookup"><span data-stu-id="ffcb8-120">If the metadata document does not specify the service element for the given service name, the service model will generate a service element with the corresponding WSDL ports for the service.</span></span>

``` syntax
WS_SERVICE_METADATA_DOCUMENT document = {0};
WS_STRING documentName = WS_STRING_VALUE(L&quot;a.wsdl&quot;);
document.name = &documentName;
document.content = &wsdlDocument
WS_SERVICE_METADATA_DOCUMENT** metadataDocuments [] = {&document};
WS_SERVICE_METADATA serviceMetadata = {0};
// Specify Metadata documents
serviceMetadata.count = WsCountOf(metadataDocuments);
serviceMetadata.documents = &metadataDocuments;
// Specify service name
serviceMetadata.serviceName = &serviceName;
serviceMetadata.serviceNs = &serviceNamespace;


WS_SERVICE_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_PROPERTY_METADATA;
serviceProperties[0].value =  &serviceMetadata;
serviceProperties[0].ValueSize = sizeof(serviceMetadata);
```

<span data-ttu-id="ffcb8-121">Notez qu’aucune vérification des documents de métadonnées individuels n’est effectuée sur les documents.</span><span class="sxs-lookup"><span data-stu-id="ffcb8-121">Note that no verification of the individual metadata documents will be performed on the documents.</span></span> <span data-ttu-id="ffcb8-122">Il incombe à l’application de valider le contenu des documents et de s’assurer que tous les chemins d’importation sont spécifiés de façon relative.</span><span class="sxs-lookup"><span data-stu-id="ffcb8-122">It is the responsiblity of the application to validate contents of the documents and ensure that all the imports paths are relatively specified.</span></span>

<span data-ttu-id="ffcb8-123">L’espace de noms spécifié est utilisé pour localiser le document dans lequel l’élément de service sera ajouté par l’hôte de service.</span><span class="sxs-lookup"><span data-stu-id="ffcb8-123">The namespace specified is used to locate the document in which the service element will be added by the service host.</span></span>

<span data-ttu-id="ffcb8-124">Ajout d’un élément de service au document WSDL</span><span class="sxs-lookup"><span data-stu-id="ffcb8-124">Addition of service element to the WSDL document</span></span>

<span data-ttu-id="ffcb8-125">L’hôte de service fournit à l’application la possibilité d’ajouter un élément de service en son nom, si aucune n’est déjà spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ffcb8-125">The service host provides facility for the application to add a service element on its behalf if one is not already specified.</span></span> <span data-ttu-id="ffcb8-126">Pour activer ce comportement, une application doit spécifier des champs serivceName et serviceNs sur la structure de [**\_ \_ métadonnées WS service**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) .</span><span class="sxs-lookup"><span data-stu-id="ffcb8-126">In order to enable this behavior an application must specify serivceName and serviceNs fields on the [**WS\_SERVICE\_METADATA**](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata) structure.</span></span> <span data-ttu-id="ffcb8-127">Si serviceName et serviceNs sont tous deux **null** , aucun élément de service n’est ajouté au document WSDL.</span><span class="sxs-lookup"><span data-stu-id="ffcb8-127">If serviceName and serviceNs are both **NULL** no service element is added to the WSDL document.</span></span> <span data-ttu-id="ffcb8-128">Ils sont tous deux utilisés pour identifier le document dans lequel le serviceElement va être ajouté.</span><span class="sxs-lookup"><span data-stu-id="ffcb8-128">Both these are used to identify document in which the serviceElement is going to be added.</span></span>

<span data-ttu-id="ffcb8-129">Si la propriété de [**\_ \_ \_ métadonnées de propriété WS service**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) n’est pas spécifiée, aucune métadonnée n’a lieu sur l’hôte de service.</span><span class="sxs-lookup"><span data-stu-id="ffcb8-129">If [**WS\_SERVICE\_PROPERTY\_METADATA**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) property is not specified no metadata exhange will take place on the service host.</span></span>

<span data-ttu-id="ffcb8-130">Spécification du port sur le point de terminaison du \_ service WS \_</span><span class="sxs-lookup"><span data-stu-id="ffcb8-130">Specifying the port on the WS\_SERVICE\_ENDPOINT</span></span>

<span data-ttu-id="ffcb8-131">Pour qu' [**un \_ point de \_ terminaison de service Web**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) soit disponible en tant que port à l’intérieur de l’élément de service dans le document WSDL, l’application doit spécifier la propriété de [**\_ \_ \_ \_ métadonnées de la propriété de point de terminaison de service WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) .</span><span class="sxs-lookup"><span data-stu-id="ffcb8-131">For a [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) to be available as a port inside the service element in the WSDL document, the application must specify [**WS\_SERVICE\_ENDPOINT\_PROPERTY\_METADATA**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) property on it.</span></span>

``` syntax
WS_SERVICE_ENDPOINT_METADATA endpointPort = {0}
endpointPort.name = &portName;
endpointPort.bindingName = &bindingName;
endpointPort.bindingNs = &bindingNs;

WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA;
serviceProperties[0].value =  &endpointPort;
serviceProperties[0].valueSize = sizeof(endpointPort);
```

<span data-ttu-id="ffcb8-132">Il est supposé que la référence au nom de liaison et à l’espace de noms existe dans les documents spécifiés sur l’hôte de service dans le cadre des \_ \_ métadonnées de propriété WS service \_ .</span><span class="sxs-lookup"><span data-stu-id="ffcb8-132">It is assumed that the reference to the binding name and namespace exists in the documents specified on the service host as part of WS\_SERVICE\_PROPERTY\_METADATA.</span></span> <span data-ttu-id="ffcb8-133">Le runtime ne vérifie pas cela au nom de l’application.</span><span class="sxs-lookup"><span data-stu-id="ffcb8-133">The runtime does not verify this on behalf of the application.</span></span>

<span data-ttu-id="ffcb8-134">Activer la maintenance de WS-MetadataExchange sur le point de terminaison de \_ service WS \_</span><span class="sxs-lookup"><span data-stu-id="ffcb8-134">Enable WS-MetadataExchange servicing on WS\_SERVICE\_ENDPOINT</span></span>

<span data-ttu-id="ffcb8-135">Pour pouvoir traiter les demandes de WS-MetadataExchange, l’hôte de service doit avoir au moins un point de terminaison activé pour la maintenance des demandes de WS-MetadataExchange.</span><span class="sxs-lookup"><span data-stu-id="ffcb8-135">In order to service WS-MetadataExchange requests,the service host must have at least one endpoint enabled for servicing WS-MetadataExchange requests.</span></span> <span data-ttu-id="ffcb8-136">Pour ce faire, définissez la version appropriée pour WS-MetadataExchange sur le [**\_ point de \_ terminaison du service WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span><span class="sxs-lookup"><span data-stu-id="ffcb8-136">This is done by setting the appropriate version for WS-MetadataExchange on the [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span></span>

``` syntax
WS_METADATA_EXCHANGE_TYPE metadataExchangeType = WS_METADATA_EXCHANGE_TYPE_MEX;
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE;
serviceProperties[0].value =  &metadataExchangeType;
serviceProperties[0].ValueSize = sizeof(metadataExchangeType);
```

<span data-ttu-id="ffcb8-137">Activer la maintenance HTTP sur le point de terminaison de \_ service WS \_</span><span class="sxs-lookup"><span data-stu-id="ffcb8-137">Enable HTTP GET servicing on WS\_SERVICE\_ENDPOINT</span></span>

<span data-ttu-id="ffcb8-138">Pour serviceHTTP les demandes d’accès, l’hôte de service doit avoir au moins un point de terminaison activé pour la maintenance des demandes de WS-MetadataExchange.</span><span class="sxs-lookup"><span data-stu-id="ffcb8-138">In order to serviceHTTP GET requests, the service host must have at least one endpoint enabled for servicing WS-MetadataExchange requests.</span></span> <span data-ttu-id="ffcb8-139">Pour ce faire, définissez la version appropriée pour WS-MetadataExchange sur le [**\_ point de \_ terminaison du service WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span><span class="sxs-lookup"><span data-stu-id="ffcb8-139">This is done by setting the appropriate version for WS-MetadataExchange on the [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span></span>

``` syntax
WS_METADATA_EXCHANGE_TYPE metadataExchangeType = WS_METADATA_EXCHANGE_TYPE_HTTP_GET;
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE;
serviceProperties[0].value =  &metadataExchangeType;
serviceProperties[0].ValueSize = sizeof(metadataExchangeType);
```

<span data-ttu-id="ffcb8-140">Spécification du suffixe d’URL pour les demandes Ws-MetadataExchange</span><span class="sxs-lookup"><span data-stu-id="ffcb8-140">Specifying URL suffix for Ws-MetadataExchange requests</span></span>

<span data-ttu-id="ffcb8-141">Une application peut éventuellement activer l’acceptation des demandes uniquement pour WS-MetadataExchange sur un chemin d’accès spécifique.</span><span class="sxs-lookup"><span data-stu-id="ffcb8-141">An application can optionally enable only accepting requests for WS-MetadataExchange on a specific path.</span></span> <span data-ttu-id="ffcb8-142">Pour ce faire, vous spécifiez un suffixe pour le point de terminaison du service WS donné \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ffcb8-142">This is done by specifying a suffix for the given WS\_SERVICE\_ENDPOINT.</span></span> <span data-ttu-id="ffcb8-143">Ce suffixe est concaténé tel quel à l’URL réelle du point de \_ terminaison du service WS \_ .</span><span class="sxs-lookup"><span data-stu-id="ffcb8-143">This suffix is concatenated as-is to the actual URL for the WS\_SERVICE\_ENDPOINT.</span></span> <span data-ttu-id="ffcb8-144">La chaîne concaténée est utilisée comme URL correspondante à l’en-tête « to » reçu.</span><span class="sxs-lookup"><span data-stu-id="ffcb8-144">The concatenated string is used as the matching URL to the 'to' header received.</span></span>

``` syntax
const WS_STRING suffix = WS_STRING_VALUE(L&quot;mex&quot;);
WS_SERVICE_ENDPOINT_PROPERTY serviceProperties[1] = {};
serviceProperties[0].id = WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_URL_SUFFIX;
serviceProperties[0].value =  &suffix;
serviceProperties[0].valueSize = sizeof(suffix);
```

<span data-ttu-id="ffcb8-145">Les éléments d’API suivants sont liés au service métadonnées.</span><span class="sxs-lookup"><span data-stu-id="ffcb8-145">The following API elements relate to service metada.</span></span>

| <span data-ttu-id="ffcb8-146">Énumération</span><span class="sxs-lookup"><span data-stu-id="ffcb8-146">Enumeration</span></span>                                                       | <span data-ttu-id="ffcb8-147">Description</span><span class="sxs-lookup"><span data-stu-id="ffcb8-147">Description</span></span>                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="ffcb8-148">**\_type d’échange de métadonnées WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ffcb8-148">**WS\_METADATA\_EXCHANGE\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_exchange_type) | <span data-ttu-id="ffcb8-149">Active ou désactive la maintenance de WS-MetadataExchange et HTTP sur le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="ffcb8-149">Enables or disables WS-MetadataExchange and HTTP GET servicing on the endpoint.</span></span> |



 



| <span data-ttu-id="ffcb8-150">Structure</span><span class="sxs-lookup"><span data-stu-id="ffcb8-150">Structure</span></span>                                                               | <span data-ttu-id="ffcb8-151">Description</span><span class="sxs-lookup"><span data-stu-id="ffcb8-151">Description</span></span>                                                           |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="ffcb8-152">**\_ \_ métadonnées du point de terminaison de service WS \_**</span><span class="sxs-lookup"><span data-stu-id="ffcb8-152">**WS\_SERVICE\_ENDPOINT\_METADATA**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_metadata) | <span data-ttu-id="ffcb8-153">Représente l’élément de port pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="ffcb8-153">Represents the port element for the endpoint.</span></span>                         |
| [<span data-ttu-id="ffcb8-154">**\_ \_ métadonnées WS service**</span><span class="sxs-lookup"><span data-stu-id="ffcb8-154">**WS\_SERVICE\_METADATA**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata)                    | <span data-ttu-id="ffcb8-155">Spécifie le tableau de documents de métadonnées du service.</span><span class="sxs-lookup"><span data-stu-id="ffcb8-155">Specifies the service metadata documents array.</span></span>                       |
| [<span data-ttu-id="ffcb8-156">**\_document de \_ métadonnées WS service \_**</span><span class="sxs-lookup"><span data-stu-id="ffcb8-156">**WS\_SERVICE\_METADATA\_DOCUMENT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_metadata_document) | <span data-ttu-id="ffcb8-157">Spécifie les documents individuels qui composent les métadonnées du service.</span><span class="sxs-lookup"><span data-stu-id="ffcb8-157">Specifies the individual documents that make up the service metadata.</span></span> |



 

 

 




