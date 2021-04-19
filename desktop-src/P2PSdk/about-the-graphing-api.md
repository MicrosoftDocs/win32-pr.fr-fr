---
description: L’API graphique de pairs permet aux applications de transmettre des données entre les pairs de manière efficace et fiable. Les concepts de base de la technologie des graphiques homologues sont les nœuds d’un graphique d’homologue et les notifications d’événements.
ms.assetid: c3530134-bde3-4a9a-b433-4f198430a607
title: À propos de l’API graphique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1b08e320f1c8d176d0bd34cc7a9a9422c6cfadc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517715"
---
# <a name="about-the-graphing-api"></a><span data-ttu-id="880c9-104">À propos de l’API graphique</span><span class="sxs-lookup"><span data-stu-id="880c9-104">About the Graphing API</span></span>

<span data-ttu-id="880c9-105">L’API graphique de pairs permet aux applications de transmettre des données entre les pairs de manière efficace et fiable.</span><span class="sxs-lookup"><span data-stu-id="880c9-105">The Peer Graphing API allows applications to pass data between peers efficiently and reliably.</span></span> <span data-ttu-id="880c9-106">Les concepts de base de la technologie des graphiques homologues sont les **nœuds** d’un graphique d’homologue et les notifications d’événements.</span><span class="sxs-lookup"><span data-stu-id="880c9-106">The core concepts of peer graph technology are the **nodes** of a peer graph, and event notices.</span></span>

## <a name="nodes"></a><span data-ttu-id="880c9-107">Nœuds</span><span class="sxs-lookup"><span data-stu-id="880c9-107">Nodes</span></span>

<span data-ttu-id="880c9-108">Un nœud représente une instance spécifique d’un homologue sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="880c9-108">A node represents a specific instance of a peer on a network.</span></span> <span data-ttu-id="880c9-109">L’infrastructure de l’API de représentation graphique des homologues garantit que chaque nœud dispose d’une vue cohérente des données dans un graphique.</span><span class="sxs-lookup"><span data-stu-id="880c9-109">The Peer Graphing API infrastructure ensures that each node has a consistent view of the data in a graph.</span></span> <span data-ttu-id="880c9-110">Un nœud possède les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="880c9-110">A node has the following features:</span></span>

-   <span data-ttu-id="880c9-111">Peut se connecter à un nœud différent et former un réseau interdépendants appelé graphique homologue.</span><span class="sxs-lookup"><span data-stu-id="880c9-111">Can connect to a different node, and form an interrelated network called a peer graph.</span></span>
-   <span data-ttu-id="880c9-112">Peut partager des données avec d’autres nœuds dans un graphique sous la forme d’un [enregistrement](records.md).</span><span class="sxs-lookup"><span data-stu-id="880c9-112">Can share data with other nodes in a graph in the form of a [record](records.md).</span></span>
-   <span data-ttu-id="880c9-113">Peut créer des connexions directes distinctes des graphiques d’homologues établis à l’aide de l' [API de regroupement](about-the-grouping-api.md)pair.</span><span class="sxs-lookup"><span data-stu-id="880c9-113">Can create direct connections separate from the peer graphs established by using the Peer [Grouping API](about-the-grouping-api.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="880c9-114">Les connexions directes permettent aux nœuds d’envoyer des données privées les unes aux autres.</span><span class="sxs-lookup"><span data-stu-id="880c9-114">Direct connections allow nodes to send private data to each other.</span></span>

     

## <a name="event-notices"></a><span data-ttu-id="880c9-115">Notifications d’événements</span><span class="sxs-lookup"><span data-stu-id="880c9-115">Event Notices</span></span>

<span data-ttu-id="880c9-116">L’API de représentation graphique d’homologue dispose d’une infrastructure d’événements qui permet à une application de s’inscrire et de recevoir une notification d’un événement homologue dans l’infrastructure de l’API de représentation graphique des homologues.</span><span class="sxs-lookup"><span data-stu-id="880c9-116">The Peer Graphing API has an event infrastructure that allows an application to register and receive notice of a peer event within the Peer Graphing API infrastructure.</span></span> <span data-ttu-id="880c9-117">En cas de modification d’un graphique homologue, une application envoie un avis d’événement pour identifier qu’une modification s’est produite.</span><span class="sxs-lookup"><span data-stu-id="880c9-117">When something changes within a peer graph, an application sends an event notice to identify that a change has occurred.</span></span>

 

 



