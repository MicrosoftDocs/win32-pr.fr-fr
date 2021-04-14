---
title: Écouteur
description: Un écouteur est utilisé par le client pour accepter un canal entrant d’un service.
ms.assetid: fffda587-23f5-4c7a-93c5-f03d9d3fafb2
keywords:
- Services Web de l’écouteur pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e372f3fa9109647e009f0258c059cc4c2065f6bc
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104383324"
---
# <a name="listener"></a><span data-ttu-id="cd087-106">Écouteur</span><span class="sxs-lookup"><span data-stu-id="cd087-106">Listener</span></span>

<span data-ttu-id="cd087-107">Un écouteur est utilisé par le client pour accepter un [canal](channel.md) entrant d’un service.</span><span class="sxs-lookup"><span data-stu-id="cd087-107">A listener is used by the client to accept an incoming [channel](channel.md) from a service.</span></span>

<span data-ttu-id="cd087-108">Pour créer un écouteur du, vous spécifiez le type de canal en tant que valeur d’énumération de [**\_ \_ type WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) , les informations de [liaison](binding.md) et l' [URL](url.md) à écouter.</span><span class="sxs-lookup"><span data-stu-id="cd087-108">To create a listner, you specify the channel type as a [**WS\_CHANNEL\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) enumeration value, the [binding](binding.md) information, and the [URL](url.md) to listen on.</span></span>


<span data-ttu-id="cd087-109">Pour commencer à écouter sur l’URL, appelez la fonction [**WsOpenListener**](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener) .</span><span class="sxs-lookup"><span data-stu-id="cd087-109">To start listening on the URL, call the [**WsOpenListener**](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener) function.</span></span>

<span data-ttu-id="cd087-110">Pour accepter les communications entrantes, appelez [**WsAcceptChannel**](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel).</span><span class="sxs-lookup"><span data-stu-id="cd087-110">To accept incoming communications, call [**WsAcceptChannel**](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel).</span></span>

<span data-ttu-id="cd087-111">Pour annuler les e/s en attente pour un écouteur, appelez [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener).</span><span class="sxs-lookup"><span data-stu-id="cd087-111">To cancel pending IO for a listener, call [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener).</span></span>

<span data-ttu-id="cd087-112">Pour plus d’informations sur les transitions d’État pour un écouteur, consultez l’énumération de l’état de l' [**\_ \_ écouteur WS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) .</span><span class="sxs-lookup"><span data-stu-id="cd087-112">For information on the state transitions for a listener, see the [**WS\_LISTENER\_STATE**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) enumeration.</span></span>

<span data-ttu-id="cd087-113">Les rappels suivants font partie de l’écouteur :</span><span class="sxs-lookup"><span data-stu-id="cd087-113">The following callbacks are part of the listener:</span></span>

-   [<span data-ttu-id="cd087-114">**rappel de l' \_ \_ écouteur WS Abort \_**</span><span class="sxs-lookup"><span data-stu-id="cd087-114">**WS\_ABORT\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_abort_listener_callback)
-   [<span data-ttu-id="cd087-115">**\_rappel de \_ canal d’acceptation WS \_**</span><span class="sxs-lookup"><span data-stu-id="cd087-115">**WS\_ACCEPT\_CHANNEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_accept_channel_callback)
-   [<span data-ttu-id="cd087-116">**rappel de l' \_ \_ écouteur WS Close \_**</span><span class="sxs-lookup"><span data-stu-id="cd087-116">**WS\_CLOSE\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_close_listener_callback)
-   [<span data-ttu-id="cd087-117">**WS \_ créer un \_ canal \_ pour le rappel de l' \_ écouteur \_**</span><span class="sxs-lookup"><span data-stu-id="cd087-117">**WS\_CREATE\_CHANNEL\_FOR\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_for_listener_callback)
-   [<span data-ttu-id="cd087-118">**création d’un \_ \_ rappel d’ÉCOUTEur WS \_**</span><span class="sxs-lookup"><span data-stu-id="cd087-118">**WS\_CREATE\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_create_listener_callback)
-   [<span data-ttu-id="cd087-119">**rappel de l' \_ \_ écouteur gratuit WS \_**</span><span class="sxs-lookup"><span data-stu-id="cd087-119">**WS\_FREE\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_free_listener_callback)
-   [<span data-ttu-id="cd087-120">**rappel de la propriété de l' \_ \_ ÉCOUTEur WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cd087-120">**WS\_GET\_LISTENER\_PROPERTY\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_get_listener_property_callback)
-   [<span data-ttu-id="cd087-121">**rappel de l' \_ \_ écouteur WS Open \_**</span><span class="sxs-lookup"><span data-stu-id="cd087-121">**WS\_OPEN\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_open_listener_callback)
-   [<span data-ttu-id="cd087-122">**rappel de l' \_ écouteur de réinitialisation WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cd087-122">**WS\_RESET\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_reset_listener_callback)
-   [<span data-ttu-id="cd087-123">**rappel de la propriété de l' \_ \_ écouteur WS Set \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cd087-123">**WS\_SET\_LISTENER\_PROPERTY\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_set_listener_property_callback)

<span data-ttu-id="cd087-124">Les énumérations suivantes font partie de l’écouteur :</span><span class="sxs-lookup"><span data-stu-id="cd087-124">The following enumerations are part of the listener:</span></span>

-   [<span data-ttu-id="cd087-125">**\_version WS IP \_**</span><span class="sxs-lookup"><span data-stu-id="cd087-125">**WS\_IP\_VERSION**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_ip_version)
-   [<span data-ttu-id="cd087-126">**ID de propriété de l' \_ écouteur WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cd087-126">**WS\_LISTENER\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id)
-   [<span data-ttu-id="cd087-127">**État de l' \_ écouteur WS \_**</span><span class="sxs-lookup"><span data-stu-id="cd087-127">**WS\_LISTENER\_STATE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state)

<span data-ttu-id="cd087-128">Les fonctions suivantes font partie de l’écouteur :</span><span class="sxs-lookup"><span data-stu-id="cd087-128">The following functions are part of the listener:</span></span>

-   [<span data-ttu-id="cd087-129">**WsAbortListener**</span><span class="sxs-lookup"><span data-stu-id="cd087-129">**WsAbortListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)
-   [<span data-ttu-id="cd087-130">**WsAcceptChannel**</span><span class="sxs-lookup"><span data-stu-id="cd087-130">**WsAcceptChannel**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel)
-   [<span data-ttu-id="cd087-131">**WsCloseListener**</span><span class="sxs-lookup"><span data-stu-id="cd087-131">**WsCloseListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscloselistener)
-   [<span data-ttu-id="cd087-132">**WsCreateListener**</span><span class="sxs-lookup"><span data-stu-id="cd087-132">**WsCreateListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener)
-   [<span data-ttu-id="cd087-133">**WsFreeListener**</span><span class="sxs-lookup"><span data-stu-id="cd087-133">**WsFreeListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreelistener)
-   [<span data-ttu-id="cd087-134">**WsGetListenerProperty**</span><span class="sxs-lookup"><span data-stu-id="cd087-134">**WsGetListenerProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetlistenerproperty)
-   [<span data-ttu-id="cd087-135">**WsOpenListener**</span><span class="sxs-lookup"><span data-stu-id="cd087-135">**WsOpenListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener)
-   [<span data-ttu-id="cd087-136">**WsResetListener**</span><span class="sxs-lookup"><span data-stu-id="cd087-136">**WsResetListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsresetlistener)
-   [<span data-ttu-id="cd087-137">**WsSetListenerProperty**</span><span class="sxs-lookup"><span data-stu-id="cd087-137">**WsSetListenerProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetlistenerproperty)

<span data-ttu-id="cd087-138">Le handle suivant fait partie de l’écouteur :</span><span class="sxs-lookup"><span data-stu-id="cd087-138">The following handle is part of the listener:</span></span>

-   [<span data-ttu-id="cd087-139">\_écouteur WS</span><span class="sxs-lookup"><span data-stu-id="cd087-139">WS\_LISTENER</span></span>](ws-listener.md)

<span data-ttu-id="cd087-140">Les structures suivantes font partie de l’écouteur :</span><span class="sxs-lookup"><span data-stu-id="cd087-140">The following structures are part of the listener:</span></span>

-   [<span data-ttu-id="cd087-141">**\_ \_ rappels de l’écouteur personnalisé WS \_**</span><span class="sxs-lookup"><span data-stu-id="cd087-141">**WS\_CUSTOM\_LISTENER\_CALLBACKS**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_custom_listener_callbacks)
-   [<span data-ttu-id="cd087-142">**\_ \_ sous- \_ chaînes de l’agent utilisateur non autorisées WS \_**</span><span class="sxs-lookup"><span data-stu-id="cd087-142">**WS\_DISALLOWED\_USER\_AGENT\_SUBSTRINGS**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_disallowed_user_agent_substrings)
-   [<span data-ttu-id="cd087-143">**\_noms d’hôte WS \_**</span><span class="sxs-lookup"><span data-stu-id="cd087-143">**WS\_HOST\_NAMES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_host_names)
-   [<span data-ttu-id="cd087-144">**Propriétés de l' \_ écouteur WS \_**</span><span class="sxs-lookup"><span data-stu-id="cd087-144">**WS\_LISTENER\_PROPERTIES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_listener_properties)
-   [<span data-ttu-id="cd087-145">**propriété de l' \_ écouteur WS \_**</span><span class="sxs-lookup"><span data-stu-id="cd087-145">**WS\_LISTENER\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_listener_property)

 

 




