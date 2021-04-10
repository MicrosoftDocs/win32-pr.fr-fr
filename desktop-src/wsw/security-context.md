---
title: Contexte de sécurité
description: Les contextes de sécurité permettent d’établir un contexte de sécurité de message conformément à WS-SecureConversation.
ms.assetid: bea92650-21bd-41d4-9dba-043d6779d85f
keywords:
- Contexte de sécurité natif-services Web
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cff86ea12ae7a4b8bd554e25cde534cba3b4dcb4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104316788"
---
# <a name="security-context"></a><span data-ttu-id="54bdf-106">Contexte de sécurité</span><span class="sxs-lookup"><span data-stu-id="54bdf-106">Security Context</span></span>

<span data-ttu-id="54bdf-107">Les contextes de sécurité permettent d’établir un contexte de sécurité de message conformément à WS-SecureConversation.</span><span class="sxs-lookup"><span data-stu-id="54bdf-107">Security contexts enable the establishment of a message security context according to WS-SecureConversation.</span></span> <span data-ttu-id="54bdf-108">Ce contexte peut ensuite être utilisé pour sécuriser les messages en guise d’alternative à la sécurité à un seul moment où les informations d’identification sont transmises pour chaque demande.</span><span class="sxs-lookup"><span data-stu-id="54bdf-108">That context can then be used to secure messages as an alternative to one-shot security where the credentials are transmitted for every request.</span></span> <span data-ttu-id="54bdf-109">Le contexte de sécurité établi est une méthode plus efficace pour sécuriser les messages lors de l’échange de plusieurs messages.</span><span class="sxs-lookup"><span data-stu-id="54bdf-109">The established security context is a more efficient method of securing messages when multiple messages are exchanged.</span></span>


<span data-ttu-id="54bdf-110">Les contextes de sécurité nécessitent la présence des informations d’identification de sécurité de démarrage utilisées pour sécuriser les messages envoyés dans le contexte.</span><span class="sxs-lookup"><span data-stu-id="54bdf-110">Security contexts require the presence of bootstrap security credentials that are used to secure the messages sent in the context.</span></span> <span data-ttu-id="54bdf-111">Les structures de liaison de sécurité de message WS [**\_ Kerberos \_ APREQ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding), de [**\_ \_ \_ \_ \_ liaison**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding)de sécurité de message de jeton WS XML et [**WS \_ UserName \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) peuvent être utilisées à cette fin.</span><span class="sxs-lookup"><span data-stu-id="54bdf-111">The [**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding), [**WS\_XML\_TOKEN\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding), and [**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) structures may be used for this purpose.</span></span>

<span data-ttu-id="54bdf-112">Les contextes de sécurité sont une fonctionnalité de sécurité des messages et sont configurés par le biais de liaisons de sécurité de message.</span><span class="sxs-lookup"><span data-stu-id="54bdf-112">Security contexts are a message security feature and are configured by way of message security bindings.</span></span>

## <a name="client"></a><span data-ttu-id="54bdf-113">Client</span><span class="sxs-lookup"><span data-stu-id="54bdf-113">Client</span></span>

<span data-ttu-id="54bdf-114">Du côté client, le contexte de sécurité est lié à un canal particulier.</span><span class="sxs-lookup"><span data-stu-id="54bdf-114">On the client side, the security context is tied to a particular channel.</span></span> <span data-ttu-id="54bdf-115">Il est configuré à l’aide de la [**liaison de sécurité de message de \_ contexte de sécurité \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding).</span><span class="sxs-lookup"><span data-stu-id="54bdf-115">It is configured using the [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding).</span></span> <span data-ttu-id="54bdf-116">Le comportement et la durée de vie du contexte sont déterminés par le canal.</span><span class="sxs-lookup"><span data-stu-id="54bdf-116">Behavior and lifetime of the context are determined by the channel.</span></span> <span data-ttu-id="54bdf-117">Lorsque le premier message est envoyé sur le canal, le contexte de sécurité est établi.</span><span class="sxs-lookup"><span data-stu-id="54bdf-117">When the first message is sent on the channel, the security context is established.</span></span> <span data-ttu-id="54bdf-118">Après cela, le contexte est renouvelé de manière proactive à un intervalle configurable.</span><span class="sxs-lookup"><span data-stu-id="54bdf-118">After that, the context is proactively renewed at a configurable interval.</span></span> <span data-ttu-id="54bdf-119">Si le serveur retourne une erreur indiquant que le contexte nécessite un renouvellement, le contexte est renouvelé lors de l’envoi du message suivant.</span><span class="sxs-lookup"><span data-stu-id="54bdf-119">If the server returns a fault indicating that the context requires renewal, the context is renewed when the next message is sent.</span></span> <span data-ttu-id="54bdf-120">Si le canal est à l’état ouvert, le contexte est annulé par un message d’annulation lorsque le canal est fermé.</span><span class="sxs-lookup"><span data-stu-id="54bdf-120">If the channel is in the open state, the context is canceled by a cancel message when the channel is closed.</span></span>

## <a name="server"></a><span data-ttu-id="54bdf-121">Serveur</span><span class="sxs-lookup"><span data-stu-id="54bdf-121">Server</span></span>

<span data-ttu-id="54bdf-122">Sur le serveur, un contexte de sécurité est configuré de la même façon que sur le client.</span><span class="sxs-lookup"><span data-stu-id="54bdf-122">On the server, a security context is configured the same way as on the client.</span></span> <span data-ttu-id="54bdf-123">Toutefois, il n’est pas lié à un canal particulier.</span><span class="sxs-lookup"><span data-stu-id="54bdf-123">However, it is not tied to any particular channel.</span></span> <span data-ttu-id="54bdf-124">Au lieu de cela, tous les canaux créés pour l’écouteur qui a le jeu de [**liaisons de sécurité de message du \_ contexte de sécurité \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) peuvent recevoir des messages avec l’un des contextes de sécurité qui ont été établis sur les canaux de cet écouteur.</span><span class="sxs-lookup"><span data-stu-id="54bdf-124">Instead, all channels created for the listener that has the [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) set are capable of receiving messages with any of the security contexts that were established on channels of that listener.</span></span>

<span data-ttu-id="54bdf-125">Lorsqu’un message arrive sur un canal qui prend en charge les contextes de sécurité, le contexte utilisé par ce message peut être obtenu en appelant la fonction [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) avec le contexte de sécurité de la [**propriété de \_ message \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id).</span><span class="sxs-lookup"><span data-stu-id="54bdf-125">When a message arrives on a channel that supports security contexts, the context used by that message can by obtained by calling the [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) function with the [**WS\_MESSAGE\_PROPERTY\_SECURITY\_CONTEXT**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id).</span></span> <span data-ttu-id="54bdf-126">La valeur récupérée peut être utilisée avec [**WsRevokeSecurityContext**](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext) et [**WsGetSecurityContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty).</span><span class="sxs-lookup"><span data-stu-id="54bdf-126">The retrieved value can be used with [**WsRevokeSecurityContext**](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext) and [**WsGetSecurityContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty).</span></span>

## <a name="metadata"></a><span data-ttu-id="54bdf-127">Métadonnées</span><span class="sxs-lookup"><span data-stu-id="54bdf-127">Metadata</span></span>

<span data-ttu-id="54bdf-128">La structure de contrainte de liaison de [**\_ \_ sécurité de \_ message de \_ \_ \_ contexte**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) de sécurité WS est utilisée pour extraire la stratégie de contexte de sécurité des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="54bdf-128">The [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) structure is used to extract the security context policy from metadata.</span></span> <span data-ttu-id="54bdf-129">Pour plus d’informations, consultez [importation de métadonnées](metadata-import.md).</span><span class="sxs-lookup"><span data-stu-id="54bdf-129">For more information, see [Metadata Import](metadata-import.md).</span></span>

<span data-ttu-id="54bdf-130">Les éléments d’API suivants sont utilisés avec les contextes de sécurité.</span><span class="sxs-lookup"><span data-stu-id="54bdf-130">The following API elements are used with security contexts.</span></span>

| <span data-ttu-id="54bdf-131">Énumération</span><span class="sxs-lookup"><span data-stu-id="54bdf-131">Enumeration</span></span>                                                                    | <span data-ttu-id="54bdf-132">Description</span><span class="sxs-lookup"><span data-stu-id="54bdf-132">Description</span></span>                                         |
|--------------------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="54bdf-133">**\_ID de \_ propriété de contexte WS Security \_ \_**</span><span class="sxs-lookup"><span data-stu-id="54bdf-133">**WS\_SECURITY\_CONTEXT\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_context_property_id) | <span data-ttu-id="54bdf-134">Identifie une propriété d’un objet de contexte de sécurité.</span><span class="sxs-lookup"><span data-stu-id="54bdf-134">Identifies a property of a security context object.</span></span> |



 



| <span data-ttu-id="54bdf-135">Fonction</span><span class="sxs-lookup"><span data-stu-id="54bdf-135">Function</span></span>                                                             | <span data-ttu-id="54bdf-136">Description</span><span class="sxs-lookup"><span data-stu-id="54bdf-136">Description</span></span>                                        |
|----------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="54bdf-137">**WsGetSecurityContextProperty**</span><span class="sxs-lookup"><span data-stu-id="54bdf-137">**WsGetSecurityContextProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty) | <span data-ttu-id="54bdf-138">Obtient une propriété du contexte de sécurité spécifié.</span><span class="sxs-lookup"><span data-stu-id="54bdf-138">Gets a property of the specified security context.</span></span> |
| [<span data-ttu-id="54bdf-139">**WsRevokeSecurityContext**</span><span class="sxs-lookup"><span data-stu-id="54bdf-139">**WsRevokeSecurityContext**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext)           | <span data-ttu-id="54bdf-140">Révoque un contexte de sécurité.</span><span class="sxs-lookup"><span data-stu-id="54bdf-140">Revokes a security context.</span></span>                        |



 



| <span data-ttu-id="54bdf-141">Handle</span><span class="sxs-lookup"><span data-stu-id="54bdf-141">Handle</span></span>                                           | <span data-ttu-id="54bdf-142">Description</span><span class="sxs-lookup"><span data-stu-id="54bdf-142">Description</span></span>                                                 |
|--------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="54bdf-143">\_contexte de sécurité WS \_</span><span class="sxs-lookup"><span data-stu-id="54bdf-143">WS\_SECURITY\_CONTEXT</span></span>](ws-security-context.md) | <span data-ttu-id="54bdf-144">Type opaque utilisé pour référencer un objet de contexte de sécurité.</span><span class="sxs-lookup"><span data-stu-id="54bdf-144">An opaque type used to reference a security context object.</span></span> |



 



| <span data-ttu-id="54bdf-145">Structure</span><span class="sxs-lookup"><span data-stu-id="54bdf-145">Structure</span></span>                                                               | <span data-ttu-id="54bdf-146">Description</span><span class="sxs-lookup"><span data-stu-id="54bdf-146">Description</span></span>                                                               |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="54bdf-147">**\_propriété de \_ contexte de sécurité WS \_**</span><span class="sxs-lookup"><span data-stu-id="54bdf-147">**WS\_SECURITY\_CONTEXT\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_property) | <span data-ttu-id="54bdf-148">Définit une propriété d’un [ \_ \_ contexte de sécurité WS](ws-security-context.md).</span><span class="sxs-lookup"><span data-stu-id="54bdf-148">Defines a property of a [WS\_SECURITY\_CONTEXT](ws-security-context.md).</span></span> |



 

 

 




