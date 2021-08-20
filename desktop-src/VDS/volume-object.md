---
description: Objet volume
ms.assetid: 92013015-b0f5-4b92-937b-c2637f65810c
title: Objet volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87887dae233a47ef168546bb4d0bab93389ab72e0e0617b64ea0c80fbfab0e83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125389"
---
# <a name="volume-object"></a>Objet volume

\[à partir de Windows 8 et Windows Server 2012, l’interface COM du [Service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion des Stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objet volume modélise une unité de stockage logique créée par un fournisseur de logiciels et présentée au système de fichiers en tant que disque. Chaque volume comprend au moins un plex de volume, qui est à son tour composé d’étendues provenant d’un ou de plusieurs disques.

## <a name="volume-types"></a>Types de volume

VDS prend en charge cinq types de volumes : simple, fractionné, agrégé par bandes, en miroir et agrégé par bandes avec parité. Les volumes simples, fractionnés et agrégés par bandes ne tolèrent pas les erreurs ; les volumes en miroir et en parité sont tolérants aux pannes. Le reste de cette section décrit chacun des types de volume VDS.

-   Un volume simple est une partie d’un disque physique qui fonctionne comme s’il s’agissait d’une unité physiquement distincte. Un volume simple peut se composer d’une seule région sur un disque ou de plusieurs régions du même disque qui sont liées entre elles.
-   Un volume fractionné associe des zones d’espace non alloué de plusieurs disques en un seul volume logique, ce qui vous permet d’utiliser plus efficacement tout l’espace et toutes les lettres de lecteur sur un système à plusieurs disques.
-   Un volume agrégé par bandes est créé en combinant les zones d’espace libre sur deux disques ou plus en un seul volume logique. Les volumes agrégés par bandes utilisent RAID-0, qui répartit les données sur plusieurs disques. Les volumes agrégés par bandes ne peuvent pas être étendus ou mis en miroir et n’offrent pas de tolérance de panne. Si l’un des disques contenant un volume agrégé par bandes échoue, l’ensemble du volume échoue. Lors de la création de volumes agrégés par bandes, il est préférable d’utiliser des disques de la même taille, du même modèle et du même fabricant.
-   Un volume en miroir est un volume à tolérance de panne qui fournit une redondance des données en utilisant deux copies, ou Plex, du volume pour dupliquer les données stockées sur le volume. Toutes les données écrites sur le volume en miroir sont écrites sur les deux Plex, qui se trouvent sur des disques physiques distincts. En cas de défaillance de l’un des disques physiques, les données du disque défaillant deviennent indisponibles, mais le système continue à fonctionner à l’aide du disque non affecté.
-   Un volume agrégé par bandes avec parité est un volume à tolérance de panne avec des données et une parité entrelacées par intermittence sur au moins trois disques physiques. En cas de défaillance d’une partie d’un disque physique, vous pouvez recréer les données qui se trouvaient sur la partie défaillante à partir des données restantes et de la parité. Ce type de volume (également appelé volume RAID-5) est une bonne solution pour la redondance des données dans un environnement informatique dans lequel la plupart des activités consistent à lire des données.

### <a name="volume-creation"></a>Création du volume

Les fournisseurs de logiciels de base et dynamiques prennent en charge la création de volumes partiellement dirigés. un appelant spécifie uniquement les attributs qui présentent un intérêt particulier et permet au fournisseur de choisir le reste. VDS monte automatiquement un volume nouvellement créé, sauf sur les plateformes Windows server 2003, Êdition Entreprise et Windows server 2003, Datacenter Edition.

### <a name="working-with-volumes"></a>Utilisation des volumes

Créez toujours un volume dans le même Pack que les disques qui y participent. Utilisez la méthode [**IVdsPack :: CreateVolume**](/windows/desktop/api/Vds/nf-vds-ivdspack-createvolume) pour créer un objet de volume. Vous pouvez déterminer les volumes contenus dans un pack spécifique en appelant la méthode [**QueryVolumes**](/windows/desktop/api/Vds/nf-vds-ivdspack-queryvolumes) , également exposée par [**IVdsPack**](/windows/desktop/api/Vds/nn-vds-ivdspack). Un appelant peut obtenir un pointeur vers un volume spécifique en sélectionnant l’objet de volume souhaité dans l’énumération retournée par **QueryVolumes**. Avec un objet volume, vous pouvez définir l’État. requête pour les plex ; Étendez et réduisez le volume ; Ajouter, rompre et supprimer des plex ; et supprimez le volume.

En plus de l’identificateur d’objet, d’un nom et d’un numéro de série, les propriétés de l’objet volume incluent le type de volume, la taille, l’État, l’intégrité, l’état de transition, les indicateurs et un type de système de fichiers recommandé.

Le tableau suivant répertorie les interfaces, énumérations et structures associées.



| Type                                              | Élément                                                                                                                                                                                                               |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces toujours exposées par cet objet | [**IVdsVolume**](/windows/desktop/api/Vds/nn-vds-ivdsvolume), [**IVdsVolumeMF**](/windows/desktop/api/Vds/nn-vds-ivdsvolumemf), [**IVdsVolumeMF2**](/windows/desktop/api/Vds/nn-vds-ivdsvolumemf2) \* , [**IVdsVolumeOnline**](/windows/desktop/api/Vds/nn-vds-ivdsvolumeonline) \* et [**IVdsVolumeShrink**](/windows/desktop/api/Vds/nn-vds-ivdsvolumeshrink) \* . |
| Énumérations associées                           | [**VDS \_ \_Indicateur de volume**](/windows/desktop/api/Vds/ne-vds-vds_volume_flag), [**\_ \_ État du volume VDS**](/windows/desktop/api/Vds/ne-vds-vds_volume_status), [**\_ \_ type de volume VDS**](/windows/desktop/api/Vds/ne-vds-vds_volume_type)et [**\_ \_ \_ type d’étendue de disque VDS**](/windows/desktop/api/Vds/ne-vds-vds_disk_extent_type).            |
| Structures associées                             | [**VDS \_ La \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_volume_prop) du volume et la [**\_ \_ notification du volume VDS**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification).                                                                                                        |



 

**\* Windows Server 2003 :** ces interfaces ne sont pas prises en charge tant que Windows Vista.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Objets de fournisseur de logiciels](software-provider-objects.md)
</dt> </dl>

 

 
