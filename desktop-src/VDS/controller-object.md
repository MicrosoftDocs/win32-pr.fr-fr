---
description: Objet contrôleur
ms.assetid: ae2c4d47-15a6-4b9d-9165-4ee04a6ff3a8
title: Objet contrôleur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7db9468c1ca4c8f07c5498724333bdad9fc53bf
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104570941"
---
# <a name="controller-object"></a><span data-ttu-id="2de2a-103">Objet contrôleur</span><span class="sxs-lookup"><span data-stu-id="2de2a-103">Controller Object</span></span>

<span data-ttu-id="2de2a-104">\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2de2a-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="2de2a-105">Un objet de contrôleur modélise un contrôleur dans un sous-système.</span><span class="sxs-lookup"><span data-stu-id="2de2a-105">A controller object models a controller in a subsystem.</span></span> <span data-ttu-id="2de2a-106">Les contrôleurs sont contenus dans les sous-systèmes, et chaque contrôleur possède un ou plusieurs ports de contrôleur via lesquels l’ordinateur hôte peut écrire et lire des numéros d’unités logiques.</span><span class="sxs-lookup"><span data-stu-id="2de2a-106">Controllers are contained by subsystems, and each controller has one or more controller ports through which the host computer can write to and read from LUNs.</span></span> <span data-ttu-id="2de2a-107">Un seul contrôleur peut être défini simultanément sur actif pour un numéro d’unité logique et inactif pour d’autres.</span><span class="sxs-lookup"><span data-stu-id="2de2a-107">A single controller can be simultaneously set to active for one LUN and inactive for others.</span></span> <span data-ttu-id="2de2a-108">Un contrôleur actif pour un numéro d’unité logique spécifié assume la responsabilité de la gestion des entrées et sorties de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="2de2a-108">A controller that is active for a specified LUN carries the responsibility for handling input to and output from the LUN.</span></span> <span data-ttu-id="2de2a-109">La figure suivante illustre cette idée.</span><span class="sxs-lookup"><span data-stu-id="2de2a-109">The following figure illustrates this idea.</span></span>

![Diagramme montrant un « contrôleur » avec un numéro d’unité logique actif sur la gauche et deux numéros d’unités logiques actifs à droite.](images/vdscontroller.png)

<span data-ttu-id="2de2a-111">**VDS 1,0 :** Chacun des contrôleurs d’un sous-système est défini sur actif ou inactif par rapport à chacun des numéros d’unités logiques que le sous-système couvre.</span><span class="sxs-lookup"><span data-stu-id="2de2a-111">**VDS 1.0:** Each of a subsystem's controllers is set to either active or inactive in relation to each of the LUNs the subsystem surfaces.</span></span>

<span data-ttu-id="2de2a-112">Les applications VDS utilisent la méthode [**IVdsSubSystem :: QueryControllers**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querycontrollers) pour déterminer les contrôleurs contenus dans un sous-système spécifique.</span><span class="sxs-lookup"><span data-stu-id="2de2a-112">VDS applications use the [**IVdsSubSystem::QueryControllers**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querycontrollers) method to determine the controllers that are contained by a specific subsystem.</span></span> <span data-ttu-id="2de2a-113">Les appelants peuvent obtenir un pointeur vers un contrôleur spécifique en sélectionnant l’objet contrôleur souhaité dans l’énumération retournée par la méthode **QueryControllers** .</span><span class="sxs-lookup"><span data-stu-id="2de2a-113">Callers can get a pointer to a specific controller by selecting the desired controller object from the enumeration that is returned by the **QueryControllers** method.</span></span> <span data-ttu-id="2de2a-114">Avec un objet contrôleur, un appelant peut définir l’état du contrôleur, interroger les numéros d’unités logiques associés, interroger ses ports de contrôleur et vider et invalider le cache.</span><span class="sxs-lookup"><span data-stu-id="2de2a-114">With a controller object, a caller can set the controller status, query for its associated LUNs, query for its controller ports, and flush and invalidate the cache.</span></span>

<span data-ttu-id="2de2a-115">En plus de l’identificateur d’objet, d’un nom et d’un numéro de série, les propriétés de l’objet contrôleur incluent l’État et l’intégrité du contrôleur, ainsi que le nombre de ports.</span><span class="sxs-lookup"><span data-stu-id="2de2a-115">In addition to an object identifier, a name, and a serial number, controller object properties include the controller status and health, and a count of the ports.</span></span>

<span data-ttu-id="2de2a-116">Le tableau suivant répertorie les interfaces, énumérations et structures associées.</span><span class="sxs-lookup"><span data-stu-id="2de2a-116">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="2de2a-117">Type</span><span class="sxs-lookup"><span data-stu-id="2de2a-117">Type</span></span>                                                                                              | <span data-ttu-id="2de2a-118">Élément</span><span class="sxs-lookup"><span data-stu-id="2de2a-118">Element</span></span>                                                                                                                        |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2de2a-119">Interfaces toujours exposées par cet objet</span><span class="sxs-lookup"><span data-stu-id="2de2a-119">Interfaces that are always exposed by this object</span></span>                                                 | [<span data-ttu-id="2de2a-120">**IVdsController**</span><span class="sxs-lookup"><span data-stu-id="2de2a-120">**IVdsController**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdscontroller)                                                                                       |
| <span data-ttu-id="2de2a-121">Interfaces toujours exposées par cet objet dans les fournisseurs de Fibre Channel VDS 1,1 et 2,0 uniquement</span><span class="sxs-lookup"><span data-stu-id="2de2a-121">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 Fibre Channel providers only</span></span> | [<span data-ttu-id="2de2a-122">**IVdsControllerControllerPort**</span><span class="sxs-lookup"><span data-stu-id="2de2a-122">**IVdsControllerControllerPort**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdscontrollercontrollerport)                                                           |
| <span data-ttu-id="2de2a-123">Interfaces qui peuvent être exposées par cet objet</span><span class="sxs-lookup"><span data-stu-id="2de2a-123">Interfaces that may be exposed by this object</span></span>                                                     | [<span data-ttu-id="2de2a-124">**IVdsMaintenance**</span><span class="sxs-lookup"><span data-stu-id="2de2a-124">**IVdsMaintenance**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance)                                                                                     |
| <span data-ttu-id="2de2a-125">Énumérations associées</span><span class="sxs-lookup"><span data-stu-id="2de2a-125">Associated enumerations</span></span>                                                                           | <span data-ttu-id="2de2a-126">[**VDS \_ \_État du contrôleur**](/windows/desktop/api/Vds/ne-vds-vds_controller_status).</span><span class="sxs-lookup"><span data-stu-id="2de2a-126">[**VDS\_CONTROLLER\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_controller_status).</span></span>                                                                      |
| <span data-ttu-id="2de2a-127">Structures associées</span><span class="sxs-lookup"><span data-stu-id="2de2a-127">Associated structures</span></span>                                                                             | <span data-ttu-id="2de2a-128">[**VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_prop) Notification du contrôleur prop et du [**\_ contrôleur \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification).</span><span class="sxs-lookup"><span data-stu-id="2de2a-128">[**VDS\_CONTROLLER\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_controller_prop) and [**VDS\_CONTROLLER\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="2de2a-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2de2a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2de2a-130">Objets de fournisseur de matériel</span><span class="sxs-lookup"><span data-stu-id="2de2a-130">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="2de2a-131">**IVdsSubSystem::QueryControllers**</span><span class="sxs-lookup"><span data-stu-id="2de2a-131">**IVdsSubSystem::QueryControllers**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querycontrollers)
</dt> </dl>

 

 
