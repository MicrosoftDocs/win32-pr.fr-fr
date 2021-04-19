---
title: Proxy
description: Un proxy réside dans l’espace d’adressage du processus appelant et agit comme un substitut pour l’objet distant.
ms.assetid: 6c82f655-ac46-4ed9-992b-0387b324a8f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a11257dd060f51bef118a4afc0cc35acf995c111
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/03/2021
ms.locfileid: "106538416"
---
# <a name="proxy"></a><span data-ttu-id="100fd-103">Proxy</span><span class="sxs-lookup"><span data-stu-id="100fd-103">Proxy</span></span>

<span data-ttu-id="100fd-104">Un proxy réside dans l’espace d’adressage du processus appelant et agit comme un substitut pour l’objet distant.</span><span class="sxs-lookup"><span data-stu-id="100fd-104">A proxy resides in the address space of the calling process and acts as a surrogate for the remote object.</span></span> <span data-ttu-id="100fd-105">Du point de vue de l’objet appelant, le proxy est l’objet.</span><span class="sxs-lookup"><span data-stu-id="100fd-105">From the perspective of the calling object, the proxy is the object.</span></span> <span data-ttu-id="100fd-106">En règle générale, le rôle du proxy consiste à empaqueter les paramètres d’interface pour les appels aux méthodes dans ses interfaces d’objet.</span><span class="sxs-lookup"><span data-stu-id="100fd-106">Typically, the proxy's role is to package the interface parameters for calls to methods in its object interfaces.</span></span> <span data-ttu-id="100fd-107">Le proxy transmet les paramètres dans une mémoire tampon de messages et passe la mémoire tampon sur le canal, qui gère le transport entre les processus.</span><span class="sxs-lookup"><span data-stu-id="100fd-107">The proxy packages the parameters into a message buffer and passes the buffer onto the channel, which handles the transport between processes.</span></span> <span data-ttu-id="100fd-108">Le proxy est implémenté sous la forme d’un objet d’agrégation, ou composite.</span><span class="sxs-lookup"><span data-stu-id="100fd-108">The proxy is implemented as an aggregate, or composite, object.</span></span> <span data-ttu-id="100fd-109">Il contient une partie fournie par le système, appelée gestionnaire proxy et un ou plusieurs composants spécifiques à l’interface appelés proxys d’interface.</span><span class="sxs-lookup"><span data-stu-id="100fd-109">It contains a system-provided, manager piece called the proxy manager and one or more interface-specific components called interface proxies.</span></span> <span data-ttu-id="100fd-110">Le nombre de proxys d’interface est égal au nombre d’interfaces d’objets qui ont été exposées à ce client particulier.</span><span class="sxs-lookup"><span data-stu-id="100fd-110">The number of interface proxies equals the number of object interfaces that have been exposed to that particular client.</span></span> <span data-ttu-id="100fd-111">Pour le client qui respecte le modèle d’objet de composant, le proxy semble être l’objet réel.</span><span class="sxs-lookup"><span data-stu-id="100fd-111">To the client complying with the component object model, the proxy appears to be the real object.</span></span>

> [!Note]  
> <span data-ttu-id="100fd-112">Avec le marshaling personnalisé, le proxy peut être implémenté de la même façon ou il peut communiquer directement avec l’objet sans utiliser de stub.</span><span class="sxs-lookup"><span data-stu-id="100fd-112">With custom marshaling, the proxy can be implemented similarly or it can communicate directly with the object without using a stub.</span></span>

 

<span data-ttu-id="100fd-113">Chaque proxy d’interface est un objet de composant qui implémente le code de marshaling pour l’une des interfaces de l’objet.</span><span class="sxs-lookup"><span data-stu-id="100fd-113">Each interface proxy is a component object that implements the marshaling code for one of the object's interfaces.</span></span> <span data-ttu-id="100fd-114">Le proxy représente l’objet pour lequel il fournit le code de marshaling.</span><span class="sxs-lookup"><span data-stu-id="100fd-114">The proxy represents the object for which it provides marshaling code.</span></span> <span data-ttu-id="100fd-115">Chaque proxy implémente également l’interface [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) .</span><span class="sxs-lookup"><span data-stu-id="100fd-115">Each proxy also implements the [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) interface.</span></span> <span data-ttu-id="100fd-116">Bien que l’interface d’objet représentée par le proxy soit publique, l’implémentation de **IRpcProxyBuffer** est privée et est utilisée en interne dans le proxy.</span><span class="sxs-lookup"><span data-stu-id="100fd-116">Although the object interface represented by the proxy is public, the **IRpcProxyBuffer** implementation is private and is used internally within the proxy.</span></span> <span data-ttu-id="100fd-117">Le gestionnaire proxy effectue le suivi des proxies d’interface et contient également l’implémentation publique de l’interface de contrôle [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) pour l’agrégat.</span><span class="sxs-lookup"><span data-stu-id="100fd-117">The proxy manager keeps track of the interface proxies and also contains the public implementation of the controlling [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface for the aggregate.</span></span> <span data-ttu-id="100fd-118">Chaque proxy d’interface peut exister dans une DLL distincte qui est chargée lorsque l’interface qu’il prend en charge est matérialisée au client.</span><span class="sxs-lookup"><span data-stu-id="100fd-118">Each interface proxy can exist in a separate DLL that is loaded when the interface it supports is materialized to the client.</span></span>

## <a name="structure-of-the-proxy"></a><span data-ttu-id="100fd-119">Structure du proxy</span><span class="sxs-lookup"><span data-stu-id="100fd-119">Structure of the Proxy</span></span>

<span data-ttu-id="100fd-120">Le diagramme suivant illustre la structure d’un proxy qui prend en charge le marshaling standard de paramètres appartenant à deux interfaces : IA1 et IA2.</span><span class="sxs-lookup"><span data-stu-id="100fd-120">The following diagram shows the structure of a proxy that supports the standard marshaling of parameters belonging to two interfaces: IA1 and IA2.</span></span> <span data-ttu-id="100fd-121">Chaque proxy d’interface implémente [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) pour la communication interne entre les éléments d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="100fd-121">Each interface proxy implements [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) for internal communication between the aggregate pieces.</span></span> <span data-ttu-id="100fd-122">Lorsque le proxy est prêt à passer ses paramètres marshalés à travers la limite de processus, il appelle des méthodes dans l’interface [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) , qui est implémentée par le canal.</span><span class="sxs-lookup"><span data-stu-id="100fd-122">When the proxy is ready to pass its marshaled parameters across the process boundary, it calls methods in the [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) interface, which is implemented by the channel.</span></span> <span data-ttu-id="100fd-123">Le canal transfère à son tour l’appel à la bibliothèque Runtime RPC afin qu’il puisse atteindre sa destination dans l’objet.</span><span class="sxs-lookup"><span data-stu-id="100fd-123">The channel in turn forwards the call to the RPC run-time library so that it can reach its destination in the object.</span></span>

![Diagramme qui montre la structure du proxy.](images/4432d8d3-dfab-4635-90f8-408aecf70134.png)

## <a name="related-topics"></a><span data-ttu-id="100fd-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="100fd-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="100fd-126">Channel</span><span class="sxs-lookup"><span data-stu-id="100fd-126">Channel</span></span>](channel.md)
</dt> <dt>

[<span data-ttu-id="100fd-127">Communication entre les objets</span><span class="sxs-lookup"><span data-stu-id="100fd-127">Inter-Object Communication</span></span>](inter-object-communication.md)
</dt> <dt>

[<span data-ttu-id="100fd-128">Détails du marshaling</span><span class="sxs-lookup"><span data-stu-id="100fd-128">Marshaling Details</span></span>](marshaling-details.md)
</dt> <dt>

[<span data-ttu-id="100fd-129">Microsoft RPC</span><span class="sxs-lookup"><span data-stu-id="100fd-129">Microsoft RPC</span></span>](microsoft-rpc.md)
</dt> <dt>

[<span data-ttu-id="100fd-130">Talon</span><span class="sxs-lookup"><span data-stu-id="100fd-130">Stub</span></span>](stub.md)
</dt> </dl>

 

 