---
description: Objet groupe du portail
ms.assetid: e5892e96-b6ad-447a-9627-b44fc6f1b27a
title: Objet groupe du portail
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c915e76debac959a1dc7684d87c9770033b4aa34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530153"
---
# <a name="portal-group-object"></a><span data-ttu-id="48d0c-103">Objet groupe du portail</span><span class="sxs-lookup"><span data-stu-id="48d0c-103">Portal Group Object</span></span>

<span data-ttu-id="48d0c-104">\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="48d0c-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="48d0c-105">Un objet groupe de portails modélise un groupe de portails iSCSI contenu dans une cible iSCSI.</span><span class="sxs-lookup"><span data-stu-id="48d0c-105">A portal group object models an iSCSI portal group that is contained within an iSCSI target.</span></span>

<span data-ttu-id="48d0c-106">Utilisez la méthode [**IVdsIscsiTarget :: QueryPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups) pour déterminer les groupes de portails contenus dans une cible spécifique.</span><span class="sxs-lookup"><span data-stu-id="48d0c-106">Use the [**IVdsIscsiTarget::QueryPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups) method to determine the portal groups that are contained by a specific target.</span></span> <span data-ttu-id="48d0c-107">Utilisez la méthode [**IVdsIscsiPortal :: QueryAssociatedPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups) pour déterminer les groupes de portails associés à un portail spécifié.</span><span class="sxs-lookup"><span data-stu-id="48d0c-107">Use the [**IVdsIscsiPortal::QueryAssociatedPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups) method to determine the portal groups that are associated with a specified portal.</span></span> <span data-ttu-id="48d0c-108">Les appelants peuvent obtenir un pointeur vers un groupe de portails spécifique en sélectionnant l’objet de groupe de portail souhaité à partir de l’énumération retournée par la méthode **QueryPortalGroups** ou la méthode **QueryAssociatedPortalGroups** .</span><span class="sxs-lookup"><span data-stu-id="48d0c-108">Callers can get a pointer to a specific portal group by selecting the desired portal group object from the enumeration that is returned by the **QueryPortalGroups** method or the **QueryAssociatedPortalGroups** method.</span></span> <span data-ttu-id="48d0c-109">Avec un objet groupe de portails, vous pouvez ajouter ou supprimer des portails et des requêtes pour les propriétés de groupe du portail, les portails associés et la cible qui contient le groupe de portails.</span><span class="sxs-lookup"><span data-stu-id="48d0c-109">With a portal group object, you can add or remove portals and query for portal group properties, associated portals, and the target that contains the portal group.</span></span>

<span data-ttu-id="48d0c-110">Les propriétés d’objet du groupe de portails incluent un [identificateur d’objet](vds-data-types.md) et la balise de groupe du portail.</span><span class="sxs-lookup"><span data-stu-id="48d0c-110">Portal group object properties include an [object identifier](vds-data-types.md) and the portal group tag.</span></span> <span data-ttu-id="48d0c-111">Pour plus d’informations sur les balises de groupe du portail, consultez la spécification iSCSI à l’adresse <https://go.microsoft.com/fwlink/p/?linkid=158752> .</span><span class="sxs-lookup"><span data-stu-id="48d0c-111">For more information about portal group tags, see the iSCSI specification at <https://go.microsoft.com/fwlink/p/?linkid=158752>.</span></span>

<span data-ttu-id="48d0c-112">Le tableau suivant répertorie les interfaces, énumérations et structures associées.</span><span class="sxs-lookup"><span data-stu-id="48d0c-112">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="48d0c-113">Type</span><span class="sxs-lookup"><span data-stu-id="48d0c-113">Type</span></span>                                                                                      | <span data-ttu-id="48d0c-114">Élément</span><span class="sxs-lookup"><span data-stu-id="48d0c-114">Element</span></span>                                                                                                                                            |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48d0c-115">Interfaces toujours exposées par cet objet dans les fournisseurs iSCSI VDS 1,1 et 2,0 uniquement</span><span class="sxs-lookup"><span data-stu-id="48d0c-115">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 iSCSI providers only</span></span> | <span data-ttu-id="48d0c-116">[**IVdsIscsiPortalGroup**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportalgroup).</span><span class="sxs-lookup"><span data-stu-id="48d0c-116">[**IVdsIscsiPortalGroup**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportalgroup).</span></span>                                                                                              |
| <span data-ttu-id="48d0c-117">Énumérations associées</span><span class="sxs-lookup"><span data-stu-id="48d0c-117">Associated enumerations</span></span>                                                                   | <span data-ttu-id="48d0c-118">Aucun</span><span class="sxs-lookup"><span data-stu-id="48d0c-118">None.</span></span>                                                                                                                                              |
| <span data-ttu-id="48d0c-119">Structures associées</span><span class="sxs-lookup"><span data-stu-id="48d0c-119">Associated structures</span></span>                                                                     | <span data-ttu-id="48d0c-120">[**VDS \_ \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portalgroup_prop) Notification de groupe du [**\_ portail VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_portal_group_notification)et PORTALGROUP iSCSI.</span><span class="sxs-lookup"><span data-stu-id="48d0c-120">[**VDS\_ISCSI\_PORTALGROUP\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portalgroup_prop) and [**VDS\_PORTAL\_GROUP\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_portal_group_notification).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="48d0c-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="48d0c-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48d0c-122">Objets de fournisseur de matériel</span><span class="sxs-lookup"><span data-stu-id="48d0c-122">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="48d0c-123">**IVdsIscsiPortal::QueryAssociatedPortalGroups**</span><span class="sxs-lookup"><span data-stu-id="48d0c-123">**IVdsIscsiPortal::QueryAssociatedPortalGroups**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups)
</dt> <dt>

[<span data-ttu-id="48d0c-124">**IVdsIscsiTarget::QueryPortalGroups**</span><span class="sxs-lookup"><span data-stu-id="48d0c-124">**IVdsIscsiTarget::QueryPortalGroups**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups)
</dt> </dl>

 

 
