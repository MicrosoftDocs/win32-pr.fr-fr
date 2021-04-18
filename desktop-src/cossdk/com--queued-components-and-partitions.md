---
description: Le service COM+ Queued Components prend entièrement en charge le concept de partitions. Autrement dit, lorsqu’un composant mis en file d’attente dans une partition est exécuté, le message est mis en file d’attente et le composant est exécuté dans la partition des composants.
ms.assetid: 08b0f7b5-6c45-4471-9634-1f42fbbf500c
title: Composants et partitions COM+ en file d’attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 589d7cb7c3e61be8ef53a248f990cde65447cf9d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523284"
---
# <a name="com-queued-components-and-partitions"></a><span data-ttu-id="44837-104">Composants et partitions COM+ en file d’attente</span><span class="sxs-lookup"><span data-stu-id="44837-104">COM+ Queued Components and Partitions</span></span>

<span data-ttu-id="44837-105">Le service COM+ Queued Components prend entièrement en charge le concept de partitions.</span><span class="sxs-lookup"><span data-stu-id="44837-105">The COM+ queued components service fully supports the concept of partitions.</span></span> <span data-ttu-id="44837-106">Autrement dit, lorsqu’un composant mis en file d’attente dans une partition est exécuté, le message est mis en file d’attente et le composant est exécuté à l’intérieur de la partition du composant.</span><span class="sxs-lookup"><span data-stu-id="44837-106">That is, when a queued component within a partition is executed, the message is queued and the component is eventually executed within the component's partition.</span></span>

## <a name="queue-names-for-partitioned-components"></a><span data-ttu-id="44837-107">Noms des files d’attente pour les composants partitionnés</span><span class="sxs-lookup"><span data-stu-id="44837-107">Queue Names for Partitioned Components</span></span>

<span data-ttu-id="44837-108">Traditionnellement, le service Queued Components utilise le nom de l’application comme nom de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="44837-108">Traditionally, the queued components service uses the application name as the queue name.</span></span> <span data-ttu-id="44837-109">Cela signifie que dans un scénario sans partitions, où une seule instance d’un nom d’application existe sur un ordinateur, chaque nom d’application possède sa propre file d’attente de messages.</span><span class="sxs-lookup"><span data-stu-id="44837-109">This means that in a non-partitions scenario, where only one instance of an application name exists on a computer, each application name has its own message queue.</span></span>

<span data-ttu-id="44837-110">Dans le cas de partitions, toutefois, lorsque plusieurs instances du même nom d’application peuvent exister sur un ordinateur, le service Queued Components utilise la même file d’attente pour tous les composants en file d’attente qui partagent le même nom d’application.</span><span class="sxs-lookup"><span data-stu-id="44837-110">In the case of partitions, however, where multiple instances of the same application name can exist on a computer, the queued components service uses the same queue for any queued components that share the same application name.</span></span>

## <a name="activating-queued-components"></a><span data-ttu-id="44837-111">Activation des composants en file d’attente</span><span class="sxs-lookup"><span data-stu-id="44837-111">Activating Queued Components</span></span>

<span data-ttu-id="44837-112">Les mêmes règles relatives à l’utilisation de l’ID de partition pour activer un composant non mis en file d’attente s’appliquent à un composant mis en file d’attente, comme suit :</span><span class="sxs-lookup"><span data-stu-id="44837-112">The same rules for how the partition ID is used to activate a non-queued component applies to a queued component, as follows:</span></span>

-   <span data-ttu-id="44837-113">Si un moniker est utilisé pour activer le composant mis en file d’attente et qu’un ID de partition est inclus, cet ID de partition est utilisé pour localiser la partition.</span><span class="sxs-lookup"><span data-stu-id="44837-113">If a moniker is used to activate the queued component and a partition ID is included, this partition ID is used to locate the partition.</span></span> <span data-ttu-id="44837-114">Cet ID de partition est prioritaire sur tout ID de partition qui peut exister dans le contexte du composant en cours d’activation.</span><span class="sxs-lookup"><span data-stu-id="44837-114">This partition ID takes precedence over any partition ID that might exist in the context for the component being activated.</span></span>
-   <span data-ttu-id="44837-115">Si aucun moniker n’est utilisé pour activer le composant, l’ID de partition qui est dans le contexte de l’objet est utilisé.</span><span class="sxs-lookup"><span data-stu-id="44837-115">If no moniker is being used to activate the component, the partition ID that is in the object's context is used.</span></span>
-   <span data-ttu-id="44837-116">Si aucun ID de partition n’existe dans le contexte de l’objet, le mappage utilisateur à partition par défaut dans Active Directory est utilisé.</span><span class="sxs-lookup"><span data-stu-id="44837-116">If no partition ID exists in the object's context, the default user-to-partition mapping within Active Directory is used.</span></span>

> [!Note]  
> <span data-ttu-id="44837-117">Si un ordinateur serveur est déconnecté du réseau et si le mappage de l’ensemble utilisateur à partition est modifié alors que le serveur est déconnecté, le cache de partition peut contenir un mappage de jeu utilisateur à partition obsolète.</span><span class="sxs-lookup"><span data-stu-id="44837-117">If a server computer is disconnected from the network and if the user-to-partition set mapping is changed while the server is disconnected, the partition cache might contain outdated user-to-partition set mapping.</span></span> <span data-ttu-id="44837-118">Cela peut entraîner une erreur d’activation si le mappage d’un ensemble d’utilisateurs à partitions est le mécanisme utilisé pour activer un composant.</span><span class="sxs-lookup"><span data-stu-id="44837-118">This could result in an activation error if user-to-partition set mapping is the mechanism used to activate a component.</span></span>

 

<span data-ttu-id="44837-119">Les événements COM+ sont entièrement intégrés aux partitions.</span><span class="sxs-lookup"><span data-stu-id="44837-119">COM+ events are fully integrated into partitions.</span></span> <span data-ttu-id="44837-120">Cela signifie qu’un abonné peut s’abonner à un serveur de publication dont l’application réside dans une partition.</span><span class="sxs-lookup"><span data-stu-id="44837-120">This means that a subscriber can subscribe to a publisher whose application resides within a partition.</span></span> <span data-ttu-id="44837-121">Pour autoriser cet abonnement, la collection de classes d’abonnés comprend deux propriétés liées à la partition : l’ID de partition de la classe d’événements et l’ID d’application de la classe d’événements.</span><span class="sxs-lookup"><span data-stu-id="44837-121">To allow this subscription, the subscriber class collection includes two partition-related properties—an event class partition ID and an event class application ID.</span></span>

## <a name="related-topics"></a><span data-ttu-id="44837-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="44837-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44837-123">Restrictions relatives à la conception d’applications</span><span class="sxs-lookup"><span data-stu-id="44837-123">Application Design Restrictions</span></span>](application-design-restrictions.md)
</dt> <dt>

[<span data-ttu-id="44837-124">Implémentation de la partition</span><span class="sxs-lookup"><span data-stu-id="44837-124">Partition Implementation</span></span>](partition-implementation.md)
</dt> <dt>

[<span data-ttu-id="44837-125">Inscription et activation de composants dans des partitions</span><span class="sxs-lookup"><span data-stu-id="44837-125">Registering and Activating Components in Partitions</span></span>](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[<span data-ttu-id="44837-126">Que sont les partitions COM+ ?</span><span class="sxs-lookup"><span data-stu-id="44837-126">What Are COM+ Partitions?</span></span>](what-are-com--partitions-.md)
</dt> </dl>

 

 



