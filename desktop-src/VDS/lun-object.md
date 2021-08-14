---
description: LUN (objet)
ms.assetid: ea22bd6d-4a7a-4674-82e9-08460914ff8e
title: LUN (objet)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d315e33b8d253e346b42b01f86a85379aadace73e517a169cc653214a9c674d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118347490"
---
# <a name="lun-object"></a>LUN (objet)

\[à partir de Windows 8 et Windows Server 2012, l’interface COM du [Service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion des Stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objet LUN (Logical Unit Number) modélise une unité logique d’espace de stockage adressable qui est créée par un fournisseur de matériel et qui est exposée par un sous-système. Chaque numéro d’unité logique comprend au moins un plex LUN, qui est à son tour composé d’étendues provenant d’un ou plusieurs lecteurs.

## <a name="lun-types"></a>Types de LUN

VDS prend en charge cinq types de LUN : simple, fractionné, agrégé par bandes, en miroir et agrégé par bandes avec parité. Les LUN simples, fractionnées et agrégées par bandes ne sont pas tolérantes aux pannes ; les LUN en miroir et en parité sont à tolérance de panne. Le reste de cette section décrit chacun des types de LUN VDS.

-   Un numéro d’unité logique simple est un numéro d’unité logique qui n’est pas tolérant aux pannes et qui est constitué d’une extension de lecteur contiguë unique à partir d’un seul lecteur. L’étendue contiguë peut comporter une seule plage de blocs ou plusieurs plages de blocs liés entre eux.
-   Un numéro d’unité logique fractionné est un numéro d’unité logique qui n’est pas à tolérance de panne et qui est constitué de plusieurs extensions discontinues de plusieurs lecteurs. Les données sont écrites de façon linéaire dans chacune des étendues du premier lecteur jusqu’à ce que toutes les premières étendues de lecteur soient remplies, puis à chacune des étendues sur le deuxième lecteur, et ainsi de suite. Les LUN fractionnées offrent une utilisation efficace de l’espace disque dans les sous-systèmes qui comportent des disques de différentes tailles.
-   Un numéro d’unité logique agrégé par bandes est un numéro d’unité logique non tolérante aux pannes composé de plusieurs extensions contiguës et entrelacées de plusieurs lecteurs. Les LUN agrégées par bandes utilisent une configuration RAID-0, de telle sorte que les données sont « entrelacées » de manière cyclique entre les étendues sur les lecteurs contributeurs. Les LUN agrégées fonctionnent mieux avec les lecteurs de la même taille, du même modèle et du même fabricant.
-   Les LUN en miroir sont des numéros d’unités logiques à tolérance de pannes qui assurent la récupération d’urgence en dupliquant les données sur plusieurs Plex LUN. Chaque Plex d’une LUN en miroir contient une copie des données stockées sur le plex d’origine. Chacun des plex réside sur un lecteur distinct. Toutes les données écrites sur un LUN mis en miroir sont écrites simultanément sur chacun de ses Plex. Si l’un des lecteurs contributeurs échoue, le plex sur ce lecteur devient indisponible, mais le système continue à fonctionner à l’aide du Plex ou des plex non affectés. Un numéro d’unité logique mis en miroir peut avoir un nombre quelconque de plex.
-   Les LUN à tolérance de panne sont agrégés par bandes avec des numéros d’unités logiques à tolérance de pannes qui permettent la récupération d’urgence en réservant les données de parité par intermittence sur trois lecteurs ou plus. Si l’un des lecteurs contributeurs échoue, les données perdues peuvent être recréées à partir des données restantes et de la parité.

## <a name="lun-creation"></a>Création de LUN

VDS prend en charge quatre modèles permettant aux applications de créer des numéros d’unités logiques : explicitement dirigés, partiellement dirigés, automagic et spécifiques au fournisseur. Tous les fournisseurs de matériel doivent prendre en charge la création de LUN explicite et partiellement dirigée, et sont vivement encouragés à prendre en charge la création de LUN automagic. (La création d’un numéro d’unité logique spécifique au fournisseur n’est pas abordée dans ce guide.)

La création de LUN explicitement dirigée permet à l’appelant de spécifier tous les attributs du numéro d’unité logique. La création d’un LUN partiellement dirigé permet à l’appelant de spécifier uniquement les attributs qui présentent un intérêt particulier, puis autorise le fournisseur à choisir le reste. La création automatique de LUN implique de permettre à l’appelant de spécifier simplement le type et la taille des numéros d’unités logiques, ainsi qu’un ensemble d’indicateurs « automagic » (préférences prédéfinies pour les attributs LUN), puis de permettre au fournisseur de créer automatiquement le numéro d’unité logique.

## <a name="lun-masking"></a>Masquage du numéro d'unité logique

VDS prend en charge le démasquage de LUN pour les sous-systèmes qui offrent cette fonctionnalité. Tous les numéros d’unités logiques sont exposés à l’ordinateur sur lequel le fournisseur est en cours d’exécution. Le démasquage de LUN permet à un appelant de « démasquer » les numéros d’unités logiques sélectionnés à d’autres ordinateurs sur le réseau. Si vous Démasquez un numéro d’unité logique sur un ordinateur, celui-ci a accès au numéro d’unité logique. Les ordinateurs pour lesquels un numéro d’unité logique est masqué ne le sont pas.

Un numéro d’unité logique non masqué expose les interfaces [**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun) et [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) à l’hôte local. Vous pouvez utiliser **IVdsDisk** pour ajouter un numéro d’unité logique à un Pack Software-Provider, créer et supprimer des volumes, attribuer des lettres de lecteur, et ainsi de suite. Pour plus d’informations sur les opérations effectuées sur un disque, consultez l' [objet Disk](disk-object.md).

Une fois qu’un numéro d’unité logique est démasqué sur un ordinateur cible ou masqué à partir d’un ordinateur cible, la visibilité de l’unité logique sur cet ordinateur risque de ne pas changer tant qu’une nouvelle analyse de bus n’est pas effectuée. L’application VDS sur l’ordinateur cible lance la nouvelle analyse du bus en appelant [**IVdsService :: reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate). Le lancement de la nouvelle analyse du bus est la responsabilité de l’application VDS, et non du fournisseur de matériel.

## <a name="lun-multipathing"></a>Multivoies LUN

Les fournisseurs de matériel qui prennent en charge MPIO (Multipath I/O) peuvent définir des stratégies d’équilibrage de charge sur les chemins entre un numéro d’unité logique et l’hôte local. Les numéros d’unités logiques qui prennent en charge cette fonctionnalité exposent l’interface [**IVdsLunMpio**](/windows/desktop/api/Vds/nn-vds-ivdslunmpio) à l’hôte local.

## <a name="working-with-luns"></a>Utilisation des numéros d’unités logiques

Utilisez la méthode [**IVdsSubSystem :: CreateLun**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-createlun) pour créer un nouvel objet lun. Vous pouvez interroger les numéros d’unités logiques qui sont exposés par un sous-système spécifique en appelant la méthode [**QueryLuns**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-queryluns) , également exposée par [**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem). Un appelant peut obtenir un pointeur vers un numéro d’unité logique spécifique en sélectionnant l’objet LUN souhaité dans l’énumération retournée par **QueryLuns**. Avec un objet LUN, vous pouvez définir l’état du numéro d’unité logique (LUN). requête pour tous les contrôleurs actifs, les plex et les indicateurs automagic ; Étendez et réduisez le numéro d’unité logique. Ajouter et supprimer des plex ; définir des masques ; appliquer des indicateurs ; et supprimez le numéro d’unité logique.

En plus de l’identificateur d’objet, d’un nom et d’un numéro de série, les propriétés de l’objet LUN incluent le type, la taille, l’État, l’intégrité, l’état de transition et les indicateurs du numéro d’unité logique. liste de démasquage ; et un paramètre de priorité de reconstruction.

Le tableau suivant répertorie les interfaces, énumérations et structures associées.



| Type                                                                                              | Élément                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces toujours exposées par cet objet                                                 | [**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun)                                                                                                                                                                                                                                                                                          |
| Interfaces toujours exposées par cet objet dans les fournisseurs de Fibre Channel VDS 1,1 et 2,0 uniquement | [**IVdsLunControllerPorts**](/windows/desktop/api/Vds/nn-vds-ivdsluncontrollerports)                                                                                                                                                                                                                                                            |
| Interfaces toujours exposées par cet objet dans les fournisseurs iSCSI VDS 1,1 et 2,0 uniquement         | [**IVdsLunIscsi**](/windows/desktop/api/Vds/nn-vds-ivdsluniscsi)                                                                                                                                                                                                                                                                                |
| Interfaces qui peuvent être exposées par cet objet\*                                                   | [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance), [**IVdsLunMpio**](/windows/desktop/api/Vds/nn-vds-ivdslunmpio), [**IVdsLunNaming**](/windows/desktop/api/Vds/nn-vds-ivdslunnaming)et [**IVdsLunNumber**](/windows/desktop/api/Vds/nn-vds-ivdslunnumber)**Windows server 2008, Windows Vista et Windows server 2003 :** l’interface [**IVdsLunNumber**](/windows/desktop/api/Vds/nn-vds-ivdslunnumber) n’est pas prise en charge.<br/> |
| Énumérations associées                                                                           | [**VDS \_ \_Indicateur LUN**](/windows/desktop/api/Vds/ne-vds-vds_lun_flag) et [**\_ \_ État LUN VDS**](/windows/desktop/api/Vds/ne-vds-vds_lun_status), et [**\_ \_ type de LUN VDS**](/windows/desktop/api/Vds/ne-vds-vds_lun_type)                                                                                                                                                                                   |
| Structures associées                                                                             | [**VDS \_ \_Informations sur le numéro d’unité logique**](/windows/desktop/api/VdsLun/ns-vdslun-vds_lun_information), la [**\_ \_ prop LUN VDS**](/windows/desktop/api/Vds/ns-vds-vds_lun_prop)et la [**\_ \_ notification de LUN VDS**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                                                                                                                                                            |



 

\* Consultez [objet Disk](disk-object.md) pour l’interface supplémentaire ([**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)) qui est exposée si le numéro d’unité logique est démasqué en tant que disque sur l’ordinateur hôte local.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Objets de fournisseur de matériel](hardware-provider-objects.md)
</dt> <dt>

[Objet Pack](pack-object.md)
</dt> <dt>

[Objet Disk](disk-object.md)
</dt> <dt>

[**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun)
</dt> <dt>

[**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)
</dt> <dt>

[Ajout d’une lettre de lecteur à un numéro d’unité logique](adding-a-drive-letter-to-a-lun.md)
</dt> </dl>

 

