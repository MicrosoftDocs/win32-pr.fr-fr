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
# <a name="portal-object"></a>Objet du portail

\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objet portail modélise un portail iSCSI qui est contenu dans un sous-système iSCSI.

Utilisez la méthode [**IVdsSubSystemIscsi :: QueryPortals**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals) pour déterminer les portails iSCSI du sous-système. Les appelants peuvent obtenir un pointeur vers un portail spécifique en sélectionnant l’objet de portail souhaité à partir de l’énumération retournée par la méthode **QueryPortals** . Avec un objet de portail, vous pouvez définir l’état du portail et la requête pour les propriétés du portail, les groupes de portails associés et le sous-système qui contient le portail.

Un objet portail ne peut être associé qu’à un seul groupe de portails d’une cible spécifiée.

Les portails servent l’un des points de terminaison des chemins d’accès MPIO dans les fournisseurs de matériel iSCSI, sur lesquels des stratégies d’équilibrage de charge peuvent être imposées.

Les propriétés de l’objet portail incluent un identificateur d’objet, une adresse IP et un port, ainsi que l’état du portail.

Le tableau suivant répertorie les interfaces, énumérations et structures associées.



| Type                                                                                      | Élément                                                                                                                 |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Interfaces toujours exposées par cet objet dans les fournisseurs iSCSI VDS 1,1 et 2,0 uniquement | [**IVdsIscsiPortal**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportal).                                                                             |
| Énumérations associées                                                                   | [**VDS \_ \_ \_ État du portail iSCSI**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_portal_status).                                                          |
| Structures associées                                                                     | [**VDS \_ La \_ \_ prop du portail iSCSI**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portal_prop) et la [**\_ \_ notification du port VDS**](/windows/desktop/api/Vds/ns-vds-vds_port_notification). |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Objets de fournisseur de matériel](hardware-provider-objects.md)
</dt> <dt>

[**IVdsSubSystemIscsi::QueryPortals**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals)
</dt> </dl>

 

 
