---
description: Un objet de pool de stockage modélise un pool de stockage dans un sous-système de stockage.
ms.assetid: a6104742-3ef9-4570-9728-3e6580953117
title: Stockage Objet de pool
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c44719b825193faa75546ba1a0f7b42155a3e49
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126856468"
---
# <a name="storage-pool-object"></a>Stockage Objet de pool

\[à partir de Windows 8 et Windows Server 2012, l’interface COM du [Service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion des Stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objet de pool de stockage modélise un pool de stockage dans un sous-système de stockage.

Un pool de stockage contient des extensions de lecteur d’un ou plusieurs lecteurs qui sont gérés par le même fournisseur de matériel.

Le tableau suivant répertorie les interfaces, énumérations et structures associées.



| Type                                              | Élément                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces toujours exposées par cet objet | [**IVdsStoragePool**](/windows/desktop/api/Vds/nn-vds-ivdsstoragepool)                                                                                                                                                                                                                                                               |
| Énumérations associées                           | [**VDS \_ \_Type RAID**](/windows/desktop/api/Vds/ne-vds-vds_raid_type), [**\_ État du \_ pool \_ de stockage VDS**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_status)et [**type de \_ \_ pool \_ de stockage VDS**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_type).                                                                                                                                  |
| Structures associées                             | [**VDS \_ HINTS2**](/windows/desktop/api/Vds/ns-vds-vds_hints2), [**\_ \_ attributs de pool VDS**](/windows/desktop/api/Vds/ns-vds-vds_pool_attributes), [**\_ \_ \_ attributs personnalisés du pool VDS**](/windows/desktop/api/Vds/ns-vds-vds_pool_custom_attributes), [**\_ \_ \_ \_ étendue du lecteur du pool de stockage VDS**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_drive_extent)et pool de [**stockage VDS \_ \_ \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_prop). |



 

 

 
