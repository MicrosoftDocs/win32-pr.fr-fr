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
ms.openlocfilehash: 4b8b213971a8d4e9872bde86f4ef9c7693eb104aa7289f5fdf3dbf32ce239ab0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089559"
---
# <a name="metadata-import"></a>Importation de métadonnées

Le WWSAPI comprend des éléments d’API qui peuvent être utilisés pour traiter WSDL et la stratégie à partir d’un point de terminaison avec l’objectif d’extraire des informations qui peuvent être utilisées pour communiquer avec le point de terminaison. Ces API sont généralement utilisées lorsque le protocole de communication pris en charge par le point de terminaison n’est pas déjà connu.


Utilisez la séquence suivante pour traiter les métadonnées :

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

Pour plus d’informations sur la façon dont les assertions WSDL et WS-Policy correspondent à l’API, consultez la rubrique [mappage de métadonnées](metadata-mapping.md) .

## <a name="security"></a>Sécurité

Les métadonnées téléchargées sont aussi efficaces que l’adresse utilisée pour le télécharger. Une application doit s’assurer que approuve l’adresse. En outre, une application doit s’assurer qu’elle utilise un protocole de sécurité pour télécharger les documents de métadonnées qui n’autorisent pas la falsification des métadonnées.

Une application doit inspecter les adresses des services exposés par les métadonnées. Par défaut, le runtime garantit que le nom d’hôte du service correspond à celui de l’URL d’origine utilisée pour télécharger les métadonnées, mais que l’application souhaite effectuer des vérifications supplémentaires. Une application peut désactiver la vérification du nom d’hôte en remplaçant la propriété de vérification des noms d’hôtes de la [**\_ \_ propriété \_ \_ \_ WS Metadata**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) . Si la vérification du nom d’hôte effectuée par défaut est désactivée, l’application doit se protéger contre les documents de métadonnées contenant l’adresse d’un service d’un tiers différent qu’il n’approuve pas d’une autre façon.

Par défaut, la quantité maximale de mémoire utilisée par l’exécution des métadonnées pour désérialiser et traiter les métadonnées est de 256 Ko, et le nombre maximal de documents pouvant être ajoutés est de 32. Ces valeurs par défaut peuvent être remplacées par les propriétés de la [**\_ \_ \_ \_ \_ taille demandée du tas de propriétés WS Metadata**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) et de la **propriété WS \_ Metadata \_ Property \_ \_ documents Max** . Ces limites sont conçues pour limiter la quantité de téléchargements et limiter la quantité de mémoire allouée pour accumuler les métadonnées. L’amélioration de ces valeurs peut entraîner une utilisation excessive de la mémoire, de l’utilisation du processeur ou de la bande passante réseau. Notez que, en raison de l’expansion des chaînes de dictionnaire au format binaire, un petit message peut aboutir à une forme désérialisée bien plus grande. par conséquent, le fait de compter sur des messages de petite taille pour limiter l’allocation de mémoire de métadonnées n’est pas suffisant lors de l’utilisation du format binaire.

Par défaut, le nombre maximal d’alternatives de stratégie est de 32, bien qu’il puisse être remplacé par la propriété [**\_ \_ propriétés \_ Max \_ alternatives de la stratégie WS**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id) . Si une application parcourt chaque alternative à la recherche d’une correspondance, il peut être nécessaire d’effectuer une recherche dans toutes les alternatives avant de trouver une correspondance. L’amélioration du nombre maximal d’alternatives peut entraîner une utilisation excessive du processeur.

Les énumérations suivantes font partie de l’importation des métadonnées :

-   [**\_ID de propriété de métadonnées WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id)
-   [**\_État des métadonnées WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_state)
-   [**\_type d' \_ extension de stratégie WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_extension_type)
-   [**\_ID de \_ propriété de stratégie WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id)
-   [**État de la \_ stratégie WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_state)
-   [**\_type de \_ contrainte de liaison de sécurité WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_constraint_type)

Les fonctions suivantes font partie de l’importation des métadonnées :

-   [**WsCreateMetadata**](/windows/desktop/api/WebServices/nf-webservices-wscreatemetadata)
-   [**WsFreeMetadata**](/windows/desktop/api/WebServices/nf-webservices-wsfreemetadata)
-   [**WsGetMetadataEndpoints**](/windows/desktop/api/WebServices/nf-webservices-wsgetmetadataendpoints)
-   [**WsGetMetadataProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmetadataproperty)
-   [**WsGetMissingMetadataDocumentAddress**](/windows/desktop/api/WebServices/nf-webservices-wsgetmissingmetadatadocumentaddress)
-   [**WsGetPolicyAlternativeCount**](/windows/desktop/api/WebServices/nf-webservices-wsgetpolicyalternativecount)
-   [**WsGetPolicyProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetpolicyproperty)
-   [**WsMatchPolicyAlternative**](/windows/desktop/api/WebServices/nf-webservices-wsmatchpolicyalternative)
-   [**WsReadMetadata**](/windows/desktop/api/WebServices/nf-webservices-wsreadmetadata)
-   [**WsResetMetadata**](/windows/desktop/api/WebServices/nf-webservices-wsresetmetadata)

Les handles suivants font partie de l’importation des métadonnées :

-   [\_métadonnées WS](ws-metadata.md)
-   [\_stratégie WS](ws-policy.md)

Les structures suivantes font partie de l’importation des métadonnées :

-   [**\_contrainte de \_ liaison de sécurité de message WS CERT \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**\_contrainte de \_ propriété de canal WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property_constraint)
-   [**EXTENSION de stratégie de point de \_ terminaison WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_policy_extension)
-   [**\_contrainte de \_ \_ liaison de \_ sécurité \_ d’en-tête \_ WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint)
-   [**\_contrainte de \_ \_ liaison de sécurité de message de jeton \_ WS \_ émis \_**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)
-   [**\_contrainte de \_ \_ liaison de \_ sécurité de message \_ \_ WS Kerberos APREQ**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**\_point de terminaison de métadonnées WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_endpoint)
-   [**\_points de terminaison de métadonnées WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_endpoints)
-   [**\_propriété de métadonnées WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_property)
-   [**\_contraintes de stratégie WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_policy_constraints)
-   [**\_extension de stratégie WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_policy_extension)
-   [**Propriétés de la \_ stratégie WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_policy_properties)
-   [**\_propriété de stratégie WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_policy_property)
-   [**\_contrainte de \_ propriété de jeton de sécurité de demande WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint)
-   [**\_contrainte de \_ liaison de sécurité WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_constraint)
-   [**\_contrainte de \_ propriété de liaison WS Security \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property_constraint)
-   [**\_contraintes de sécurité WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_constraints)
-   [**\_contrainte de \_ \_ liaison de sécurité de message de contexte \_ de \_ sécurité WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint)
-   [**\_contrainte de \_ propriété de sécurité WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_property_constraint)
-   [**\_contrainte de \_ liaison de sécurité de transport WS SSL \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint)
-   [**contrainte de liaison de sécurité de transport de WS \_ TCP \_ SSPI \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint)
-   [**\_contrainte de \_ liaison de sécurité de message WS username \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)

 

 




