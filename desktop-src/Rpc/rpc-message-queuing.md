---
title: Message Queuing RPC
description: Message Queuing (MSMQ) permet aux utilisateurs de communiquer sur des réseaux et des systèmes, quel que soit l’état actuel des applications et systèmes communicants.
ms.assetid: f1c8665b-3754-4c2e-b3ac-bba1f4b329e1
keywords:
- Appel de procédure distante RPC, décrit, Message Queuing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b72e9e35ec2aa1cc440c0d0356c681c4fe8548c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029624"
---
# <a name="rpc-message-queuing"></a><span data-ttu-id="87088-104">Message Queuing RPC</span><span class="sxs-lookup"><span data-stu-id="87088-104">RPC Message Queuing</span></span>

<span data-ttu-id="87088-105">Message Queuing (MSMQ) permet aux utilisateurs de communiquer sur des réseaux et des systèmes, quel que soit l’état actuel des applications et systèmes communicants.</span><span class="sxs-lookup"><span data-stu-id="87088-105">Message Queuing (MSMQ) lets users communicate across networks and systems regardless of the current state of the communicating applications and systems.</span></span> <span data-ttu-id="87088-106">Les applications envoient et reçoivent des messages via les files d’attente de messages gérées par MSMQ.</span><span class="sxs-lookup"><span data-stu-id="87088-106">Applications send and receive messages through message queues that MSMQ maintains.</span></span> <span data-ttu-id="87088-107">Les files d’attente de messages continuent de fonctionner même lorsque l’application cliente ou serveur n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="87088-107">The message queues continue to function even when the client or server application is not running.</span></span> <span data-ttu-id="87088-108">Message Queuing fournit les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="87088-108">Message queuing provides:</span></span>

-   <span data-ttu-id="87088-109">**Messagerie asynchrone.**</span><span class="sxs-lookup"><span data-stu-id="87088-109">**Asynchronous messaging.**</span></span> <span data-ttu-id="87088-110">Avec la messagerie asynchrone MSMQ, une application cliente peut envoyer un message à un serveur et effectuer un retour immédiatement, même si l’ordinateur cible ou le programme serveur ne répond pas.</span><span class="sxs-lookup"><span data-stu-id="87088-110">With MSMQ asynchronous messaging, a client application can send a message to a server and return immediately, even if the target computer or server program is not responding.</span></span>
-   <span data-ttu-id="87088-111">**Remise des messages garantie.**</span><span class="sxs-lookup"><span data-stu-id="87088-111">**Guaranteed message delivery.**</span></span> <span data-ttu-id="87088-112">Lorsqu’une application envoie un message via MSMQ, le message atteint sa destination même si l’application de destination n’est pas en cours d’exécution en même temps ou si les réseaux et systèmes sont hors connexion.</span><span class="sxs-lookup"><span data-stu-id="87088-112">When an application sends a message through MSMQ, the message will reach its destination even if the destination application is not running at the same time or the networks and systems are offline.</span></span>
-   <span data-ttu-id="87088-113">**Le routage et la configuration dynamique.**</span><span class="sxs-lookup"><span data-stu-id="87088-113">**Routing and dynamic configuration.**</span></span> <span data-ttu-id="87088-114">MSMQ assure un routage flexible sur des réseaux hétérogènes.</span><span class="sxs-lookup"><span data-stu-id="87088-114">MSMQ provides flexible routing over heterogeneous networks.</span></span> <span data-ttu-id="87088-115">La configuration de ces réseaux peut être modifiée de manière dynamique sans modification majeure des systèmes et réseaux eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="87088-115">The configuration of such networks can be changed dynamically without any major changes to systems and networks themselves.</span></span>
-   <span data-ttu-id="87088-116">**Messagerie sans connexion.**</span><span class="sxs-lookup"><span data-stu-id="87088-116">**Connectionless messaging.**</span></span> <span data-ttu-id="87088-117">Les applications utilisant MSMQ n’ont pas besoin de configurer des sessions directes avec les applications cibles.</span><span class="sxs-lookup"><span data-stu-id="87088-117">Applications using MSMQ do not need to set up direct sessions with target applications.</span></span>
-   <span data-ttu-id="87088-118">[Sécurité](security.md).</span><span class="sxs-lookup"><span data-stu-id="87088-118">[Security](security.md).</span></span> <span data-ttu-id="87088-119">MSMQ fournit une communication sécurisée basée sur la sécurité Windows et l’API de chiffrement (CryptoAPI) pour le chiffrement et les signatures numériques.</span><span class="sxs-lookup"><span data-stu-id="87088-119">MSMQ provides secure communication based on Windows security and the Cryptographic API (CryptoAPI) for encryption and digital signatures.</span></span>
-   <span data-ttu-id="87088-120">**Messagerie hiérarchisée.**</span><span class="sxs-lookup"><span data-stu-id="87088-120">**Prioritized Messaging.**</span></span> <span data-ttu-id="87088-121">MSMQ transfère les messages sur les réseaux en fonction de leur priorité, ce qui permet une communication plus rapide pour les applications critiques.</span><span class="sxs-lookup"><span data-stu-id="87088-121">MSMQ transfers messages across networks based on priority, allowing faster communication for critical applications.</span></span>

<span data-ttu-id="87088-122">Microsoft RPC étend le modèle OSF (Open Software Foundation – Data communication Equipment) pour les appels de procédure distante en permettant aux applications distribuées d’utiliser MSMQ comme transport et de contrôler un grand nombre de ses fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="87088-122">Microsoft RPC extends the Open Software Foundation–Data Communications Equipment (OSF-DCE) model for remote procedure calls by allowing distributed applications to use MSMQ as a transport and to control many of its features.</span></span> <span data-ttu-id="87088-123">Cette fonctionnalité est disponible à la fois pour les applications RPC conventionnelles et, via l’interface **IRPCOptions** , aux applications com.</span><span class="sxs-lookup"><span data-stu-id="87088-123">This functionality is available both to conventional RPC applications and, through the **IRPCOptions** interface, to COM applications.</span></span>

> [!Note]  
> <span data-ttu-id="87088-124">La mise en file d’attente des messages RPC est disponible uniquement sur Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="87088-124">RPC message queuing is available only on Windows 2000.</span></span> <span data-ttu-id="87088-125">Les versions ultérieures de Windows ne prennent pas en charge la mise en file d’attente de messages RPC.</span><span class="sxs-lookup"><span data-stu-id="87088-125">Later versions of Windows do not support RPC message queuing.</span></span>

 

<span data-ttu-id="87088-126">Les rubriques suivantes fournissent une vue d’ensemble de Message Queuing :</span><span class="sxs-lookup"><span data-stu-id="87088-126">The following topics provide an overview of message queuing:</span></span>

-   [<span data-ttu-id="87088-127">Vue d’ensemble de l’architecture des services Message Queuing</span><span class="sxs-lookup"><span data-stu-id="87088-127">Overview of Message Queuing Services Architecture</span></span>](overview-of-message-queuing-services-architecture.md)
-   [<span data-ttu-id="87088-128">Propriétés des messages et des files d’attente de messages</span><span class="sxs-lookup"><span data-stu-id="87088-128">Message and Message Queue Properties</span></span>](message-and-message-queue-properties.md)
-   [<span data-ttu-id="87088-129">Utilisation de MSMQ en tant que transport RPC</span><span class="sxs-lookup"><span data-stu-id="87088-129">Using MSMQ as an RPC Transport</span></span>](using-msmq-as-an-rpc-transport.md)
-   [<span data-ttu-id="87088-130">Configuration système requise pour les applications RPC-message \_ Queuing</span><span class="sxs-lookup"><span data-stu-id="87088-130">System Requirements for RPC-Message\_Queuing Applications</span></span>](system-requirements-for-rpc-message-queuing-applications.md)
-   [<span data-ttu-id="87088-131">Développement d’applications de mise en file d’attente RPC-Message</span><span class="sxs-lookup"><span data-stu-id="87088-131">Developing RPC-Message Queuing Applications</span></span>](developing-rpc-message-queuing-applications.md)
-   [<span data-ttu-id="87088-132">Services de sécurité MSMQ</span><span class="sxs-lookup"><span data-stu-id="87088-132">MSMQ Security Services</span></span>](msmq-security-services.md)

 

 




