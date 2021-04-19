---
description: Objets de fournisseur de matériel
ms.assetid: d1724219-1487-485b-9c52-5003069fe9e2
title: Objets de fournisseur de matériel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1aaebf61e97487b48a6b8bf0dbd91cc6aa3e0bd
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "106527719"
---
# <a name="hardware-provider-objects"></a><span data-ttu-id="0fbc3-103">Objets de fournisseur de matériel</span><span class="sxs-lookup"><span data-stu-id="0fbc3-103">Hardware Provider Objects</span></span>

<span data-ttu-id="0fbc3-104">\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0fbc3-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="0fbc3-105">Le modèle d’objet VDS comprend un ensemble d’objets pour interroger et configurer des entités de fournisseur de matériel.</span><span class="sxs-lookup"><span data-stu-id="0fbc3-105">The VDS object model includes a set of objects to query and configure hardware provider entities.</span></span> <span data-ttu-id="0fbc3-106">(Notez que bien que VDS comprenne un fournisseur de logiciels, vous devez acheter un fournisseur de matériel et le matériel associé séparément pour tirer parti des objets de fournisseur de matériel.) Ces objets de fournisseur de matériel représentent des appareils physiques (tels que des sous-systèmes, des lecteurs et des contrôleurs) et des périphériques virtuels (tels que les LUN et les plex de LUN).</span><span class="sxs-lookup"><span data-stu-id="0fbc3-106">(Note that while VDS includes a software provider, you must purchase a hardware provider and the associated hardware separately to take advantage of the hardware provider objects.) These hardware provider objects represent physical devices (such as subsystems, drives, and controllers) and virtual devices (such as LUNs and LUN plexes).</span></span>

<span data-ttu-id="0fbc3-107">Un fournisseur de matériel doit créer un objet COM pour chaque appareil physique ou virtuel.</span><span class="sxs-lookup"><span data-stu-id="0fbc3-107">A hardware provider should create one COM object for each physical or virtual device.</span></span>

<span data-ttu-id="0fbc3-108">L’illustration qui suit montre la relation entre l’objet fournisseur et le jeu d’objets de fournisseur de matériel, ainsi que la relation entre les différents objets de fournisseur de matériel eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="0fbc3-108">The illustration that follows shows the relationship between the provider object and the set of hardware provider objects, as well as the relationship between the various hardware provider objects themselves.</span></span>

![<span data-ttu-id="0fbc3-109">Diagramme qui montre la relation entre le « fournisseur » et le « sous-système », le « contrôleur », le numéro d’unité logique, le « LUN Plex », le « lecteur » et le « fuseau ».</span><span class="sxs-lookup"><span data-stu-id="0fbc3-109">Diagram that shows the relationship between the 'Provider' and 'Subsystem', 'Controller', 'LUN', 'LUN plex', 'Drive', and 'Spindle'.</span></span> ](images/vdshwobjects.png)

<span data-ttu-id="0fbc3-110">Un objet fournisseur peut contenir un nombre quelconque de sous-systèmes.</span><span class="sxs-lookup"><span data-stu-id="0fbc3-110">A provider object can contain any number of subsystems.</span></span> <span data-ttu-id="0fbc3-111">Tous les fournisseurs de matériel peuvent gérer plusieurs instances du même modèle de sous-système.</span><span class="sxs-lookup"><span data-stu-id="0fbc3-111">All hardware providers are capable of managing multiple instances of the same subsystem model.</span></span> <span data-ttu-id="0fbc3-112">De nombreux fournisseurs de matériel peuvent également gérer plusieurs instances de différents modèles de sous-système.</span><span class="sxs-lookup"><span data-stu-id="0fbc3-112">Many hardware providers are also capable of managing multiple instances of different subsystem models.</span></span> <span data-ttu-id="0fbc3-113">Un même ordinateur peut héberger un nombre quelconque de fournisseurs de matériel.</span><span class="sxs-lookup"><span data-stu-id="0fbc3-113">A single computer can host any number of hardware providers.</span></span>

<span data-ttu-id="0fbc3-114">Un objet sous-système peut contenir un nombre quelconque de contrôleurs et de lecteurs, et peut surfacer un nombre quelconque de numéros d’unités logiques.</span><span class="sxs-lookup"><span data-stu-id="0fbc3-114">A subsystem object can contain any number of controllers and drives, and can surface any number of LUNs.</span></span> <span data-ttu-id="0fbc3-115">Un objet LUN comprend au moins un plex LUN, et chaque Plex LUN est mappé à un ou plusieurs lecteurs, selon le type de plex.</span><span class="sxs-lookup"><span data-stu-id="0fbc3-115">A LUN object comprises of at least one LUN plex, and each LUN plex maps to one or more drives, depending on the plex type.</span></span> <span data-ttu-id="0fbc3-116">Les objets de contrôleur peuvent gérer l’entrée/sortie de données pour un nombre quelconque d’objets LUN.</span><span class="sxs-lookup"><span data-stu-id="0fbc3-116">Controller objects can manage data input/output for any number of LUN objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0fbc3-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0fbc3-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0fbc3-118">Modèle d’objet VDS</span><span class="sxs-lookup"><span data-stu-id="0fbc3-118">VDS Object Model</span></span>](vds-object-model.md)
</dt> </dl>

 

 
