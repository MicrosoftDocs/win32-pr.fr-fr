---
title: Importation de métadonnées
description: Le WWSAPI comprend des éléments d’API qui peuvent être utilisés pour traiter WSDL et la stratégie à partir d’un point de terminaison avec l’objectif d’extraire des informations qui peuvent être utilisées pour communiquer avec le point de terminaison.
ms.assetid: 77738bf1-ef8b-4fd6-a36a-43f1932868dd
keywords:
- Services Web d’importation de métadonnées pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74c36ffdf9bcbf0d63bdef473cc52cd4d545e5a3
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734989"
---
# <a name="metadata-import"></a><span data-ttu-id="12cb0-106">Importation de métadonnées</span><span class="sxs-lookup"><span data-stu-id="12cb0-106">Metadata Import</span></span>

<span data-ttu-id="12cb0-107">Le WWSAPI comprend des éléments d’API qui peuvent être utilisés pour traiter WSDL et la stratégie à partir d’un point de terminaison avec l’objectif d’extraire des informations qui peuvent être utilisées pour communiquer avec le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="12cb0-107">The WWSAPI includes API elements that can be used to process WSDL and Policy from an endpoint with the goal of extracting information that can be used to communicate with the endpoint.</span></span> <span data-ttu-id="12cb0-108">Ces API sont généralement utilisées lorsque le protocole de communication pris en charge par le point de terminaison n’est pas déjà connu.</span><span class="sxs-lookup"><span data-stu-id="12cb0-108">These APIs are typically used when the communication protocol supported by the endpoint is not already known.</span></span>


<span data-ttu-id="12cb0-109">Utilisez la séquence suivante pour traiter les métadonnées :</span><span class="sxs-lookup"><span data-stu-id="12cb0-109">Use the following sequence to process metadata:</span></span>

``` syntax
WsCreateMetadata    // create a metadata object

while there are metadata documents to add
{
    // retrieve the metadata document from it's location
    // (download, read from file, etc)

    // add the document to the metadata object
    WsReadMetadata

    // optionally query the metadata object for any missing documents
    WsGetMissingMetadataDocumentAddress?
}

// get the endpoints from the metadata object
WsGetMetadataEndpoints

for each endpoint
{            
    // examine the endpoint information to see if 
    // the endpoint is relevant for the particular scenario

    if the endpoint is relevant
    {
        // get the policy object from the endpoint

        // get the number of policy alternatives in the policy
        WsGetPolicyAlternativeCount

        for each policy alternative
        {
            // construct a policy constraints structure that specifies
            // what policy is acceptable and what information to extract
            // from the policy

            // see if the policy alternative matches the constraints
            WsMatchPolicyAlternative

            // if there is a match, then use it

            // if there is not a match, then it is also possible to 
            // try with a different constraint structure
        }
    }
}

// If reusing the metadata object for a different set of documents
WsResetMetadata? // reset metadata object, which removes all documents

WsFreeMetadata // free the metadata object
```

<span data-ttu-id="12cb0-110">Pour plus d’informations sur la façon dont les assertions WSDL et WS-Policy correspondent à l’API, consultez la rubrique [mappage de métadonnées](metadata-mapping.md) .</span><span class="sxs-lookup"><span data-stu-id="12cb0-110">for information about how WSDL and WS-Policy assertions correspond to the API, see the [Metadata Mapping](metadata-mapping.md) topic.</span></span>

## <a name="security"></a><span data-ttu-id="12cb0-111">Sécurité</span><span class="sxs-lookup"><span data-stu-id="12cb0-111">Security</span></span>

<span data-ttu-id="12cb0-112">Les métadonnées téléchargées sont aussi efficaces que l’adresse utilisée pour le télécharger.</span><span class="sxs-lookup"><span data-stu-id="12cb0-112">The metadata downloaded is only as good as the address used to download it.</span></span> <span data-ttu-id="12cb0-113">Une application doit s’assurer que approuve l’adresse.</span><span class="sxs-lookup"><span data-stu-id="12cb0-113">An application should ensure that is trusts the address.</span></span> <span data-ttu-id="12cb0-114">En outre, une application doit s’assurer qu’elle utilise un protocole de sécurité pour télécharger les documents de métadonnées qui n’autorisent pas la falsification des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="12cb0-114">Also, an application should ensure that it uses a security protocol to download the metadata documents that does not allow tampering with the metadata.</span></span>

<span data-ttu-id="12cb0-115">Une application doit inspecter les adresses des services exposés par les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="12cb0-115">An application should inspect the addresses of the services exposed by the metadata.</span></span> <span data-ttu-id="12cb0-116">Par défaut, le runtime garantit que le nom d’hôte du service correspond à celui de l’URL d’origine utilisée pour télécharger les métadonnées, mais que l’application souhaite effectuer des vérifications supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="12cb0-116">By default, the runtime ensures that the host name of the service matches that of the original URL used to download the metadata, but the application may want to perform additional checks.</span></span> <span data-ttu-id="12cb0-117">Une application peut désactiver la vérification du nom d’hôte en remplaçant la propriété de vérification des noms d’hôtes de la [**\_ \_ propriété \_ \_ \_ WS Metadata**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) .</span><span class="sxs-lookup"><span data-stu-id="12cb0-117">An application can disable the host name verification by overwriting [**WS\_METADATA\_PROPERTY\_VERIFY\_HOST\_NAMES**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) property.</span></span> <span data-ttu-id="12cb0-118">Si la vérification du nom d’hôte effectuée par défaut est désactivée, l’application doit se protéger contre les documents de métadonnées contenant l’adresse d’un service d’un tiers différent qu’il n’approuve pas d’une autre façon.</span><span class="sxs-lookup"><span data-stu-id="12cb0-118">If the hostname check that is done by default is disabled, the application will need to protect itself against the metadata documents containing the address of a service from a different party that it does not trust in some other way.</span></span>

<span data-ttu-id="12cb0-119">Par défaut, la quantité maximale de mémoire utilisée par l’exécution des métadonnées pour désérialiser et traiter les métadonnées est de 256 Ko, et le nombre maximal de documents pouvant être ajoutés est de 32.</span><span class="sxs-lookup"><span data-stu-id="12cb0-119">By default, the maximum amount of memory used by the metadata runtime to deserialize and process the metadata is 256k, and the maximum number of documents that may be added is 32.</span></span> <span data-ttu-id="12cb0-120">Ces valeurs par défaut peuvent être remplacées par les propriétés de la [**\_ \_ \_ \_ \_ taille demandée du tas de propriétés WS Metadata**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) et de la **propriété WS \_ Metadata \_ Property \_ \_ documents Max** .</span><span class="sxs-lookup"><span data-stu-id="12cb0-120">These default values can be overwritten by [**WS\_METADATA\_PROPERTY\_HEAP\_REQUESTED\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) and **WS\_METADATA\_PROPERTY\_MAX\_DOCUMENTS** properties.</span></span> <span data-ttu-id="12cb0-121">Ces limites sont conçues pour limiter la quantité de téléchargements et limiter la quantité de mémoire allouée pour accumuler les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="12cb0-121">These bounds are designed to limit the amount of downloads and limit the amount of memory allocated in order to accumulate the metadata.</span></span> <span data-ttu-id="12cb0-122">L’amélioration de ces valeurs peut entraîner une utilisation excessive de la mémoire, de l’utilisation du processeur ou de la bande passante réseau.</span><span class="sxs-lookup"><span data-stu-id="12cb0-122">Increasing these values may lead to excessive memory usage, CPU usage, or network bandwidth consumption.</span></span> <span data-ttu-id="12cb0-123">Notez que, en raison de l’expansion des chaînes de dictionnaire au format binaire, un petit message peut aboutir à une forme désérialisée bien plus grande. par conséquent, le fait de compter sur des messages de petite taille pour limiter l’allocation de mémoire de métadonnées n’est pas suffisant lors de l’utilisation du format binaire.</span><span class="sxs-lookup"><span data-stu-id="12cb0-123">Note that due to expansion of dictionary strings in the binary format, a small message may lead to a much larger deserialized form, so relying on small messages to limit metadata memory allocation is not sufficient when using the binary format.</span></span>

<span data-ttu-id="12cb0-124">Par défaut, le nombre maximal d’alternatives de stratégie est de 32, bien qu’il puisse être remplacé par la propriété [**\_ \_ propriétés \_ Max \_ alternatives de la stratégie WS**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id) .</span><span class="sxs-lookup"><span data-stu-id="12cb0-124">By default, the maximum number of policy alternatives is 32, though it can be overwritten by [**WS\_POLICY\_PROPERTY\_MAX\_ALTERNATIVES**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id) property.</span></span> <span data-ttu-id="12cb0-125">Si une application parcourt chaque alternative à la recherche d’une correspondance, il peut être nécessaire d’effectuer une recherche dans toutes les alternatives avant de trouver une correspondance.</span><span class="sxs-lookup"><span data-stu-id="12cb0-125">If an application loops through each alternative looking for a match, it may need to search all alternatives before finding a match.</span></span> <span data-ttu-id="12cb0-126">L’amélioration du nombre maximal d’alternatives peut entraîner une utilisation excessive du processeur.</span><span class="sxs-lookup"><span data-stu-id="12cb0-126">Increasing the maximum number of alternatives may lead to excessive CPU utilization.</span></span>

<span data-ttu-id="12cb0-127">Les énumérations suivantes font partie de l’importation des métadonnées :</span><span class="sxs-lookup"><span data-stu-id="12cb0-127">The following enumerations are part of metadata import:</span></span>

-   [<span data-ttu-id="12cb0-128">**\_ID de propriété de métadonnées WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="12cb0-128">**WS\_METADATA\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id)
-   [<span data-ttu-id="12cb0-129">**\_État des métadonnées WS \_**</span><span class="sxs-lookup"><span data-stu-id="12cb0-129">**WS\_METADATA\_STATE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_state)
-   [<span data-ttu-id="12cb0-130">**\_type d' \_ extension de stratégie WS \_**</span><span class="sxs-lookup"><span data-stu-id="12cb0-130">**WS\_POLICY\_EXTENSION\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_policy_extension_type)
-   [<span data-ttu-id="12cb0-131">**\_ID de \_ propriété de stratégie WS \_**</span><span class="sxs-lookup"><span data-stu-id="12cb0-131">**WS\_POLICY\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id)
-   [<span data-ttu-id="12cb0-132">**État de la \_ stratégie WS \_**</span><span class="sxs-lookup"><span data-stu-id="12cb0-132">**WS\_POLICY\_STATE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_policy_state)
-   [<span data-ttu-id="12cb0-133">**\_type de \_ contrainte de liaison de sécurité WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="12cb0-133">**WS\_SECURITY\_BINDING\_CONSTRAINT\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_constraint_type)

<span data-ttu-id="12cb0-134">Les fonctions suivantes font partie de l’importation des métadonnées :</span><span class="sxs-lookup"><span data-stu-id="12cb0-134">The following functions are part of metadata import:</span></span>

-   [<span data-ttu-id="12cb0-135">**WsCreateMetadata**</span><span class="sxs-lookup"><span data-stu-id="12cb0-135">**WsCreateMetadata**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatemetadata)
-   [<span data-ttu-id="12cb0-136">**WsFreeMetadata**</span><span class="sxs-lookup"><span data-stu-id="12cb0-136">**WsFreeMetadata**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreemetadata)
-   [<span data-ttu-id="12cb0-137">**WsGetMetadataEndpoints**</span><span class="sxs-lookup"><span data-stu-id="12cb0-137">**WsGetMetadataEndpoints**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetmetadataendpoints)
-   [<span data-ttu-id="12cb0-138">**WsGetMetadataProperty**</span><span class="sxs-lookup"><span data-stu-id="12cb0-138">**WsGetMetadataProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetmetadataproperty)
-   [<span data-ttu-id="12cb0-139">**WsGetMissingMetadataDocumentAddress**</span><span class="sxs-lookup"><span data-stu-id="12cb0-139">**WsGetMissingMetadataDocumentAddress**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetmissingmetadatadocumentaddress)
-   [<span data-ttu-id="12cb0-140">**WsGetPolicyAlternativeCount**</span><span class="sxs-lookup"><span data-stu-id="12cb0-140">**WsGetPolicyAlternativeCount**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetpolicyalternativecount)
-   [<span data-ttu-id="12cb0-141">**WsGetPolicyProperty**</span><span class="sxs-lookup"><span data-stu-id="12cb0-141">**WsGetPolicyProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetpolicyproperty)
-   [<span data-ttu-id="12cb0-142">**WsMatchPolicyAlternative**</span><span class="sxs-lookup"><span data-stu-id="12cb0-142">**WsMatchPolicyAlternative**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsmatchpolicyalternative)
-   [<span data-ttu-id="12cb0-143">**WsReadMetadata**</span><span class="sxs-lookup"><span data-stu-id="12cb0-143">**WsReadMetadata**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadmetadata)
-   [<span data-ttu-id="12cb0-144">**WsResetMetadata**</span><span class="sxs-lookup"><span data-stu-id="12cb0-144">**WsResetMetadata**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsresetmetadata)

<span data-ttu-id="12cb0-145">Les handles suivants font partie de l’importation des métadonnées :</span><span class="sxs-lookup"><span data-stu-id="12cb0-145">The following handles are part of metadata import:</span></span>

-   [<span data-ttu-id="12cb0-146">\_métadonnées WS</span><span class="sxs-lookup"><span data-stu-id="12cb0-146">WS\_METADATA</span></span>](ws-metadata.md)
-   [<span data-ttu-id="12cb0-147">\_stratégie WS</span><span class="sxs-lookup"><span data-stu-id="12cb0-147">WS\_POLICY</span></span>](ws-policy.md)

<span data-ttu-id="12cb0-148">Les structures suivantes font partie de l’importation des métadonnées :</span><span class="sxs-lookup"><span data-stu-id="12cb0-148">The following structures are part of metadata import:</span></span>

-   [<span data-ttu-id="12cb0-149">**\_contrainte de \_ liaison de sécurité de message WS CERT \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="12cb0-149">**WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [<span data-ttu-id="12cb0-150">**\_contrainte de \_ propriété de canal WS \_**</span><span class="sxs-lookup"><span data-stu-id="12cb0-150">**WS\_CHANNEL\_PROPERTY\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property_constraint)
-   [<span data-ttu-id="12cb0-151">**EXTENSION de stratégie de point de \_ terminaison WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="12cb0-151">**WS\_ENDPOINT\_POLICY\_EXTENSION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_policy_extension)
-   [<span data-ttu-id="12cb0-152">**\_contrainte de \_ \_ liaison de \_ sécurité \_ d’en-tête \_ WS http**</span><span class="sxs-lookup"><span data-stu-id="12cb0-152">**WS\_HTTP\_HEADER\_AUTH\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint)
-   [<span data-ttu-id="12cb0-153">**\_contrainte de \_ \_ liaison de sécurité de message de jeton \_ WS \_ émis \_**</span><span class="sxs-lookup"><span data-stu-id="12cb0-153">**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)
-   [<span data-ttu-id="12cb0-154">**\_contrainte de \_ \_ liaison de \_ sécurité de message \_ \_ WS Kerberos APREQ**</span><span class="sxs-lookup"><span data-stu-id="12cb0-154">**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [<span data-ttu-id="12cb0-155">**\_point de terminaison de métadonnées WS \_**</span><span class="sxs-lookup"><span data-stu-id="12cb0-155">**WS\_METADATA\_ENDPOINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_endpoint)
-   [<span data-ttu-id="12cb0-156">**\_points de terminaison de métadonnées WS \_**</span><span class="sxs-lookup"><span data-stu-id="12cb0-156">**WS\_METADATA\_ENDPOINTS**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_endpoints)
-   [<span data-ttu-id="12cb0-157">**\_propriété de métadonnées WS \_**</span><span class="sxs-lookup"><span data-stu-id="12cb0-157">**WS\_METADATA\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_property)
-   [<span data-ttu-id="12cb0-158">**\_contraintes de stratégie WS \_**</span><span class="sxs-lookup"><span data-stu-id="12cb0-158">**WS\_POLICY\_CONSTRAINTS**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_policy_constraints)
-   [<span data-ttu-id="12cb0-159">**\_extension de stratégie WS \_**</span><span class="sxs-lookup"><span data-stu-id="12cb0-159">**WS\_POLICY\_EXTENSION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_policy_extension)
-   [<span data-ttu-id="12cb0-160">**Propriétés de la \_ stratégie WS \_**</span><span class="sxs-lookup"><span data-stu-id="12cb0-160">**WS\_POLICY\_PROPERTIES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_policy_properties)
-   [<span data-ttu-id="12cb0-161">**\_propriété de stratégie WS \_**</span><span class="sxs-lookup"><span data-stu-id="12cb0-161">**WS\_POLICY\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_policy_property)
-   [<span data-ttu-id="12cb0-162">**\_contrainte de \_ propriété de jeton de sécurité de demande WS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="12cb0-162">**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint)
-   [<span data-ttu-id="12cb0-163">**\_contrainte de \_ liaison de sécurité WS \_**</span><span class="sxs-lookup"><span data-stu-id="12cb0-163">**WS\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_constraint)
-   [<span data-ttu-id="12cb0-164">**\_contrainte de \_ propriété de liaison WS Security \_ \_**</span><span class="sxs-lookup"><span data-stu-id="12cb0-164">**WS\_SECURITY\_BINDING\_PROPERTY\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property_constraint)
-   [<span data-ttu-id="12cb0-165">**\_contraintes de sécurité WS \_**</span><span class="sxs-lookup"><span data-stu-id="12cb0-165">**WS\_SECURITY\_CONSTRAINTS**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_constraints)
-   [<span data-ttu-id="12cb0-166">**\_contrainte de \_ \_ liaison de sécurité de message de contexte \_ de \_ sécurité WS \_**</span><span class="sxs-lookup"><span data-stu-id="12cb0-166">**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint)
-   [<span data-ttu-id="12cb0-167">**\_contrainte de \_ propriété de sécurité WS \_**</span><span class="sxs-lookup"><span data-stu-id="12cb0-167">**WS\_SECURITY\_PROPERTY\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_property_constraint)
-   [<span data-ttu-id="12cb0-168">**\_contrainte de \_ liaison de sécurité de transport WS SSL \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="12cb0-168">**WS\_SSL\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint)
-   [<span data-ttu-id="12cb0-169">**contrainte de liaison de sécurité de transport de WS \_ TCP \_ SSPI \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="12cb0-169">**WS\_TCP\_SSPI\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint)
-   [<span data-ttu-id="12cb0-170">**\_contrainte de \_ liaison de sécurité de message WS username \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="12cb0-170">**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)

 

 




