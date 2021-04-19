---
title: Talon
description: Le stub, comme le proxy, est constitué d’un ou plusieurs éléments d’interface et d’un responsable.
ms.assetid: ed7d5546-2d19-4055-b078-62b39d0317b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 109936ae16827dce7779b080902dbca74a8dfc51
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/03/2021
ms.locfileid: "106523738"
---
# <a name="stub"></a><span data-ttu-id="89386-103">Talon</span><span class="sxs-lookup"><span data-stu-id="89386-103">Stub</span></span>

<span data-ttu-id="89386-104">Le stub, comme le proxy, est constitué d’un ou plusieurs éléments d’interface et d’un responsable.</span><span class="sxs-lookup"><span data-stu-id="89386-104">The stub, like the proxy, is made up of one or more interface pieces and a manager.</span></span> <span data-ttu-id="89386-105">Chaque stub d’interface fournit du code pour démarshaler les paramètres et le code qui appelle l’une des interfaces prises en charge par l’objet.</span><span class="sxs-lookup"><span data-stu-id="89386-105">Each interface stub provides code to unmarshal the parameters and code that calls one of the object's supported interfaces.</span></span> <span data-ttu-id="89386-106">Chaque stub fournit également une interface pour la communication interne.</span><span class="sxs-lookup"><span data-stu-id="89386-106">Each stub also provides an interface for internal communication.</span></span> <span data-ttu-id="89386-107">Le gestionnaire de stub effectue le suivi des stubs d’interface disponibles.</span><span class="sxs-lookup"><span data-stu-id="89386-107">The stub manager keeps track of the available interface stubs.</span></span>

<span data-ttu-id="89386-108">Toutefois, il existe les différences suivantes entre le stub et le proxy :</span><span class="sxs-lookup"><span data-stu-id="89386-108">There are, however, the following differences between the stub and the proxy:</span></span>

-   <span data-ttu-id="89386-109">La différence la plus importante est que le stub représente le client dans l’espace d’adressage de l’objet.</span><span class="sxs-lookup"><span data-stu-id="89386-109">The most important difference is that the stub represents the client in the object's address space.</span></span>
-   <span data-ttu-id="89386-110">Le stub n’est pas implémenté comme un objet d’agrégation, car il n’est pas nécessaire que le client soit affiché en tant qu’unité unique ; chaque élément du stub est un composant distinct.</span><span class="sxs-lookup"><span data-stu-id="89386-110">The stub is not implemented as an aggregate object because there is no requirement that the client be viewed as a single unit; each piece in the stub is a separate component.</span></span>
-   <span data-ttu-id="89386-111">Les stubs d’interface sont privés et non publics.</span><span class="sxs-lookup"><span data-stu-id="89386-111">The interface stubs are private rather than public.</span></span>
-   <span data-ttu-id="89386-112">Les stubs d’interface implémentent [**IRpcStubBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcstubbuffer), et non [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer).</span><span class="sxs-lookup"><span data-stu-id="89386-112">The interface stubs implement [**IRpcStubBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcstubbuffer), not [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer).</span></span>
-   <span data-ttu-id="89386-113">Au lieu d’empaqueter les paramètres à marshaler, le stub les décompresse après qu’ils ont été marshalés, puis empaquette la réponse.</span><span class="sxs-lookup"><span data-stu-id="89386-113">Instead of packaging parameters to be marshaled, the stub unpackages them after they have been marshaled and then packages the reply.</span></span>

## <a name="structure-of-the-stub"></a><span data-ttu-id="89386-114">Structure du stub</span><span class="sxs-lookup"><span data-stu-id="89386-114">Structure of the Stub</span></span>

<span data-ttu-id="89386-115">Le diagramme suivant illustre la structure du stub.</span><span class="sxs-lookup"><span data-stu-id="89386-115">The following diagram shows the structure of the stub.</span></span> <span data-ttu-id="89386-116">Chaque stub d’interface est connecté à une interface sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="89386-116">Each interface stub is connected to an interface on the object.</span></span> <span data-ttu-id="89386-117">Le canal distribue les messages entrants au stub d’interface approprié.</span><span class="sxs-lookup"><span data-stu-id="89386-117">The channel dispatches incoming messages to the appropriate interface stub.</span></span> <span data-ttu-id="89386-118">Tous les composants communiquent avec le canal via [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer), l’interface qui fournit l’accès à la bibliothèque Runtime RPC.</span><span class="sxs-lookup"><span data-stu-id="89386-118">All the components talk to the channel through [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer), the interface that provides access to the RPC run-time library.</span></span>

![Capture d’écran qui montre la structure du stub.](images/98714a22-733e-432f-bb90-408bbeecc23f.png)

## <a name="related-topics"></a><span data-ttu-id="89386-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="89386-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89386-121">Channel</span><span class="sxs-lookup"><span data-stu-id="89386-121">Channel</span></span>](channel.md)
</dt> <dt>

[<span data-ttu-id="89386-122">Communication entre les objets</span><span class="sxs-lookup"><span data-stu-id="89386-122">Inter-Object Communication</span></span>](inter-object-communication.md)
</dt> <dt>

[<span data-ttu-id="89386-123">Détails du marshaling</span><span class="sxs-lookup"><span data-stu-id="89386-123">Marshaling Details</span></span>](marshaling-details.md)
</dt> <dt>

[<span data-ttu-id="89386-124">Microsoft RPC</span><span class="sxs-lookup"><span data-stu-id="89386-124">Microsoft RPC</span></span>](microsoft-rpc.md)
</dt> <dt>

[<span data-ttu-id="89386-125">Proxy</span><span class="sxs-lookup"><span data-stu-id="89386-125">Proxy</span></span>](proxy.md)
</dt> </dl>

 

 