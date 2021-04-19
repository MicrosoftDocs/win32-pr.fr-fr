---
description: Le service de disque virtuel (VDS) gère un large éventail de configurations de stockage, des postes de travail à disque unique aux groupes de stockage externes. Le service expose une interface de programmation d’applications (API).
ms.assetid: 536aafd2-cc04-48cc-8ee7-920efbba2a5f
title: Service Disque virtuel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcfef0c5a73fcb2e6911395c829380c4bdfe56ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534528"
---
# <a name="virtual-disk-service"></a><span data-ttu-id="1db1f-104">Service Disque virtuel</span><span class="sxs-lookup"><span data-stu-id="1db1f-104">Virtual Disk Service</span></span>

<span data-ttu-id="1db1f-105">\[À compter de Windows 8 et de Windows Server 2012, l’interface COM du service de disque virtuel est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1db1f-105">\[Beginning with Windows 8 and Windows Server 2012, the Virtual Disk Service COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

## <a name="purpose"></a><span data-ttu-id="1db1f-106">Objectif</span><span class="sxs-lookup"><span data-stu-id="1db1f-106">Purpose</span></span>

<span data-ttu-id="1db1f-107">Le service de disque virtuel (VDS) gère un large éventail de configurations de stockage, des postes de travail à disque unique aux groupes de stockage externes.</span><span class="sxs-lookup"><span data-stu-id="1db1f-107">The Virtual Disk Service (VDS) manages a wide range of storage configurations, from single-disk desktops to external storage arrays.</span></span> <span data-ttu-id="1db1f-108">Le service expose une interface de programmation d’applications (API).</span><span class="sxs-lookup"><span data-stu-id="1db1f-108">The service exposes an application programming interface (API).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="1db1f-109">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="1db1f-109">Where applicable</span></span>

<span data-ttu-id="1db1f-110">À compter de Windows 8 et de Windows Server 8, l’interface COM du service de disque virtuel est remplacée par l’API de gestion du stockage, une interface de programmation basée sur WMI.</span><span class="sxs-lookup"><span data-stu-id="1db1f-110">Beginning with Windows 8 and Windows Server 8, the Virtual Disk Service COM interface is superseded by the Storage Management API, a WMI-based programming interface.</span></span> <span data-ttu-id="1db1f-111">Pour la gestion des sous-systèmes de stockage (Windows), des partitions et des volumes, nous vous recommandons fortement d’utiliser l’API de gestion du stockage.</span><span class="sxs-lookup"><span data-stu-id="1db1f-111">For managing storage subsystems, (Windows) disks, partitions, and volumes, we strongly recommend using the Storage Management API.</span></span> <span data-ttu-id="1db1f-112">Pour plus d’informations, consultez [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).</span><span class="sxs-lookup"><span data-stu-id="1db1f-112">For more information, see the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).</span></span>

<span data-ttu-id="1db1f-113">Pour toutes les utilisations, à l’exception des volumes de démarrage miroir (à l’aide d’un volume miroir pour héberger le système d’exploitation), les disques dynamiques sont déconseillés.</span><span class="sxs-lookup"><span data-stu-id="1db1f-113">For all usages except mirror boot volumes (using a mirror volume to host the operating system ), dynamic disks are deprecated.</span></span> <span data-ttu-id="1db1f-114">Pour les données qui nécessitent une résilience contre les défaillances de disque, utilisez des espaces de stockage, une solution de virtualisation de stockage résiliente.</span><span class="sxs-lookup"><span data-stu-id="1db1f-114">For data that requires resiliency against drive failure, use Storage Spaces, a resilient storage virtualization solution.</span></span> <span data-ttu-id="1db1f-115">Pour plus d’informations, consultez [Storage Spaces Technical Preview](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="1db1f-115">For more information, see [Storage Spaces Technical Preview](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11)).</span></span>

<span data-ttu-id="1db1f-116">Les développeurs d’applications qui utilisent les interfaces décrites dans ce guide peuvent interroger et configurer un ensemble hétérogène de stockage géré en interne et fourni par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="1db1f-116">Application developers who use the interfaces described in this guide can query and configure a heterogeneous set of vendor-supplied and internally managed storage.</span></span> <span data-ttu-id="1db1f-117">VDS masque les applications complexes associées au stockage, ce qui rend le service indépendant des fournisseurs et des technologies.</span><span class="sxs-lookup"><span data-stu-id="1db1f-117">VDS hides from applications the complexities associated with storage, making the service both vendor and technology neutral.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="1db1f-118">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="1db1f-118">Developer audience</span></span>

<span data-ttu-id="1db1f-119">Cette documentation est destinée aux développeurs d’applications qui connaissent les capacités de stockage des plates-formes Microsoft Windows et qui connaissent le développement COM.</span><span class="sxs-lookup"><span data-stu-id="1db1f-119">This documentation is intended for application developers who are familiar with the storage capabilities of Microsoft Windows platforms and who are knowledgeable about COM development.</span></span>

<span data-ttu-id="1db1f-120">Ce guide est également destiné aux fabricants de matériel sous-système qui développent et prennent en charge les programmes fournisseurs de matériel VDS.</span><span class="sxs-lookup"><span data-stu-id="1db1f-120">The guide is also intended for hardware subsystem manufacturers who develop and support VDS hardware provider programs.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="1db1f-121">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="1db1f-121">Run-time requirements</span></span>

<span data-ttu-id="1db1f-122">VDS est pris en charge sur Windows Server 2003, Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1db1f-122">VDS is supported on Windows Server 2003, Windows Vista, and later.</span></span> <span data-ttu-id="1db1f-123">Pour plus d’informations sur les exigences d’exécution d’un élément de programmation particulier, consultez la section Configuration requise de la documentation relative à cet élément.</span><span class="sxs-lookup"><span data-stu-id="1db1f-123">For information about run-time requirements for a particular programming element, see the Requirements section of the documentation for that element.</span></span>

<span data-ttu-id="1db1f-124">L’exécution d’applications VDS 32 bits sous WOW64 est prise en charge, mais les fournisseurs VDS 64 bits doivent s’exécuter en tant qu’applications natives sur les versions de Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="1db1f-124">Running 32-bit VDS applications under WOW64 is supported, but 64-bit VDS providers must run as native applications on 64-bit Windows versions.</span></span>

<span data-ttu-id="1db1f-125">VDS est disponible dans le kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="1db1f-125">VDS is available in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1db1f-126">Vous pouvez installer le kit de développement logiciel (SDK) pour Windows 7 et Windows Server 2008 R2 à partir du [Centre de téléchargement Windows](https://www.microsoft.com/download/details.aspx?id=8279).</span><span class="sxs-lookup"><span data-stu-id="1db1f-126">You can install the SDK for Windows 7 and Windows Server 2008 R2 from the [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=8279).</span></span> <span data-ttu-id="1db1f-127">Cette version de la SDK Windows peut être utilisée pour développer des applications VDS pour Windows Server 2003, Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1db1f-127">This version of the Windows SDK can be used to develop VDS applications for Windows Server 2003, Windows Vista, and later.</span></span> <span data-ttu-id="1db1f-128">Vous pouvez également télécharger la [version ISO](https://www.microsoft.com/download/details.aspx?id=8442) du kit de développement logiciel (SDK) à partir du centre de téléchargement Windows.</span><span class="sxs-lookup"><span data-stu-id="1db1f-128">You can also download the [ISO version](https://www.microsoft.com/download/details.aspx?id=8442) of the SDK from the Windows Download Center.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1db1f-129">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="1db1f-129">In this section</span></span>



| <span data-ttu-id="1db1f-130">Rubrique</span><span class="sxs-lookup"><span data-stu-id="1db1f-130">Topic</span></span>                                         | <span data-ttu-id="1db1f-131">Description</span><span class="sxs-lookup"><span data-stu-id="1db1f-131">Description</span></span>                                                                                            |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1db1f-132">À propos de VDS</span><span class="sxs-lookup"><span data-stu-id="1db1f-132">About VDS</span></span>](about-vds.md)<br/>         | <span data-ttu-id="1db1f-133">Décrit le modèle d’objet VDS, les stratégies de configuration de stockage et les notifications VDS.</span><span class="sxs-lookup"><span data-stu-id="1db1f-133">Describes the VDS object model, storage-configuration strategies, and VDS notifications.</span></span><br/>    |
| [<span data-ttu-id="1db1f-134">Utilisation de VDS</span><span class="sxs-lookup"><span data-stu-id="1db1f-134">Using VDS</span></span>](using-vds.md)<br/>         | <span data-ttu-id="1db1f-135">Décrit comment utiliser VDS pour interroger et configurer des périphériques de stockage.</span><span class="sxs-lookup"><span data-stu-id="1db1f-135">Describes how to use VDS to query and configure storage devices.</span></span><br/>                            |
| [<span data-ttu-id="1db1f-136">Référence VDS</span><span class="sxs-lookup"><span data-stu-id="1db1f-136">VDS Reference</span></span>](vds-reference.md)<br/> | <span data-ttu-id="1db1f-137">Décrit les constantes, les types de données, les énumérations, les interfaces, les structures et les codes d’erreur VDS.</span><span class="sxs-lookup"><span data-stu-id="1db1f-137">Describes VDS constants, data types, enumerations, interfaces, structures, and error codes.</span></span><br/> |



 

 

