---
description: Ce qui est répliqué
ms.assetid: d1f0bc92-37bc-4de2-876a-e6b8b09da58d
title: Ce qui est répliqué
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2739cb0ff615ddc38f30a7aa9b0a572be5e28a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519218"
---
# <a name="what-gets-replicated"></a><span data-ttu-id="7a1dd-103">Ce qui est répliqué</span><span class="sxs-lookup"><span data-stu-id="7a1dd-103">What Gets Replicated</span></span>

## <a name="applications"></a><span data-ttu-id="7a1dd-104">Applications</span><span class="sxs-lookup"><span data-stu-id="7a1dd-104">Applications</span></span>

<span data-ttu-id="7a1dd-105">Toutes les applications installées sur l’ordinateur source sont répliquées, à l’exception des suivantes :</span><span class="sxs-lookup"><span data-stu-id="7a1dd-105">All applications installed on the source computer are replicated except for the following:</span></span>

<dl> <dt>

<span data-ttu-id="7a1dd-106"><span id="Non-COM__application_elements_and_dependencies"></span><span id="non-com__application_elements_and_dependencies"></span><span id="NON-COM__APPLICATION_ELEMENTS_AND_DEPENDENCIES"></span>Éléments et dépendances non-COM + application</span><span class="sxs-lookup"><span data-stu-id="7a1dd-106"><span id="Non-COM__application_elements_and_dependencies"></span><span id="non-com__application_elements_and_dependencies"></span><span id="NON-COM__APPLICATION_ELEMENTS_AND_DEPENDENCIES"></span>Non-COM+ application elements and dependencies</span></span>
</dt> <dd>

<span data-ttu-id="7a1dd-107">L’administrateur est chargé de répliquer tout ce dont dépend une application COM+, mais qui ne fait pas correctement partie de l’application elle-même, comme les fichiers de données et les dll.</span><span class="sxs-lookup"><span data-stu-id="7a1dd-107">The administrator is responsible for replicating anything that a COM+ application depends on but which is not properly part of the application itself, such as data files and DLLs.</span></span> <span data-ttu-id="7a1dd-108">COMREPL ne réplique rien en dehors des éléments de l’application COM+.</span><span class="sxs-lookup"><span data-stu-id="7a1dd-108">COMREPL will not replicate anything outside of COM+ application elements.</span></span>

</dd> <dt>

<span data-ttu-id="7a1dd-109"><span id="COM__preinstalled_applications"></span><span id="com__preinstalled_applications"></span><span id="COM__PREINSTALLED_APPLICATIONS"></span>Applications préinstallées par COM+</span><span class="sxs-lookup"><span data-stu-id="7a1dd-109"><span id="COM__preinstalled_applications"></span><span id="com__preinstalled_applications"></span><span id="COM__PREINSTALLED_APPLICATIONS"></span>COM+ preinstalled applications</span></span>
</dt> <dd>

<span data-ttu-id="7a1dd-110">Les applications qui sont utilisées en interne par COM+ et qui sont installées via le programme d’installation de COM+ ne sont pas répliquées.</span><span class="sxs-lookup"><span data-stu-id="7a1dd-110">Applications that are used internally by COM+ and are installed via the COM+ setup program are not replicated.</span></span> <span data-ttu-id="7a1dd-111">Ces options en question sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="7a1dd-111">These include the following:</span></span>

-   <span data-ttu-id="7a1dd-112">Application système</span><span class="sxs-lookup"><span data-stu-id="7a1dd-112">System application</span></span>
-   <span data-ttu-id="7a1dd-113">Utilitaires COM+</span><span class="sxs-lookup"><span data-stu-id="7a1dd-113">COM+ utilities</span></span>
-   <span data-ttu-id="7a1dd-114">Écouteur de file d’attente de lettres mortes QC COM+</span><span class="sxs-lookup"><span data-stu-id="7a1dd-114">COM+ QC Dead Letter Queue Listener</span></span>

</dd> <dt>

<span data-ttu-id="7a1dd-115"><span id="Applications_created_by_IIS"></span><span id="applications_created_by_iis"></span><span id="APPLICATIONS_CREATED_BY_IIS"></span>Applications créées par IIS</span><span class="sxs-lookup"><span data-stu-id="7a1dd-115"><span id="Applications_created_by_IIS"></span><span id="applications_created_by_iis"></span><span id="APPLICATIONS_CREATED_BY_IIS"></span>Applications created by IIS</span></span>
</dt> <dd>

<span data-ttu-id="7a1dd-116">Ces applications ne sont pas répliquées et incluent les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="7a1dd-116">These applications are not replicated and include the following:</span></span>

-   <span data-ttu-id="7a1dd-117">Applications IIS in-process</span><span class="sxs-lookup"><span data-stu-id="7a1dd-117">IIS in-process applications</span></span>
-   <span data-ttu-id="7a1dd-118">Utilitaires IIS</span><span class="sxs-lookup"><span data-stu-id="7a1dd-118">IIS utilities</span></span>
-   <span data-ttu-id="7a1dd-119">Toutes les applications créées pour les racines virtuelles isolées ou regroupées</span><span class="sxs-lookup"><span data-stu-id="7a1dd-119">All applications created for isolated or pooled virtual roots</span></span>

</dd> </dl>

## <a name="computer-list"></a><span data-ttu-id="7a1dd-120">Liste des ordinateurs</span><span class="sxs-lookup"><span data-stu-id="7a1dd-120">Computer List</span></span>

<span data-ttu-id="7a1dd-121">Les ordinateurs distants nommés dans le dossier **ordinateurs** de l’outil d’administration Services de composants ne seront pas répliqués à partir de la source vers l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="7a1dd-121">The remote computers named in the **Computers** folder in the Component Services administration tool will not be replicated from source to target computer.</span></span>

## <a name="properties"></a><span data-ttu-id="7a1dd-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7a1dd-122">Properties</span></span>

<span data-ttu-id="7a1dd-123">Les propriétés de collection **LocalComputer** suivantes sont répliquées :</span><span class="sxs-lookup"><span data-stu-id="7a1dd-123">The following **LocalComputer** collection properties are replicated:</span></span>

-   <span data-ttu-id="7a1dd-124">TransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="7a1dd-124">TransactionTimeout</span></span>
-   <span data-ttu-id="7a1dd-125">ResourcePoolingEnabled</span><span class="sxs-lookup"><span data-stu-id="7a1dd-125">ResourcePoolingEnabled</span></span>
-   <span data-ttu-id="7a1dd-126">DCOMEnabled</span><span class="sxs-lookup"><span data-stu-id="7a1dd-126">DCOMEnabled</span></span>
-   <span data-ttu-id="7a1dd-127">DefaultAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="7a1dd-127">DefaultAuthenticationLevel</span></span>
-   <span data-ttu-id="7a1dd-128">DefaultImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="7a1dd-128">DefaultImpersonationLevel</span></span>
-   <span data-ttu-id="7a1dd-129">SecurityTrackingEnabled</span><span class="sxs-lookup"><span data-stu-id="7a1dd-129">SecurityTrackingEnabled</span></span>
-   <span data-ttu-id="7a1dd-130">CISEnabled</span><span class="sxs-lookup"><span data-stu-id="7a1dd-130">CISEnabled</span></span>
-   <span data-ttu-id="7a1dd-131">SecureReferencesEnabled</span><span class="sxs-lookup"><span data-stu-id="7a1dd-131">SecureReferencesEnabled</span></span>
-   <span data-ttu-id="7a1dd-132">InternetPortsListed</span><span class="sxs-lookup"><span data-stu-id="7a1dd-132">InternetPortsListed</span></span>
-   <span data-ttu-id="7a1dd-133">DeafultToInternetPorts</span><span class="sxs-lookup"><span data-stu-id="7a1dd-133">DeafultToInternetPorts</span></span>
-   <span data-ttu-id="7a1dd-134">Ports</span><span class="sxs-lookup"><span data-stu-id="7a1dd-134">Ports</span></span>
-   <span data-ttu-id="7a1dd-135">RpcProxyEnabled</span><span class="sxs-lookup"><span data-stu-id="7a1dd-135">RpcProxyEnabled</span></span>

<span data-ttu-id="7a1dd-136">Les propriétés de collection **LocalComputer** suivantes ne sont pas répliquées :</span><span class="sxs-lookup"><span data-stu-id="7a1dd-136">The following **LocalComputer** collection properties are not replicated:</span></span>

-   <span data-ttu-id="7a1dd-137">Description</span><span class="sxs-lookup"><span data-stu-id="7a1dd-137">Description</span></span>
-   <span data-ttu-id="7a1dd-138">ApplicationProxyRSN</span><span class="sxs-lookup"><span data-stu-id="7a1dd-138">ApplicationProxyRSN</span></span>
-   <span data-ttu-id="7a1dd-139">IsRouter</span><span class="sxs-lookup"><span data-stu-id="7a1dd-139">IsRouter</span></span>

<span data-ttu-id="7a1dd-140">Pour obtenir une description des propriétés de la collection **LocalComputer** , consultez [**LocalComputer**](localcomputer.md).</span><span class="sxs-lookup"><span data-stu-id="7a1dd-140">For descriptions of the **LocalComputer** collection properties, see [**LocalComputer**](localcomputer.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a1dd-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7a1dd-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a1dd-142">Gestion des fichiers</span><span class="sxs-lookup"><span data-stu-id="7a1dd-142">File Management</span></span>](file-management.md)
</dt> <dt>

[<span data-ttu-id="7a1dd-143">Journalisation et rapports d’erreurs</span><span class="sxs-lookup"><span data-stu-id="7a1dd-143">Logging and Error Reporting</span></span>](logging-and-error-reporting.md)
</dt> <dt>

[<span data-ttu-id="7a1dd-144">Phases de réplication</span><span class="sxs-lookup"><span data-stu-id="7a1dd-144">Replication Phases</span></span>](replication-phases.md)
</dt> <dt>

[<span data-ttu-id="7a1dd-145">Utilisation de COMREPL</span><span class="sxs-lookup"><span data-stu-id="7a1dd-145">Using COMREPL</span></span>](using-comrepl.md)
</dt> </dl>

 

 



