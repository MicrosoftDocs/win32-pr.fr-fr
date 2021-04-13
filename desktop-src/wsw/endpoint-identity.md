---
title: Identité du point de terminaison
description: Les types définis dans cette section sont utilisés pour définir l’identité de sécurité d’une adresse de point de terminaison.
ms.assetid: 39639b9a-32e2-44d2-9bda-a2ad23850de8
keywords:
- Services Web de l’identité du point de terminaison pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7a3f7b95d5fc1b926d8bafb49b06f96c7d68fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379635"
---
# <a name="endpoint-identity"></a><span data-ttu-id="64b5f-106">Identité du point de terminaison</span><span class="sxs-lookup"><span data-stu-id="64b5f-106">Endpoint Identity</span></span>

<span data-ttu-id="64b5f-107">Les types définis dans cette section sont utilisés pour définir l’identité de sécurité d’une adresse de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="64b5f-107">The types defined in this section are used to define the security identity of an endpoint address.</span></span>

<span data-ttu-id="64b5f-108">Les éléments d’API suivants font partie de la mise en retrait du point de terminaison :</span><span class="sxs-lookup"><span data-stu-id="64b5f-108">The following API elements are part of endpoint indentity:</span></span>



| <span data-ttu-id="64b5f-109">Énumération</span><span class="sxs-lookup"><span data-stu-id="64b5f-109">Enumeration</span></span>                                                       | <span data-ttu-id="64b5f-110">Description</span><span class="sxs-lookup"><span data-stu-id="64b5f-110">Description</span></span>                                                                                                                   |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64b5f-111">**TYPE d’identité du point de \_ terminaison WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="64b5f-111">**WS\_ENDPOINT\_IDENTITY\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_endpoint_identity_type) | <span data-ttu-id="64b5f-112">Type de l’identité du point de terminaison, utilisé comme sélecteur pour les sous-types de l' [**\_ \_ identité du point de terminaison WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_identity).</span><span class="sxs-lookup"><span data-stu-id="64b5f-112">The type of the endpoint identity, used as a selector for subtypes of [**WS\_ENDPOINT\_IDENTITY**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_identity).</span></span> |



 



| <span data-ttu-id="64b5f-113">Structure</span><span class="sxs-lookup"><span data-stu-id="64b5f-113">Structure</span></span>                                                               | <span data-ttu-id="64b5f-114">Description</span><span class="sxs-lookup"><span data-stu-id="64b5f-114">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64b5f-115">**\_identité du \_ point de terminaison du certificat WS \_**</span><span class="sxs-lookup"><span data-stu-id="64b5f-115">**WS\_CERT\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_endpoint_identity)       | <span data-ttu-id="64b5f-116">Type de l’identité du point de terminaison du certificat.</span><span class="sxs-lookup"><span data-stu-id="64b5f-116">The type for certificate endpoint identity .</span></span>                                                 |
| [<span data-ttu-id="64b5f-117">**\_identité du \_ point de terminaison WS DNS \_**</span><span class="sxs-lookup"><span data-stu-id="64b5f-117">**WS\_DNS\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_dns_endpoint_identity)         | <span data-ttu-id="64b5f-118">Type pour la spécification d’une identité de point de terminaison représentée par un nom DNS.</span><span class="sxs-lookup"><span data-stu-id="64b5f-118">The type for specifying an endpoint identity represented by a DNS name.</span></span>                      |
| [<span data-ttu-id="64b5f-119">**\_identité du point de terminaison WS \_**</span><span class="sxs-lookup"><span data-stu-id="64b5f-119">**WS\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_identity)                  | <span data-ttu-id="64b5f-120">Type de base pour toutes les identités de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="64b5f-120">The base type for all endpoint identities.</span></span>                                                   |
| [<span data-ttu-id="64b5f-121">**\_identité du \_ point de terminaison WS RSA \_**</span><span class="sxs-lookup"><span data-stu-id="64b5f-121">**WS\_RSA\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_rsa_endpoint_identity)         | <span data-ttu-id="64b5f-122">Type de l’identité du point de terminaison RSA.</span><span class="sxs-lookup"><span data-stu-id="64b5f-122">Type for RSA endpoint identity.</span></span>                                                              |
| [<span data-ttu-id="64b5f-123">**\_identité du \_ point de terminaison WS SPN \_**</span><span class="sxs-lookup"><span data-stu-id="64b5f-123">**WS\_SPN\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_spn_endpoint_identity)         | <span data-ttu-id="64b5f-124">Type pour la spécification d’une identité de point de terminaison représentée par un SPN (nom de principal du service).</span><span class="sxs-lookup"><span data-stu-id="64b5f-124">The type for specifying an endpoint identity represented by an SPN (service principal name).</span></span> |
| [<span data-ttu-id="64b5f-125">**\_identité du \_ point de terminaison WS inconnue \_**</span><span class="sxs-lookup"><span data-stu-id="64b5f-125">**WS\_UNKNOWN\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_unknown_endpoint_identity) | <span data-ttu-id="64b5f-126">Type pour une identité de point de terminaison inconnue.</span><span class="sxs-lookup"><span data-stu-id="64b5f-126">The type for an unknown endpoint identity.</span></span>                                                   |
| [<span data-ttu-id="64b5f-127">**\_identité du \_ point de terminaison UPN WS \_**</span><span class="sxs-lookup"><span data-stu-id="64b5f-127">**WS\_UPN\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_upn_endpoint_identity)         | <span data-ttu-id="64b5f-128">Type pour la spécification d’une identité de point de terminaison représentée par un UPN (nom d’utilisateur principal).</span><span class="sxs-lookup"><span data-stu-id="64b5f-128">The type for specifying an endpoint identity represented by a UPN (user principal name).</span></span>     |



 

 

 




