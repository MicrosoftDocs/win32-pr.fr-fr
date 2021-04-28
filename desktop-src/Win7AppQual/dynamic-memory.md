---
description: Mémoire dynamique
ms.assetid: 0ea1de35-34ea-4e94-b90d-0f89503cb3fb
title: Mémoire dynamique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfcc54a1b85f4fc39bf6383e05a2e6e535edd1d4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088467"
---
# <a name="dynamic-memory"></a><span data-ttu-id="373c8-103">Mémoire dynamique</span><span class="sxs-lookup"><span data-stu-id="373c8-103">Dynamic Memory</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="373c8-104">Plateformes affectées</span><span class="sxs-lookup"><span data-stu-id="373c8-104">Affected Platforms</span></span>

<span data-ttu-id="373c8-105">**Clients (s’exécutant en tant qu’ordinateurs virtuels)** -Windows Vista \| Windows 7</span><span class="sxs-lookup"><span data-stu-id="373c8-105">**Clients (running as virtual machines)** - Windows Vista \| Windows 7</span></span>  
<span data-ttu-id="373c8-106">**Serveurs** -Windows Server 2008 R2 Hyper-V SP1</span><span class="sxs-lookup"><span data-stu-id="373c8-106">**Servers** - Windows Server 2008 R2 Hyper-V SP1</span></span>  


## <a name="feature-impact"></a><span data-ttu-id="373c8-107">Impact sur les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="373c8-107">Feature Impact</span></span>

 <span data-ttu-id="373c8-108">**Gravité** -faible</span><span class="sxs-lookup"><span data-stu-id="373c8-108">**Severity** - Low</span></span>  
<span data-ttu-id="373c8-109">**Fréquence** -élevée</span><span class="sxs-lookup"><span data-stu-id="373c8-109">**Frequency** - High</span></span>  






## <a name="description"></a><span data-ttu-id="373c8-110">Description</span><span class="sxs-lookup"><span data-stu-id="373c8-110">Description</span></span>

<span data-ttu-id="373c8-111">À un niveau élevé, Hyper-V Mémoire dynamique est une amélioration de la gestion de la mémoire pour le rôle Hyper-V inclus dans Windows Server 2008 R2 SP1.</span><span class="sxs-lookup"><span data-stu-id="373c8-111">At a high level, Hyper-V Dynamic Memory is a memory management enhancement for the Hyper-V role included in Windows Server 2008 R2 SP1.</span></span> <span data-ttu-id="373c8-112">Il est conçu pour une utilisation en production et permet aux clients d’obtenir des ratios plus élevés de densité de machines virtuelles et de consolidation tout en optimisant l’utilisation de la mémoire sur l’ordinateur physique.</span><span class="sxs-lookup"><span data-stu-id="373c8-112">It is designed for production use and enables customers to achieve higher consolidation/virtual machine (VM) density ratios while optimizing the memory utilization in the physical machine.</span></span> <span data-ttu-id="373c8-113">L’allocation de mémoire statique est réduite et la mémoire supplémentaire est allouée en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="373c8-113">The static memory allocation is reduced and additional memory is allocated on an as needed basis.</span></span> <span data-ttu-id="373c8-114">Mémoire dynamique a un impact sur les développeurs de logiciels qui souhaitent s’assurer que leurs logiciels fonctionnent correctement dans un environnement de machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="373c8-114">Dynamic Memory impacts software developers who want to ensure that their software works correctly in a virtual machine environment.</span></span>

## <a name="usage-scenario"></a><span data-ttu-id="373c8-115">Scénario d'utilisation</span><span class="sxs-lookup"><span data-stu-id="373c8-115">Usage Scenario</span></span>

<span data-ttu-id="373c8-116">Il existe deux scénarios d’utilisation de la clé où Mémoire dynamique entre en lecture, les applications côté hôte et les applications côté invité.</span><span class="sxs-lookup"><span data-stu-id="373c8-116">There are two key usage scenarios where Dynamic Memory comes into play, host-side applications and guest-side applications.</span></span>

<span data-ttu-id="373c8-117">**Applications côté hôte (outils de gestion)**</span><span class="sxs-lookup"><span data-stu-id="373c8-117">**Host-side applications (management tools)**</span></span>

<span data-ttu-id="373c8-118">Les anciens outils qui gèrent un nouveau serveur Windows Server 2008 R2 SP1 ne seront pas en mesure d’accéder aux nouveaux paramètres de Mémoire dynamique.</span><span class="sxs-lookup"><span data-stu-id="373c8-118">Old tools managing a new Windows Server 2008 R2 SP1 server will not be able to access the new Dynamic Memory settings.</span></span> <span data-ttu-id="373c8-119">De nouvelles API WMI et des compteurs de performances ont été développés pour gérer les nouveaux paramètres de Mémoire dynamique pour les machines virtuelles Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="373c8-119">New WMI APIs and performance counters have been developed to manage the new Dynamic Memory settings for Hyper-V virtual machines.</span></span> <span data-ttu-id="373c8-120">Les développeurs de logiciels qui travaillent sur des outils de gestion doivent tirer parti de ces API et compteurs pour une utilisation avec Windows Server 2008 R2 SP1 avec le rôle Hyper-V installé.</span><span class="sxs-lookup"><span data-stu-id="373c8-120">Software developers working on management tools should take advantage of these APIs and counters for use with Windows Server 2008 R2 SP1 with the Hyper-V role installed.</span></span> <span data-ttu-id="373c8-121">Des détails sur ces nouvelles API seront disponibles via [la documentation du fournisseur WMI Hyper-V sur MSDN](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider).</span><span class="sxs-lookup"><span data-stu-id="373c8-121">Details about these new APIs will be available via [Hyper-V WMI Provider documentation on MSDN](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider).</span></span>

<span data-ttu-id="373c8-122">**Applications côté invité**</span><span class="sxs-lookup"><span data-stu-id="373c8-122">**Guest-side applications**</span></span>

<span data-ttu-id="373c8-123">Les développeurs qui écrivent des logiciels pour une utilisation au sein d’une machine virtuelle configurée pour utiliser Mémoire dynamique doivent garder à l’esprit que la mémoire système de la machine virtuelle n’est plus constante.</span><span class="sxs-lookup"><span data-stu-id="373c8-123">Developers writing software for use inside a virtual machine configured to use Dynamic Memory need to keep in mind that VM system memory is no longer constant.</span></span> <span data-ttu-id="373c8-124">Par conséquent, leur application doit libérer de la mémoire lorsqu’il n’est plus nécessaire d’autoriser d’autres applications à tirer parti de la ressource.</span><span class="sxs-lookup"><span data-stu-id="373c8-124">Consequently, their application should free memory when it is no longer needed to allow other applications to take advantage of the resource.</span></span>

<span data-ttu-id="373c8-125">Les allocations et les désallocations de mémoire continuent de fonctionner normalement pour les applications utilisateur.</span><span class="sxs-lookup"><span data-stu-id="373c8-125">Memory allocations and de-allocations continue to work as normal for user applications.</span></span> <span data-ttu-id="373c8-126">Mémoire dynamique est complètement transparent pour la plupart des applications des utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="373c8-126">Dynamic Memory is completely transparent to most end user applications.</span></span> <span data-ttu-id="373c8-127">Toutefois, si le logiciel en cours de développement utilise des compteurs de performances de la mémoire dans l’ordinateur virtuel, un test minutieux doit être effectué dans un environnement Mémoire dynamique activé pour s’assurer que le logiciel prend en compte les modifications apportées à l’allocation de mémoire du système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="373c8-127">However if the software being developed makes use of memory performance counters in the virtual machine then careful testing should be performed in a Dynamic Memory enabled environment to ensure that the software takes the changes that are made to the Guest operating system memory allocation into account.</span></span> <span data-ttu-id="373c8-128">La mémoire disponible n’est plus « statique » du point de vue de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="373c8-128">Available memory is no longer "static" from the virtual machine?s perspective.</span></span>

## <a name="solutions"></a><span data-ttu-id="373c8-129">Solutions</span><span class="sxs-lookup"><span data-stu-id="373c8-129">Solutions</span></span>

<span data-ttu-id="373c8-130">Les machines virtuelles doivent disposer d’une version mise à jour d’Integration Services (SP1) pour pouvoir tirer parti de Mémoire dynamique.</span><span class="sxs-lookup"><span data-stu-id="373c8-130">Virtual machines must have updated integration services (SP1) installed in order to take advantage of Dynamic Memory.</span></span> <span data-ttu-id="373c8-131">Assurez-vous que tous les ordinateurs utilisés dans la gestion des ordinateurs virtuels Hyper-V utilisent la dernière version de Windows Server 2008 R2 SP1.</span><span class="sxs-lookup"><span data-stu-id="373c8-131">Ensure that all machines used in the management of Hyper-V virtual machines are using the latest Windows Server 2008 R2 SP1 bits.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="373c8-132">Liens vers d’autres ressources</span><span class="sxs-lookup"><span data-stu-id="373c8-132">Links to Other Resources</span></span>

-   [<span data-ttu-id="373c8-133">Mémoire dynamique en provenance du blog Hyper-V</span><span class="sxs-lookup"><span data-stu-id="373c8-133">Dynamic Memory Coming To Hyper-V blog</span></span>](https://blogs.technet.com/b/virtualization/archive/2010/03/18/dynamic-memory-coming-to-hyper-v.aspx)
-   [<span data-ttu-id="373c8-134">Utilisation du fournisseur WMI Hyper-V</span><span class="sxs-lookup"><span data-stu-id="373c8-134">Using the Hyper-V WMI Provider</span></span>](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider)

## <a name="disclaimer"></a><span data-ttu-id="373c8-135">Clause d'exclusion de responsabilité</span><span class="sxs-lookup"><span data-stu-id="373c8-135">Disclaimer</span></span>

<span data-ttu-id="373c8-136">Les informations contenues dans ce document concernent le produit logiciel en version préliminaire qui peut être considérablement modifié avant sa première version commerciale.</span><span class="sxs-lookup"><span data-stu-id="373c8-136">The information contained in this document relates to prerelease software product that may be substantially modified before its first commercial release.</span></span> <span data-ttu-id="373c8-137">En conséquence, les informations peuvent ne pas décrire ou refléter le produit logiciel lors de la première publication commercialisée.</span><span class="sxs-lookup"><span data-stu-id="373c8-137">Accordingly, the information may not accurately describe or reflect the software product when first commercially released.</span></span> <span data-ttu-id="373c8-138">Ce document est fourni à titre d’information uniquement.</span><span class="sxs-lookup"><span data-stu-id="373c8-138">This document is for informational purposes only.</span></span> <span data-ttu-id="373c8-139">MICROSOFT MAKES NO WARRANTIES, EXPRESS OR IMPLIED, IN THIS DOCUMENT.</span><span class="sxs-lookup"><span data-stu-id="373c8-139">MICROSOFT MAKES NO WARRANTIES, EXPRESS OR IMPLIED, IN THIS DOCUMENT.</span></span>

 

 
