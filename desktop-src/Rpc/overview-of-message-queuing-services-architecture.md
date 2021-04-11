---
title: Vue d’ensemble de l’architecture des services Message Queuing
description: Les services de Message Queuing (MSMQ) utilisent un modèle site/entreprise. En règle générale, un site est un emplacement physique, tel qu’un immeuble. Une entreprise se compose d’un ou de plusieurs sites et représente une organisation.
ms.assetid: f5c54c58-8ec5-49b7-a184-aed9a8100960
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2226c185d32cb628529b34ba33d5569bd51ac28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310725"
---
# <a name="overview-of-message-queuing-services-architecture"></a><span data-ttu-id="647ef-105">Vue d’ensemble de l’architecture des services Message Queuing</span><span class="sxs-lookup"><span data-stu-id="647ef-105">Overview of Message Queuing Services Architecture</span></span>

<span data-ttu-id="647ef-106">Les services de Message Queuing (MSMQ) utilisent un modèle site/entreprise.</span><span class="sxs-lookup"><span data-stu-id="647ef-106">Message Queuing Services (MSMQ) uses a site/enterprise model.</span></span> <span data-ttu-id="647ef-107">En règle générale, un site est un emplacement physique, tel qu’un immeuble.</span><span class="sxs-lookup"><span data-stu-id="647ef-107">Typically, a site is a physical location, such as a building.</span></span> <span data-ttu-id="647ef-108">Une entreprise se compose d’un ou de plusieurs sites et représente une organisation.</span><span class="sxs-lookup"><span data-stu-id="647ef-108">An enterprise consists of one or more sites and represents an organization.</span></span>

<span data-ttu-id="647ef-109">Le diagramme suivant illustre l’architecture du service MSMQ.</span><span class="sxs-lookup"><span data-stu-id="647ef-109">The following diagram illustrates the architecture of the MSMQ Service.</span></span>

![architecture MSMQ](images/msmq.png)

<span data-ttu-id="647ef-111">Au cœur de MSMQ se trouve la base de données MQIS (message queue Information Service), qui s’exécute sur SQL Server.</span><span class="sxs-lookup"><span data-stu-id="647ef-111">At the heart of MSMQ is the Message Queue Information Service (MQIS) database, which runs on top of SQL Server.</span></span> <span data-ttu-id="647ef-112">Une entreprise possède un MQIS maître unique, appelé contrôleur d’entreprise principal.</span><span class="sxs-lookup"><span data-stu-id="647ef-112">An enterprise has a single master MQIS, called the Primary Enterprise Controller.</span></span> <span data-ttu-id="647ef-113">Chaque site dispose de son propre MQIS, appelé *contrôleur de site principal* et zéro ou plusieurs *contrôleurs de site de sauvegarde*.</span><span class="sxs-lookup"><span data-stu-id="647ef-113">Each site has its own MQIS, called a *primary site controller* and zero or more *backup site controllers*.</span></span> <span data-ttu-id="647ef-114">Enfin, il existe des ordinateurs clients individuels, chacun ayant son propre gestionnaire de files d’attente, implémenté comme un service.</span><span class="sxs-lookup"><span data-stu-id="647ef-114">Finally, there are the individual client computers, each of which has its own queue manager, implemented as a service.</span></span> <span data-ttu-id="647ef-115">Le contrôleur principal d’entreprise peut également être un contrôleur principal de site, et tout contrôleur peut également être un client.</span><span class="sxs-lookup"><span data-stu-id="647ef-115">The Primary Enterprise Controller can also be a Primary Site Controller, and any controller can also be a client.</span></span>

<span data-ttu-id="647ef-116">Les files d’attente de messages peuvent être publiques ou privées.</span><span class="sxs-lookup"><span data-stu-id="647ef-116">Message queues can be either public or private.</span></span> <span data-ttu-id="647ef-117">Les files d’attente publiques sont inscrites dans Active Directory et sont accessibles sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="647ef-117">Public queues are registered in Active Directory and are accessible across the network.</span></span> <span data-ttu-id="647ef-118">Les messages d’une file d’attente publique sont routés au sein de l’entreprise, sous le contrôle de MSMQ.</span><span class="sxs-lookup"><span data-stu-id="647ef-118">Messages in a public queue are routed throughout the enterprise, under the control of MSMQ.</span></span> <span data-ttu-id="647ef-119">Les messages d’application cliente sont déplacés du gestionnaire de files d’attente du client vers la file d’attente de destination en circulant entre les gestionnaires de files d’attente des contrôleurs de site.</span><span class="sxs-lookup"><span data-stu-id="647ef-119">Client application messages move from the client's queue manager to the destination queue by traveling between the queue managers of the site controllers.</span></span>

<span data-ttu-id="647ef-120">Les files d’attente privées sont gérées par le gestionnaire de files d’attente local et ne sont pas inscrites dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="647ef-120">Private queues are maintained by the local queue manager and are not registered in Active Directory.</span></span> <span data-ttu-id="647ef-121">L’étendue des messages de file d’attente privée est limitée à l’ordinateur sur lequel ils résident.</span><span class="sxs-lookup"><span data-stu-id="647ef-121">The scope of private queue messages is limited to the computer on which they reside.</span></span>

 

 




