---
description: Le format de disque dur virtuel (VHD) est une spécification de format d’image disponible publiquement qui permet l’encapsulation du disque dur dans un fichier individuel utilisable par le système d’exploitation en tant que disque virtuel dans les mêmes modes d’utilisation des disques durs physiques.
MS-HAID: vhd.about\_vhd
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: À propos du disque dur virtuel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29ea37851360e70c1108e0715a47c77163c2c2fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751524"
---
# <a name="span-idvhdabout_vhdspanabout-vhd"></a><span id="vhd.about_vhd"></span>À propos du disque dur virtuel

Le format de disque dur virtuel (VHD) est une [spécification](https://download.microsoft.com/download/f/f/e/ffef50a5-07dd-4cf8-aaa3-442c0673a029/Virtual%20Hard%20Disk%20Format%20Spec_10_18_06.doc) de format d’image disponible publiquement qui permet l’encapsulation du disque dur dans un fichier individuel utilisable par le système d’exploitation en tant que *disque virtuel* dans les mêmes modes d’utilisation des disques durs physiques. Ces disques virtuels peuvent héberger des systèmes de fichiers natifs (NTFS, FAT, exFAT et UDF) tout en prenant en charge les opérations de disque et de fichier standard. La prise en charge des API VHD permet de gérer les disques virtuels. Les disques virtuels créés avec l’API VHD peuvent fonctionner en tant que disques de démarrage.

L’utilisation des fichiers VHD est un exemple de la fonctionnalité [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) dans Windows 7, windows Server 2008, Virtual Server et Windows Virtual PC. Ces produits utilisent l’API VHD pour contenir l’image du système d’exploitation Windows utilisée par une machine virtuelle comme disque de démarrage système.

Le kit de développement logiciel (SDK) Microsoft Windows intègre la prise en charge du disque dur virtuel natif pour l’utilisation des disques virtuels, ce qui permet aux développeurs et aux administrateurs de créer, gérer et déployer plus facilement des images Windows dans des fichiers VHD à l’aide des outils de gestion ou de prise en charge des API de plateforme. Il n’est pas nécessaire d’installer des applications distinctes ou d’implémenter un analyseur de format VHD pour activer ces opérations. Ces API permettent l’utilisation générique de disques virtuels indépendamment des autres technologies de virtualisation.

## <a name="span-idterminologyspanspan-idterminologyspanspan-idterminologyspanterminology"></a><span id="Terminology"></span><span id="terminology"></span><span id="TERMINOLOGY"></span>Correspondance

Le *magasin* de stockage de terme est utilisé pour faire référence au fichier physique qui existe sur le disque dur réel. Le magasin de stockage est représenté par un *fichier image de disque dur virtuel*.

Les termes *dynamique*, *extensible* et *épars* sont souvent utilisés indifféremment lorsque vous faites référence à des disques virtuels extensibles de façon dynamique. Pour la technologie de disque dur virtuel, ces termes sont identiques.

## <a name="span-idvhd_system_features_overviewspanspan-idvhd_system_features_overviewspanspan-idvhd_system_features_overviewspanvhd-system-features-overview"></a><span id="VHD_System_Features_Overview"></span><span id="vhd_system_features_overview"></span><span id="VHD_SYSTEM_FEATURES_OVERVIEW"></span>Vue d’ensemble des fonctionnalités du système VHD

Le diagramme suivant présente une vue d’ensemble des fonctionnalités de disque dur virtuel et de leurs relations.

![diagramme de blocs VHD](images/vhd.png)

Vous trouverez ci-dessous une explication récapitulative des fonctionnalités décrites précédemment.

API Windows natives en mode utilisateur :

-   VirtDisk.dll-bibliothèque commune pour les API de gestion du disque dur virtuel.

Wrappers de gestion spécifiques au domaine en mode utilisateur :

-   [API VHD VDS](/windows/desktop/VDS/about-vds) -wrappers de modèle objet VDS pour les API Windows VHD.

Pilotes en mode noyau :

-   VDrvRoot.sys-énumérateur de lecteur virtuel racine.
-   FsDepends.sys-gestion des dépendances de volume imbriquée.
-   Vhdmp.sys-l’analyseur VHD et le fournisseur de propriétés de dépendance.

La documentation du kit de développement logiciel (SDK) de cette section traite des API de disque dur virtuel Windows natives en mode utilisateur.

## <a name="span-idvirtual_disk_typesspanspan-idvirtual_disk_typesspanspan-idvirtual_disk_typesspanvirtual-disk-types"></a><span id="Virtual_Disk_Types"></span><span id="virtual_disk_types"></span><span id="VIRTUAL_DISK_TYPES"></span>Types de disques virtuels

Il existe des considérations relatives à l’utilisation des disques virtuels, ainsi que les types de disques virtuels disponibles :

-   **Résolu**: le fichier image de disque dur virtuel est pré-alloué sur le magasin de stockage pour la taille maximale demandée.
-   **Extensible**, également connu sous le nom de « dynamique », « extensible dynamiquement » et « fragmenté », le fichier image de disque dur virtuel utilise uniquement l’espace disponible sur le magasin de stockage, si nécessaire, pour stocker les données réelles que le disque virtuel contient actuellement. Lors de la création de ce type de disque virtuel, l’API VHD ne teste pas l’espace libre sur le disque physique en fonction de la taille maximale demandée. par conséquent, il est possible de créer un disque virtuel dynamique avec une taille maximale supérieure à l’espace libre disponible sur le disque physique. Pour plus d’informations, consultez [**ExpandVirtualDisk**](/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk).
    **Remarque**  La taille maximale d’un disque virtuel dynamique est de 2 040 Go.

     

-   **Différenciation**: un disque virtuel parent est utilisé comme base de ce type, avec toutes les écritures suivantes écrites sur le disque virtuel en tant que différences par le nouveau fichier image de disque dur virtuel de différenciation, et le fichier image de disque dur virtuel parent n’est pas modifié. Par exemple, si vous disposez d’un disque virtuel de système d’exploitation de démarrage système propre au système d’exploitation en tant que parent et que vous désignez le disque virtuel de différenciation comme disque virtuel actuel à utiliser par le système, le système d’exploitation sur le disque virtuel parent reste dans son état d’origine pour une récupération rapide ou pour créer rapidement davantage d’images de démarrage basées sur des disques virtuels Pour plus d’informations, consultez [**MergeVirtualDisk**](/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk).
    **Remarque**  La taille maximale d’un disque virtuel de différenciation est de 2 040 Go.

     

Tous les types de disques virtuels ont une taille minimale de 3 Mo.

## <a name="span-idrelated_topicsspanrelated-topics"></a><span id="related_topics"></span>Rubriques connexes

[À propos de VDS](/windows/desktop/VDS/about-vds)

[Référence VHD](vhd-reference.md)

[Spécification de format d’image de disque dur virtuel](https://download.microsoft.com/download/f/f/e/ffef50a5-07dd-4cf8-aaa3-442c0673a029/Virtual%20Hard%20Disk%20Format%20Spec_10_18_06.doc)

 

 
