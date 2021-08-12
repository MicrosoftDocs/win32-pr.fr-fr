---
description: SUBSYSTEM (objet)
ms.assetid: f605a5de-9256-4b43-8e12-3d78fd6cd9f1
title: SUBSYSTEM (objet)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4af9837da90497b07d133362c0a61549a63665f2c75d4c97b2d07369e4589fa7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603147"
---
# <a name="subsystem-object"></a>SUBSYSTEM (objet)

\[à partir de Windows 8 et Windows Server 2012, l’interface COM du [Service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion des Stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objet sous-système modélise un sous-système de stockage. Un sous-système est soit un boîtier RAID, soit une carte RAID PCI. Un seul ordinateur hôte peut être connecté à n’importe quel nombre de sous-systèmes. Chaque sous-système est géré par un seul fournisseur de matériel. Dans une configuration SAN, la classe de sous-système représente un boîtier de stockage SAN.

Un sous-système peut contenir un nombre quelconque de contrôleurs et de lecteurs, et peut surfacer (démasquer) un nombre quelconque de numéros d’unités logiques sur l’ordinateur sur lequel le fournisseur de matériel s’exécute. Les sous-systèmes de plus haut niveau peuvent démasquer des numéros d’unités logiques sur d’autres ordinateurs sur le réseau. Chaque lecteur de disque d’un sous-système est connecté à un bus et occupe un emplacement dans le bus. Chaque contrôleur au sein d’un sous-système possède un ou plusieurs ports de contrôleur.

L’illustration suivante montre les périphériques physiques contenus dans un sous-système (les numéros d’unités logiques ne sont pas affichés) et les relations entre eux.

![Diagramme montrant un sous-système commençant par « ports » sur la gauche, passant à « Controllers », puis un « bus » avec « Slots » menant à des « lecteurs » individuels.](images/vdssubsystem.png)

Les applications VDS utilisent la méthode [**IVdsHwProvider :: QuerySubSystems**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems) pour interroger les sous-systèmes appartenant à un fournisseur de matériel spécifique. Les appelants peuvent obtenir un pointeur vers un sous-système spécifique en sélectionnant l’objet sous-système souhaité à partir de l’énumération retournée par la méthode **QuerySubSystems** . Avec un objet de sous-système, vous pouvez définir l’état du sous-système, créer des numéros d’unités logiques, remplacer les lecteurs et interroger les contrôleurs, les lecteurs et les numéros d’unités logiques.

En plus de l’identificateur d’objet, d’un nom et d’un numéro de série, les propriétés de l’objet sous-système incluent l’État, l’intégrité et les indicateurs du sous-système. le nombre de contrôleurs, d’emplacements et de bus ; et un paramètre de priorité de reconstruction.

Le tableau suivant répertorie les interfaces, énumérations et structures associées.



| Type                                                                                      | Élément                                                                                                                          |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| Interfaces toujours exposées par cet objet                                         | [**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem).                                                                                          |
| Interfaces toujours exposées par cet objet dans les fournisseurs iSCSI VDS 1,1 et 2,0 uniquement | [**IVdsSubSystemIscsi**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemiscsi) et [**IVdsSubSystemImportTarget**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemimporttarget).             |
| Interfaces qui peuvent être exposées par cet objet                                             | [**IVdsSubSystemNaming**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemnaming) et [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance).                               |
| Énumérations associées                                                                   | [**VDS \_ \_ \_ Indicateur de sous-système**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_flag) et [**\_ État du sous \_ -système \_ VDS**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_status).             |
| Structures associées                                                                     | [**VDS \_ SOUS \_ -système \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_prop) et [**\_ notification du sous \_ -système \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification). |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Objets de fournisseur de matériel](hardware-provider-objects.md)
</dt> <dt>

[**IVdsHwProvider::QuerySubSystems**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems)
</dt> </dl>

 

 
