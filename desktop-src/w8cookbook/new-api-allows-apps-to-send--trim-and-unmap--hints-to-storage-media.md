---
title: La nouvelle API permet aux applications d’envoyer des indicateurs « supprimer et annuler le mappage » sur des supports de stockage
description: La nouvelle API permet aux applications d’envoyer \ 0034 ; TRIM et DEMAPPAGE \ 0034 ; indications sur les supports de stockage
ms.assetid: DDBC3592-BD4D-4826-83FE-387564DA07E8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78d79d47dceb5c8bf2e7575836c9a40ddf0347b7e5c616ab4b7196b547742c97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028827"
---
# <a name="new-api-allows-apps-to-send-trim-and-unmap-hints-to-storage-media"></a>La nouvelle API permet aux applications d’envoyer des indicateurs « supprimer et annuler le mappage » sur des supports de stockage

## <a name="platforms"></a>Plateformes

**Clients** – Windows 8  
**serveurs** – Windows Server 2012  


## <a name="description"></a>Description

Les indicateurs de découpage informent le lecteur que certains secteurs qui ont été alloués précédemment ne sont plus nécessaires à l’application et peuvent être purgés. Cette valeur est généralement utilisée lorsqu’une application effectue des allocations d’espace importantes par le biais d’un fichier, puis gère automatiquement les allocations dans le fichier (par exemple, les fichiers de disque dur virtuel).

**Qu’est-ce que TRIM ?**

Les disques SSD (Solid State Drives) sont généralement des appareils avec effacement de blocs basés sur la mémoire flash ; Cela signifie que lorsque les données sont écrites dans le SSD, elles ne peuvent pas être remplacées et doivent être écrites ailleurs jusqu’à ce que le bloc puisse être récupéré par le garbage collector. Étant donné que le SSD n’a pas de mécanisme interne pour déterminer que certains blocs sont supprimés et que d’autres sont nécessaires. La seule fois où le SSD peut marquer un « impropre » de secteur est lorsqu’il est trop écrit. Dans d’autres cas, par exemple lors de la suppression d’un fichier, le disque SSD conserve ces secteurs, car la suppression est effectuée en tant que modification de table de fichiers maîtres (MFT) uniquement, et non en tant qu’opération à tous les secteurs du fichier. dans Windows 7, nous avons introduit une méthode standard de communication avec les disques ssd à propos des secteurs qui ne sont plus nécessaires. Cette commande est définie dans la [spécification T13](https://www.t13.org/Standards/Default.aspx?DocumentType=3) comme commande Trim ; NTFS envoie la commande TRIM pour certaines opérations Inline normales, telles que « DeleteFile ».

**Autres utilisations du découpage dans le monde du stockage**

comme les disques ssd, les réseaux de zone de stockage (san) et le nouveau Windows 8 les implémentations d’espaces logiciels consomment les indicateurs de commande TRIM pour gérer leurs espaces dans les environnements alloués dynamiquement. Les espaces San et logiciels allouent des régions de stockage dans des tailles supérieures à celles des secteurs ou des clusters (n’importe où entre 1 Mo et 1 Go). Lorsqu’ils reçoivent des indicateurs de découpage pour la taille d’allocation (ou supérieur à la taille d’allocation), le SAN/SSD peut désallouer une région pour libérer de l’espace pour d’autres fichiers. Ils transmettent généralement tous les indicateurs de découpage au média sous-jacent (SSD ou HDD) afin qu’ils puissent consommer l’espace libéré comme il convient. Elles ne déplacent généralement pas les données dans les régions de désallocation, ni n’effectuent le suivi des zones de découpage dans les zones désallouées (lorsque la région est vide).

Les réseaux San alloués dynamiquement utilisent les indicateurs de découpage qui leur sont transmis pour réduire l’encombrement de stockage physique global, réduisant ainsi les coûts. La [spécification SCSI de T10](https://www.t10.org) définit la commande’Annuler' (semblable à la commande Trim). ici, la commande s’applique à tous les types de stockage, y compris les disques durs, les disques SSD et d’autres. La commande de mappage permet de supprimer des blocs physiques de l’allocation du SAN.

## <a name="how-to-use-the-new-api"></a>Utilisation de la nouvelle API


```
#define FSCTL_FILE_LEVEL_TRIM CTL_CODE(FILE_DEVICE_FILE_SYSTEM, 130, METHOD_BUFFERED, FILE_WRITE_DATA)

Where 
typedef struct _EXTENT_PAIR {
    ULONGLONG Offset;
    ULONGLONG Length;
} EXTENT_PAIR, *PEXTENT_PAIR;

typedef struct _FILE_LEVEL_TRIM {
    //
    // A count of how many Offset:Length pairs are given
    //
    DWORD PairCount;
    //
    // All the pairs.
    //
    EXTENT_PAIR Pairs[1];
} FILE_LEVEL_TRIM, *PFILE_LEVEL_TRIM;
```



Le découpage de fichier est passé via la mémoire tampon si possible ou de manière asynchrone (sans mise en mémoire tampon) au découpage de commande du DSM IOCTL d’appareil. Elle est mappée à la commande TRIM pour les périphériques ATA et à la commande de mappage pour les périphériques SCSI. Le code d’ajustement de fichier envoie les régions un par un, comme spécifié par les étendues ci-dessus.

Le découpage de fichier n’attend pas les retours de l’appareil, car les commandes TRIM et DEMAPPAGE sont définies comme indicateurs sur le support de stockage sous-jacent et les codes de retour ne sont pas attendus.

**Flux de travail de bout en bout :**

1.  Découper le fichier d’appel
    1.  L’ajustement de fichier examine les entrées pour rechercher les erreurs
    2.  La suppression de fichier fractionne les étendues dans les régions LCN
    3.  La suppression des fichiers est arrondie à la taille des régions mal alignées qui sont passées à la suppression
    4.  La suppression de fichiers purge les entrées du cache qui se rapportent aux zones de suppression.
    5.  La suppression de fichier passe le \_ DSM ioctl (Trim) par région
2.  La suppression du fichier renvoie ou des erreurs
    1.  La vérification des erreurs est effectuée au niveau de la validité de l’entrée
    2.  Si seules certaines étendues sont valides, une erreur est retournée pour l’appel complet de l’API

**Cas d’utilisation**

**Disque dur virtuel (VHD) de consommateur monté sur un disque SSD :**

Le disque dur virtuel est initialement monté sur le média non utilisé « Clean ». Au fur et à mesure que le disque dur virtuel est utilisé, le disque dur virtuel consomme des parties du support de stockage pour les fichiers, etc. Lorsqu’il supprime des fichiers du support de stockage, ces fichiers ne sont pas supprimés du disque SSD puisque le VHD complet est stocké sous la forme d’un fichier sur le disque SSD. L’environnement Hyper-V appelle la suppression de fichiers pour toutes les régions qui sont supprimées lorsque Delete-File se produit dans l’environnement VHD. Les \_ suppressions de fichiers sont traduites dans le SSD pour permettre l’optimisation des performances des disques SSD.

**VHD de consommateur monté sur un réseau SAN alloué dynamiquement :**

Le disque dur virtuel est initialement monté sur une plaque minimale d’un environnement dynamiquement approvisionné. Au fur et à mesure que les fichiers sont stockés dans le disque dur virtuel, l’encombrement de stockage du disque dur virtuel augmente en multiples de tablettes. Lorsque des fichiers sont supprimés du disque dur virtuel, Hyper-V appelle la \_ Suppression de fichiers sur le réseau San sous-jacent alloué dynamiquement. Si les SUPPRESSIONs sont supérieures à la granularité de la dalle, le réseau SAN peut maintenant supprimer une dalle et, par conséquent, réduire l’encombrement du disque dur virtuel sur ce réseau SAN.

si le disque dur virtuel réside sur un serveur Windows 8, l’optimiseur de Stockage enverra également des découpages pour réduire l’encombrement des dalles du disque dur virtuel à partir du disque dur virtuel monté.

## <a name="tests"></a>Tests

Il n’existe pas d’API comparables dans les versions antérieures du système d’exploitation. L’API elle-même ne doit pas avoir d’impact sur les performances. Toutefois, le support de stockage (s’il est implémenté correctement) peut présenter de meilleures performances en écriture. L’API doit être utilisée très attentivement ; seules les extensions qui ne sont plus nécessaires doivent être transmises, car celles-ci sont définitivement supprimées du support de stockage.

## <a name="resources"></a>Ressources

-   [Spécification T13](http://www.t13.org/Standards/Default.aspx?DocumentType=3)
-   [Spécification SCSI de T10](https://www.t10.org/)

 

 




