---
description: Objet groupe du portail
ms.assetid: e5892e96-b6ad-447a-9627-b44fc6f1b27a
title: Objet groupe du portail
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1021d74a3c8a6a612372db56952be1dabe5380e8e4a49b1b83c5ae2fe54754
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057957"
---
# <a name="portal-group-object"></a>Objet groupe du portail

\[à partir de Windows 8 et Windows Server 2012, l’interface COM du [Service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion des Stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objet groupe de portails modélise un groupe de portails iSCSI contenu dans une cible iSCSI.

Utilisez la méthode [**IVdsIscsiTarget :: QueryPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups) pour déterminer les groupes de portails contenus dans une cible spécifique. Utilisez la méthode [**IVdsIscsiPortal :: QueryAssociatedPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups) pour déterminer les groupes de portails associés à un portail spécifié. Les appelants peuvent obtenir un pointeur vers un groupe de portails spécifique en sélectionnant l’objet de groupe de portail souhaité à partir de l’énumération retournée par la méthode **QueryPortalGroups** ou la méthode **QueryAssociatedPortalGroups** . Avec un objet groupe de portails, vous pouvez ajouter ou supprimer des portails et des requêtes pour les propriétés de groupe du portail, les portails associés et la cible qui contient le groupe de portails.

Les propriétés d’objet du groupe de portails incluent un [identificateur d’objet](vds-data-types.md) et la balise de groupe du portail. Pour plus d’informations sur les balises de groupe du portail, consultez la spécification iSCSI à l’adresse <https://go.microsoft.com/fwlink/p/?linkid=158752> .

Le tableau suivant répertorie les interfaces, énumérations et structures associées.



| Type                                                                                      | Élément                                                                                                                                            |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces toujours exposées par cet objet dans les fournisseurs iSCSI VDS 1,1 et 2,0 uniquement | [**IVdsIscsiPortalGroup**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportalgroup).                                                                                              |
| Énumérations associées                                                                   | Aucun.                                                                                                                                              |
| Structures associées                                                                     | [**VDS \_ \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portalgroup_prop) Notification de groupe du [**\_ portail VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_portal_group_notification)et PORTALGROUP iSCSI. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Objets de fournisseur de matériel](hardware-provider-objects.md)
</dt> <dt>

[**IVdsIscsiPortal::QueryAssociatedPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups)
</dt> <dt>

[**IVdsIscsiTarget::QueryPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups)
</dt> </dl>

 

 
