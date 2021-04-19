---
description: Objet du portail
ms.assetid: 6655bbae-07d3-416b-9e45-ddcbe3433f40
title: Objet du portail
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01328d8dccfe7a29c0686cde9b531df63d56e63e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543747"
---
# <a name="portal-object"></a><span data-ttu-id="83c92-103">Objet du portail</span><span class="sxs-lookup"><span data-stu-id="83c92-103">Portal Object</span></span>

<span data-ttu-id="83c92-104">\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="83c92-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="83c92-105">Un objet portail modélise un portail iSCSI qui est contenu dans un sous-système iSCSI.</span><span class="sxs-lookup"><span data-stu-id="83c92-105">A portal object models an iSCSI portal that is contained within an iSCSI subsystem.</span></span>

<span data-ttu-id="83c92-106">Utilisez la méthode [**IVdsSubSystemIscsi :: QueryPortals**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals) pour déterminer les portails iSCSI du sous-système.</span><span class="sxs-lookup"><span data-stu-id="83c92-106">Use the [**IVdsSubSystemIscsi::QueryPortals**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals) method to determine the iSCSI portals of the subsystem.</span></span> <span data-ttu-id="83c92-107">Les appelants peuvent obtenir un pointeur vers un portail spécifique en sélectionnant l’objet de portail souhaité à partir de l’énumération retournée par la méthode **QueryPortals** .</span><span class="sxs-lookup"><span data-stu-id="83c92-107">Callers can get a pointer to a specific portal by selecting the desired portal object from the enumeration that is returned by the **QueryPortals** method.</span></span> <span data-ttu-id="83c92-108">Avec un objet de portail, vous pouvez définir l’état du portail et la requête pour les propriétés du portail, les groupes de portails associés et le sous-système qui contient le portail.</span><span class="sxs-lookup"><span data-stu-id="83c92-108">With a portal object, you can set the portal status and query for portal properties, associated portal groups, and the subsystem that contains the portal.</span></span>

<span data-ttu-id="83c92-109">Un objet portail ne peut être associé qu’à un seul groupe de portails d’une cible spécifiée.</span><span class="sxs-lookup"><span data-stu-id="83c92-109">A portal object can only be associated with at most one portal group of a specified target.</span></span>

<span data-ttu-id="83c92-110">Les portails servent l’un des points de terminaison des chemins d’accès MPIO dans les fournisseurs de matériel iSCSI, sur lesquels des stratégies d’équilibrage de charge peuvent être imposées.</span><span class="sxs-lookup"><span data-stu-id="83c92-110">Portals serve as one of the endpoints of MPIO paths in iSCSI hardware providers, upon which load balancing policies can be imposed.</span></span>

<span data-ttu-id="83c92-111">Les propriétés de l’objet portail incluent un identificateur d’objet, une adresse IP et un port, ainsi que l’état du portail.</span><span class="sxs-lookup"><span data-stu-id="83c92-111">Portal object properties include an object identifier, an IP address and port, and the portal status.</span></span>

<span data-ttu-id="83c92-112">Le tableau suivant répertorie les interfaces, énumérations et structures associées.</span><span class="sxs-lookup"><span data-stu-id="83c92-112">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="83c92-113">Type</span><span class="sxs-lookup"><span data-stu-id="83c92-113">Type</span></span>                                                                                      | <span data-ttu-id="83c92-114">Élément</span><span class="sxs-lookup"><span data-stu-id="83c92-114">Element</span></span>                                                                                                                 |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83c92-115">Interfaces toujours exposées par cet objet dans les fournisseurs iSCSI VDS 1,1 et 2,0 uniquement</span><span class="sxs-lookup"><span data-stu-id="83c92-115">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 iSCSI providers only</span></span> | <span data-ttu-id="83c92-116">[**IVdsIscsiPortal**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportal).</span><span class="sxs-lookup"><span data-stu-id="83c92-116">[**IVdsIscsiPortal**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportal).</span></span>                                                                             |
| <span data-ttu-id="83c92-117">Énumérations associées</span><span class="sxs-lookup"><span data-stu-id="83c92-117">Associated enumerations</span></span>                                                                   | <span data-ttu-id="83c92-118">[**VDS \_ \_ \_ État du portail iSCSI**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_portal_status).</span><span class="sxs-lookup"><span data-stu-id="83c92-118">[**VDS\_ISCSI\_PORTAL\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_portal_status).</span></span>                                                          |
| <span data-ttu-id="83c92-119">Structures associées</span><span class="sxs-lookup"><span data-stu-id="83c92-119">Associated structures</span></span>                                                                     | <span data-ttu-id="83c92-120">[**VDS \_ La \_ \_ prop du portail iSCSI**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portal_prop) et la [**\_ \_ notification du port VDS**](/windows/desktop/api/Vds/ns-vds-vds_port_notification).</span><span class="sxs-lookup"><span data-stu-id="83c92-120">[**VDS\_ISCSI\_PORTAL\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portal_prop) and [**VDS\_PORT\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_port_notification).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="83c92-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="83c92-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83c92-122">Objets de fournisseur de matériel</span><span class="sxs-lookup"><span data-stu-id="83c92-122">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="83c92-123">**IVdsSubSystemIscsi::QueryPortals**</span><span class="sxs-lookup"><span data-stu-id="83c92-123">**IVdsSubSystemIscsi::QueryPortals**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals)
</dt> </dl>

 

 
