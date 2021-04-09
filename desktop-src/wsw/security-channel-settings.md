---
title: Paramètres de canal de sécurité
description: Les paramètres de canal de sécurité contrôlent la façon dont la sécurité est appliquée et vérifiée sur un canal.
ms.assetid: ad964874-0bc7-4f03-8ceb-33627ff99f08
keywords:
- Paramètres de canal de sécurité services Web pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fcd0b42b2d5581a5b7c489e9ada70f32abfefa
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104102573"
---
# <a name="security-channel-settings"></a><span data-ttu-id="30882-106">Paramètres de canal de sécurité</span><span class="sxs-lookup"><span data-stu-id="30882-106">Security Channel Settings</span></span>

<span data-ttu-id="30882-107">Les paramètres de canal de sécurité contrôlent la façon dont la sécurité est appliquée et vérifiée sur un canal.</span><span class="sxs-lookup"><span data-stu-id="30882-107">Security channel settings control the way security is applied and verified on a channel.</span></span> <span data-ttu-id="30882-108">Chaque paramètre de canal de sécurité est représenté par une collection de paires propriété-valeur, avec les clés de propriété définies par l’ID de propriété d’énumération [**WS \_ Security \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id).</span><span class="sxs-lookup"><span data-stu-id="30882-108">Each security channel setting is represented by a collection of property-value pairs, with the property keys defined by the enumeration [**WS\_SECURITY\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id).</span></span> <span data-ttu-id="30882-109">Chaque propriété de la collection a une valeur par défaut raisonnable.</span><span class="sxs-lookup"><span data-stu-id="30882-109">Each property in the collection has a reasonable default value.</span></span> <span data-ttu-id="30882-110">En raison de ces valeurs par défaut, il est possible de définir et d’utiliser une description de sécurité sans spécifier les paramètres du canal de sécurité.</span><span class="sxs-lookup"><span data-stu-id="30882-110">Because of these default values, it is possible to define and use a security description without specifying any of the security channel settings.</span></span>


<span data-ttu-id="30882-111">Les [paramètres de liaison de sécurité](security-binding-settings.md) contiennent des collections similaires de paires propriété-valeur dont les clés sont définies par la structure de [**\_ \_ \_ propriété de liaison de sécurité WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property) .</span><span class="sxs-lookup"><span data-stu-id="30882-111">[Security binding settings](security-binding-settings.md) contain similar collections of property-value pairs whose keys are defined by the [**WS\_SECURITY\_BINDING\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property) structure.</span></span> <span data-ttu-id="30882-112">La différence entre ces deux types de paramètres est que les paramètres de canal de sécurité sont étendus à une description de sécurité (autrement dit, ils contiennent des propriétés de sécurité au niveau du canal), alors que les paramètres de liaison de sécurité sont étendus à l’une des liaisons de sécurité et qu’il peut y avoir de nombreuses liaisons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="30882-112">The difference between these two sorts of settings is that the security channel settings are scoped to a security description (that is, they contain channel-wide security properties), whereas security binding settings are scoped to one of the security bindings, and there may be many security bindings.</span></span> <span data-ttu-id="30882-113">Par exemple, une description de sécurité personnalisée qui contient trois liaisons de sécurité aura un sac de paramètres de canal de sécurité pour le canal entier et trois conteneurs de paramètres de liaison de sécurité, un pour chaque liaison de sécurité.</span><span class="sxs-lookup"><span data-stu-id="30882-113">Consequently, for example, a custom security description that contains three security bindings will have one security channel settings bag for the entire channel and three security binding settings bags, one for each security binding.</span></span>

<span data-ttu-id="30882-114">Les énumérations suivantes sont utilisées avec les paramètres de canal de sécurité :</span><span class="sxs-lookup"><span data-stu-id="30882-114">The following enumerations are used with security channel settings:</span></span>

-   [<span data-ttu-id="30882-115">**\_niveau de protection WS \_**</span><span class="sxs-lookup"><span data-stu-id="30882-115">**WS\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level)
-   [<span data-ttu-id="30882-116">**\_ID de \_ propriété du jeton de sécurité de demande WS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="30882-116">**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id)
-   [<span data-ttu-id="30882-117">**\_ID d' \_ algorithme WS Security \_**</span><span class="sxs-lookup"><span data-stu-id="30882-117">**WS\_SECURITY\_ALGORITHM\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_algorithm_id)
-   [<span data-ttu-id="30882-118">**ID de propriété de l' \_ algorithme de sécurité WS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="30882-118">**WS\_SECURITY\_ALGORITHM\_PROPERTY\_ID**</span></span>](/windows/win32/api/webservices/ne-webservices-ws_move_to)
-   [<span data-ttu-id="30882-119">**\_disposition d' \_ en-tête WS Security \_**</span><span class="sxs-lookup"><span data-stu-id="30882-119">**WS\_SECURITY\_HEADER\_LAYOUT**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_header_layout)
-   [<span data-ttu-id="30882-120">**\_version d' \_ en-tête WS Security \_**</span><span class="sxs-lookup"><span data-stu-id="30882-120">**WS\_SECURITY\_HEADER\_VERSION**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_header_version)
-   [<span data-ttu-id="30882-121">**\_ID de \_ propriété de sécurité WS \_**</span><span class="sxs-lookup"><span data-stu-id="30882-121">**WS\_SECURITY\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)
-   [<span data-ttu-id="30882-122">**\_utilisation des \_ horodateurs de sécurité WS \_**</span><span class="sxs-lookup"><span data-stu-id="30882-122">**WS\_SECURITY\_TIMESTAMP\_USAGE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage)
-   [<span data-ttu-id="30882-123">**\_ID de \_ propriété du jeton de sécurité WS XML \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="30882-123">**WS\_XML\_SECURITY\_TOKEN\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_security_token_property_id)

<span data-ttu-id="30882-124">Les structures suivantes sont utilisées avec les paramètres de canal de sécurité :</span><span class="sxs-lookup"><span data-stu-id="30882-124">The following structures are used with security channel settings:</span></span>

-   [<span data-ttu-id="30882-125">**\_propriété de \_ jeton de sécurité de demande WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="30882-125">**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property)
-   [<span data-ttu-id="30882-126">**propriété de l' \_ algorithme de sécurité WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="30882-126">**WS\_SECURITY\_ALGORITHM\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_algorithm_property)
-   [<span data-ttu-id="30882-127">**\_suite d' \_ algorithmes de sécurité de WS \_**</span><span class="sxs-lookup"><span data-stu-id="30882-127">**WS\_SECURITY\_ALGORITHM\_SUITE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_algorithm_suite)
-   [<span data-ttu-id="30882-128">**\_propriété de sécurité WS \_**</span><span class="sxs-lookup"><span data-stu-id="30882-128">**WS\_SECURITY\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_property)
-   [<span data-ttu-id="30882-129">**\_propriété de \_ jeton de sécurité WS XML \_ \_**</span><span class="sxs-lookup"><span data-stu-id="30882-129">**WS\_XML\_SECURITY\_TOKEN\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_security_token_property)

 

 




