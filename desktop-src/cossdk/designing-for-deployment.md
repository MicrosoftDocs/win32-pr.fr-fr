---
description: Conception pour le déploiement
ms.assetid: 31244998-34f5-4fd8-95f6-adcc134bcaf3
title: Conception pour le déploiement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e60ac561bd05d08253433e52c7f00c2def54df3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483048"
---
# <a name="designing-for-deployment"></a><span data-ttu-id="d1a3b-103">Conception pour le déploiement</span><span class="sxs-lookup"><span data-stu-id="d1a3b-103">Designing for Deployment</span></span>

<span data-ttu-id="d1a3b-104">La planification de l’étendue des applications COM+ est une tâche de conception importante que vous devez prendre en compte au début.</span><span class="sxs-lookup"><span data-stu-id="d1a3b-104">Planning the scope of COM+ applications is an important design task you should consider early on.</span></span> <span data-ttu-id="d1a3b-105">Les systèmes distribués qui sont destinés à s’exécuter à l’aide de COM+ doivent être conçus pour le déploiement avec le moins de configurations individuelles et pour utiliser le plus efficacement chaque processus.</span><span class="sxs-lookup"><span data-stu-id="d1a3b-105">Distributed systems that are intended to run using COM+ should be designed for deployment with the least amount of individual configuration and to most efficiently use each process.</span></span> <span data-ttu-id="d1a3b-106">Vous pouvez également utiliser des techniques qui vous permettront d’obtenir des performances optimales lors du déploiement d’une application COM+.</span><span class="sxs-lookup"><span data-stu-id="d1a3b-106">There are also techniques you can use that will enable you to achieve optimal performance when deploying a COM+ application.</span></span> <span data-ttu-id="d1a3b-107">(Pour plus d’informations, consultez [déploiement pour une communication plus rapide](deploying-for-faster-communication.md).)</span><span class="sxs-lookup"><span data-stu-id="d1a3b-107">(For more information, see [Deploying for Faster Communication](deploying-for-faster-communication.md).)</span></span>

<span data-ttu-id="d1a3b-108">Lorsqu’il est affiché avec l’outil d’administration Services de composants, chaque application COM+ apparaît sous la forme d’un dossier dans lequel les jeux de composants sont regroupés logiquement.</span><span class="sxs-lookup"><span data-stu-id="d1a3b-108">When viewed with the Component Services administrative tool, each COM+ application appears as a folder within which sets of components are logically grouped.</span></span> <span data-ttu-id="d1a3b-109">Bien que vous puissiez déplacer des composants individuels entre des dossiers de **composants** d’application COM+ (en d’autres termes, d’une application à une autre), plusieurs services définis au niveau de l’application com+, tels que la sécurité, peuvent différer.</span><span class="sxs-lookup"><span data-stu-id="d1a3b-109">While you can move individual components between COM+ application **Components** folders (in other words, from one application to another), several services set at the COM+ application level, such as security, may differ.</span></span> <span data-ttu-id="d1a3b-110">Ces paramètres de service peuvent avoir une incidence sur la portabilité.</span><span class="sxs-lookup"><span data-stu-id="d1a3b-110">These service settings can affect portability.</span></span>

## <a name="a-com-server-application-defines-a-process-boundary"></a><span data-ttu-id="d1a3b-111">Une application serveur COM+ définit une limite de processus</span><span class="sxs-lookup"><span data-stu-id="d1a3b-111">A COM+ Server Application Defines a Process Boundary</span></span>

<span data-ttu-id="d1a3b-112">Lorsque vous créez une nouvelle application serveur COM+, vous définissez en fait une nouvelle limite de processus.</span><span class="sxs-lookup"><span data-stu-id="d1a3b-112">When you create a new COM+ server application, you are really defining a new process boundary.</span></span> <span data-ttu-id="d1a3b-113">(Notez l’exception pour les applications de bibliothèque expliquées ci-dessous.) Ce processus devient l’instance d’application de contrôle pour les composants contenus dans l’application COM+.</span><span class="sxs-lookup"><span data-stu-id="d1a3b-113">(Note the exception for library applications explained below.) This process becomes the controlling application instance for the components that are contained in the COM+ application.</span></span> <span data-ttu-id="d1a3b-114">Ces composants sont tous exécutés in-process dans une nouvelle instance du programme exécutable COM+ chaque fois qu’un programme appelle une application COM+ pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="d1a3b-114">These components all run in-process in a new instance of the COM+ executable program whenever a program calls into a COM+ application for the first time.</span></span> <span data-ttu-id="d1a3b-115">Cela signifie que tous les composants dans le dossier des **composants** d’une application com+ donnée s’exécutent dans un espace de processus unique qui sert de serveur DCOM.</span><span class="sxs-lookup"><span data-stu-id="d1a3b-115">This means that all of the components within a given COM+ application's **Components** folder run in a single process space that serves as the DCOM server.</span></span> <span data-ttu-id="d1a3b-116">Dans l’application COM+, COM+ gère la mémoire, la coordination avec le Distributed Transaction Coordinator (DTC), l’activation de l’instance du composant juste-à-temps, la détection et la récupération des incidents et la sécurité basée sur les rôles.</span><span class="sxs-lookup"><span data-stu-id="d1a3b-116">Within the COM+ application, COM+ manages memory, coordination with the Distributed Transaction Coordinator (DTC), just-in-time component instance activation, crash detection and recovery, and role-based security.</span></span>

## <a name="calling-across-com-application-boundaries"></a><span data-ttu-id="d1a3b-117">Appel à travers les limites d’application COM+</span><span class="sxs-lookup"><span data-stu-id="d1a3b-117">Calling Across COM+ Application Boundaries</span></span>

<span data-ttu-id="d1a3b-118">Étant donné que chaque application COM+ est normalement implémentée en tant qu’exécutable distinct, le fractionnement d’une application distribuée entre plusieurs applications COM+ présente des appels COM out-of-process lorsque les composants d’une application COM+ appellent les composants dans une autre application COM+.</span><span class="sxs-lookup"><span data-stu-id="d1a3b-118">Because each COM+ application normally is implemented as a separate executable, the effect of splitting a distributed application across multiple COM+ applications introduces out-of-process COM calls when components in one COM+ application call the components in another COM+ application.</span></span> <span data-ttu-id="d1a3b-119">Cela introduit une dégradation des performances en raison de la charge supplémentaire qui consiste à marshaler les paramètres COM entre les processus.</span><span class="sxs-lookup"><span data-stu-id="d1a3b-119">This introduces performance degradation due to the extra burden that marshaling COM parameters across processes imposes.</span></span>

> [!Note]  
> <span data-ttu-id="d1a3b-120">Il n’y a rien de mal par nature avec cette altération des performances ; il vous suffit de savoir qu’il va se produire.</span><span class="sxs-lookup"><span data-stu-id="d1a3b-120">There is nothing inherently wrong with incurring this performance penalty; you just need to be aware that it is going to occur.</span></span> <span data-ttu-id="d1a3b-121">En fonction du temps de réponse requis, du nombre d’utilisateurs qui demanderont simultanément des services d’entreprise et de la charge de démarrage ajoutée que chaque composant ajoute à chaque application COM+, vous pouvez constater que l’impact sur les performances attribuable aux appels inter-applications est acceptable.</span><span class="sxs-lookup"><span data-stu-id="d1a3b-121">Depending on the required response time, the number of users that will simultaneously request business services, and the added start-up burden that each component adds to each COM+ application, you may find that the performance hit attributable to cross-application calls is acceptable.</span></span>

 

<span data-ttu-id="d1a3b-122">L’une des possibilités qui élimine la baisse des performances de l’appel entre les limites d’application COM+ consiste à marquer une application COM+ donnée comme une application de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="d1a3b-122">One possibility that eliminates the performance penalty of calling across COM+ application boundaries is to mark a given COM+ application as a library application.</span></span> <span data-ttu-id="d1a3b-123">Une application de bibliothèque COM+ s’exécute dans le processus du client qui la crée.</span><span class="sxs-lookup"><span data-stu-id="d1a3b-123">A COM+ library application runs in the process of the client that creates it.</span></span> <span data-ttu-id="d1a3b-124">Bien sûr, aucun gain de performance n’a un coût nul.</span><span class="sxs-lookup"><span data-stu-id="d1a3b-124">Of course, no performance gain has zero cost.</span></span> <span data-ttu-id="d1a3b-125">Dans ce cas, le compromis implique les limitations des applications de bibliothèque COM+.</span><span class="sxs-lookup"><span data-stu-id="d1a3b-125">In this case, the trade-off involves the limitations of COM+ library applications.</span></span> <span data-ttu-id="d1a3b-126">Une application de bibliothèque peut utiliser la sécurité basée sur les rôles, mais elle ne peut pas prendre en charge les composants en file d’attente ou l’accès à distance.</span><span class="sxs-lookup"><span data-stu-id="d1a3b-126">While a library application can use role-based security, it cannot support queued components or remote access.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1a3b-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d1a3b-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1a3b-128">Déploiement pour une communication plus rapide</span><span class="sxs-lookup"><span data-stu-id="d1a3b-128">Deploying for Faster Communication</span></span>](deploying-for-faster-communication.md)
</dt> <dt>

[<span data-ttu-id="d1a3b-129">Conception pour la disponibilité</span><span class="sxs-lookup"><span data-stu-id="d1a3b-129">Designing for Availability</span></span>](designing-for-availability.md)
</dt> <dt>

[<span data-ttu-id="d1a3b-130">Conception pour l’évolutivité</span><span class="sxs-lookup"><span data-stu-id="d1a3b-130">Designing for Scalability</span></span>](designing-for-scalability.md)
</dt> <dt>

[<span data-ttu-id="d1a3b-131">Conception pour la sécurité</span><span class="sxs-lookup"><span data-stu-id="d1a3b-131">Designing for Security</span></span>](designing-for-security.md)
</dt> </dl>

 

 



