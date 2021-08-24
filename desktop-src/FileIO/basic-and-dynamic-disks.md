---
description: Décrit deux types de stockage sur disque et décrit les styles de partition.
ms.assetid: 5d511654-92e0-4236-80e7-bb2417403186
title: Disques de base et dynamiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f134f0dd7c8d81522733d26a6c5efb433d0e425978e1cbffd7edf3b0937b949
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582626"
---
# <a name="basic-and-dynamic-disks"></a>Disques de base et dynamiques

Avant de partitionner un lecteur ou d’obtenir des informations sur la disposition des partitions d’un lecteur, vous devez d’abord comprendre les fonctionnalités et les limitations des types de stockage de disque de base et dynamique.

dans le cadre de cette rubrique, le terme *volume* est utilisé pour faire référence au concept d’une partition de disque formatée avec un système de fichiers valide, le plus souvent NTFS, utilisé par le système d’exploitation Windows pour stocker les fichiers. Un volume a un nom de chemin d’accès Win32, peut être énuméré par les fonctions [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) et [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) , et une lettre de lecteur lui est généralement affectée, par exemple C :. Pour plus d’informations sur les volumes et les systèmes de fichiers, consultez [systèmes de fichiers](file-systems.md).

Dans cette rubrique :

-   [Disques de base](#basic-disks)
-   [Disques dynamiques](#dynamic-disks)
-   [Styles de partition](#partition-styles)
    -   [Enregistrement de démarrage principal](#master-boot-record)
    -   [Table de partition GUID](#guid-partition-table)
-   [Détection du type de disque](#detecting-the-type-of-disk)
-   [Rubriques connexes](#related-topics)

Il existe deux types de disques lorsque vous faites référence aux types de stockage dans ce contexte : *disques de base* et *disques dynamiques*. Notez que les types de stockage présentés ici ne sont pas les mêmes que les disques physiques ou les styles de partition, qui sont liés mais des concepts distincts. Par exemple, le fait de faire référence à un disque de base n’implique pas un style de partition particulier : le style de partition utilisé pour le disque faisant l’objet d’une discussion doit également être spécifié. Pour obtenir une description simplifiée de la façon dont un type de stockage disque de base est associé à un disque dur physique, consultez [unités de disque et partitions](disk-devices-and-partitions.md).

## <a name="basic-disks"></a>Disques de base

Les *disques de base* sont les types de stockage les plus souvent utilisés avec Windows. Le terme *disque de base* fait référence à un disque qui contient des partitions, telles que des partitions principales et des lecteurs logiques, qui, à leur tour, sont généralement formatés avec un système de fichiers pour devenir un volume de stockage de fichiers. Les disques de base offrent une solution de stockage simple qui peut s’adapter à un tableau utile de scénarios de besoins de stockage en constante évolution. Les disques de base prennent également en charge les disques en cluster, les disques IEEE (Institute of Electrical and Electronics Engineers) 1394 et les lecteurs amovibles USB (Universal Serial Bus). pour la compatibilité descendante, les disques de base utilisent généralement le même style de partition d’enregistrement de démarrage principal (MBR) que les disques utilisés par le système d’exploitation Microsoft MS-DOS et toutes les versions de Windows mais peuvent également prendre en charge les partitions de Table de partition **GUID** (GPT) sur les systèmes qui le prennent en charge. Pour plus d’informations sur les styles de partition MBR et GPT, consultez la section [styles de partition](#partition-styles) .

Vous pouvez ajouter plus d’espace à des partitions principales et des lecteurs logiques existants en les étendant dans un espace non alloué contigu et adjacent sur le même disque. Pour étendre un volume de base, celui-ci doit être formaté avec le système de fichiers NTFS. Vous pouvez étendre un lecteur logique dans un espace libre contigu, dans la partition étendue qui le contient. Si vous étendez un lecteur logique au-delà de l’espace libre disponible dans la partition étendue, cette partition étendue s’agrandit pour contenir le lecteur logique à condition qu’elle soit suivie d’un espace non alloué contigu. Pour plus d’informations, consultez fonctionnement des [disques et des volumes de base](/previous-versions/windows/it-pro/windows-server-2003/cc739412(v=ws.10)).

Les opérations suivantes ne peuvent être effectuées que sur des disques de base :

-   Créez et supprimez des partitions principales et étendues.
-   Créez et supprimez des lecteurs logiques dans une partition étendue.
-   Formater une partition et la marquer comme active.

## <a name="dynamic-disks"></a>Disques dynamiques

> [!NOTE]
> Pour toutes les utilisations, à l’exception des volumes de démarrage miroir (à l’aide d’un volume miroir pour héberger le système d’exploitation), les disques dynamiques sont déconseillés. pour les données qui nécessitent une résilience contre les défaillances de disque, utilisez espaces de stockage, une solution de virtualisation de stockage résiliente. pour plus d’informations, consultez [espaces de stockage vue d’ensemble](/windows-server/storage/storage-spaces/overview).

Les *disques dynamiques* offrent des fonctionnalités qui ne sont pas des disques de base, telles que la possibilité de créer des volumes qui s’étendent sur plusieurs disques (volumes fractionnés et agrégés par bandes) et la possibilité de créer des volumes à tolérance de panne (volumes en miroir et RAID-5). Comme les disques de base, les disques dynamiques peuvent utiliser les styles de partition MBR ou GPT sur les systèmes qui prennent en charge les deux. Tous les volumes sur des disques dynamiques sont appelés volumes dynamiques. Les disques dynamiques offrent une plus grande souplesse pour la gestion des volumes, car ils utilisent une base de données pour effectuer le suivi des informations sur les volumes dynamiques sur le disque et sur d’autres disques dynamiques de l’ordinateur. Étant donné que chaque disque dynamique d’un ordinateur stocke un réplica de la base de données de disque dynamique, par exemple, une base de données de disque dynamique endommagée peut réparer un disque dynamique à l’aide de la base de données sur un autre disque dynamique. L’emplacement de la base de données est déterminé par le style de partition du disque. Sur les partitions MBR, la base de données est contenue au dernier mégaoctet (Mo) du disque. Sur les partitions GPT, la base de données est contenue dans une partition réservée (masquée) de 1 Mo.

Les disques dynamiques constituent une forme distincte de la gestion des volumes, qui permet d’avoir des étendues non contiguës sur un ou plusieurs disques physiques. Les disques et les volumes dynamiques s’appuient sur le gestionnaire de disque logique (LDM) et le service de disque virtuel (VDS) et leurs fonctionnalités associées. Ces fonctionnalités vous permettent d’effectuer des tâches telles que la conversion de disques de base en disques dynamiques et la création de volumes à tolérance de panne. Pour encourager l’utilisation de disques dynamiques, la prise en charge des volumes de plusieurs partitions a été supprimée des disques de base et est désormais exclusivement prise en charge sur les disques dynamiques.

Les opérations suivantes ne peuvent être effectuées que sur des disques dynamiques :

-   Créez et supprimez des volumes simples, fractionnés, agrégés par bandes, en miroir et RAID-5.
-   Étendre un volume simple ou fractionné.
-   Supprimer un miroir d’un volume en miroir ou diviser le volume en miroir en deux volumes.
-   Réparez les volumes en miroir ou RAID-5.
-   Réactiver un disque manquant ou hors connexion.

Une autre différence entre les disques de base et les disques dynamiques est que les volumes de disques dynamiques peuvent être composés d’un ensemble d’étendues non contiguës sur un ou plusieurs disques physiques. En revanche, un volume sur un disque de base se compose d’un ensemble d’étendues contiguës sur un seul disque. en raison de l’emplacement et de la taille de l’espace disque requis par la base de données LDM, Windows ne peut pas convertir un disque de base en disque dynamique à moins qu’il n’y ait au moins 1 mo d’espace inutilisé sur le disque.

Que les disques dynamiques d’un système utilisent ou non le style de partition MBR ou GPT, vous pouvez créer jusqu’à 2 000 volumes dynamiques sur un système, bien que le nombre recommandé de volumes dynamiques soit inférieur ou égal à 32. Pour plus d’informations et pour connaître les autres considérations relatives à l’utilisation des disques et des volumes dynamiques, consultez [disques et volumes dynamiques](/previous-versions/windows/it-pro/windows-server-2003/cc757696(v=ws.10)).

Pour plus d’informations sur les fonctionnalités et les scénarios d’utilisation des disques dynamiques, consultez [que sont les disques et les volumes dynamiques ?](/previous-versions/windows/it-pro/windows-server-2003/cc737048(v=ws.10)).

Les opérations communes aux disques de base et dynamiques sont les suivantes :

-   Prend en charge les styles de partition MBR et GPT.
-   Vérifiez les propriétés du disque, telles que la capacité, l’espace libre disponible et l’état actuel.
-   Affichez les propriétés de partition, telles que le décalage, la longueur, le type et si la partition peut être utilisée comme volume système au démarrage.
-   Affichez les propriétés du volume, telles que la taille, l’affectation des lettres de lecteur, l’étiquette, le type, le nom du chemin d’accès Win32, le type de partition et le système de fichiers.
-   Établissez des attributions de lettres de lecteur pour les volumes de disque ou les partitions, et pour les lecteurs de CD-ROM.
-   Conversion d’un disque de base en disque dynamique ou d’un disque dynamique en disque de base.

sauf indication contraire, Windows partitionne initialement un lecteur en tant que disque de base par défaut. Vous devez convertir explicitement un disque de base en disque dynamique. Toutefois, les considérations relatives à l’espace disque doivent être prises en compte avant d’essayer de le faire. pour plus d’informations, consultez [comment convertir en disques de base et dynamiques dans Windows XP Professional](https://support.microsoft.com/kb/309044).

## <a name="partition-styles"></a>Styles de partition

Les *styles de partition*, parfois appelés schémas de *partition*, sont un terme qui fait référence à la structure sous-jacente particulière de la disposition du disque et à la façon dont le partitionnement est organisé, quelles sont les fonctionnalités et également quelles sont les limitations. pour démarrer Windows, les implémentations BIOS des ordinateurs x86 et x64 nécessitent un disque de base qui doit contenir au moins une partition d’enregistrement de démarrage principal (MBR) marquée comme active où les informations sur le système d’exploitation Windows (mais pas nécessairement l’ensemble de l’installation du système d’exploitation) et les informations sur les partitions stockées sur le disque. Ces informations sont placées à des emplacements distincts, et ces deux emplacements peuvent se trouver dans des partitions distinctes ou dans une partition unique. Tous les autres types de stockage de disque physique peuvent être configurés comme différentes combinaisons des deux styles de partition disponibles, décrits dans les sections suivantes. Pour plus d’informations sur les autres types de système, consultez la rubrique TechNet sur les [styles de partition](/previous-versions/windows/it-pro/windows-server-2003/cc738081(v=ws.10)).

Les disques dynamiques suivent des scénarios d’utilisation légèrement différents, comme indiqué précédemment, et la façon dont ils utilisent les deux styles de partition est affectée par cette utilisation. Étant donné que les disques dynamiques ne sont généralement pas utilisés pour contenir des volumes de démarrage système, cette discussion est simplifiée pour exclure les scénarios de cas spéciaux. Pour plus d’informations sur les dispositions des blocs de données de partition et sur les scénarios d’utilisation de disque de base ou dynamique liés aux styles de partition, consultez fonctionnement des disques et des volumes de [base](/previous-versions/windows/it-pro/windows-server-2003/cc739412(v=ws.10)) et fonctionnement des [disques et des volumes dynamiques](/previous-versions/windows/it-pro/windows-server-2003/cc758035(v=ws.10)).

### <a name="master-boot-record"></a>Enregistrement de démarrage principal

tous les ordinateurs x86 et x64 exécutant Windows peuvent utiliser le style de partition connu sous le nom d' *enregistrement de démarrage principal* (MBR). Le style de partition MBR contient une table de partition qui décrit où se trouvent les partitions sur le disque. comme MBR est le seul style de partition disponible sur les ordinateurs x86 avant Windows Server 2003 avec Service Pack 1 (SP1), vous n’avez pas besoin de choisir ce style. Elle est utilisée automatiquement.

Vous pouvez créer jusqu’à quatre partitions sur un disque de base à l’aide du schéma de partition MBR : soit quatre partitions principales, soit trois partitions principales et une étendue. La partition étendue peut contenir un ou plusieurs lecteurs logiques. La figure suivante illustre un exemple de présentation de trois partitions principales et une partition étendue sur un disque de base à l’aide de MBR. La partition étendue contient quatre lecteurs logiques étendus. La partition étendue peut être située à la fin du disque, mais il s’agit toujours d’un espace contigu unique pour les lecteurs logiques 1-n.

![trois partitions principales et une partition étendue sur un disque de base à l’aide de MBR](images/basic-mbr.png)

chaque partition, qu’elle soit principale ou étendue, peut être mise en forme de façon à être un volume Windows, avec une corrélation un-à-un de volume à partition. En d’autres termes, une partition unique ne peut pas contenir plus d’un seul volume. dans cet exemple, il existe un total de sept volumes disponibles pour Windows pour le stockage de fichiers. Une partition non mise en forme n’est pas disponible pour le stockage de fichiers dans Windows.

La disposition MBR du disque dynamique ressemble beaucoup à la disposition MBR du disque de base, sauf qu’une seule partition principale est autorisée (appelée « Partition LDM »), qu’aucune partition étendue n’est autorisée et qu’il existe une partition cachée à la fin du disque pour la base de données LDM. Pour plus d’informations sur le LDM, consultez la section [disques dynamiques](#basic-and-dynamic-disks) .

### <a name="guid-partition-table"></a>Table de partition GUID

les systèmes exécutant Windows Server 2003 avec SP1 et versions ultérieures peuvent utiliser un style de partition connu sous le nom de table de partition d’identificateur global unique (**GUID**), en plus du style de partition MBR. Un disque de base utilisant le style de partition GPT peut contenir jusqu’à 128 partitions principales, tandis que les disques dynamiques comporteront une seule partition LDM comme avec le partitionnement MBR. Étant donné que les disques de base utilisant le partitionnement GPT ne vous limitent pas à quatre partitions, vous n’avez pas besoin de créer des partitions étendues ou des lecteurs logiques.

Le style de partition GPT présente également les propriétés suivantes :

-   Autorise des partitions de plus de 2 téraoctets.
-   La fiabilité a été ajoutée à la protection de la réplication et de la vérification de redondance cyclique (CRC) de la table de partition.
-   Prise en charge des **GUID** de type de partition supplémentaires définis par les fabricants OEM (Original Equipment Manufacturers), les éditeurs de logiciels indépendants (ISV) et d’autres systèmes d’exploitation.

La disposition de partitionnement GPT pour un disque de base est illustrée dans la figure suivante.

![disposition GPT](images/basic-gpt.png)

La zone MBR de protection existe sur une disposition de partition GPT pour la compatibilité descendante avec les utilitaires de gestion des disques qui fonctionnent sur MBR. L’en-tête GPT définit la plage d’adresses de bloc logiques qui sont utilisables par les entrées de partition. L’en-tête GPT définit également son emplacement sur le disque, son **GUID** et une somme de contrôle de la redondance cyclique 32 bits (crc32) qui est utilisée pour vérifier l’intégrité de l’en-tête GPT. Chaque entrée de partition **GUID** commence par un GUID de type de partition. Le **GUID** du type de partition à 16 octets, qui est similaire à un ID de système dans la table de partition d’un disque MBR, identifie le type de données contenu dans la partition et identifie le mode d’utilisation de la partition, par exemple s’il s’agit d’un disque de base ou d’un disque dynamique. Notez que chaque entrée de partition **GUID** a une copie de sauvegarde.

Les dispositions de partition **GPT** de disque dynamique ressemblent à cet exemple de disque de base, mais comme indiqué précédemment, une seule entrée de partition LDM au lieu de 1-n partitions principales est autorisée sur les disques de base. Il existe également une partition de base de données LDM cachée avec une entrée de partition **GUID** correspondante. Pour plus d’informations sur le LDM, consultez la section [disques dynamiques](#basic-and-dynamic-disks) .

## <a name="detecting-the-type-of-disk"></a>Détection du type de disque

Il n’existe aucune fonction spécifique pour détecter par programme le type de disque sur lequel se trouve un fichier ou un répertoire particulier. Il existe une méthode indirecte.

* Transmettez le chemin d’accès du fichier ou du répertoire à [**GetVolumePathName**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew) pour obtenir le point de montage.
* Transmettez le point de montage à [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) pour obtenir le nom du volume.
* Supprimez la barre oblique inverse à la fin du nom du volume.
* Transmettez le nom du volume sans la barre oblique inverse de fin à [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) pour ouvrir le volume.
* Utilisez [**les \_ \_ \_ \_ \_ Extensions**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_volume_get_volume_disk_extents) du volume d’obtention de volume du volume IOCTL avec le descripteur de volume pour obtenir les numéros de disque.
* Utilisez les numéros de disque pour construire les chemins d’accès aux disques, tels que « \\ \\ ? \\ PhysicalDrive *X*».
* Transmettez chaque chemin d’accès au disque à [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) pour ouvrir le disque.
* Utilisez [**le \_ disque IOCTL \_ obtenir la disposition du \_ lecteur \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_disk_get_drive_layout_ex) , par exemple, pour obtenir la liste des partitions.
* Vérifiez les **PartitionType** pour chaque entrée de la liste des partitions.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de la gestion des volumes](about-volume-management.md)
</dt> <dt>

[Informations techniques de référence sur les disques et les volumes de base](/previous-versions/windows/it-pro/windows-server-2003/cc784732(v=ws.10))
</dt> <dt>

[Informations techniques de référence sur les disques et les volumes dynamiques](/previous-versions/windows/it-pro/windows-server-2003/cc785638(v=ws.10))
</dt> <dt>

[Stockage de base et Stockage dynamique dans Windows XP]( https://support.microsoft.com/kb/314343/)
</dt> </dl>

 

 
