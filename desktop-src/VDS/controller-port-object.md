---
description: Objet Port du contrôleur
ms.assetid: 5f94bcdc-93ab-4522-88bd-009a049b5dc9
title: Objet Port du contrôleur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7547581358bd79212b1093384ce1589e331f6ee0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516439"
---
# <a name="controller-port-object"></a><span data-ttu-id="0623d-103">Objet Port du contrôleur</span><span class="sxs-lookup"><span data-stu-id="0623d-103">Controller Port Object</span></span>

<span data-ttu-id="0623d-104">\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0623d-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="0623d-105">Un objet Port de contrôleur modélise un port de contrôleur dans un sous-système.</span><span class="sxs-lookup"><span data-stu-id="0623d-105">A controller port object models a controller port in a subsystem.</span></span> <span data-ttu-id="0623d-106">Les ordinateurs hôtes peuvent écrire et lire des numéros d’unités logiques via des ports de contrôleur.</span><span class="sxs-lookup"><span data-stu-id="0623d-106">Host computers can write to and read from LUNs through controller ports.</span></span> <span data-ttu-id="0623d-107">Les ports de contrôleur sont contenus par les contrôleurs dans un sous-système.</span><span class="sxs-lookup"><span data-stu-id="0623d-107">Controller ports are contained by controllers in a subsystem.</span></span> <span data-ttu-id="0623d-108">Dans VDS 1,1 et VDS 2.0, chacun des ports de contrôleur d’un sous-système est défini comme actif ou inactif par rapport à chacun des numéros d’unités logiques que le sous-système couvre.</span><span class="sxs-lookup"><span data-stu-id="0623d-108">In VDS 1.1 and VDS2.0, each of a subsystem's controller ports is set to either active or inactive in relation to each of the LUNs the subsystem surfaces.</span></span> <span data-ttu-id="0623d-109">Un seul port de contrôleur, alors, peut être défini simultanément sur actif pour un numéro d’unité logique et inactif pour d’autres.</span><span class="sxs-lookup"><span data-stu-id="0623d-109">A single controller port, then, can be simultaneously set to active for one LUN and inactive for others.</span></span> <span data-ttu-id="0623d-110">Un port de contrôleur actif pour un numéro d’unité logique donné est responsable de la gestion des entrées et sorties de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="0623d-110">A controller port that is active for a given LUN carries responsibility for handling input to and output from the LUN.</span></span>

<span data-ttu-id="0623d-111">Les ports de contrôleur actifs servent l’un des points de terminaison des chemins d’accès MPIO dans Fibre Channel fournisseurs de matériel, sur lesquels des stratégies d’équilibrage de charge peuvent être imposées.</span><span class="sxs-lookup"><span data-stu-id="0623d-111">Active controller ports serve as one of the endpoints of MPIO paths in Fibre Channel hardware providers, upon which load balancing policies can be imposed.</span></span>

<span data-ttu-id="0623d-112">Utilisez la méthode [**IVdsControllerControllerPort :: QueryControllerPorts**](/windows/desktop/api/Vds/nf-vds-ivdscontrollercontrollerport-querycontrollerports) pour déterminer les ports de contrôleur contenus dans un contrôleur spécifique.</span><span class="sxs-lookup"><span data-stu-id="0623d-112">Use the [**IVdsControllerControllerPort::QueryControllerPorts**](/windows/desktop/api/Vds/nf-vds-ivdscontrollercontrollerport-querycontrollerports) method to determine the controller ports that are contained by a specific controller.</span></span> <span data-ttu-id="0623d-113">Les appelants peuvent obtenir un pointeur vers un port de contrôleur spécifique en sélectionnant l’objet de port de contrôleur souhaité dans l’énumération retournée par la méthode **QueryControllerPorts** .</span><span class="sxs-lookup"><span data-stu-id="0623d-113">Callers can get a pointer to a specific controller port by selecting the desired controller port object from the enumeration that is returned by the **QueryControllerPorts** method.</span></span> <span data-ttu-id="0623d-114">Avec un objet contrôleur, un appelant peut définir l’état du port du contrôleur et la requête pour les numéros d’unités logiques qui lui sont associés.</span><span class="sxs-lookup"><span data-stu-id="0623d-114">With a controller object, a caller can set the controller port status and query for its associated LUNs.</span></span>

<span data-ttu-id="0623d-115">Les propriétés de l’objet contrôleur incluent un identificateur d’objet, un nom, un numéro de série et l’état du port du contrôleur.</span><span class="sxs-lookup"><span data-stu-id="0623d-115">Controller object properties include an object identifier, a name, a serial number, and the controller port status.</span></span>

<span data-ttu-id="0623d-116">Le tableau suivant répertorie les interfaces, énumérations et structures associées.</span><span class="sxs-lookup"><span data-stu-id="0623d-116">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="0623d-117">Type</span><span class="sxs-lookup"><span data-stu-id="0623d-117">Type</span></span>                                                                                              | <span data-ttu-id="0623d-118">Élément</span><span class="sxs-lookup"><span data-stu-id="0623d-118">Element</span></span>                                                                                               |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0623d-119">Interfaces toujours exposées par cet objet dans les fournisseurs de Fibre Channel VDS 1,1 et 2,0 uniquement</span><span class="sxs-lookup"><span data-stu-id="0623d-119">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 Fibre Channel providers only</span></span> | [<span data-ttu-id="0623d-120">**IVdsControllerPort**</span><span class="sxs-lookup"><span data-stu-id="0623d-120">**IVdsControllerPort**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdscontrollerport)                                                      |
| <span data-ttu-id="0623d-121">Énumérations associées</span><span class="sxs-lookup"><span data-stu-id="0623d-121">Associated enumerations</span></span>                                                                           | [<span data-ttu-id="0623d-122">**\_État du port VDS \_**</span><span class="sxs-lookup"><span data-stu-id="0623d-122">**VDS\_PORT\_STATUS**</span></span>](/windows/desktop/api/Vds/ne-vds-vds_port_status)                                                          |
| <span data-ttu-id="0623d-123">Structures associées</span><span class="sxs-lookup"><span data-stu-id="0623d-123">Associated structures</span></span>                                                                             | <span data-ttu-id="0623d-124">[**VDS \_ PORT \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_port_prop) et [ **\_ \_ notification de port VDS**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)</span><span class="sxs-lookup"><span data-stu-id="0623d-124">[**VDS\_PORT\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_port_prop) and [**VDS\_PORT\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="0623d-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0623d-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0623d-126">Objets de fournisseur de matériel</span><span class="sxs-lookup"><span data-stu-id="0623d-126">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="0623d-127">**IVdsControllerControllerPort::QueryControllerPorts**</span><span class="sxs-lookup"><span data-stu-id="0623d-127">**IVdsControllerControllerPort::QueryControllerPorts**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdscontrollercontrollerport-querycontrollerports)
</dt> </dl>

 

 
