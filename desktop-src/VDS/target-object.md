---
description: Objet cible
ms.assetid: e88d65ad-9b56-4620-a0f5-573c5e245b3e
title: Objet cible
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e1e81ea94a2f608378eba069defc83a721e0fb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521971"
---
# <a name="target-object"></a><span data-ttu-id="f0628-103">Objet cible</span><span class="sxs-lookup"><span data-stu-id="f0628-103">Target Object</span></span>

<span data-ttu-id="f0628-104">\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f0628-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="f0628-105">Un objet cible modélise une cible iSCSI contenue dans un sous-système iSCSI.</span><span class="sxs-lookup"><span data-stu-id="f0628-105">A target object models an iSCSI target that is contained within an iSCSI subsystem.</span></span>

<span data-ttu-id="f0628-106">Utilisez la méthode [**IVdsSubSystemIscsi :: QueryTargets**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets) pour déterminer les cibles iSCSI du sous-système.</span><span class="sxs-lookup"><span data-stu-id="f0628-106">Use the [**IVdsSubSystemIscsi::QueryTargets**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets) method to determine the iSCSI targets of the subsystem.</span></span> <span data-ttu-id="f0628-107">Les appelants peuvent obtenir un pointeur vers une cible spécifique en sélectionnant l’objet cible souhaité à partir de l’énumération retournée par la méthode **QueryTargets** .</span><span class="sxs-lookup"><span data-stu-id="f0628-107">Callers can get a pointer to a specific target by selecting the desired target object from the enumeration that is returned by the **QueryTargets** method.</span></span> <span data-ttu-id="f0628-108">Avec un objet cible, vous pouvez définir le nom convivial et la requête de la cible pour les propriétés cibles, les numéros d’unités logiques associés et le sous-système qui contient la cible.</span><span class="sxs-lookup"><span data-stu-id="f0628-108">With a target object, you can set the target's friendly name and query for target properties, associated LUNs, and the subsystem that contains the target.</span></span>

<span data-ttu-id="f0628-109">Les ordinateurs hôtes doivent se connecter aux cibles pour accéder aux numéros d’unités logiques qui leur sont associés.</span><span class="sxs-lookup"><span data-stu-id="f0628-109">Host computers must log on to targets to access their associated LUNs.</span></span> <span data-ttu-id="f0628-110">Pour effectuer une ouverture de session sur une cible, la cible doit avoir au moins un portail associé dans l’un de ses groupes de portails.</span><span class="sxs-lookup"><span data-stu-id="f0628-110">To perform a logon to a target, the target must have at least one associated portal in one of its portal groups.</span></span> <span data-ttu-id="f0628-111">L’entrée et la sortie des numéros d’unités logiques associés sont gérées par le biais de cette session de connexion.</span><span class="sxs-lookup"><span data-stu-id="f0628-111">Input to and output from associated LUNs is handled through this logon session.</span></span>

<span data-ttu-id="f0628-112">Les propriétés de l’objet cible incluent un identificateur d’objet, un nom iSCSI, un nom convivial et un indicateur CHAP.</span><span class="sxs-lookup"><span data-stu-id="f0628-112">Target object properties include an object identifier, an iSCSI name, a friendly name, and a CHAP-enabled flag.</span></span>

<span data-ttu-id="f0628-113">Le tableau suivant répertorie les interfaces, énumérations et structures associées.</span><span class="sxs-lookup"><span data-stu-id="f0628-113">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="f0628-114">Type</span><span class="sxs-lookup"><span data-stu-id="f0628-114">Type</span></span>                                                                                      | <span data-ttu-id="f0628-115">Élément</span><span class="sxs-lookup"><span data-stu-id="f0628-115">Element</span></span>                                                                                                                     |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0628-116">Interfaces toujours exposées par cet objet dans les fournisseurs iSCSI VDS 1,1 et 2,0 uniquement</span><span class="sxs-lookup"><span data-stu-id="f0628-116">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 iSCSI providers only</span></span> | <span data-ttu-id="f0628-117">[**IVdsIscsiTarget**](/windows/desktop/api/Vds/nn-vds-ivdsiscsitarget).</span><span class="sxs-lookup"><span data-stu-id="f0628-117">[**IVdsIscsiTarget**](/windows/desktop/api/Vds/nn-vds-ivdsiscsitarget).</span></span>                                                                                 |
| <span data-ttu-id="f0628-118">Énumérations associées</span><span class="sxs-lookup"><span data-stu-id="f0628-118">Associated enumerations</span></span>                                                                   | <span data-ttu-id="f0628-119">Aucun</span><span class="sxs-lookup"><span data-stu-id="f0628-119">None.</span></span>                                                                                                                       |
| <span data-ttu-id="f0628-120">Structures associées</span><span class="sxs-lookup"><span data-stu-id="f0628-120">Associated structures</span></span>                                                                     | <span data-ttu-id="f0628-121">[**VDS \_ La \_ \_ prop cible iSCSI**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_target_prop) et la [**\_ \_ notification cible VDS**](/windows/desktop/api/Vds/ns-vds-vds_target_notification).</span><span class="sxs-lookup"><span data-stu-id="f0628-121">[**VDS\_ISCSI\_TARGET\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_target_prop) and [**VDS\_TARGET\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_target_notification).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f0628-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f0628-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0628-123">Objets de fournisseur de matériel</span><span class="sxs-lookup"><span data-stu-id="f0628-123">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="f0628-124">**IVdsSubSystemIscsi::QueryTargets**</span><span class="sxs-lookup"><span data-stu-id="f0628-124">**IVdsSubSystemIscsi::QueryTargets**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets)
</dt> </dl>

 

 
