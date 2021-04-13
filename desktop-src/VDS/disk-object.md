---
description: Objet Disk
ms.assetid: 65e14273-8127-4667-b5c8-362ad54b4782
title: Objet Disk
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d629f642d83c9e2c6954a4f09fe09091a2bbce9
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104554272"
---
# <a name="disk-object"></a>Objet Disk

\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objet Disk modélise un disque physique basé sur l’hôte. Le fournisseur de logiciels en cours d’exécution sur l’hôte local peut accéder à un numéro d’unité logique en tant que disque lorsque l’objet LUN est démasqué sur l’hôte local. Pour plus d’informations sur le masquage des LUN, consultez l' [objet lun](lun-object.md).

Chaque objet Disk contribue à un seul objet Pack. Toutefois, un disque peut fournir des étendues à un nombre quelconque de volumes au sein d’un Pack. Vous pouvez désigner un disque comme disque de rechange à chaud.

## <a name="partition-to-volume-mapping"></a>Mappage de partition à volume

Le système d’exploitation prend en charge les disques de base et dynamiques. VDS fournit un fournisseur de base et un fournisseur dynamique pour gérer ces types de disques. Les disques de base ne sont jamais tolérants aux pannes. Les disques dynamiques peuvent être tolérants aux pannes Si le système d’exploitation autorise une telle liaison de volume. Les disques de base et dynamiques peuvent contenir des partitions structurées selon l’un des styles de partition suivants : enregistrement de démarrage principal (MBR) ou table de partition GUID (GPT). Le partitionnement MBR comporte jusqu’à quatre partitions principales, ou trois partitions principales et une partition étendue avec des lecteurs logiques infinis. Le partitionnement GPT fournit jusqu’à 128 partitions principales.

La description suivante est générale par nature. Il montre la relation classique entre les partitions et les volumes, à laquelle il existe plusieurs exceptions. Pour obtenir une description détaillée du mappage de partition à volume, consultez l’interface [**IVdsAdvancedDisk**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk) . Le mappage de partition à volume varie selon le type de disque, de base ou dynamique.

-   Disques de base

    Une partition sur un disque de base est mappée directement à un volume, dans la plupart des cas, et peut être stylisée en tant que partition MBR ou GPT. L’illustration suivante montre le mappage pour les deux versions de partitions MBR. Dans le premier cas, les partitions (P1 à P4) sont mappées directement aux volumes (v1 à v4). Une partition étendue (ext) remplace P4 dans le deuxième style de MBR. Le nombre de lecteurs logiques à l’intérieur de la partition étendue mappés aux volumes est illimité.

    ![Affiche deux options de mappage pour les partitions M B R.](images/vdsbasicmapping.png)

    Dans l’illustration suivante, les partitions GPT (P1 à P128) sont mappées directement aux volumes (v1 à V128) si toutes les partitions disponibles sont en cours d’utilisation. Un disque GPT n’utilise pas une partition étendue pour améliorer la convivialité.

    ![Affiche une partition GPT.](images/vdsbasicmappinggpt.png)

-   Disques dynamiques

    Un type de partition spécial sur un disque dynamique est mappé à un grand nombre de volumes. Pour une limite estimée imposée par le fournisseur dynamique, consultez l' [objet Pack](pack-object.md). Comme le montre l’illustration suivante, il peut y avoir un nombre d’extensions dans P1 qui mappent aux volumes.

    ![Affiche un type de partition spécial sur un disque dynamique.](images/vdsdynamicmapping.png)

Quel que soit le type de disque, un disque peut contenir une ou plusieurs étendues de disque. Une extension de disque est une plage contiguë de blocs logiques exposés par le disque. Par exemple, une extension de disque peut représenter un volume entier, une partie d’un volume fractionné, un membre d’un volume agrégé par bandes ou un plex d’un volume en miroir.

### <a name="working-with-disks"></a>Utilisation des disques

Utilisez la méthode [**IVdsPack :: AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) pour ajouter un disque à un pack existant. Les appelants peuvent obtenir un pointeur vers un disque spécifique en sélectionnant l’objet disque souhaité dans l’énumération retournée par la méthode [**IVdsPack :: QueryDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-querydisks) . De même, vous pouvez appeler la méthode [**IVdsDisk :: GetPack**](/windows/desktop/api/Vds/nf-vds-ivdsdisk-getpack) pour déterminer quel Pack contient un disque donné.

Vous pouvez déplacer un disque d’un pack à un autre en appelant la méthode [**IVdsPack :: MigrateDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks) . (VDS ne prend pas en charge la migration d’un disque de base entre les packs contrôlés par le fournisseur de base.) Vous pouvez également déplacer un Pack vers un autre hôte en déplaçant physiquement tous les disques du Pack vers le nouvel hôte. Le Pack se déplace avec les disques et apparaît comme un pack étranger sur le nouvel hôte. Pour obtenir des instructions, consultez [Ajout de disques étrangers à un pack](adding-foreign-disks-to-a-pack.md).

En plus de l’identificateur d’objet, d’un nom, d’une adresse, d’un type de périphérique et d’un type de média, les propriétés de l’objet disque incluent l’état du disque, l’intégrité et les indicateurs ; taille en octets, octets par secteur, secteurs par piste et pistes par cylindre ; et le type de bus et de partition.

Le tableau suivant répertorie les interfaces, énumérations et structures associées.



| Type                                              | Élément                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces toujours exposées par cet objet | [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk), [**IVdsDiskOnline**](/windows/desktop/api/Vds/nn-vds-ivdsdiskonline), [**IVdsAdvancedDisk**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk), [**IVdsAdvancedDisk2**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk2), [**IVdsDiskPartitionMF**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf), [**IVdsDiskPartitionMF2**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2)et [**IVdsCreatePartitionEx**](/windows/desktop/api/Vds/nn-vds-ivdscreatepartitionex). **Windows Server 2008 :** L’interface [**IVdsDiskPartitionMF2**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2) n’est pas prise en charge.<br/> **Windows Vista :** L’interface [**IVdsDiskOnline**](/windows/desktop/api/Vds/nn-vds-ivdsdiskonline) n’est pas prise en charge tant que Windows Vista avec Service Pack 1 (SP1) n’est pas pris en charge ; Utilisez [**IVdsDisk2**](/windows/desktop/api/Vds/nn-vds-ivdsdisk2) à la place. L’interface [**IVdsDiskPartitionMF2**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2) n’est pas prise en charge.<br/> **Windows Server 2003 :** Les interfaces [**IVdsAdvancedDisk2**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk2), [**IVdsDisk2**](/windows/desktop/api/Vds/nn-vds-ivdsdisk2), [**IVdsDiskOnline**](/windows/desktop/api/Vds/nn-vds-ivdsdiskonline), [**IVdsDiskPartitionMF**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf)et [**IVdsDiskPartitionMF2**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2) ne sont pas prises en charge.<br/> |
| Interfaces qui peuvent être exposées par cet objet     | [**IVdsRemovable**](/windows/desktop/api/Vds/nn-vds-ivdsremovable). (Voir l' [objet lun](lun-object.md) pour les interfaces supplémentaires qui sont exposées si le disque est un numéro d’unité logique.)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Énumérations associées                           | [**VDS \_ \_Indicateur de disque**](/windows/desktop/api/Vds/ne-vds-vds_disk_flag), [**\_ \_ État du disque VDS**](/windows/desktop/api/Vds/ne-vds-vds_disk_status), [**\_ \_ indicateur de partition VDS**](/windows/desktop/api/Vds/ne-vds-vds_partition_flag), [**\_ \_ style de partition VDS**](/windows/win32/api/vds/ne-vds-__vds_partition_style)et [**\_ \_ \_ type d’étendue de disque VDS**](/windows/desktop/api/Vds/ne-vds-vds_disk_extent_type).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Structures associées                             | [**VDS \_ DISK \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_disk_prop), [**\_ \_ notification de disque VDS**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification), [**\_ \_ disque d’entrée VDS**](/windows/desktop/api/Vds/ns-vds-vds_input_disk), [**\_ \_ prop partition prop**](/windows/desktop/api/Vds/ns-vds-vds_partition_prop), [**VDS \_ partition \_ info \_ GPT**](/windows/desktop/api/Vds/ns-vds-vds_partition_info_gpt), [**VDS \_ partition \_ info \_ MBR**](/windows/desktop/api/Vds/ns-vds-vds_partition_info_mbr)et [**\_ \_ extension de disque VDS**](/windows/desktop/api/Vds/ns-vds-vds_disk_extent).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Objets de fournisseur de logiciels](software-provider-objects.md)
</dt> <dt>

[Objet Pack](pack-object.md)
</dt> <dt>

[LUN (objet)](lun-object.md)
</dt> <dt>

[Ajout de disques étrangers à un Pack](adding-foreign-disks-to-a-pack.md)
</dt> </dl>

 

