---
title: Adresse du point de terminaison
description: Une adresse de point de terminaison représente l’adresse d’un service sur le réseau.
ms.assetid: 5df9c0da-6648-42a0-ae87-06844461042a
keywords:
- Service Web d’adresse de point de terminaison pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 787326197bc73d57945720c34773d33b613a4aab
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2021
ms.locfileid: "104553592"
---
# <a name="endpoint-address"></a><span data-ttu-id="c717d-106">Adresse du point de terminaison</span><span class="sxs-lookup"><span data-stu-id="c717d-106">Endpoint Address</span></span>

<span data-ttu-id="c717d-107">Une adresse de point de terminaison représente l’adresse d’un service sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="c717d-107">An endpoint address represents the address of a service on the network.</span></span> <span data-ttu-id="c717d-108">Lorsque vous ouvrez un [canal](channel.md), en appelant la fonction [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) , vous devez fournir l’adresse du point de terminaison du service avec lequel vous communiquez, ainsi que la spécification du canal que vous souhaitez ouvrir.</span><span class="sxs-lookup"><span data-stu-id="c717d-108">When you open a [channel](channel.md), by calling the [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) function, you need to provide the endpoint address of the service you which to communicate with, as well as specifying the channel you wish to open.</span></span>


<span data-ttu-id="c717d-109">Une adresse de point de terminaison se compose des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="c717d-109">An endpoint address consists of:</span></span>

-   <span data-ttu-id="c717d-110">une [URL](url.md)</span><span class="sxs-lookup"><span data-stu-id="c717d-110">a [URL](url.md)</span></span>
-   <span data-ttu-id="c717d-111">un ensemble d’en-têtes (facultatif)</span><span class="sxs-lookup"><span data-stu-id="c717d-111">a set of headers (optional)</span></span>
-   <span data-ttu-id="c717d-112">ensemble d’extensions (facultatif)</span><span class="sxs-lookup"><span data-stu-id="c717d-112">a set of extensions (optional)</span></span>
-   <span data-ttu-id="c717d-113">[identité](endpoint-identity.md) facultative représentant l’identité de sécurité du service.</span><span class="sxs-lookup"><span data-stu-id="c717d-113">an optional [identity](endpoint-identity.md) representing the security identity of the service.</span></span>

<span data-ttu-id="c717d-114">Lorsqu’un message est adressé, l’URL devient l’en-tête « to » du message.</span><span class="sxs-lookup"><span data-stu-id="c717d-114">When a message is addressed, the URL becomes the "To" header of the message.</span></span> <span data-ttu-id="c717d-115">Tous les en-têtes qui font partie de l’adresse du point de terminaison sont également ajoutés au message.</span><span class="sxs-lookup"><span data-stu-id="c717d-115">Any headers that are part of the endpoint address are also added to the message.</span></span>

![Diagramme montrant les en-têtes d’adresse de point de terminaison ajoutés à un message.](images/endpointaddress.png)

<span data-ttu-id="c717d-117">Les canaux traitent automatiquement tous les messages envoyés à l’aide de la structure d' [**\_ \_ adresse du point de terminaison WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) qui a été transmise à [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel).</span><span class="sxs-lookup"><span data-stu-id="c717d-117">Channels automatically address any messages that are sent, using the [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) structure that was passed to the [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel).</span></span> <span data-ttu-id="c717d-118">Vous pouvez également utiliser la fonction [**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) pour remplacer ce comportement par défaut.</span><span class="sxs-lookup"><span data-stu-id="c717d-118">You can also use the [**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) function to override this default behavior.</span></span>

<span data-ttu-id="c717d-119">Lorsque [**l' \_ \_ adresse du point de terminaison WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) est transmise en tant que paramètre, les fonctions [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) et [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) créent une copie du paramètre d' **\_ \_ adresse du point de terminaison WS** en mémoire et sa taille est limitée par 65536 octets.</span><span class="sxs-lookup"><span data-stu-id="c717d-119">When [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) is passed as a parameter, the [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) and [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) functions create a copy of the **WS\_ENDPOINT\_ADDRESS** parameter in memory and its size is limited by 65536 bytes.</span></span> <span data-ttu-id="c717d-120">[**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) n’a pas cette limitation, car il ne nécessite pas la création d’une copie du paramètre d' **\_ \_ adresse du point de terminaison WS** .</span><span class="sxs-lookup"><span data-stu-id="c717d-120">[**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) does not have this limitation because it does not require creating a copy of the **WS\_ENDPOINT\_ADDRESS** parameter.</span></span>

<span data-ttu-id="c717d-121">Les extensions spécifiées dans le champ **Extensions** de l' [**adresse de point de \_ terminaison \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) ne sont pas utilisées pour traiter le message, mais sont plutôt un mécanisme d’extensibilité qui peut être utilisé pour fournir des informations supplémentaires (par exemple, des métadonnées) sur le service.</span><span class="sxs-lookup"><span data-stu-id="c717d-121">The extensions specified in the **extensions** field of [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) are not used for addressing the message but instead are an extensibility mechanism that can be used to provide additional information (for example, metadata) about the service.</span></span> <span data-ttu-id="c717d-122">Les extensions communes peuvent être lues à l’aide de la fonction [**WsReadEndpointAddressExtension**](/windows/desktop/api/WebServices/nf-webservices-wsreadendpointaddressextension) .</span><span class="sxs-lookup"><span data-stu-id="c717d-122">Common extensions can be read with the [**WsReadEndpointAddressExtension**](/windows/desktop/api/WebServices/nf-webservices-wsreadendpointaddressextension) function.</span></span>

<span data-ttu-id="c717d-123">Le champ d’identité facultatif de l’adresse du point de terminaison peut inclure, par exemple, le nom DNS de l’ordinateur sur lequel le service est en cours d’exécution, ou l’UPN du compte Windows sous lequel le service s’exécute.</span><span class="sxs-lookup"><span data-stu-id="c717d-123">The optional identity field of the endpoint address can include, for example, the DNS name of the machine on which the service is running, or the UPN of the Windows account under which the service is running.</span></span> <span data-ttu-id="c717d-124">Le champ d’identité n’est pas utilisé pour traiter le message, mais peut être utilisé pour obtenir un jeton de sécurité pour le service (par exemple, pour obtenir un ticket Kerberos pour l’UPN cible) et pour vérifier l’identité des réponses du service (par exemple, une identité DNS utilisée pour les contrôles de nom sur le certificat de service renvoyé pendant le protocole SSL).</span><span class="sxs-lookup"><span data-stu-id="c717d-124">The identity field is not used in addressing the message, but may be used for obtaining a security token for the service (for example, for obtaining a Kerberos ticket to the target UPN) and for verifying the identity of the service replies (for example, a DNS identity used for name checks on the service certificate returned during SSL).</span></span>

<span data-ttu-id="c717d-125">Les adresses de point de terminaison peuvent être lues et écrites à l’aide de la [sérialisation](serialization.md) avec la valeur d’énumération du type d’adresse du **point de \_ terminaison \_ \_ WS** du [**\_ type WS**](/windows/desktop/api/WebServices/ne-webservices-ws_type).</span><span class="sxs-lookup"><span data-stu-id="c717d-125">Endpoint addresses can be read and written using [serialization](serialization.md) with the **WS\_ENDPOINT\_ADDRESS\_TYPE** enumeration value from [**WS\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_type).</span></span> <span data-ttu-id="c717d-126">Remarque pour sérialiser une adresse de point de terminaison, vous devez connaître la version de la spécification utilisée pour les en-têtes d’adressage, comme spécifié dans l’énumération de la [**\_ \_ version de l’adressage WS**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) .</span><span class="sxs-lookup"><span data-stu-id="c717d-126">Note in order to serialize an endpoint address, you must know the version of the specification used for the addressing headers, as specified in the [**WS\_ADDRESSING\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) enumeration.</span></span>

 

 




