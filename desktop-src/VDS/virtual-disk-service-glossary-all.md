---
description: Cette section fournit un glossaire des termes techniques utilisés dans la documentation du service de disque virtuel (VDS).
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 1cf28cfb-ce96-4659-955d-0088bddcb9ce
title: Glossaire du service de disque virtuel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7e73e9de8f6c30b69f2e39e78fae36e5c3ea547cccfed2f25f9a15327e3f8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118602992"
---
# <a name="virtual-disk-service-glossary"></a>Glossaire du service de disque virtuel

\[à partir de Windows 8 et Windows Server 2012, l’interface COM du [Service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion des Stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Cette section fournit un glossaire des termes techniques utilisés dans la documentation du service de disque virtuel (VDS).

<dl> <dt>

<span id="base.automagic_configuration"></span><span id="BASE.AUTOMAGIC_CONFIGURATION"></span>**configuration automatique**
</dt> <dd>

Fournisseur RAID matériel fournissant un ensemble de règles pour le choix du remappage de bloc logique LUN basé sur des attributs simples. Les fournisseurs automagic peuvent également modifier dynamiquement le mappage pour la gestion des erreurs ou des performances.

</dd> <dt>

<span id="base.binding_hints"></span><span id="BASE.BINDING_HINTS"></span>**indicateurs automagic**
</dt> <dd>

Informations fournies à un fournisseur automagic pour guider la configuration du bloc logique LUN. Les indicateurs incluent des informations sur la tolérance de panne, l’atomicité physique et le modèle d’accès aux e/s prévus.

</dd> <dt>

<span id="base.basic_disk"></span><span id="BASE.BASIC_DISK"></span>**disque de base**
</dt> <dd>

Un disque géré par le fournisseur de logiciels le plus simple possible. Le fournisseur de disque de base prend en charge uniquement les volumes qui sont directement mappés aux structures de données de configuration de partition.

</dd> <dt>

<span id="base.binding"></span><span id="BASE.BINDING"></span>**liant**
</dt> <dd>

Sélection pour un ensemble de mappages aux ressources physiques.

</dd> <dt>

<span id="base.convert"></span><span id="BASE.CONVERT"></span>**passer**
</dt> <dd>

Processus de conversion d’un disque de base en disque dynamique.

</dd> <dt>

<span id="base.configuration"></span><span id="BASE.CONFIGURATION"></span>**configuré**
</dt> <dd>

Collection des paramètres de fonctionnement qui fournissent le mappage d’un volume ou d’un numéro d’unité logique aux ressources physiques.

</dd> <dt>

<span id="base.controller"></span><span id="BASE.CONTROLLER"></span>**SideWinder**
</dt> <dd>

Programme logiciel qui contient l’intelligence du runtime pour un fournisseur de matériel.

</dd> <dt>

<span id="base.disk"></span><span id="BASE.DISK"></span>**libérer**
</dt> <dd>

Un disque physique ou un LUN RAID matériel. Les disques sont des cibles pour la charge d’e/s de stockage d’exécution ; Plug-and-Play (PNP) ne fait pas la distinction entre JBOD et les LUN.

</dd> <dt>

<span id="base.disk_platter"></span><span id="BASE.DISK_PLATTER"></span>**disque plateau**
</dt> <dd>

Sous-ensemble d’un Pack utilisé pour exporter ou importer des volumes à partir d’un Pack.

</dd> <dt>

<span id="base.disk_pack"></span><span id="BASE.DISK_PACK"></span>**Pack de disques**
</dt> <dd>

Consultez *Pack*.

</dd> <dt>

<span id="base.drive"></span><span id="BASE.DRIVE"></span>**unités**
</dt> <dd>

Une pile de disques physiques au sein d’un sous-système RAID matériel. Les lecteurs sont liés aux numéros d’unités logiques par le sous-système.

</dd> <dt>

<span id="base.dynamic_disk"></span><span id="BASE.DYNAMIC_DISK"></span>**disque dynamique**
</dt> <dd>

Un disque géré par un fournisseur RAID logiciel avec prise en charge de la reconfiguration de volume flexible. Un disque dynamique utilise une partition comme conteneur pour les volumes ; Il n’existe aucun mappage garanti.

</dd> <dt>

<span id="base.explicit_configuration"></span><span id="BASE.EXPLICIT_CONFIGURATION"></span>**configuration explicite**
</dt> <dd>

Configuration avec les paramètres, y compris le type de volume et la disposition exacte, pour une collection de volumes cibles.

</dd> <dt>

<span id="base.export"></span><span id="BASE.EXPORT"></span>**exporter**
</dt> <dd>

Action consistant à déplacer un plateau de disque et tous les volumes qu’il contient à l’extérieur d’un Pack.

</dd> <dt>

<span id="base.extent"></span><span id="BASE.EXTENT"></span>**étendue**
</dt> <dd>

Plage contiguë de secteurs logiques contribuant à un volume ou à un disque unique. Une étendue peut également être une plage de secteurs non alloués. En règle générale, un système de fichiers affiche les détails de l’étendue à un utilisateur final.

</dd> <dt>

<span id="base.guid_partition_table_gpt"></span><span id="BASE.GUID_PARTITION_TABLE_GPT"></span>**Table de partition GUID (GPT)**
</dt> <dd>

Structures utilisées par le microprogramme EFI. GPT est l’un des deux formats de données de configuration de logiciel de niveau le plus bas utilisés par le microprogramme de la plateforme pour localiser un système d’exploitation de démarrage ou une autre image exécutable.

</dd> <dt>

<span id="base.hardware_provider"></span><span id="BASE.HARDWARE_PROVIDER"></span>**fournisseur de matériel**
</dt> <dd>

Ensemble de logiciels qui s’exécutent sur l’ordinateur hôte, un adaptateur de bus et éventuellement un sous-système de stockage externe qui fonctionne ensemble pour faire surface et gérer les LUN RAID. Les fournisseurs de matériel pour la plupart des sous-systèmes de stockage externes contiennent uniquement des logiciels basés sur l’hôte et en mode utilisateur.

</dd> <dt>

<span id="base.health"></span><span id="BASE.HEALTH"></span>**assurance**
</dt> <dd>

État actuel de la gestion des erreurs d’un volume ou d’un numéro d’unité logique.

</dd> <dt>

<span id="base.hot_spotting"></span><span id="BASE.HOT_SPOTTING"></span>**remplacement à chaud**
</dt> <dd>

Ajout temporaire d’un plex de volume à un volume.

</dd> <dt>

<span id="base.import"></span><span id="BASE.IMPORT"></span>**port**
</dt> <dd>

Action consistant à déplacer un plateau de disque et tous ses volumes dans un pack existant.

</dd> <dt>

<span id="base.JBOD"></span><span id="base.jbod"></span><span id="BASE.JBOD"></span>**juste une série de disques (JBOD)**
</dt> <dd>

Collection de piles physiques sans le contrôle coordonné fourni par un périphérique RAID matériel.

</dd> <dt>

<span id="base.logical_block_number_LBN"></span><span id="base.logical_block_number_lbn"></span><span id="BASE.LOGICAL_BLOCK_NUMBER_LBN"></span>**Numéro de bloc logique (LBN)**
</dt> <dd>

Plus petite unité adressable de données de stockage. LBN est utilisé avec les protocoles de commande d’e/s.

</dd> <dt>

<span id="base.logical_block_mapping"></span><span id="BASE.LOGICAL_BLOCK_MAPPING"></span>**mappage de bloc logique**
</dt> <dd>

Transformation des blocs logiques présentés à un fournisseur à ceux exposés par le fournisseur.

</dd> <dt>

<span id="base.logical_Unit_Number_LUN"></span><span id="base.logical_unit_number_lun"></span><span id="BASE.LOGICAL_UNIT_NUMBER_LUN"></span>**Numéro d’unité logique (LUN)**
</dt> <dd>

Unité de stockage physiquement adressable, telle qu’elle est exposée par un sous-système RAID matériel. Ce terme peut également faire référence à l’identificateur SCSI pour l’unité de stockage.

</dd> <dt>

<span id="base.LUN_number"></span><span id="base.lun_number"></span><span id="BASE.LUN_NUMBER"></span>**Numéro de LUN**
</dt> <dd>

Nombre qu’un fournisseur de matériel VDS attribue à un numéro d’unité logique (LUN) dans un groupe. Ce n’est pas le même que le « numéro d’unité logique » dans l’adresse SCSI du disque.

</dd> <dt>

<span id="base.management_service"></span><span id="BASE.MANAGEMENT_SERVICE"></span>**service de gestion**
</dt> <dd>

Programme logiciel qui s’exécute en fonction des besoins pour effectuer la configuration du volume, l’analyse ou la gestion des erreurs.

</dd> <dt>

<span id="base.mapping"></span><span id="BASE.MAPPING"></span>**mappage**
</dt> <dd>

Un volume exposé au système d’exploitation et ayant un nom de volume associé (une lettre de lecteur). Un volume est accessible par un système de fichiers.

</dd> <dt>

<span id="base.masking"></span><span id="BASE.MASKING"></span>**masquage**
</dt> <dd>

Un disque non reconnu par le système d’exploitation. Un disque peut être masqué par le sous-système RAID matériel, le commutateur, la réserve SCSI par un autre ordinateur hôte ou le logiciel dans la pile de disques.

</dd> <dt>

<span id="base.master_Boot_Record_partitioning_MBR"></span><span id="base.master_boot_record_partitioning_mbr"></span><span id="BASE.MASTER_BOOT_RECORD_PARTITIONING_MBR"></span>**partitionnement d’enregistrement de démarrage principal (MBR)**
</dt> <dd>

MBR est l’un des deux formats de données de configuration de logiciel de niveau le plus bas et est utilisé par le microprogramme BIOS pour localiser une image de système d’exploitation amorçable.

</dd> <dt>

<span id="base.member"></span><span id="BASE.MEMBER"></span>**membre**
</dt> <dd>

Collection d’étendues de disque concaténées contenues sur un ou plusieurs disques. Un disque ne peut contribuer qu’à un seul membre d’un volume.

</dd> <dt>

<span id="base.mirror"></span><span id="BASE.MIRROR"></span>**mémoire**
</dt> <dd>

Un mappage de volume ou de disque qui gère au moins deux copies de données identiques. Le type de mappage est également appelé RAID niveau 1.

</dd> <dt>

<span id="base.pack"></span><span id="BASE.PACK"></span>**presse**
</dt> <dd>

Collection de volumes logiques et de disques sous-jacents. Un Pack est l’unité de fermeture transitive pour un volume. Les Disk packs et les groupes de disques dynamiques sont des termes pour le même élément.

</dd> <dt>

<span id="base.parity_stripe"></span><span id="BASE.PARITY_STRIPE"></span>**entrelacement de parité**
</dt> <dd>

Un mappage de volume ou de disque qui gère les informations de contrôle de parité ainsi que les données. Chaque fournisseur fournit le schéma de protection et de mappage exacts. Comprend les configurations RAID 3, 4, 5 et 6.

</dd> <dt>

<span id="base.partially_directed_configuration"></span><span id="BASE.PARTIALLY_DIRECTED_CONFIGURATION"></span>**configuration partiellement dirigée**
</dt> <dd>

Configuration de volume ou de disque qui n’est pas entièrement explicite. Le type de liaison et une collection de ressources cibles sont spécifiés ; la disposition réelle n’est pas. La configuration partiellement dirigée est la configuration de volume la plus courante.

</dd> <dt>

<span id="base.partition"></span><span id="BASE.PARTITION"></span>**non**
</dt> <dd>

Plage contiguë de secteurs logiques décrite par une seule entrée dans la structure MBR ou GPT. Sur les disques de base, les partitions correspondent directement aux volumes simples. Les structures de partition sont partagées entre le microprogramme du BIOS ou de la plateforme EFI et un système d’exploitation ou une autre image de démarrage.

</dd> <dt>

<span id="base.path"></span><span id="BASE.PATH"></span>**d**
</dt> <dd>

Le chemin d’accès entre un ordinateur et un disque ou un numéro d’unité logique matériel externe.

</dd> <dt>

<span id="base.plex"></span><span id="BASE.PLEX"></span>**duplex**
</dt> <dd>

Un membre d’un volume ou d’un numéro d’unité logique mis en miroir.

</dd> <dt>

<span id="base.port"></span><span id="BASE.PORT"></span>**importer**
</dt> <dd>

Point de terminaison d’un chemin d’accès sur un disque.

</dd> <dt>

<span id="base.redundant_array_of_independent_disks_RAID"></span><span id="base.redundant_array_of_independent_disks_raid"></span><span id="BASE.REDUNDANT_ARRAY_OF_INDEPENDENT_DISKS_RAID"></span>**baie redondante de disques indépendants (RAID)**
</dt> <dd>

Ensemble de techniques pour la gestion de plusieurs disques.

</dd> <dt>

<span id="base.runtime_service"></span><span id="BASE.RUNTIME_SERVICE"></span>**service Runtime**
</dt> <dd>

Programme logiciel qui s’exécute sur la base d’une demande d’e/s.

</dd> <dt>

<span id="base.simple_disk"></span><span id="BASE.SIMPLE_DISK"></span>**disque simple**
</dt> <dd>

Une broche qui n’est pas connectée à un contrôleur RAID matériel. Voir aussi simplement une série de disques (JBOD).

</dd> <dt>

<span id="base.software_provider"></span><span id="BASE.SOFTWARE_PROVIDER"></span>**fournisseur de logiciels**
</dt> <dd>

Logiciel basé sur l’hôte qui expose des volumes logiques et s’exécute sur des disques. Un fournisseur de logiciels comprend des services d’exécution en mode noyau, des données de configuration et des services de gestion en mode utilisateur.

</dd> <dt>

<span id="base.span"></span><span id="BASE.SPAN"></span>**répartis**
</dt> <dd>

Un mappage linéaire de volume ou de disque de plusieurs extensions de disque ou de lecteur discontinues. Les étendues peuvent se trouver sur un ou plusieurs axes ou numéros d’unités logiques.

</dd> <dt>

<span id="base.spindle"></span><span id="BASE.SPINDLE"></span>**pivot**
</dt> <dd>

Unité physique de stockage sur disque.

</dd> <dt>

<span id="base.stacking"></span><span id="BASE.STACKING"></span>**empilement**
</dt> <dd>

Opération de construction d’un volume ou d’un numéro d’unité logique en effectuant plusieurs opérations de mappage de bloc logique. Un volume agrégé par bandes en miroir en est un exemple. L’empilement le plus courant se produit lorsque le RAID logiciel est utilisé sur des numéros d’unités logiques créés par RAID matériel.

</dd> <dt>

<span id="base.stripe"></span><span id="BASE.STRIPE"></span>**Stripe**
</dt> <dd>

Un mappage de volume ou de disque qui entrelace les extensions contiguës sur plusieurs volumes, disques ou lecteurs. Ce mappage est également appelé RAID 0.

</dd> <dt>

<span id="base.status"></span><span id="BASE.STATUS"></span>**statu**
</dt> <dd>

Disponibilité actuelle d’un volume, d’un disque ou d’un lecteur.

</dd> <dt>

<span id="base.subsystem"></span><span id="BASE.SUBSYSTEM"></span>**sous-système**
</dt> <dd>

Instanciation du logiciel du fournisseur de matériel. Un sous-système contient au moins un contrôleur et un lecteur. Si le sous-système est externe à l’ordinateur, un ou plusieurs chemins d’accès réseau connectent le sous-système à l’ordinateur.

</dd> <dt>

<span id="base.jello"></span><span id="BASE.JELLO"></span>**État de transition**
</dt> <dd>

État du mappage logique à physique qui est en cours de modification.

</dd> <dt>

<span id="base.uninitialized_disk"></span><span id="BASE.UNINITIALIZED_DISK"></span>**disque non initialisé**
</dt> <dd>

Disque qui n’est pas membre d’un Pack.

</dd> <dt>

<span id="base.unmasked_disk"></span><span id="BASE.UNMASKED_DISK"></span>**disque non masqué**
</dt> <dd>

Disque visible par le système d’exploitation. Le contenu d’un disque non masqué est visible pour les gestionnaires de volume logiciel, les systèmes de fichiers, etc.

</dd> <dt>

<span id="base.volume"></span><span id="BASE.VOLUME"></span>**agrégat**
</dt> <dd>

Un certain nombre d’étendues de disque liées à une plage pratiquement contiguë de blocs logiques. Un volume est accessible par le biais d’une lettre de lecteur, d’un dossier monté ou d’un chemin d’accès de GUID de volume.

</dd> </dl>

 

 
