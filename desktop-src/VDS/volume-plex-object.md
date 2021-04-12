---
description: Objet de plex du volume
ms.assetid: 9e770bfc-2bcb-45f0-a7fc-ba526349839e
title: Objet de plex du volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54a858bc6ce98761bb687e8dca473b1b68879da8
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104321333"
---
# <a name="volume-plex-object"></a>Objet de plex du volume

\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objet de plex de volume modélise un plex de volume contenu dans un volume. Seul un volume en miroir peut avoir plusieurs Plex ; tous les autres types de volumes ont un Plex. Chaque Plex contient une copie des données sur le volume. VDS prend en charge quatre types de plex de volume : simple, fractionné, agrégé par bandes et avec parité. Pour obtenir une description de chacun de ces types de volumes, consultez l' [objet volume](volume-object.md).

Il existe deux façons de créer un volume avec plusieurs Plex. Vous pouvez utiliser la méthode [**IVdsPack :: CreateVolume**](/windows/desktop/api/Vds/nf-vds-ivdspack-createvolume) pour créer le volume en miroir directement ou utiliser la méthode [**IVdsVolume :: AddPlex**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-addplex) pour ajouter un volume à un autre volume. Les volumes (et les disques sous-jacents) doivent se trouver dans le même package. L’illustration suivante montre un exemple d’ajout d’un volume (B) en tant que Plex à un autre volume (A) et du volume multiplexé résultant (A). Les données sur le volume A restent intactes, tandis que les données sur le volume B deviennent une copie miroir des données sur le volume A.

![Diagramme montrant deux Plex uniques, l’un avec le volume simple A et l’autre avec le volume B simple, égal à plusieurs Plex avec le volume en miroir A.](images/vdsplex.png)

Vous pouvez interroger les plex de volume en appelant la méthode [**IVdsVolume :: QueryPlexes**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-queryplexes) . Vous pouvez obtenir un pointeur vers un plex de volume spécifique en sélectionnant l’objet Plex souhaité à partir de l’énumération retournée par **QueryPlexes**. À l’exception du dernier Plex, les plex existants peuvent être interrompus ou supprimés. Utilisez [**IVdsVolume :: BreakPlex**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-breakplex) pour fractionner un plex d’un volume et convertir l’objet Plex rompu en un objet volume. Utilisez [**IVdsVolume :: RemovePlex**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-removeplex) pour supprimer complètement le plex. Vous pouvez tenter de réparer un Plex à tolérance de panne en appelant la méthode [**IVdsVolumePlex :: Repair**](/windows/desktop/api/Vds/nf-vds-ivdsvolumeplex-repair) , qui déplace les membres incorrects vers les bons disques.

En plus de l’identificateur d’objet et du type de plex, les propriétés des objets Plex du volume incluent l’État, l’intégrité et l’état de transition du Plex. Cet objet n’a pas d’indicateur.

Le tableau suivant répertorie les interfaces, énumérations et structures associées.



| Type                                              | Élément                                                                                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces toujours exposées par cet objet | [**IVdsVolumePlex**](/windows/desktop/api/Vds/nn-vds-ivdsvolumeplex).                                                                                                                                          |
| Énumérations associées                           | [**VDS \_ \_ \_ État du Plex du volume**](/windows/desktop/api/Vds/ne-vds-vds_volume_plex_status), [**\_ \_ \_ type de plex du volume VDS**](/windows/desktop/api/Vds/ne-vds-vds_volume_plex_type)et [**\_ \_ \_ type d’étendue de disque VDS**](/windows/desktop/api/Vds/ne-vds-vds_disk_extent_type). |
| Structures associées                             | [**VDS \_ \_ \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_volume_plex_prop). du Plex du volume.                                                                                                                           |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Objets de fournisseur de logiciels](software-provider-objects.md)
</dt> <dt>

[Objet volume](volume-object.md)
</dt> </dl>

 

 
