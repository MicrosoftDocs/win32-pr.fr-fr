---
description: Présentation de la configuration
ms.assetid: 5cdc21a1-ff55-4c36-8106-b045256778ce
title: Présentation de la configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4db13827bf08ee65ed8015f0c19ba2980a9a71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951108"
---
# <a name="configuration-overview"></a><span data-ttu-id="49722-103">Présentation de la configuration</span><span class="sxs-lookup"><span data-stu-id="49722-103">Configuration Overview</span></span>

<span data-ttu-id="49722-104">\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="49722-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="49722-105">Si vous n’êtes pas familiarisé avec les objets définis par VDS, consultez le [modèle d’objet VDS](vds-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="49722-105">If you are unfamiliar with the objects that are defined by VDS, see the [VDS Object Model](vds-object-model.md).</span></span>

<span data-ttu-id="49722-106">La complexité de la configuration d’un disque virtuel peut aller de très simple à affiné.</span><span class="sxs-lookup"><span data-stu-id="49722-106">The configuration complexity of a virtual disk can range from very simple to finely tuned.</span></span> <span data-ttu-id="49722-107">Les disques virtuels sans souci, Free-of-Care et Enterprise définissent trois perspectives de configuration standard.</span><span class="sxs-lookup"><span data-stu-id="49722-107">No-care, free-from-care, and enterprise virtual disks define three typical configuration perspectives.</span></span> <span data-ttu-id="49722-108">Chaque perspective présente des exigences différentes :</span><span class="sxs-lookup"><span data-stu-id="49722-108">Each perspective presents somewhat different requirements:</span></span>

-   <span data-ttu-id="49722-109">Les disques virtuels sans prudence sont peu configurés, peut-être uniquement pour automatiser le partitionnement et la mise en forme de nouveaux disques, ou pour créer temporairement un volume en miroir pour la migration des données d’un disque vers un autre sans temps d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="49722-109">No-care virtual disks are lightly configured, perhaps only to automate the partitioning and formatting of new disks, or to temporarily create a mirrored volume for migrating data from one disk to another without downtime.</span></span> <span data-ttu-id="49722-110">Ces disques sont corrects pour les ordinateurs portables et les autres systèmes avec un ou plusieurs disques.</span><span class="sxs-lookup"><span data-stu-id="49722-110">Such disks are good for notebook computers and other systems with one or a few disks.</span></span>
-   <span data-ttu-id="49722-111">Les disques virtuels Free-of-Care offrent un stockage qui s’affiche, autorépare, auto-réparable et disponible ; utilise des volumes agrégés par bandes et des numéros d’unités logiques pour obtenir de meilleures performances. utilise des volumes et des numéros d’unités logiques en miroir pour obtenir une meilleure disponibilité. et utilise des packs pour que les modes d’échec soient propres et contenus.</span><span class="sxs-lookup"><span data-stu-id="49722-111">Free-from-care virtual disks provide storage that appears self-configuring, self-healing, and available; uses striped volumes and LUNs to achieve better performance; uses mirrored volumes and LUNs to achieve better availability; and uses packs to make the failure modes clean and contained.</span></span> <span data-ttu-id="49722-112">Ce niveau de configuration est idéal pour remplacer les anciens disques système lents par les nouveaux disques rapides, de grande taille.</span><span class="sxs-lookup"><span data-stu-id="49722-112">This configuration level is ideal when replacing old, small, slow system disks with new, large, fast disks is routine.</span></span> <span data-ttu-id="49722-113">Il est également idéal pour la mise en miroir de données avec le remplacement à chaud automatique. une seule pile de rechange peut protéger de nombreux axes.</span><span class="sxs-lookup"><span data-stu-id="49722-113">It is also ideal for mirroring data with automated hot sparing—a single spare spindle can protect many spindles.</span></span> <span data-ttu-id="49722-114">Pour plus d’informations, consultez [remplacement à chaud](hot-sparing.md).</span><span class="sxs-lookup"><span data-stu-id="49722-114">For details, see [Hot Sparing](hot-sparing.md).</span></span>

    <span data-ttu-id="49722-115">Les San à petite échelle dépendent de la flexibilité et de l’automatisation offertes par ce niveau de configuration, comme les appliances NAS (Network Attached Storage).</span><span class="sxs-lookup"><span data-stu-id="49722-115">Small-scale SANs depend on the flexibility and automation that is offered by this configuration level, as do Network Attached Storage (NAS) appliances.</span></span> <span data-ttu-id="49722-116">Les disques virtuels libres de soins simplifient la tâche de consolidation du stockage des applications, par exemple, le stockage pour SQL et Exchange, sans consolider les serveurs.</span><span class="sxs-lookup"><span data-stu-id="49722-116">Free-from-care virtual disks simplify the task of consolidating application storage—for example, the storage for SQL and Exchange—without consolidating the servers.</span></span>

-   <span data-ttu-id="49722-117">Les disques virtuels d’entreprise contiennent des configurations d’entreprise très volumineuses ou complexes avec des exigences supplémentaires spécifiques au site ou à l’application.</span><span class="sxs-lookup"><span data-stu-id="49722-117">Enterprise virtual disks contain very large or complex enterprise configurations with additional site-specific or application-specific requirements.</span></span> <span data-ttu-id="49722-118">Les administrateurs règlent le sous-système de stockage pour une seule application qui peut s’exécuter rarement, par exemple un travail de création de rapports par lots mensuel sur un système de transaction de commande.</span><span class="sxs-lookup"><span data-stu-id="49722-118">Administrators tune the storage subsystem for a single application that might run only infrequently, such as a monthly batch reporting job on an order-taking transaction system.</span></span> <span data-ttu-id="49722-119">Les disques virtuels d’entreprise doivent être mis à l’échelle, afficher l’activité en temps réel du sous-système de stockage et répondre aux besoins des administrateurs pratiques.</span><span class="sxs-lookup"><span data-stu-id="49722-119">Enterprise virtual disks must scale, show the real-time activity of the storage subsystem, and satisfy the requirements of hands-on administrators.</span></span>

<span data-ttu-id="49722-120">Pour plus d’informations sur les miroirs, les bandes et les autres options de configuration dans VDS, consultez [liaison de volume et de LUN](volume-and-lun-binding.md).</span><span class="sxs-lookup"><span data-stu-id="49722-120">For additional information about mirrors, stripes, and the other configuration options in VDS, see [Volume and LUN Binding](volume-and-lun-binding.md).</span></span> <span data-ttu-id="49722-121">Une technique de configuration avancée, appelée empilement, vous permet de combiner les configurations associées aux volumes et LUN existants.</span><span class="sxs-lookup"><span data-stu-id="49722-121">An advanced configuration technique, called stacking, enables you to combine the configurations that are associated with existing volumes and LUNs.</span></span> <span data-ttu-id="49722-122">Pour plus d’informations, consultez [pile de configurations](configuration-stacking.md).</span><span class="sxs-lookup"><span data-stu-id="49722-122">For details, see [Configuration Stacking](configuration-stacking.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="49722-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="49722-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49722-124">Service Disque virtuel</span><span class="sxs-lookup"><span data-stu-id="49722-124">Virtual Disk Service</span></span>](virtual-disk-service-portal.md)
</dt> <dt>

[<span data-ttu-id="49722-125">Modèle d’objet VDS</span><span class="sxs-lookup"><span data-stu-id="49722-125">VDS Object Model</span></span>](vds-object-model.md)
</dt> <dt>

[<span data-ttu-id="49722-126">Remplacement à chaud</span><span class="sxs-lookup"><span data-stu-id="49722-126">Hot Sparing</span></span>](hot-sparing.md)
</dt> <dt>

[<span data-ttu-id="49722-127">Liaison de volume et de numéro d’unité logique</span><span class="sxs-lookup"><span data-stu-id="49722-127">Volume and LUN Binding</span></span>](volume-and-lun-binding.md)
</dt> <dt>

[<span data-ttu-id="49722-128">Empilement de configurations</span><span class="sxs-lookup"><span data-stu-id="49722-128">Configuration Stacking</span></span>](configuration-stacking.md)
</dt> </dl>

 

 
