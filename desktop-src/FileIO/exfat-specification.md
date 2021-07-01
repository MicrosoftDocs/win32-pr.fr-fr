---
description: Spécification du système de fichiers exFat.
title: spécification du système de fichiers exFAT
ms.topic: article
ms.date: 08/27/2019
ms.openlocfilehash: 94b5bcdc69201573bc92290c148a7d3ce8304868
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119014"
---
# <a name="exfat-file-system-specification"></a>spécification du système de fichiers exFAT

## <a name="1-introduction"></a>1 Introduction

Le système de fichiers exFAT est le successeur de FAT32 dans la famille de systèmes de fichiers FAT. Cette spécification décrit le système de fichiers exFAT et fournit toutes les informations nécessaires pour implémenter le système de fichiers exFAT.

### <a name="11-design-goals"></a>1,1 objectifs de conception

Le système de fichiers exFAT a trois objectifs de conception centraux (voir la liste ci-dessous).

1. *Conserver la simplicité des systèmes de fichiers basés sur FAT.*

   > Deux des avantages des systèmes de fichiers basés sur FAT sont la simplicité et la facilité d’implémentation. Dans l’esprit de ses prédécesseurs, les implémenteurs doivent trouver le exFAT relativement simple et facile à implémenter.

2. *Activez les fichiers et les périphériques de stockage de très grande taille.*

   > Le système de fichiers exFAT utilise 64 bits pour décrire la taille des fichiers, ce qui permet d’activer les applications qui dépendent de fichiers volumineux. Le système de fichiers exFAT autorise également les clusters d’une taille de 32 Mo, ce qui permet de disposer d’un grand nombre de périphériques de stockage.

3. *Intégrez l’extensibilité pour une innovation future.*

   > Le système de fichiers exFAT intègre l’extensibilité dans sa conception, ce qui permet au système de fichiers de suivre le rythme des innovations en matière de stockage et de modifications de l’utilisation.

### <a name="12-specific-terminology"></a>Terminologie spécifique à 1,2

Dans le contexte de cette spécification, certains termes (voir le [tableau 1](#table-1-definition-of-terms-which-carry-very-specific-meaning)) transmettent une signification spécifique pour la conception et l’implémentation du système de fichiers exFAT.

<div id="table-1-definition-of-terms-which-carry-very-specific-meaning" />

**Tableau 1 définition des termes qui ont une signification très spécifique**

<table>
<thead>
<tr class="header">
<th><strong>Terme</strong></th>
<th><strong>Définition</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Arrête</td>
<td>Cette spécification utilise le terme « doit » pour décrire un comportement qui est obligatoire.</td>
</tr>
<tr class="even">
<td>Recommandé</td>
<td>Cette spécification utilise le terme « doit » pour décrire un comportement recommandé, mais ne rend pas obligatoire.</td>
</tr>
<tr class="odd">
<td>Mai</td>
<td>Cette spécification utilise le terme « peut » pour décrire un comportement qui est facultatif.</td>
</tr>
<tr class="even">
<td>Obligatoire</td>
<td>Ce terme décrit un champ ou une structure qu’une implémentation doit modifier et doit interpréter comme décrit dans cette spécification.</td>
</tr>
<tr class="odd">
<td>Facultatif</td>
<td>Ce terme décrit un champ ou une structure qu’une implémentation peut ou non prendre en charge. Si une implémentation de prend en charge un champ ou une structure facultatif donné, elle est modifiée et doit interpréter le champ ou la structure comme décrit dans cette spécification.</td>
</tr>
<tr class="even">
<td>Indéfini</td>
<td>Ce terme décrit le contenu d’un champ ou d’une structure que l’implémentation peut modifier si nécessaire (par exemple, si elle est définie sur zéro lors de la définition de champs ou de structures environnants) et ne doit pas interpréter pour conserver une signification spécifique.</td>
</tr>
<tr class="odd">
<td>Réservé</td>
<td><p>Ce terme décrit les implémentations de champ ou de structure :</p>
<ol type="1">
<li><p>Doit s’initialiser à zéro et ne doit pas être utilisé à quelque fin que ce soit</p></li>
<li><p>Ne doit pas interpréter, sauf en cas de calcul de somme de contrôle</p></li>
<li><p>Préserve les opérations qui modifient les champs ou structures environnantes</p></li>
</ol></td>
</tr>
</tbody>
</table>

### <a name="13-full-text-of-common-acronyms"></a>1,3 texte intégral des acronymes courants

Cette spécification utilise des acronymes couramment utilisés dans le secteur des ordinateurs personnels (voir [tableau 2](#table-2-full-text-of-common-acronyms)).

<div id="table-2-full-text-of-common-acronyms" />

**Tableau 2 texte intégral des acronymes courants**

| **Acronyme** | **Texte complet**                                      |
|-------------|----------------------------------------------------|
| ASCII       | code ASCII |
| BIOS        | Système de sortie d’entrée de base                          |
| Processeur         | Unité centrale de traitement                            |
| exFAT       | Table d’allocation de fichiers extensible                   |
| FAT         | Table d’allocation de fichiers                              |
| FAT12       | Table d’allocation de fichiers, index de cluster 12 bits      |
| FAT16       | Table d’allocation de fichiers, index de cluster 16 bits      |
| FAT32       | Table d’allocation de fichiers, index de cluster 32 bits      |
| GPT         | Table de partition GUID                               |
| GUID        | Identificateur global unique (voir la [Section 10,1](#101-globally-unique-identifiers-guids))      |
| INT         | Suspendre                                          |
| partition         | Enregistrement de démarrage principal                                 |
| texFAT      | ExFAT sécurisé pour les transactions                             |
| UTC         | Temps universel coordonné                         |

### <a name="14-default-field-and-structure-qualifiers"></a>Qualificateurs de champ et de structure par défaut 1,4

Les champs et les structures de cette spécification ont les qualificateurs suivants (voir la liste ci-dessous), sauf indication contraire dans les notes de spécification.

1. Non signé

2. Utilisez la notation décimale pour décrire les valeurs, dans le cas contraire ; Cette spécification utilise la lettre « h » après correction pour indiquer les nombres hexadécimaux et encadre les GUID entre accolades.

3. Sont au format Little endian

4. Ne pas exiger un caractère de fin null pour les chaînes

### <a name="15-windows-ce-and-texfat"></a>1,5 Windows CE et TexFAT

TexFAT est une extension de exFAT qui ajoute une sémantique opérationnelle de transactions sécurisées par-dessus le système de fichiers de base. TexFAT est utilisé par Windows CE.
TexFAT requiert l’utilisation des deux graisses et des bitmaps d’allocation pour une utilisation dans les transactions. Il définit également plusieurs structures supplémentaires, notamment les descripteurs de remplissage et les descripteurs de sécurité.

## <a name="2-volume-structure"></a>2 structure du volume

Un volume est l’ensemble de toutes les structures de système de fichiers et de l’espace de données nécessaires pour stocker et récupérer des données utilisateur. Tous les volumes exFAT contiennent quatre régions (voir le [tableau 3](#table-3-volume-structure)).

<div id="table-3-volume-structure" />

**Tableau 3-structure du volume**

<table>
<thead>
<tr class="header">
<th><strong>Nom de la sous-région</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>secteur</strong></p></th>
<th><p><strong>Taille</strong></p>
<p><strong>Sector</strong></p></th>
<th><strong>Commentaires</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Région de démarrage principale</strong></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>Secteur de démarrage principal</td>
<td>0</td>
<td>1</td>
<td>Cette sous-région est obligatoire et la <a href="#31-main-and-backup-boot-sector-sub-regions">Section 3,1</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>Principaux secteurs de démarrage étendus</td>
<td>1</td>
<td>8</td>
<td>Cette sous-région est obligatoire et la <a href="#32-main-and-backup-extended-boot-sectors-sub-regions">Section 3,2</a>) définit son contenu.</td>
</tr>
<tr class="even">
<td>Principaux paramètres OEM</td>
<td>9</td>
<td>1</td>
<td>Cette sous-région est obligatoire et la <a href="#33-main-and-backup-oem-parameters-sub-regions">Section 3,3</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>Principal réservé</td>
<td>10</td>
<td>1</td>
<td>Cette sous-région est obligatoire et son contenu est réservé.</td>
</tr>
<tr class="even">
<td>Somme de contrôle de démarrage principale</td>
<td>11</td>
<td>1</td>
<td>Cette sous-région est obligatoire et la <a href="#34-main-and-backup-boot-checksum-sub-regions">Section 3,4</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td><strong>Région de démarrage de sauvegarde</strong></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>Secteur de démarrage de sauvegarde</td>
<td>12</td>
<td>1</td>
<td>Cette sous-région est obligatoire et la <a href="#31-main-and-backup-boot-sector-sub-regions">Section 3,1</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>Sauvegarder les secteurs de démarrage étendu</td>
<td>13</td>
<td>8</td>
<td>Cette sous-région est obligatoire et la <a href="#32-main-and-backup-extended-boot-sectors-sub-regions">Section 3,2</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>Paramètres OEM de sauvegarde</td>
<td>21</td>
<td>1</td>
<td>Cette sous-région est obligatoire et la <a href="#33-main-and-backup-oem-parameters-sub-regions">Section 3,3</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>Sauvegarde réservée</td>
<td>22</td>
<td>1</td>
<td>Cette sous-région est obligatoire et son contenu est réservé.</td>
</tr>
<tr class="even">
<td>Somme de contrôle de démarrage de sauvegarde</td>
<td>23</td>
<td>1</td>
<td>Cette sous-région est obligatoire et la <a href="#34-main-and-backup-boot-checksum-sub-regions">Section 3,4</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td><strong>Région FAT</strong></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>Alignement FAT</td>
<td>24</td>
<td>FatOffset – 24</td>
<td><p>Cette sous-région est obligatoire et son contenu, le cas échéant, n’est pas défini.</p>
<p>Remarque : les secteurs de démarrage principal et de sauvegarde contiennent tous les deux le champ FatOffset.</p></td>
</tr>
<tr class="odd">
<td>Premier FAT</td>
<td>FatOffset</td>
<td>FatLength</td>
<td><p>Cette sous-région est obligatoire et la <a href="#41-first-and-second-fat-sub-regions">Section 4,1</a> définit son contenu.</p>
<p>Remarque : les secteurs de démarrage principal et de sauvegarde contiennent tous les deux les champs FatOffset et FatLength.</p></td>
</tr>
<tr class="even">
<td>Deuxième FAT</td>
<td>FatOffset + FatLength</td>
<td>FatLength * (NumberOfFats – 1)</td>
<td><p>Cette sous-région est obligatoire et la <a href="#41-first-and-second-fat-sub-regions">Section 4,1</a> définit son contenu, le cas échéant.</p>
<p>Remarque : les secteurs de démarrage principal et de sauvegarde contiennent tous les deux les champs FatOffset, FatLength et NumberOfFats. Le champ NumberOfFats peut contenir uniquement les valeurs 1 et 2.</p></td>
</tr>
<tr class="odd">
<td><strong>Région de données</strong></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>Alignement du tas du cluster</td>
<td>FatOffset + FatLength * NumberOfFats</td>
<td>ClusterHeapOffset – (FatOffset + FatLength * NumberOfFats)</td>
<td><p>Cette sous-région est obligatoire et son contenu, le cas échéant, n’est pas défini.</p>
<p>Remarque : les secteurs de démarrage principal et de sauvegarde contiennent tous les deux les champs FatOffset, FatLength, NumberOfFats et ClusterHeapOffset. Les valeurs valides du champ NumberOfFats sont 1 et 2.</p></td>
</tr>
<tr class="odd">
<td>Segment de mémoire de cluster</td>
<td>ClusterHeapOffset</td>
<td>Clustercount, * 2<sup>SectorsPerClusterShift</sup></td>
<td><p>Cette sous-région est obligatoire et la <a href="#51-cluster-heap-sub-region">Section 5,1</a> définit son contenu.</p>
<p>Remarque : les secteurs de démarrage principal et de sauvegarde contiennent tous les deux les champs ClusterHeapOffset, Clustercount, et SectorsPerClusterShift.</p></td>
</tr>
<tr class="even">
<td>Espace excédentaire</td>
<td>ClusterHeapOffset + Clustercount, * 2<sup>SectorsPerClusterShift</sup></td>
<td>VolumeLength – (ClusterHeapOffset + Clustercount, * 2<sup>SectorsPerClusterShift</sup>)</td>
<td><p>Cette sous-région est obligatoire et son contenu, le cas échéant, n’est pas défini.</p>
<p>Remarque : les secteurs de démarrage principal et de sauvegarde contiennent tous les deux les champs ClusterHeapOffset, Clustercount,, SectorsPerClusterShift et VolumeLength.</p></td>
</tr>
</tbody>
</table>

## <a name="3-main-and-backup-boot-regions"></a>3 régions de démarrage principales et de sauvegarde

La région de démarrage principale fournit toutes les instructions d’amorçage nécessaires, les informations d’identification et les paramètres du système de fichiers pour permettre à une implémentation d’effectuer les opérations suivantes :

1. Amorcer le système d’un ordinateur à partir d’un volume exFAT.

2. Identifiez le système de fichiers sur le volume en tant que exFAT.

3. Découvrez l’emplacement des structures de système de fichiers exFAT.

La région de démarrage de la sauvegarde est une sauvegarde de la région de démarrage principale. Il aide à la récupération du volume exFAT en cas de région de démarrage principale dans un état incohérent. Sauf dans des circonstances peu fréquentes, telles que la mise à jour des instructions de démarrage, les implémentations ne doivent pas modifier le contenu de la région de démarrage de sauvegarde.

### <a name="31-main-and-backup-boot-sector-sub-regions"></a>Sous-régions du secteur de démarrage principal et de sauvegarde 3,1

Le secteur de démarrage principal contient du code pour Boot-cerclage à partir d’un volume exFAT et des paramètres exFAT fondamentaux qui décrivent la structure du volume (voir [tableau 4](#table-4-main-and-backup-boot-sector-structure)). Le BIOS, les MBR, ou d’autres agents de transfert de démarrage peuvent inspecter ce secteur et peuvent charger et exécuter toutes les instructions de démarrage qui y sont contenues.

Le secteur de démarrage de sauvegarde est une sauvegarde du secteur de démarrage principal et a la même structure (voir le [tableau 4](#table-4-main-and-backup-boot-sector-structure)). Le secteur de démarrage de sauvegarde peut aider les opérations de récupération ; Toutefois, les implémentations traitent le contenu des champs VolumeFlags et PercentInUse comme obsolètes.

Avant d’utiliser le contenu du secteur de démarrage principal ou de sauvegarde, les implémentations doivent vérifier leur contenu en validant leur somme de contrôle de démarrage respective et en veillant à ce que tous leurs champs soient dans leur plage de valeurs valide.

Tandis que l’opération de format initial Initialise le contenu des secteurs de démarrage principal et secondaire, les implémentations peuvent mettre à jour ces secteurs (et mettre à jour leur somme de contrôle de démarrage respective) si nécessaire. Toutefois, les implémentations peuvent mettre à jour les champs VolumeFlags ou PercentInUse sans mettre à jour leur somme de contrôle de démarrage respective (la somme de contrôle exclut spécifiquement ces deux champs).

<div id="table-4-main-and-backup-boot-sector-structure" />

**Tableau 4 structure du secteur de démarrage principal et de sauvegarde**

<table>
<thead>
<tr class="header">
<th><strong>Nom du champ</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>poids</strong></p></th>
<th><p><strong>Taille</strong></p>
<p><strong>bits</strong></p></th>
<th><strong>Commentaires</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>JumpBoot</td>
<td>0</td>
<td>3</td>
<td>Ce champ est obligatoire et la <a href="#311-jumpboot-field">section 3.1.1</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>FileSystemName</td>
<td>3</td>
<td>8</td>
<td>Ce champ est obligatoire et la <a href="#312-filesystemname-field">section 3.1.2</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>MustBeZero</td>
<td>11</td>
<td>53</td>
<td>Ce champ est obligatoire et la <a href="#313-mustbezero-field">section 3.1.3</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>PartitionOffset</td>
<td>64</td>
<td>8</td>
<td>Ce champ est obligatoire et la <a href="#314-partitionoffset-field">section 3.1.4</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>VolumeLength</td>
<td>72</td>
<td>8</td>
<td>Ce champ est obligatoire et la <a href="#315-volumelength-field">section 3.1.5</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>FatOffset</td>
<td>80</td>
<td>4</td>
<td>Ce champ est obligatoire et la <a href="#316-fatoffset-field">section 3.1.6</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>FatLength</td>
<td>84</td>
<td>4</td>
<td>Ce champ est obligatoire et la <a href="#317-fatlength-field">section 3.1.7</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>ClusterHeapOffset</td>
<td>88</td>
<td>4</td>
<td>Ce champ est obligatoire et la <a href="#318-clusterheapoffset-field">section 3.1.8</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>Clustercount,</td>
<td>92</td>
<td>4</td>
<td>Ce champ est obligatoire et la <a href="#319-clustercount-field">section 3.1.9</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>FirstClusterOfRootDirectory</td>
<td>96</td>
<td>4</td>
<td>Ce champ est obligatoire et la <a href="#3110-firstclusterofrootdirectory-field">section 3.1.10</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>VolumeSerialNumber</td>
<td>100</td>
<td>4</td>
<td>Ce champ est obligatoire et la <a href="#3111-volumeserialnumber-field">section 3.1.11</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>FileSystemRevision</td>
<td>104</td>
<td>2</td>
<td>Ce champ est obligatoire et la <a href="#3112-filesystemrevision-field">section 3.1.12</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>VolumeFlags</td>
<td>106</td>
<td>2</td>
<td>Ce champ est obligatoire et la <a href="#3113-volumeflags-field">section 3.1.13</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>BytesPerSectorShift</td>
<td>108</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#3114-bytespersectorshift-field">section 3.1.14</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>SectorsPerClusterShift</td>
<td>109</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#3115-sectorsperclustershift-field">section 3.1.15</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>NumberOfFats</td>
<td>110</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#3116-numberoffats-field">section 3.1.16</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>DriveSelect</td>
<td>111</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#3117-driveselect-field">section 3.1.17</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>PercentInUse</td>
<td>112</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#3118-percentinuse-field">section 3.1.18</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>Réservé</td>
<td>113</td>
<td>7</td>
<td>Ce champ est obligatoire et son contenu est réservé.</td>
</tr>
<tr class="even">
<td>Écrire</td>
<td>120</td>
<td>390</td>
<td>Ce champ est obligatoire et la <a href="#3119-bootcode-field">section 3.1.19</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>BootSignature</td>
<td>510</td>
<td>2</td>
<td>Ce champ est obligatoire et la <a href="#3120-bootsignature-field">section 3.1.20</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>ExcessSpace</td>
<td>512</td>
<td>2<sup>BytesPerSectorShift</sup> – 512</td>
<td><p>Ce champ est obligatoire et son contenu, le cas échéant, n’est pas défini.</p>
<p>Remarque : les secteurs de démarrage principal et de sauvegarde contiennent tous les deux le champ BytesPerSectorShift.</p></td>
</tr>
</tbody>
</table>

#### <a name="311-jumpboot-field"></a>3.1.1 champ JumpBoot

Le champ JumpBoot contient l’instruction de saut pour les UC communes aux ordinateurs personnels, qui, lorsqu’il est exécuté, « déplace » le processeur pour exécuter les instructions de démarrage dans le champ de démarrage.

La valeur valide pour ce champ est (par ordre de poids faible pour octet de poids fort) EBh 76h 90h.

#### <a name="312-filesystemname-field"></a>3.1.2 champ FileSystemName

Le champ FileSystemName doit contenir le nom du système de fichiers sur le volume.

La valeur valide pour ce champ est, en caractères ASCII, « EXFAT », qui comprend trois espaces blancs de fin.

#### <a name="313-mustbezero-field"></a>3.1.3 champ MustBeZero

Le champ MustBeZero correspond directement à la plage d’octets que le bloc de paramètres du BIOS compressé consomme sur les volumes FAT12/16/32.

La valeur valide pour ce champ est 0, ce qui permet d’empêcher les implémentations de FAT12/16/32 de monter par erreur un volume exFAT.

#### <a name="314-partitionoffset-field"></a>Champ PartitionOffset 3.1.4

Le champ PartitionOffset doit décrire le décalage de secteur relatif au support de la partition qui héberge le volume exFAT donné. Ce champ contribue au démarrage-cerclage à partir du volume à l’aide de l’extension INT 13h sur les ordinateurs personnels.

Toutes les valeurs possibles pour ce champ sont valides ; Toutefois, la valeur 0 indique que les implémentations doivent ignorer ce champ.

#### <a name="315-volumelength-field"></a>Champ VolumeLength 3.1.5

Le champ VolumeLength doit décrire la taille du volume exFAT donné dans secteurs.

La plage de valeurs valide pour ce champ doit être :

- Au moins 2<sup>20</sup>/2<sup>BytesPerSectorShift</sup>, ce qui garantit que le plus petit volume ne doit pas être inférieur à 1 Mo

- Au plus 2<sup>64</sup>-1, la plus grande valeur que ce champ peut décrire

Toutefois, si la taille de la sous-région d’espace excédentaire est 0, la valeur de ce champ est ClusterHeapOffset + (2<sup>32</sup>-11) \* 2<sup>SectorsPerClusterShift</sup>.

#### <a name="316-fatoffset-field"></a>Champ 3.1.6 FatOffset

Le champ FatOffset décrit le décalage de secteur relatif au volume du premier système FAT. Ce champ permet aux implémentations d’aligner le premier système FAT sur les caractéristiques du support de stockage sous-jacent.

La plage de valeurs valide pour ce champ doit être :

- Au moins 24, qui tient compte des secteurs utilisés par les régions de démarrage principales et de sauvegarde

- Au plus ClusterHeapOffset-(FatLength \* NumberOfFats), qui tient compte des secteurs consommés par le tas du cluster

#### <a name="317-fatlength-field"></a>Champ 3.1.7 FatLength

Le champ FatLength doit décrire la longueur, en secteurs, de chaque table FAT (le volume peut contenir jusqu’à deux graisses).

La plage de valeurs valide pour ce champ doit être :

- Au moins (Clustercount, + 2) \* 2<sup>2</sup>/2<sup>BytesPerSectorShift</sup>arrondi à l’entier le plus proche, ce qui garantit que chaque Fat a suffisamment d’espace pour décrire tous les clusters dans le segment de mémoire du cluster

- Au plus (ClusterHeapOffset-FatOffset)/NumberOfFats arrondi à l’entier le plus proche, ce qui garantit que les graisses existent avant le tas de cluster

Ce champ peut contenir une valeur dépassant sa limite inférieure (comme décrit ci-dessus) pour activer la deuxième FAT, le cas échéant, pour qu’elle soit également alignée sur les caractéristiques du support de stockage sous-jacent. Le contenu de l’espace qui dépasse ce que le FAT lui-même requiert, le cas échéant, n’est pas défini.

#### <a name="318-clusterheapoffset-field"></a>Champ 3.1.8 ClusterHeapOffset

Le champ ClusterHeapOffset doit décrire le décalage de secteur relatif au volume du segment de mémoire du cluster. Ce champ permet aux implémentations d’aligner le tas de cluster sur les caractéristiques du support de stockage sous-jacent.

La plage de valeurs valide pour ce champ doit être :

- Au moins FatOffset + FatLength \* NumberOfFats, pour prendre en compte les secteurs que toutes les régions précédentes utilisent

- Au maximum 2<sup>32</sup>-1 ou VolumeLength-(Clustercount, \* 2<sup>SectorsPerClusterShift</sup>), quel que soit le calcul le moins élevé

#### <a name="319-clustercount-field"></a>Champ 3.1.9 Clustercount,

Le champ Clustercount, doit décrire le nombre de clusters que contient le tas du cluster.

La valeur valide pour ce champ sera la plus petite des valeurs suivantes :

- (VolumeLength-ClusterHeapOffset)/2<sup>SectorsPerClusterShift</sup>arrondi à l’entier le plus proche, qui correspond exactement au nombre de clusters qui peut être compris entre le début du segment de mémoire du cluster et la fin du volume

- 2<sup>32</sup>-11, qui est le nombre maximal de clusters qu’un FAT peut décrire

La valeur du champ Clustercount, détermine la taille minimale d’un volume FAT. Pour éviter les matières grasses extrêmement volumineuses, les implémentations peuvent contrôler le nombre de clusters dans le segment de mémoire du cluster en accroissant la taille du cluster (via le champ SectorsPerClusterShift). Cette spécification ne recommande pas plus de deux clusters de<sup>24</sup>-2 dans le segment de mémoire du cluster. Toutefois, les implémentations doivent être en mesure de gérer des volumes comportant jusqu’à 2<sup>32</sup>à 11 clusters dans le segment de mémoire du cluster.

#### <a name="3110-firstclusterofrootdirectory-field"></a>Champ 3.1.10 FirstClusterOfRootDirectory

Le champ FirstClusterOfRootDirectory doit contenir l’index de cluster du premier cluster du répertoire racine. Les implémentations doivent faire chaque effort pour placer le premier cluster du répertoire racine dans le premier cluster non défectueux après que les clusters utilisent la bitmap d’allocation et la table de cas.

La plage de valeurs valide pour ce champ doit être :

- Au moins 2, l’index du premier cluster dans le segment de mémoire du cluster

- Au plus Clustercount, + 1, index du dernier cluster dans le segment de mémoire du cluster

#### <a name="3111-volumeserialnumber-field"></a>Champ 3.1.11 VolumeSerialNumber

Le champ VolumeSerialNumber doit contenir un numéro de série unique. Cela aide les implémentations à faire la distinction entre les différents volumes exFAT.
Les implémentations doivent générer le numéro de série en combinant la date et l’heure de mise en forme du volume exFAT. Le mécanisme permettant de combiner la date et l’heure pour former un numéro de série est spécifique à l’implémentation.

Toutes les valeurs possibles pour ce champ sont valides.

#### <a name="3112-filesystemrevision-field"></a>Champ 3.1.12 FileSystemRevision

Le champ FileSystemRevision décrit les numéros de révision majeurs et mineurs des structures exFAT sur le volume donné.

L’octet de poids fort est le numéro de révision majeur et l’octet de poids faible est le numéro de révision mineur. Par exemple, si l’octet de poids fort contient la valeur 01H et si l’octet de poids faible contient la valeur 05h, le champ FileSystemRevision décrit le numéro de révision 1,05.
De même, si l’octet de poids fort contient la valeur 0Ah et si l’octet de poids faible contient la valeur 0Fh, le champ FileSystemRevision décrit le numéro de révision 10,15.

La plage de valeurs valide pour ce champ doit être :

- Au moins 0 pour l’octet de poids faible et 1 pour l’octet de poids fort

- Au plus 99 pour l’octet de poids faible et 99 pour l’octet de poids fort

Le numéro de révision de exFAT que cette spécification décrit est 1,00.
Les implémentations de cette spécification doivent monter tout volume exFAT avec le numéro de révision majeur 1 et ne pas monter de volumes exFAT avec un autre numéro de révision majeur. Les implémentations doivent honorer le numéro de révision mineur et ne pas effectuer d’opérations ou créer toute structure de système de fichiers non décrite dans la spécification correspondante du numéro de révision mineure donné.

#### <a name="3113-volumeflags-field"></a>Champ 3.1.13 VolumeFlags

Le champ VolumeFlags doit contenir des indicateurs qui indiquent l’état de diverses structures de système de fichiers sur le volume exFAT (voir [tableau 5](#table-5-volumeflags-field-structure)).

Les implémentations ne doivent pas inclure ce champ lors du calcul de la somme de contrôle respective du démarrage ou de la région de démarrage de la sauvegarde. Lorsque vous faites référence au secteur de démarrage de sauvegarde, les implémentations traitent ce champ comme obsolète.

<div id="table-5-volumeflags-field-structure" />

**Tableau 5-structure de champs VolumeFlags**

<table>
<thead>
<tr class="header">
<th><strong>Nom du champ</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>64bits</strong></p></th>
<th><p><strong>Taille</strong></p>
<p><strong>bits</strong></p></th>
<th><strong>Commentaires</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ActiveFat</td>
<td>0</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#31131-activefat-field">section 3.1.13.1</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>VolumeDirty</td>
<td>1</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#31132-volumedirty-field">section 3.1.13.2</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>MediaFailure</td>
<td>2</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#31133-mediafailure-field">section 3.1.13.3</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>ClearToZero</td>
<td>3</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#31134-cleartozero-field">section 3.1.13.4</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>Réservé</td>
<td>4</td>
<td>12</td>
<td>Ce champ est obligatoire et son contenu est réservé.</td>
</tr>
</tbody>
</table>

##### <a name="31131-activefat-field"></a>Champ 3.1.13.1 ActiveFat

Le champ ActiveFat décrit les fichiers FAT et les bitmaps d’allocation actifs (et les implémentations doivent utiliser), comme suit :

- 0, ce qui signifie que les premières FAT et première bitmap d’allocation sont actives

- 1, ce qui signifie que la deuxième FAT et la deuxième bitmap d’allocation sont actives et ne sont possibles que si le champ NumberOfFats contient la valeur 2

Les implémentations considèrent la FAT inactive et la bitmap d’allocation comme obsolètes. Seules les implémentations compatibles TexFAT doivent basculer les bitmaps de la FAT et de l’allocation active (voir la [Section 7,1](#71-allocation-bitmap-directory-entry)).

##### <a name="31132-volumedirty-field"></a>Champ 3.1.13.2 VolumeDirty

Le champ VolumeDirty indique si le volume est impropre ou non, comme suit :

- 0, ce qui signifie que le volume est probablement dans un état cohérent

- 1, ce qui signifie que le volume est probablement dans un état incohérent

Les implémentations doivent définir la valeur de ce champ sur 1 en cas d’incohérence des métadonnées du système de fichiers qu’ils ne résolvent pas. Si, au moment du montage d’un volume, la valeur de ce champ est 1, seules les implémentations qui résolvent les incohérences de métadonnées du système de fichiers peuvent effacer la valeur de ce champ à 0. Ces implémentations n’effacent que la valeur de ce champ à 0 après avoir vérifié que le système de fichiers est dans un état cohérent.

Si, lors du montage d’un volume, la valeur de ce champ est 0, les implémentations doivent affecter la valeur 1 à ce champ avant de mettre à jour les métadonnées du système de fichiers et décocher ce champ sur 0, de la même façon que l’ordre d’écriture recommandé décrit dans la [Section 8,1](#81-recommended-write-ordering).

##### <a name="31133-mediafailure-field"></a>Champ 3.1.13.3 MediaFailure

Le champ MediaFailure indique si une implémentation a détecté des échecs de média ou non, comme suit :

- 0, ce qui signifie que le média d’hébergement n’a pas signalé d’échecs ou que des échecs connus sont déjà enregistrés dans le FAT en tant que clusters « incorrects »

- 1, ce qui signifie que le média d’hébergement a signalé des échecs (c’est-à-dire qu’il a échoué des opérations de lecture ou d’écriture)

Une implémentation doit affecter la valeur 1 à ce champ dans les cas suivants :

1. Les tentatives d’accès au support d’hébergement échouent dans une région du volume

2. L’implémentation a épuisé les algorithmes de nouvelle tentative d’accès, le cas échéant

Si, lors du montage d’un volume, la valeur de ce champ est 1, les implémentations qui analysent l’ensemble du volume des défaillances de support et enregistrent tous les échecs en tant que clusters « incorrects » dans le FAT (ou résolvent les défaillances de support), vous pouvez désactiver la valeur de ce champ à 0.

##### <a name="31134-cleartozero-field"></a>Champ 3.1.13.4 ClearToZero

Le champ ClearToZero n’a pas de sens significatif dans cette spécification.

Les valeurs valides pour ce champ sont les suivantes :

- 0, qui n’a pas de signification particulière

- 1, ce qui signifie que les implémentations doivent effacer ce champ à 0 avant de modifier des structures, des répertoires ou des fichiers de système de fichiers

#### <a name="3114-bytespersectorshift-field"></a>Champ 3.1.14 BytesPerSectorShift

Le champ BytesPerSectorShift décrira les octets par secteur exprimés comme log<sub>2</sub>(n), où N est le nombre d’octets par secteur. Par exemple, pour 512 octets par secteur, la valeur de ce champ est 9.

La plage de valeurs valide pour ce champ doit être :

- Au moins 9 (taille de secteur de 512 octets), qui est le plus petit secteur possible pour un volume exFAT

- Au maximum 12 (taille de secteur de 4096 octets), qui est la taille de page de la mémoire des UC communes aux ordinateurs personnels

#### <a name="3115-sectorsperclustershift-field"></a>Champ 3.1.15 SectorsPerClusterShift

Le champ SectorsPerClusterShift décrit les secteurs par cluster, exprimés sous la forme log<sub>2</sub>(n), où N est le nombre de secteurs par cluster. Par exemple, pour 8 secteurs par cluster, la valeur de ce champ est 3.

La plage de valeurs valide pour ce champ doit être :

- Au moins 0 (1 secteur par cluster), qui est le plus petit cluster possible

- Au maximum 25-BytesPerSectorShift, qui correspond à une taille de cluster de 32 Mo

#### <a name="3116-numberoffats-field"></a>Champ 3.1.16 NumberOfFats

Le champ NumberOfFats décrit le nombre de graisses et les bitmaps d’allocation que le volume contient.

La plage de valeurs valide pour ce champ doit être :

- 1, qui indique que le volume contient uniquement la première image FAT et la première bitmap d’allocation

- 2, qui indique que le volume contient la première FAT, la deuxième FAT, la première et la deuxième bitmap d’allocation ; Cette valeur est valide uniquement pour les volumes TexFAT

#### <a name="3117-driveselect-field"></a>Champ 3.1.17 DriveSelect

Le champ DriveSelect doit contenir le numéro de lecteur étendu INT 13h, qui aide à démarrer l’utilisation de ce volume à l’aide de l’extension INT 13h sur les ordinateurs personnels.

Toutes les valeurs possibles pour ce champ sont valides. Les champs similaires dans les systèmes de fichiers FAT précédents contiennent souvent la valeur 80h.

#### <a name="3118-percentinuse-field"></a>Champ 3.1.18 PercentInUse

Le champ PercentInUse décrit le pourcentage de clusters dans le tas de cluster qui sont alloués.

La plage de valeurs valide pour ce champ doit être :

- Entre 0 et 100 inclus, qui est le pourcentage de clusters alloués dans le tas de cluster, arrondi à l’entier le plus proche

- Exactement FFh, qui indique que le pourcentage de clusters alloués dans le tas de cluster n’est pas disponible

Les implémentations modifient la valeur de ce champ pour refléter les modifications apportées à l’allocation des clusters dans le segment de mémoire du cluster ou le remplacent par FFh.

Les implémentations ne doivent pas inclure ce champ lors du calcul de la somme de contrôle respective du démarrage ou de la région de démarrage de la sauvegarde. Lorsque vous faites référence au secteur de démarrage de sauvegarde, les implémentations traitent ce champ comme obsolète.

#### <a name="3119-bootcode-field"></a>Champ de démarrage 3.1.19

Le champ de démarrage doit contenir des instructions Boot-cerclage.
Les implémentations peuvent remplir ce champ avec les instructions d’UC nécessaires pour le démarrage d’un système informatique. Les implémentations qui ne fournissent pas d’instructions Boot-cerclage initialisent chaque octet de ce champ sur F4h (l’instruction Halt pour les UC communes aux ordinateurs personnels) dans le cadre de leur opération de formatage.

#### <a name="3120-bootsignature-field"></a>Champ 3.1.20 BootSignature

Le champ BootSignature indique si l’intention d’un secteur donné est qu’il s’agit d’un secteur d’amorçage ou non.

La valeur valide pour ce champ est AA55h. Toute autre valeur dans ce champ invalide son secteur d’amorçage respectif. Les implémentations doivent vérifier le contenu de ce champ avant de dépendre d’un autre champ dans son secteur d’amorçage respectif.

### <a name="32-main-and-backup-extended-boot-sectors-sub-regions"></a>3,2 principaux et sauvegardes-sous-régions des secteurs de démarrage étendu

Chaque secteur des principaux secteurs de démarrage étendus a la même structure ; Toutefois, chaque secteur peut contenir des instructions de démarrage distinctes (voir tableau 6). Les agents de démarrage, tels que les instructions Boot-cerclage dans le secteur de démarrage principal, les autres implémentations du BIOS ou le microprogramme d’un système incorporé, peuvent charger ces secteurs et exécuter les instructions qu’ils contiennent.

Les secteurs de démarrage étendus de sauvegarde sont une sauvegarde des principaux secteurs de démarrage étendus et ont la même structure (voir le [tableau 6](#table-6-extended-boot-sector-structure)).

Avant d’exécuter les instructions des secteurs de démarrage étendu ou de sauvegarde étendue, les implémentations doivent vérifier leur contenu en veillant à ce que le champ ExtendedBootSignature de chaque secteur contienne sa valeur prescrite.

Bien que l’opération de formatage initial Initialise le contenu des secteurs de démarrage étendu et de sauvegarde étendu, les implémentations peuvent mettre à jour ces secteurs (et mettre à jour leur somme de contrôle de démarrage respective) si nécessaire.

<div id="table-6-extended-boot-sector-structure" />

**Tableau 6 structure du secteur de démarrage étendu**

<table>
<thead>
<tr class="header">
<th><strong>Nom du champ</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>poids</strong></p></th>
<th><p><strong>Taille</strong></p>
<p><strong>bits</strong></p></th>
<th><strong>Commentaires</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ExtendedBootCode</td>
<td>0</td>
<td>2<sup>BytesPerSectorShift</sup> – 4</td>
<td><p>Ce champ est obligatoire et la <a href="#321-extendedbootcode-field">section 3.2.1</a> définit son contenu.</p>
<p>Remarque : les secteurs de démarrage principal et de sauvegarde contiennent tous les deux le champ BytesPerSectorShift.</p></td>
</tr>
<tr class="even">
<td>ExtendedBootSignature</td>
<td>2<sup>BytesPerSectorShift</sup> – 4</td>
<td>4</td>
<td><p>Ce champ est obligatoire et la <a href="#322-extendedbootsignature-field">section 3.2.2</a> définit son contenu.</p>
<p>Remarque : les secteurs de démarrage principal et de sauvegarde contiennent tous les deux le champ BytesPerSectorShift.</p></td>
</tr>
</tbody>
</table>

#### <a name="321-extendedbootcode-field"></a>3.2.1 champ ExtendedBootCode

Le champ ExtendedBootCode doit contenir des instructions Boot-cerclage.
Les implémentations peuvent remplir ce champ avec les instructions d’UC nécessaires pour le démarrage d’un système informatique. Les implémentations qui ne fournissent pas d’instructions Boot-cerclage doivent initialiser chaque octet de ce champ à 00h dans le cadre de leur opération de formatage.

#### <a name="322-extendedbootsignature-field"></a>Champ ExtendedBootSignature 3.2.2

Le champ ExtendedBootSignature indique si l’intention d’un secteur donné est qu’il s’agit d’un secteur d’amorçage étendu.

La valeur valide pour ce champ est AA550000h. Toute autre valeur dans ce champ invalide son secteur de démarrage principal ou de sauvegarde étendu respectif.
Les implémentations doivent vérifier le contenu de ce champ avant de dépendre d’un autre champ dans son secteur de démarrage étendu respectif.

### <a name="33-main-and-backup-oem-parameters-sub-regions"></a>3,3 principales et paramètres OEM de sauvegarde des sous-régions

La sous-région des paramètres OEM principale contient dix structures de paramètres qui peuvent contenir des informations spécifiques au fabricant (voir le [tableau 7](#table-7-oem-parameters-structure)). Chacune des dix structures de paramètres dérive du modèle de paramètres génériques (voir la [section 3.3.2](#332-generic-parameters-template)). Les fabricants peuvent dériver leurs propres structures de paramètres personnalisés à partir du modèle de paramètres génériques. Cette spécification définit deux structures de paramètres : les paramètres null (voir la [section 3.3.3](#333-null-parameters)) et les paramètres Flash (voir la [section 3.3.4](#334-flash-parameters)).

Les paramètres OEM de sauvegarde sont une sauvegarde des principaux paramètres OEM et ont la même structure (voir le [tableau 7](#table-7-oem-parameters-structure)).

Avant d’utiliser le contenu des paramètres OEM principal ou de sauvegarde, les implémentations vérifient leur contenu en validant leur somme de contrôle de démarrage respective.

Les fabricants doivent remplir les paramètres OEM principal et secondaire avec leurs propres structures de paramètres personnalisés, le cas échéant, et toute autre structure de paramètres. Les opérations de mise en forme suivantes préservent le contenu des paramètres OEM principal et de sauvegarde.

Les implémentations peuvent mettre à jour les paramètres OEM principal et secondaire en fonction des besoins (et doivent également mettre à jour leur somme de contrôle de démarrage respective).

<div id="table-7-oem-parameters-structure" />

**Tableau 7-structure des paramètres OEM**

<table>
<thead>
<tr class="header">
<th><strong>Nom du champ</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>poids</strong></p></th>
<th><p><strong>Taille</strong></p>
<p><strong>bits</strong></p></th>
<th><strong>Commentaires</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Paramètres [0]</td>
<td>0</td>
<td>48</td>
<td>Ce champ est obligatoire et la <a href="#331-parameters0--parameters9">section 3.3.1</a> définit son contenu.</td>
</tr>
<tr class="even">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="odd">
<td>Paramètres [9]</td>
<td>432</td>
<td>48</td>
<td>Ce champ est obligatoire et la <a href="#331-parameters0--parameters9">section 3.3.1</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>Réservé</td>
<td>480</td>
<td>2<sup>BytesPerSectorShift</sup> – 480</td>
<td><p>Ce champ est obligatoire et son contenu est réservé.</p>
<p>Remarque : les secteurs de démarrage principal et de sauvegarde contiennent tous les deux le champ BytesPerSectorShift.</p></td>
</tr>
</tbody>
</table>

#### <a name="331-parameters0--parameters9"></a>3.3.1 paramètres \[ 0 \] ... Paramètres \[ 9\]

Chaque champ de paramètres de ce tableau contient une structure de paramètres, qui dérive du modèle de paramètres génériques (voir la [section 3.3.2](#332-generic-parameters-template)).
Tout champ de paramètres inutilisés doit être décrit comme contenant une structure de paramètres null (voir la [section 3.3.3](#333-null-parameters)).

#### <a name="332-generic-parameters-template"></a>3.3.2 modèle de paramètres génériques

Le modèle de paramètres génériques fournit la définition de base d’une structure de paramètres (voir [tableau 8](#table-8-generic-parameters-template)). Toutes les structures de paramètres dérivent de ce modèle. La prise en charge de ce modèle de paramètres génériques est obligatoire.

<div id="table-8-generic-parameters-template" />

**Tableau 8 modèle de paramètres génériques**

<table>
<thead>
<tr class="header">
<th><strong>Nom du champ</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>poids</strong></p></th>
<th><p><strong>Taille</strong></p>
<p><strong>bits</strong></p></th>
<th><strong>Commentaires</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ParametersGuid</td>
<td>0</td>
<td>16</td>
<td>Ce champ est obligatoire et la <a href="#3321-parametersguid-field">section 3.3.2.1</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>CustomDefined</td>
<td>16</td>
<td>32</td>
<td>Ce champ est obligatoire et les structures qui dérivent de ce modèle définissent son contenu.</td>
</tr>
</tbody>
</table>

##### <a name="3321-parametersguid-field"></a>Champ 3.3.2.1 ParametersGuid

Le champ ParametersGuid doit décrire un GUID, qui détermine la disposition du reste de la structure de paramètres donnée.

Toutes les valeurs possibles pour ce champ sont valides ; Toutefois, les fabricants doivent utiliser un outil de génération de GUID, tel que GuidGen.exe, pour sélectionner un GUID lors de la dérivation de structures de paramètres personnalisés à partir de ce modèle.

#### <a name="333-null-parameters"></a>3.3.3 paramètres null

La structure de paramètres null dérive du modèle de paramètres génériques (voir la [section 3.3.2](#332-generic-parameters-template)) et décrit un champ de paramètres inutilisé (voir le [tableau 9](#table-9-null-parameters-structure)). Lors de la création ou de la mise à jour de la structure de paramètres OEM, les implémentations doivent remplir les champs de paramètres inutilisés avec la structure de paramètres null. De même, lors de la création ou de la mise à jour de la structure de paramètres OEM, les implémentations doivent consolider les structures de paramètres null à la fin du tableau, laissant ainsi toutes les autres structures de paramètres au début de la structure de paramètres OEM.

La prise en charge de la structure de paramètres null est obligatoire.

<div id="table-9-null-parameters-structure" />

**Structure des paramètres null du tableau 9**

<table>
<thead>
<tr class="header">
<th><strong>Nom du champ</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>poids</strong></p></th>
<th><p><strong>Taille</strong></p>
<p><strong>bits</strong></p></th>
<th><strong>Commentaires</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ParametersGuid</td>
<td>0</td>
<td>16</td>
<td>Ce champ est obligatoire et la <a href="#3331-parametersguid-field">section 3.3.3.1</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>Réservé</td>
<td>16</td>
<td>32</td>
<td>Ce champ est obligatoire et son contenu est réservé.</td>
</tr>
</tbody>
</table>

##### <a name="3331-parametersguid-field"></a>Champ 3.3.3.1 ParametersGuid

Le champ ParametersGuid doit être conforme à la définition fournie par le modèle de paramètres génériques (voir la [section 3.3.2.1](#3321-parametersguid-field)).

La valeur valide pour ce champ, en notation GUID, est {00000000-0000-0000-0000-000000000000} .

#### <a name="334-flash-parameters"></a>Paramètres Flash 3.3.4

La structure du paramètre Flash dérive du modèle de paramètres génériques (voir la [section 3.3.2](#332-generic-parameters-template)) et contient des paramètres pour le média Flash (voir le [tableau 10](#table-10-flash-parameters-structure)). Les fabricants de périphériques de stockage basés sur Flash peuvent remplir un champ de paramètres (de préférence le champ des paramètres \[ 0 \] ) avec cette structure de paramètres. Les implémentations peuvent utiliser les informations contenues dans la structure des paramètres Flash pour optimiser les opérations d’accès pendant les opérations de lecture/écriture et pour l’alignement des structures du système de fichiers Durning la mise en forme du média.

La prise en charge de la structure des paramètres flash est facultative.

<div id="table-10-flash-parameters-structure" />

**Tableau 10-structure des paramètres Flash**

<table>
<thead>
<tr class="header">
<th><strong>Nom du champ</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>poids</strong></p></th>
<th><p><strong>Taille</strong></p>
<p><strong>bits</strong></p></th>
<th><strong>Commentaires</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ParametersGuid</td>
<td>0</td>
<td>16</td>
<td>Ce champ est obligatoire et la <a href="#3341-parametersguid-field">section 3.3.4.1</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>EraseBlockSize</td>
<td>16</td>
<td>4</td>
<td>Ce champ est obligatoire et la <a href="#3342-eraseblocksize-field">section 3.3.4.2</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>PageSize</td>
<td>20</td>
<td>4</td>
<td>Ce champ est obligatoire et la <a href="#3343-pagesize-field">section 3.3.4.3</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>SpareSectors</td>
<td>24</td>
<td>4</td>
<td>Ce champ est obligatoire et la <a href="#3344-sparesectors-field">section 3.3.4.4</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>RandomAccessTime</td>
<td>28</td>
<td>4</td>
<td>Ce champ est obligatoire et la <a href="#3345-randomaccesstime-field">section 3.3.4.5</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>ProgrammingTime</td>
<td>32</td>
<td>4</td>
<td>Ce champ est obligatoire et la <a href="#3346-programmingtime-field">section 3.3.4.6</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>ReadCycle</td>
<td>36</td>
<td>4</td>
<td>Ce champ est obligatoire et la <a href="#3347-readcycle-field">section 3.3.4.7</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>WriteCycle</td>
<td>40</td>
<td>4</td>
<td>Ce champ est obligatoire et la <a href="#3348-writecycle-field">section 3.3.4.8</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>Réservé</td>
<td>44</td>
<td>4</td>
<td>Ce champ est obligatoire et son contenu est réservé.</td>
</tr>
</tbody>
</table>

Toutes les valeurs possibles pour tous les champs de paramètres Flash, à l’exception du champ ParametersGuid, sont valides. Toutefois, la valeur 0 indique que le champ est en fait inutile (les implémentations doivent ignorer le champ donné).

##### <a name="3341-parametersguid-field"></a>Champ 3.3.4.1 ParametersGuid

Le champ ParametersGuid doit être conforme à la définition fournie dans le modèle de paramètres génériques (voir la [section 3.3.2.1](#3321-parametersguid-field)).

La valeur valide pour ce champ, en notation GUID, est {0A0C7E46-3399-4021-90C8-FA6D389C4BA2}.

##### <a name="3342-eraseblocksize-field"></a>Champ 3.3.4.2 EraseBlockSize

Le champ EraseBlockSize doit décrire la taille, en octets, du bloc d’effacement du média Flash.

##### <a name="3343-pagesize-field"></a>Champ PageSize 3.3.4.3

Le champ PageSize doit décrire la taille, en octets, de la page du média Flash.

##### <a name="3344-sparesectors-field"></a>Champ 3.3.4.4 SpareSectors

Le champ SpareSectors décrira le nombre de secteurs disponibles pour les opérations de remplacement internes du support Flash.

##### <a name="3345-randomaccesstime-field"></a>Champ 3.3.4.5 RandomAccessTime

Le champ RandomAccessTime doit décrire le temps d’accès aléatoire moyen du média Flash, en nanosecondes.

##### <a name="3346-programmingtime-field"></a>Champ 3.3.4.6 ProgrammingTime

Le champ ProgrammingTime doit décrire le temps moyen de programmation du média Flash, en nanosecondes.

##### <a name="3347-readcycle-field"></a>Champ 3.3.4.7 ReadCycle

Le champ ReadCycle doit décrire la durée moyenne de cycle de lecture du média Flash, en nanosecondes.

##### <a name="3348-writecycle-field"></a>Champ 3.3.4.8 WriteCycle

Le champ WriteCycle décrit la durée moyenne de cycle d’écriture, en nanosecondes.

### <a name="34-main-and-backup-boot-checksum-sub-regions"></a>3,4 principales et les sous-régions de somme de contrôle de démarrage de sauvegarde

Les sommes de contrôle de démarrage principales et de sauvegarde contiennent chacune un modèle répétitif de la somme de contrôle de quatre octets du contenu de toutes les autres sous-régions dans leurs régions de démarrage respectives. Le calcul de la somme de contrôle ne doit pas inclure les champs VolumeFlags et PercentInUse dans leur secteur de démarrage respectif (voir la [figure 1](#figure-1-boot-checksum-computation)). Le modèle répétitif de la somme de contrôle de 4 octets remplit sa sous-région de somme de contrôle de démarrage respective à partir du début jusqu’à la fin de la sous-région.

Avant d’utiliser le contenu de l’une des autres sous-régions dans les régions de démarrage principales ou de sauvegarde, les implémentations vérifient leur contenu en validant leur somme de contrôle de démarrage respective.

Tandis que l’opération de formatage initiale remplit à la fois les sommes de contrôle de démarrage principales et de sauvegarde avec le modèle de somme de contrôle répétée, les implémentations mettent à jour ces secteurs au fur et à mesure que le contenu des autres secteurs dans leurs régions de démarrage respectives change.

<div id="figure-1-boot-checksum-computation" />

**Figure 1 calcul de la somme de contrôle de démarrage**

```c
UInt32 BootChecksum
(
    UCHAR  * Sectors,        // points to an in-memory copy of the 11 sectors
    USHORT   BytesPerSector
)
{
    UInt32 NumberOfBytes = (UInt32)BytesPerSector * 11;
    UInt32 Checksum = 0;
    UInt32 Index;

    for (Index = 0; Index < NumberOfBytes; Index++)
    {
        if ((Index == 106) || (Index == 107) || (Index == 112))
        {
            continue;
        }
        Checksum = ((Checksum&1) ? 0x80000000 : 0) + (Checksum>>1) + (UInt32)Sectors[Index];
    }

    return Checksum;
}
```

## <a name="4-file-allocation-table-region"></a>4 région de table d’allocation de fichiers

La région de table d’allocation de fichiers (FAT) peut contenir jusqu’à deux graisses, une dans la première sous-région FAT et une autre dans la deuxième sous-région FAT.
Le champ NumberOfFats décrit le nombre de graisses que cette région contient. Les valeurs valides pour le champ NumberOfFats sont 1 et 2. Par conséquent, la première sous-région FAT contient toujours un volume FAT. Si le champ NumberOfFats est défini sur deux, la deuxième sous-région FAT contient également un volume FAT.

Le champ ActiveFat du champ VolumeFlags décrit le FAT qui est actif. Seul le champ VolumeFlags du secteur de démarrage principal est actif.
Les implémentations traitent le FAT qui n’est pas actif comme obsolète. L’utilisation de la FAT inactive et le basculement entre les graisses sont spécifiques à l’implémentation.

### <a name="41-first-and-second-fat-sub-regions"></a>4,1 première et deuxième sous-régions FAT

Un système de fichiers FAT doit décrire les chaînes de cluster dans le segment de mémoire du cluster (voir le [tableau 11](#table-11-file-allocation-table-structure)).
Une chaîne de cluster est une série de clusters qui fournit de l’espace pour l’enregistrement du contenu de fichiers, de répertoires et d’autres structures de système de fichiers. Un système FAT représente une chaîne de clusters en tant que liste d’index de clusters à liaison unique. À l’exception des deux premières entrées, chaque entrée d’un FAT représente exactement un cluster.

<div id="table-11-file-allocation-table-structure" />

**Tableau 11-structure de table d’allocation de fichiers**

<table>
<thead>
<tr class="header">
<th><strong>Nom du champ</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>poids</strong></p></th>
<th><p><strong>Taille</strong></p>
<p><strong>bits</strong></p></th>
<th><strong>Commentaires</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FatEntry [0]</td>
<td>0</td>
<td>4</td>
<td>Ce champ est obligatoire et la <a href="#412-fatentry1-field">section 4.1.2</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>FatEntry [1]</td>
<td>4</td>
<td>4</td>
<td>Ce champ est obligatoire et la <a href="#412-fatentry1-field">section 4.1.2</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>FatEntry [2]</td>
<td>8</td>
<td>4</td>
<td>Ce champ est obligatoire et la <a href="#413-fatentry2--fatentryclustercount1-fields">section 4.1.3</a> définit son contenu.</td>
</tr>
<tr class="even">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="odd">
<td>FatEntry [Clustercount, + 1]</td>
<td>(Clustercount, + 1) * 4</td>
<td>4</td>
<td><p>Ce champ est obligatoire et la <a href="#413-fatentry2--fatentryclustercount1-fields">section 4.1.3</a> définit son contenu.</p>
<p>Clustercount, + 1 ne peut jamais dépasser FFFFFFF6h.</p>
<p>Remarque : les secteurs de démarrage principal et de sauvegarde contiennent tous les deux le champ Clustercount,.</p></td>
</tr>
<tr class="even">
<td>ExcessSpace</td>
<td>(Clustercount, + 2) * 4</td>
<td>(FatLength * 2<sup>BytesPerSectorShift</sup>) – ((clustercount, + 2) * 4)</td>
<td><p>Ce champ est obligatoire et son contenu, le cas échéant, n’est pas défini.</p>
<p>Remarque : les secteurs de démarrage principal et de sauvegarde contiennent tous les deux les champs Clustercount,, FatLength et BytesPerSectorShift.</p></td>
</tr>
</tbody>
</table>

#### <a name="411-fatentry0-field"></a>4.1.1 \[ champ FatEntry 0 \]

Le \[ champ FatEntry 0 \] doit décrire le type de support dans le premier octet (l’octet d’ordre le plus bas) et doit contenir FFH dans les trois octets restants.

Le type de média (le premier octet) doit être F8h.

#### <a name="412-fatentry1-field"></a>4.1.2 FatEntry \[ 1 \] champ

Le \[ champ FatEntry 1 \] n’existe qu’en raison de la priorité historique et ne décrit rien d’intérêt.

La valeur valide pour ce champ est FFFFFFFFh. Les implémentations doivent initialiser ce champ à sa valeur prescrite et ne doivent pas utiliser ce champ à quelque fin que ce soit. Les implémentations ne doivent pas interpréter ce champ et doivent conserver son contenu entre les opérations qui modifient les champs environnants.

#### <a name="413-fatentry2--fatentryclustercount1-fields"></a>4.1.3 FatEntry \[ 2 \] ... \[Champs FatEntry clustercount, + 1 \]

Chaque champ FatEntry de ce tableau doit représenter un cluster dans le segment de mémoire du cluster. FatEntry \[ 2 \] représente le premier cluster dans le segment de mémoire de cluster et FatEntry \[ clustercount, + 1 \] représente le dernier cluster dans le segment de mémoire du cluster.

La plage valide de valeurs pour ces champs doit être :

- Entre 2 et Clustercount, + 1, inclus, qui pointe vers le FatEntry suivant dans la chaîne de clusters donnée ; le FatEntry donné ne doit pas pointer vers un FatEntry qui le précède dans la chaîne de clusters donnée

- Exactement FFFFFFF7h, qui marque le cluster correspondant du FatEntry donné comme étant « incorrect »

- Exactement FFFFFFFFh, qui marque le cluster correspondant du FatEntry donné comme dernier cluster d’une chaîne de cluster ; Il s’agit de la seule valeur valide pour le dernier FatEntry d’une chaîne de clusters donnée

## <a name="5-data-region"></a>5 région de données

La région de données contient le tas de cluster, qui fournit l’espace managé pour les structures, les répertoires et les fichiers du système de fichiers.

### <a name="51-cluster-heap-sub-region"></a>Sous-région du tas de cluster 5,1

La structure du tas du cluster est très simple (voir le [tableau 12](#table-12-cluster-heap-structure)); chaque série de secteurs consécutives décrit un cluster, puisque le champ SectorsPerClusterShift définit. Important encore, le premier cluster du segment de mémoire de cluster possède l’index deux, qui correspond directement à l’index de FatEntry \[ 2 \] .

Dans un volume exFAT, une image bitmap d’allocation (voir la [section 7.1.5](#715-allocation-bitmap)) conserve l’enregistrement de l’état d’allocation de tous les clusters. Il s’agit d’une différence importante par rapport aux prédécesseurs de exFAT (FAT12, FAT16 et FAT32), dans lesquels un volume FAT a conservé un enregistrement de l’état d’allocation de tous les clusters dans le segment de mémoire du cluster.

<div id="table-12-cluster-heap-structure" />

**Tableau 12 structure du tas de cluster**

<table>
<thead>
<tr class="header">
<th><strong>Nom du champ</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>secteur</strong></p></th>
<th><p><strong>Taille</strong></p>
<p><strong>Sector</strong></p></th>
<th><strong>Commentaires</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Cluster [2]</td>
<td>ClusterHeapOffset</td>
<td>2<sup>SectorsPerClusterShift</sup></td>
<td><p>Ce champ est obligatoire et la <a href="#511-cluster2--clusterclustercount1-fields">section 5.1.1</a> définit son contenu.</p>
<p>Remarque : les secteurs de démarrage principal et de sauvegarde contiennent tous les deux les champs ClusterHeapOffset et SectorsPerClusterShift.</p></td>
</tr>
<tr class="even">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="odd">
<td>Cluster [Clustercount, + 1]</td>
<td>ClusterHeapOffset + (Clustercount, – 1) * 2<sup>SectorsPerClusterShift</sup></td>
<td>2<sup>SectorsPerClusterShift</sup></td>
<td><p>Ce champ est obligatoire et la <a href="#511-cluster2--clusterclustercount1-fields">section 5.1.1</a> définit son contenu.</p>
<p>Remarque : les secteurs de démarrage principal et de sauvegarde contiennent tous les deux les champs Clustercount,, ClusterHeapOffset et SectorsPerClusterShift.</p></td>
</tr>
</tbody>
</table>

#### <a name="511-cluster2--clusterclustercount1-fields"></a>5.1.1 cluster \[ 2 \] ... \[Champs clustercount, + 1 du cluster \]

Chaque champ de cluster de ce tableau est une série de secteurs contigus, dont la taille est définie par le champ SectorsPerClusterShift.

## <a name="6-directory-structure"></a>6 structure de répertoires

Le système de fichiers exFAT utilise une approche d’arborescence de répertoires pour gérer les structures et fichiers du système de fichiers qui existent dans le segment de mémoire du cluster. Les répertoires ont une relation un-à-plusieurs entre le parent et l’enfant dans l’arborescence de répertoires.

Le répertoire auquel le champ FirstClusterOfRootDirectory fait référence est la racine de l’arborescence de répertoires. Tous les autres répertoires sont décroissants du répertoire racine dans un mode de liaison unique.

Chaque répertoire se compose d’une série d’entrées de répertoire (voir le [tableau 13](#table-13-directory-structure)).

Une ou plusieurs entrées de répertoire sont combinées dans un jeu d’entrées de répertoire qui décrit un élément intéressant, tel qu’une structure de système de fichiers, un sous-répertoire ou un fichier.

<div id="table-13-directory-structure" />

**Tableau 13-structure de répertoires**

<table>
<thead>
<tr class="header">
<th><strong>Nom du champ</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>poids</strong></p></th>
<th><p><strong>Taille</strong></p>
<p><strong>poids</strong></p></th>
<th><strong>Commentaires</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DirectoryEntry [0]</td>
<td>0</td>
<td>32</td>
<td>Ce champ est obligatoire et la <a href="#61-directoryentry0--directoryentryn--1">Section 6,1</a> définit son contenu.</td>
</tr>
<tr class="even">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="odd">
<td>DirectoryEntry [N-1]</td>
<td>(N – 1) * 32</td>
<td>32</td>
<td><p>Ce champ est obligatoire et la <a href="#61-directoryentry0--directoryentryn--1">Section 6,1</a> définit son contenu.</p>
<p>N, le nombre de champs DirectoryEntry est la taille, en octets, de la chaîne de cluster qui contient le répertoire donné, divisée par la taille d’un champ DirectoryEntry, 32 octets.</p></td>
</tr>
</tbody>
</table>

### <a name="61-directoryentry0--directoryentryn--1"></a>6,1 DirectoryEntry \[ 0 \] ... DirectoryEntry \[ N--1\]

Chaque champ DirectoryEntry de ce tableau est dérivé du modèle DirectoryEntry générique (voir la [Section 6,2](#62-generic-directoryentry-template)).

### <a name="62-generic-directoryentry-template"></a>Modèle DirectoryEntry générique 6,2

Le modèle DirectoryEntry générique fournit la définition de base pour les entrées de répertoire (voir le [tableau 14](#table-14-generic-directoryentry-template)). Toutes les structures d’entrée de répertoire dérivent de ce modèle et seules les structures d’entrée de répertoire définies par Microsoft sont valides (exFAT n’a pas de dispositions pour les structures d’entrée de répertoire définies par le fabricant, sauf comme défini dans la [section 7,8](#78-vendor-extension-directory-entry) et la [section 7,9](#79-vendor-allocation-directory-entry)). La possibilité d’interpréter le modèle DirectoryEntry générique est obligatoire.

<div id="table-14-generic-directoryentry-template" />

**Tableau 14 modèle DirectoryEntry générique**

<table>
<thead>
<tr class="header">
<th><strong>Nom du champ</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>poids</strong></p></th>
<th><p><strong>Taille</strong></p>
<p><strong>poids</strong></p></th>
<th><strong>Commentaires</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#621-entrytype-field">section 6.2.1</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>CustomDefined</td>
<td>1</td>
<td>19</td>
<td>Ce champ est obligatoire et les structures qui dérivent de ce modèle peuvent définir son contenu.</td>
</tr>
<tr class="odd">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Ce champ est obligatoire et la <a href="#622-firstcluster-field">section 6.2.2</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Ce champ est obligatoire et la <a href="#623-datalength-field">section 6.2.3</a> définit son contenu.</td>
</tr>
</tbody>
</table>

#### <a name="621-entrytype-field"></a>6.2.1 champ EntryType

Le champ EntryType a trois modes d’utilisation que la valeur du champ définit (voir la liste ci-dessous).

- 00h, qui est un marqueur de fin de répertoire et les conditions suivantes s’appliquent :

  - Tous les autres champs du DirectoryEntry donné sont réellement réservés

  - Toutes les entrées de répertoire suivantes dans le répertoire donné sont également des marqueurs de fin de répertoire

  - Les marqueurs de fin de répertoire ne sont valides qu’en dehors des ensembles d’entrées de répertoire

  - Les implémentations peuvent remplacer les marqueurs de fin de répertoire en fonction des besoins

- Entre 01H et 7Fh, qui est un marqueur d’entrée de répertoire inutilisé et les conditions suivantes s’appliquent :

  - Tous les autres champs du DirectoryEntry donné sont réellement non définis

  - Les entrées d’annuaire inutilisées ne sont valides qu’en dehors des jeux d’entrées de répertoire

  - Les implémentations peuvent remplacer les entrées d’annuaire inutilisées si nécessaire.

  - Cette plage de valeurs correspond au champ InUse (voir la [section 6.2.1.4](#6214-inuse-field)) contenant la valeur 0

- Entre 81h et FFh, qui est une entrée de répertoire standard et les conditions suivantes s’appliquent :

  - Le contenu du champ EntryType (voir le [tableau 15](#table-15-generic-entrytype-field-structure)) détermine la disposition du reste de la structure DirectoryEntry

  - Cette plage de valeurs et uniquement cette plage de valeurs sont valides dans un jeu d’entrées de répertoire.

  - Cette plage de valeurs correspond directement au champ InUse (voir la [section 6.2.1.4](#6214-inuse-field)) contenant la valeur 1

Pour empêcher toute modification apportée au champ InUse (voir la [section 6.2.1.4](#6214-inuse-field)) provoquant par erreur un marqueur de fin de répertoire, la valeur 80h n’est pas valide.

<div id="table-15-generic-entrytype-field-structure" />

**Tableau 15-structure de champs EntryType générique**

<table>
<thead>
<tr class="header">
<th><strong>Nom du champ</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>64bits</strong></p></th>
<th><p><strong>Taille</strong></p>
<p><strong>bits</strong></p></th>
<th><strong>Commentaires</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>TypeCode</td>
<td>0</td>
<td>5</td>
<td>Ce champ est obligatoire et la <a href="#6211-typecode-field">section 6.2.1.1</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>TypeImportance</td>
<td>5</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#6212-typeimportance-field">section section 6.2.1.2</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>TypeCategory</td>
<td>6</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#6213-typecategory-field">section 6.2.1.3</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>InUse</td>
<td>7</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#6214-inuse-field">section 6.2.1.4</a> définit son contenu.</td>
</tr>
</tbody>
</table>

##### <a name="6211-typecode-field"></a>Champ TypeCode 6.2.1.1

Le champ TypeCode décrit partiellement le type spécifique de l’entrée de répertoire donnée. Ce champ, ainsi que les champs TypeImportance et TypeCategory (voir la [section 6.2.1.2](#6212-typeimportance-field) et la [section 6.2.1.3](#6213-typecategory-field), respectivement) identifient de façon unique le type de l’entrée de répertoire donnée.

Toutes les valeurs possibles de ce champ sont valides, à moins que les champs TypeImportance et TypeCategory contiennent tous les deux la valeur 0 ; dans ce cas, la valeur 0 n’est pas valide pour ce champ.

##### <a name="6212-typeimportance-field"></a>Champ 6.2.1.2 TypeImportance

Le champ TypeImportance doit décrire l’importance de l’entrée de répertoire donnée.

Les valeurs valides pour ce champ sont les suivantes :

- 0, ce qui signifie que l’entrée de répertoire donnée est critique (voir la [section 6.3.1.2.1](#63121-critical-primary-directory-entries) et la [section 6.4.1.2.1](#64121-critical-secondary-directory-entries) pour les entrées de répertoire secondaires principales critiques et critiques, respectivement)

- 1, ce qui signifie que l’entrée de répertoire donnée est sans gravité (voir la [section 6.3.1.2.2](#63122-benign-primary-directory-entries) et la [section 6.4.1.2.2](#64122-benign-secondary-directory-entries) pour les entrées de répertoire secondaires principales et bénignes, respectivement)

##### <a name="6213-typecategory-field"></a>Champ TypeCategory 6.2.1.3

Le champ TypeCategory décrit la catégorie de l’entrée d’annuaire donnée.

Les valeurs valides pour ce champ sont les suivantes :

- 0, ce qui signifie que l’entrée de répertoire donnée est principale (voir la [Section 6,3](#63-generic-primary-directoryentry-template))

- 1, ce qui signifie que l’entrée de répertoire donnée est secondaire (voir la [Section 6,4](#64-generic-secondary-directoryentry-template))

##### <a name="6214-inuse-field"></a>Champ 6.2.1.4 InUse

Le champ InUse décrit si l’entrée de répertoire spécifiée est utilisée ou non.

Les valeurs valides pour ce champ sont les suivantes :

- 0, ce qui signifie que l’entrée de répertoire donnée n’est pas en cours d’utilisation ; Cela signifie que la structure donnée est effectivement une entrée d’annuaire inutilisée

- 1, ce qui signifie que l’entrée de répertoire spécifiée est en cours d’utilisation ; Cela signifie que la structure donnée est une entrée de répertoire standard

#### <a name="622-firstcluster-field"></a>6.2.2, champ FirstCluster

Le champ FirstCluster doit contenir l’index du premier cluster d’une allocation dans le segment de mémoire de cluster associé à l’entrée de répertoire donnée.

La plage de valeurs valide pour ce champ doit être :

- Exactement 0, ce qui signifie qu’il n’existe aucune allocation de cluster

- Entre 2 et Clustercount, + 1, qui est la plage d’index de cluster valides

Les structures qui dérivent de ce modèle peuvent redéfinir les champs FirstCluster et DataLength, si une allocation de cluster n’est pas compatible avec la structure dérivée.

#### <a name="623-datalength-field"></a>6.2.3-champ DataLength

Le champ DataLength décrit la taille, en octets, des données contenues dans l’allocation de cluster associée.

La plage de valeurs valide pour ce champ est :

- Au moins 0 ; Si le champ FirstCluster contient la valeur 0, la seule valeur valide de ce champ est 0

- Au plus Clustercount, \* 2<sup>SectorsPerClusterShift</sup> \* 2<sup>BytesPerSectorShift</sup>

Les structures qui dérivent de ce modèle peuvent redéfinir les champs FirstCluster et DataLength, si une allocation de cluster n’est pas possible pour la structure dérivée.

### <a name="63-generic-primary-directoryentry-template"></a>Modèle DirectoryEntry principal générique 6,3

La première entrée d’annuaire dans un jeu d’entrées de répertoire doit être une entrée d’annuaire primaire. Toutes les entrées de répertoire ultérieures, le cas échéant, dans l’ensemble d’entrées de répertoire sont des entrées de répertoire secondaires (voir la [Section 6,4](#64-generic-secondary-directoryentry-template)).

La possibilité d’interpréter le modèle DirectoryEntry principal générique est obligatoire.

Toutes les structures d’entrée de répertoire principal dérivent du modèle DirectoryEntry générique principal (voir le [tableau 16](#table-16-generic-primary-directoryentry-template)), qui dérive du modèle DirectoryEntry générique (voir la [section 6,2](#62-generic-directoryentry-template)).

<div id="table-16-generic-primary-directoryentry-template" />

**Tableau 16 modèle DirectoryEntry générique principal**

<table>
<thead>
<tr class="header">
<th><strong>Nom du champ</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>poids</strong></p></th>
<th><p><strong>Taille</strong></p>
<p><strong>poids</strong></p></th>
<th><strong>Commentaires</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#631-entrytype-field">section 6.3.1</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>SecondaryCount</td>
<td>1</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#632-secondarycount-field">section 6.3.2</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>SetChecksum</td>
<td>2</td>
<td>2</td>
<td>Ce champ est obligatoire et la <a href="#633-setchecksum-field">section 6.3.3</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>GeneralPrimaryFlags</td>
<td>4</td>
<td>2</td>
<td>Ce champ est obligatoire et la <a href="#634-generalprimaryflags-field">section 6.3.4</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>CustomDefined</td>
<td>6</td>
<td>14</td>
<td>Ce champ est obligatoire et les structures qui dérivent de ce modèle définissent son contenu.</td>
</tr>
<tr class="even">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Ce champ est obligatoire et la <a href="#635-firstcluster-field">section 6.3.5</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Ce champ est obligatoire et la <a href="#636-datalength-field">section 6.3.6</a> définit son contenu.</td>
</tr>
</tbody>
</table>

#### <a name="631-entrytype-field"></a>6.3.1 champ EntryType

Le champ EntryType doit être conforme à la définition fournie dans le modèle DirectoryEntry générique (voir la [section 6.2.1](#621-entrytype-field)).

##### <a name="6311-typecode-field"></a>Champ TypeCode 6.3.1.1

Le champ TypeCode doit se conformer à la définition fournie dans le modèle DirectoryEntry générique (voir la [section 6.2.1.1](#6211-typecode-field)).

##### <a name="6312-typeimportance-field"></a>Champ 6.3.1.2 TypeImportance

Le champ TypeImportance doit être conforme à la définition fournie dans le modèle DirectoryEntry générique (voir la [section 6.2.1.2](#6212-typeimportance-field)).

###### <a name="63121-critical-primary-directory-entries"></a>Entrées de répertoire principal critiques 6.3.1.2.1

Les entrées d’annuaire principales critiques contiennent des informations qui sont essentielles à la gestion appropriée d’un volume exFAT. Seul le répertoire racine contient des entrées de répertoire principales critiques (les entrées de répertoire de fichier sont une exception, consultez la [Section 7,4](#74-file-directory-entry)).

La définition des entrées d’annuaire principales critiques est corrélée avec le numéro de révision exFAT majeur. Les implémentations doivent prendre en charge toutes les entrées d’annuaire principales critiques et enregistrer uniquement les structures d’entrée de répertoire principales critiques définies par cette spécification.

###### <a name="63122-benign-primary-directory-entries"></a>6.3.1.2.2 les entrées de répertoire principal bénignes

Les entrées de répertoire principales bénignes contiennent des informations supplémentaires qui peuvent être utiles pour gérer un volume exFAT. N’importe quel répertoire peut contenir des entrées de répertoire principal bénignes.

La définition des entrées d’annuaire principales bénignes correspond au numéro de révision exFAT mineur. La prise en charge de toute entrée de répertoire primaire bénigne de cette spécification, ou de toute spécification ultérieure, définit est facultative. Une entrée d’annuaire principal Bénin non reconnue rend l’ensemble de l’entrée de répertoire non reconnue (au-delà de la définition des modèles d’entrée de répertoire applicables).

##### <a name="6313-typecategory-field"></a>Champ 6.3.1.3 TypeCategory

Le champ TypeCategory doit être conforme à la définition fournie dans le modèle DirectoryEntry générique (voir la [section 6.2.1.3](#6213-typecategory-field)).

Pour ce modèle, la valeur valide pour ce champ doit être 0.

##### <a name="6314-inuse-field"></a>Champ 6.3.1.4 InUse

Le champ InUse doit se conformer à la définition fournie dans le modèle DirectoryEntry générique (voir la [section 6.2.1.4](#6214-inuse-field)).

#### <a name="632-secondarycount-field"></a>6.3.2 champ SecondaryCount

Le champ SecondaryCount doit décrire le nombre d’entrées de répertoire secondaire qui suivent immédiatement l’entrée d’annuaire primaire donnée. Ces entrées de répertoire secondaires, ainsi que l’entrée d’annuaire primaire donnée, constituent le jeu d’entrées de répertoire.

La plage de valeurs valide pour ce champ doit être :

- Au moins 0, ce qui signifie que cette entrée d’annuaire primaire est la seule entrée dans le jeu d’entrées de répertoire

- Au plus 255, ce qui signifie que les 255 entrées de répertoire suivantes et cette entrée d’annuaire principale comprennent le jeu d’entrées de répertoire

Les structures d’entrée de répertoire principales critiques qui dérivent de ce modèle peuvent redéfinir les champs SecondaryCount et SetCheckSum,.

#### <a name="633-setchecksum-field"></a>Champ 6.3.3 SetCheckSum,

Le champ SetCheckSum, doit contenir la somme de contrôle de toutes les entrées de répertoire dans le jeu d’entrées de répertoire donné. Toutefois, la somme de contrôle exclut ce champ (voir [figure 2](#figure-2-entrysetchecksum-computation)). Les implémentations doivent vérifier que le contenu de ce champ est valide avant d’utiliser une autre entrée de répertoire dans le jeu d’entrées de répertoire donné.

Les structures d’entrée de répertoire principales critiques qui dérivent de ce modèle peuvent redéfinir les champs SecondaryCount et SetCheckSum,.

<div id="figure-2-entrysetchecksum-computation" />

**Figure 2 calcul EntrySetChecksum**

```C
UInt16 EntrySetChecksum
(
    UCHAR * Entries,       // points to an in-memory copy of the directory entry set
    UCHAR   SecondaryCount
)
{
    UInt16 NumberOfBytes = ((UInt16)SecondaryCount + 1) * 32;
    UInt16 Checksum = 0;
    UInt16 Index;

    for (Index = 0; Index < NumberOfBytes; Index++)
    {
        if ((Index == 2) || (Index == 3))
        {
            continue;
        }
        Checksum = ((Checksum&1) ? 0x8000 : 0) + (Checksum>>1) +  (UInt16)Entries[Index];
    }
    return Checksum;
}
```

#### <a name="634-generalprimaryflags-field"></a>Champ 6.3.4 GeneralPrimaryFlags

Le champ GeneralPrimaryFlags contient des indicateurs (voir [tableau 17](#table-17-generic-generalprimaryflags-field-structure)).

Les structures d’entrée de répertoire principales critiques qui dérivent de ce modèle peuvent redéfinir ce champ.

<div id="table-17-generic-generalprimaryflags-field-structure" />

**Tableau 17 structure des champs GeneralPrimaryFlags génériques**

<table>
<thead>
<tr class="header">
<th><strong>Nom du champ</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>64bits</strong></p></th>
<th><p><strong>Taille</strong></p>
<p><strong>bits</strong></p></th>
<th><strong>Commentaires</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AllocationPossible</td>
<td>0</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#6341-allocationpossible-field">section 6.3.4.1</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>NoFatChain</td>
<td>1</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#6342-nofatchain-field">section 6.3.4.2</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>CustomDefined</td>
<td>2</td>
<td>14</td>
<td>Ce champ est obligatoire et les structures qui dérivent de ce modèle peuvent définir ce champ.</td>
</tr>
</tbody>
</table>

##### <a name="6341-allocationpossible-field"></a>Champ 6.3.4.1 AllocationPossible

Le champ AllocationPossible indique si une allocation dans le segment de mémoire de cluster est possible pour l’entrée de répertoire donnée.

Les valeurs valides pour ce champ sont les suivantes :

- 0, ce qui signifie qu’une allocation associée de clusters n’est pas possible et que les champs FirstCluster et DataLength sont réellement non définis (les structures qui dérivent de ce modèle peuvent redéfinir ces champs)

- 1, ce qui signifie qu’une allocation associée de clusters est possible et que les champs FirstCluster et DataLength sont définis

##### <a name="6342-nofatchain-field"></a>Champ 6.3.4.2 NoFatChain

Le champ NoFatChain indique si la FAT active décrit la chaîne de cluster de l’allocation donnée.

Les valeurs valides pour ce champ sont les suivantes :

- 0, ce qui signifie que les entrées FAT correspondantes pour la chaîne de cluster de l’allocation sont valides et que les implémentations doivent les interpréter ; Si le champ AllocationPossible contient la valeur 0, ou si le champ AllocationPossible contient la valeur 1 et que le champ FirstCluster contient la valeur 0, la seule valeur valide de ce champ est 0

- 1, ce qui signifie que l’allocation associée est une série contiguë de clusters ; les entrées FAT correspondantes pour les clusters ne sont pas valides et les implémentations ne doivent pas les interpréter ; les implémentations peuvent utiliser l’équation suivante pour calculer la taille de l’allocation associée : DataLength/(2<sup>SectorsPerClusterShift</sup> \* 2<sup>BytesPerSectorShift</sup>) arrondi à l’entier le plus proche

Si les structures d’entrée de répertoire principales critiques qui dérivent de ce modèle redéfinissent le champ GeneralPrimaryFlags, les entrées FAT correspondantes pour toute chaîne de cluster d’allocation associée sont valides.

#### <a name="635-firstcluster-field"></a>Champ 6.3.5 FirstCluster

Le champ FirstCluster doit être conforme à la définition fournie dans le modèle DirectoryEntry générique (voir la [section 6.2.2](#622-firstcluster-field)).

Si le bit NoFatChain est 1, FirstCluster doit pointer vers un cluster valide dans le tas de cluster.

Les structures d’entrée de répertoire principales critiques qui dérivent de ce modèle peuvent redéfinir les champs FirstCluster et DataLength. Les autres structures qui dérivent de ce modèle peuvent redéfinir les champs FirstCluster et DataLength uniquement si le champ AllocationPossible contient la valeur 0.

#### <a name="636-datalength-field"></a>Champ 6.3.6 DataLength

Le champ DataLength doit se conformer à la définition fournie dans le modèle DirectoryEntry générique (voir la [section 6.2.3](#623-datalength-field)).

Si le bit NoFatChain est 1, DataLength ne doit pas être égal à zéro. Si le champ FirstCluster est égal à zéro, DataLength doit également avoir la valeur zéro.

Les structures d’entrée de répertoire principales critiques qui dérivent de ce modèle peuvent redéfinir les champs FirstCluster et DataLength. Les autres structures qui dérivent de ce modèle peuvent redéfinir les champs FirstCluster et DataLength uniquement si le champ AllocationPossible contient la valeur 0.

### <a name="64-generic-secondary-directoryentry-template"></a>Modèle DirectoryEntry secondaire générique 6,4

L’objectif principal des entrées d’annuaire secondaires est de fournir des informations supplémentaires sur un jeu d’entrées de répertoire. La possibilité d’interpréter le modèle DirectoryEntry secondaire générique est obligatoire.

La définition des entrées d’annuaire secondaire critiques et bénignes est corrélée avec le numéro de révision exFAT mineur. La prise en charge d’une entrée d’annuaire secondaire critique ou Bénin dans cette spécification, ou sur les spécifications suivantes, définit est facultative.

Toutes les structures d’entrée de répertoire secondaires dérivent du modèle DirectoryEntry secondaire générique (voir le [tableau 18](#table-18-generic-secondary-directoryentry-template)), qui dérive du modèle DirectoryEntry générique (voir la [section 6,2](#62-generic-directoryentry-template)).

<div id="table-18-generic-secondary-directoryentry-template" />

**Tableau 18 modèle DirectoryEntry générique secondaire**

<table>
<thead>
<tr class="header">
<th><strong>Nom du champ</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>poids</strong></p></th>
<th><p><strong>Taille</strong></p>
<p><strong>poids</strong></p></th>
<th><strong>Commentaires</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#641-entrytype-field">section section 6.4.1</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#642-generalsecondaryflags-field">section 6.4.2</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>CustomDefined</td>
<td>2</td>
<td>18</td>
<td>Ce champ est obligatoire et les structures qui dérivent de ce modèle définissent son contenu.</td>
</tr>
<tr class="even">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Ce champ est obligatoire et la <a href="#643-firstcluster-field">section 6.4.3</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Ce champ est obligatoire et la <a href="#644-datalength-field">section 6.4.4</a> définit son contenu.</td>
</tr>
</tbody>
</table>

#### <a name="641-entrytype-field"></a>Champ 6.4.1 EntryType

Le champ EntryType doit être conforme à la définition fournie dans le modèle DirectoryEntry générique (voir la [section 6.2.1](#621-entrytype-field)).

##### <a name="6411-typecode-field"></a>Champ TypeCode 6.4.1.1

Le champ TypeCode doit se conformer à la définition fournie dans le modèle DirectoryEntry générique (voir la [section 6.2.1.1](#6211-typecode-field)).

##### <a name="6412-typeimportance-field"></a>Champ 6.4.1.2 TypeImportance

Le champ TypeImportance doit être conforme à la définition fournie dans le modèle DirectoryEntry générique (voir la [section 6.2.1.2](#6212-typeimportance-field)).

###### <a name="64121-critical-secondary-directory-entries"></a>Entrées d’annuaire secondaire critique 6.4.1.2.1

Les entrées de répertoire secondaires critiques contiennent des informations qui sont essentielles à la gestion correcte de l’ensemble d’entrées de répertoire qui les contient.
Bien que la prise en charge d’une entrée d’annuaire secondaire critique spécifique soit facultative, une entrée de répertoire critique non reconnue rend le jeu d’entrées de répertoire entier non reconnu (au-delà de la définition des modèles d’entrée de répertoire applicables).

Toutefois, si un jeu d’entrées de répertoire contient au moins une entrée d’annuaire secondaire critique qu’une implémentation ne reconnaît pas, l’implémentation doit, au plus, interpréter les modèles des entrées d’annuaire dans le jeu d’entrées d’annuaire et non pas les données qu’une allocation associée à une entrée d’annuaire dans le jeu d’entrées de répertoire contient (les entrées de répertoire de fichiers sont une [7,4](#74-file-directory-entry)exception.

###### <a name="64122-benign-secondary-directory-entries"></a>Entrées de répertoire secondaire 6.4.1.2.2 bénignes

Les entrées de répertoire secondaires bénignes contiennent des informations supplémentaires qui peuvent être utiles pour gérer l’ensemble d’entrées de répertoire qui les contient. La prise en charge d’une entrée de répertoire secondaire inoffensif spécifique est facultative.
Les entrées d’annuaire secondaire non reconnues n’affichent pas l’intégralité de l’entrée de répertoire définie comme non reconnue.

Les implémentations peuvent ignorer toute entrée secondaire bénigne qu’elle ne reconnaît pas.

##### <a name="6413-typecategory-field"></a>Champ 6.4.1.3 TypeCategory

Le champ TypeCategory doit être conforme à la définition fournie dans le modèle DirectoryEntry générique (voir la [section 6.2.1.3](#6213-typecategory-field)).

Pour ce modèle, la valeur valide pour ce champ est 1.

##### <a name="6414-inuse-field"></a>Champ 6.4.1.4 InUse

Le champ InUse doit se conformer à la définition fournie dans le modèle DirectoryEntry générique (voir la [section 6.2.1.4](#6214-inuse-field)).

#### <a name="642-generalsecondaryflags-field"></a>6.4.2 champ GeneralSecondaryFlags

Le champ GeneralSecondaryFlags contient des indicateurs (voir [tableau 19](#table-19-generic-generalsecondaryflags-field-structure)).

<div id="table-19-generic-generalsecondaryflags-field-structure" />

**Tableau 19-structure de champs GeneralSecondaryFlags générique**

<table>
<thead>
<tr class="header">
<th><strong>Nom du champ</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>64bits</strong></p></th>
<th><p><strong>Taille</strong></p>
<p><strong>bits</strong></p></th>
<th><strong>Commentaires</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AllocationPossible</td>
<td>0</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#6421-allocationpossible-field">section 6.4.2.1</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>NoFatChain</td>
<td>1</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#6422-nofatchain-field">section 6.4.2.2</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>CustomDefined</td>
<td>2</td>
<td>6</td>
<td>Ce champ est obligatoire et les structures qui dérivent de ce modèle peuvent définir ce champ.</td>
</tr>
</tbody>
</table>

##### <a name="6421-allocationpossible-field"></a>Champ 6.4.2.1 AllocationPossible

Le champ AllocationPossible doit avoir la même définition que le champ portant le même nom dans le modèle DirectoryEntry principal générique (voir la [section 6.3.4.1](#6341-allocationpossible-field)).

##### <a name="6422-nofatchain-field"></a>Champ 6.4.2.2 NoFatChain

Le champ NoFatChain doit avoir la même définition que le champ portant le même nom dans le modèle DirectoryEntry principal générique (voir la [section 6.3.4.2](#6342-nofatchain-field)).

#### <a name="643-firstcluster-field"></a>Champ 6.4.3 FirstCluster

Le champ FirstCluster doit être conforme à la définition fournie dans le modèle DirectoryEntry générique (voir la [section 6.2.2](#622-firstcluster-field)).

Si le bit NoFatChain est 1, FirstCluster doit pointer vers un cluster valide dans le tas de cluster.

#### <a name="644-datalength-field"></a>Champ 6.4.4 DataLength

Le champ DataLength doit se conformer à la définition fournie dans le modèle DirectoryEntry générique (voir la [section 6.2.3](#623-datalength-field)).

Si le bit NoFatChain est 1, DataLength ne doit pas être égal à zéro. Si le champ FirstCluster est égal à zéro, DataLength doit également avoir la valeur zéro.

## <a name="7-directory-entry-definitions"></a>7 définitions d’entrée de répertoire

La révision 1,00 du système de fichiers exFAT définit les entrées de répertoire suivantes :

- Clé principale critique

  - Bitmap d’allocation ([Section 7,1](#71-allocation-bitmap-directory-entry))

  - Table de cas ([Section 7,2](#72-up-case-table-directory-entry))

  - Nom de volume ([Section 7,3](#73-volume-label-directory-entry))

  - Fichier ([Section 7,4](#74-file-directory-entry))

- Principal Bénin

  - GUID du volume ([Section 7,5](#75-volume-guid-directory-entry))

  - TexFAT de remplissage ([Section 7,10](#710-texfat-padding-directory-entry))

<!-- -->

- Secondaire critique

  - Extension de flux ([Section 7,6](#76-stream-extension-directory-entry))

  - Nom de fichier ([Section 7,7](#77-file-name-directory-entry))

- Secondaire sans gravité

  - Extension de fournisseur ([Section 7,8](#78-vendor-extension-directory-entry))

  - Allocation du fournisseur ([Section 7,9](#79-vendor-allocation-directory-entry))

### <a name="71-allocation-bitmap-directory-entry"></a>7,1 entrée de répertoire de l’allocation de bitmap

Dans le système de fichiers exFAT, FAT ne décrit pas l’état d’allocation des clusters ; au lieu de cela, une bitmap d’allocation. Les bitmaps d’allocation existent dans le segment de mémoire du cluster (voir la [section 7.1.5](#715-allocation-bitmap)) et ont des entrées d’annuaire principales critiques correspondantes dans le répertoire racine (voir [tableau 20](#table-20-allocation-bitmap-directoryentry-structure)).

Le champ NumberOfFats détermine le nombre d’entrées de répertoires de la bitmap d’allocation valides dans le répertoire racine. Si le champ NumberOfFats contient la valeur 1, le seul nombre valide d’entrées de l’arborescence de la bitmap d’allocation est 1. En outre, l’entrée de répertoire de l’image bitmap d’allocation est valide uniquement si elle décrit la première bitmap d’allocation (voir la [section 7.1.2.1](#7121-bitmapidentifier-field)). Si le champ NumberOfFats contient la valeur 2, le seul nombre valide d’entrées de l’annuaire de la bitmap d’allocation est 2.
En outre, les deux entrées de répertoire de la bitmap d’allocation sont valides uniquement si l’une d’elles décrit la première bitmap d’allocation et l’autre décrit la deuxième bitmap d’allocation.

<div id="table-20-allocation-bitmap-directoryentry-structure" />

**Table 20 bitmap d’allocation, structure DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nom du champ</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>poids</strong></p></th>
<th><p><strong>Taille</strong></p>
<p><strong>poids</strong></p></th>
<th><strong>Commentaires</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#711-entrytype-field">section 7.1.1</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>BitmapFlags</td>
<td>1</td>
<td>1</td>
<td>Ce champ est obligatoire et le <a href="#712-bitmapflags-field">chapitre 7.1.2</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>Réservé</td>
<td>2</td>
<td>18</td>
<td>Ce champ est obligatoire et son contenu est réservé.</td>
</tr>
<tr class="even">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Ce champ est obligatoire et la <a href="#713-firstcluster-field">section 7.1.3</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Ce champ est obligatoire et la <a href="#714-datalength-field">section 7.1.4</a> définit son contenu.</td>
</tr>
</tbody>
</table>

#### <a name="711-entrytype-field"></a>7.1.1 champ EntryType

Le champ EntryType doit être conforme à la définition fournie dans le modèle DirectoryEntry principal générique (voir la [section 6.3.1](#631-entrytype-field)).

##### <a name="7111-typecode-field"></a>7.1.1.1 champ TypeCode

Le champ TypeCode doit se conformer à la définition fournie dans le modèle DirectoryEntry principal générique (voir la [section 6.3.1.1](#6311-typecode-field)).

Pour une entrée d’annuaire d’une bitmap d’allocation, la valeur valide pour ce champ est 1.

##### <a name="7112-typeimportance-field"></a>7.1.1.2 champ TypeImportance

Le champ TypeImportance doit être conforme à la définition fournie dans le modèle DirectoryEntry principal générique (voir la [section 6.3.1.2](#6312-typeimportance-field)).

Pour une entrée de répertoire d’une bitmap d’allocation, la valeur valide pour ce champ est 0.

##### <a name="7113-typecategory-field"></a>Champ 7.1.1.3 TypeCategory

Le champ TypeCategory doit être conforme à la définition fournie dans le modèle DirectoryEntry principal générique (voir la [section 6.3.1.3](#6313-typecategory-field)).

##### <a name="7114-inuse-field"></a>Champ 7.1.1.4 InUse

Le champ InUse doit se conformer à la définition fournie dans le modèle DirectoryEntry principal générique (voir la [section 6.3.1.4](#6314-inuse-field)).

#### <a name="712-bitmapflags-field"></a>7.1.2 champ BitmapFlags

Le champ BitmapFlags contient des indicateurs (voir le [tableau 21](#table-21-bitmapflags-field-structure)).

<div id="table-21-bitmapflags-field-structure" />

**Tableau 21-structure de champs BitmapFlags**

<table>
<thead>
<tr class="header">
<th><strong>Nom du champ</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>64bits</strong></p></th>
<th><p><strong>Taille</strong></p>
<p><strong>bits</strong></p></th>
<th><strong>Commentaires</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>BitmapIdentifier</td>
<td>0</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#7121-bitmapidentifier-field">section 7.1.2.1</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>Réservé</td>
<td>1</td>
<td>7</td>
<td>Ce champ est obligatoire et son contenu est réservé.</td>
</tr>
</tbody>
</table>

##### <a name="7121-bitmapidentifier-field"></a>Champ 7.1.2.1 BitmapIdentifier

Le champ BitmapIdentifier indique la bitmap d’allocation décrite par l’entrée d’annuaire donnée. Les implémentations utilisent la première bitmap d’allocation conjointement avec le premier système FAT et utilisent la deuxième bitmap d’allocation conjointement avec la deuxième FAT. Le champ ActiveFat décrit les fichiers FAT et les bitmaps d’allocation actifs.

Les valeurs valides pour ce champ sont les suivantes :

- 0, ce qui signifie que l’entrée de répertoire donnée décrit la première bitmap d’allocation

- 1, ce qui signifie que l’entrée de répertoire donnée décrit la deuxième bitmap d’allocation et n’est possible que lorsque NumberOfFats contient la valeur 2

#### <a name="713-firstcluster-field"></a>Champ FirstCluster 7.1.3

Le champ FirstCluster doit être conforme à la définition fournie dans le modèle DirectoryEntry principal générique (voir la [section 6.3.5](#635-firstcluster-field)).

Ce champ contient l’index du premier cluster de la chaîne de cluster, comme décrit dans le FAT, qui héberge la bitmap d’allocation.

#### <a name="714-datalength-field"></a>Champ 7.1.4 DataLength

Le champ DataCluster doit être conforme à la définition fournie dans le modèle DirectoryEntry principal générique (voir la [section 6.3.6](#636-datalength-field)).

#### <a name="715-allocation-bitmap"></a>Bitmap d’allocation 7.1.5

Une bitmap d’allocation enregistre l’état d’allocation des clusters dans le segment de mémoire du cluster. Chaque bit d’une bitmap d’allocation indique si son cluster correspondant est disponible pour l’allocation ou non.

Une bitmap d’allocation représente les clusters de l’index le plus bas au plus haut (voir le [tableau 22](#table-22-allocation-bitmap-structure)). Pour des raisons historiques, le premier cluster possède l’index 2.
Remarque : le premier bit de la bitmap est le bit d’ordre le plus bas du premier octet.

<div id="table-22-allocation-bitmap-structure" />

**Tableau 22 structure d’une bitmap d’allocation**

<table>
<thead>
<tr class="header">
<th><strong>Nom du champ</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>64bits</strong></p></th>
<th><p><strong>Taille</strong></p>
<p><strong>bits</strong></p></th>
<th><strong>Commentaires</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>BitmapEntry [2]</td>
<td>0</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#7151-bitmapentry2--bitmapentryclustercount1-fields">section section 7.1.5.1</a> définit son contenu.</td>
</tr>
<tr class="even">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="odd">
<td>BitmapEntry [Clustercount, + 1]</td>
<td>Clustercount,-1</td>
<td>1</td>
<td><p>Ce champ est obligatoire et la <a href="#7151-bitmapentry2--bitmapentryclustercount1-fields">section 7.1.5.1</a> définit son contenu.</p>
<p>Remarque : les secteurs de démarrage principal et de sauvegarde contiennent tous les deux le champ Clustercount,.</p></td>
</tr>
<tr class="even">
<td>Réservé</td>
<td>Clustercount,</td>
<td>(DataLength * 8) – Clustercount,</td>
<td><p>Ce champ est obligatoire et son contenu, le cas échéant, est réservé.</p>
<p>Remarque : les secteurs de démarrage principal et de sauvegarde contiennent tous les deux le champ Clustercount,.</p></td>
</tr>
</tbody>
</table>

##### <a name="7151-bitmapentry2--bitmapentryclustercount1-fields"></a>7.1.5.1 BitmapEntry \[ 2 \] ... \[Champs BitmapEntry clustercount, + 1 \]

Chaque champ BitmapEntry de ce tableau représente un cluster dans le segment de mémoire du cluster. BitmapEntry \[ 2 \] représente le premier cluster dans le segment de mémoire de cluster et BitmapEntry \[ clustercount, + 1 \] représente le dernier cluster dans le segment de mémoire du cluster.

Les valeurs valides pour ces champs doivent être :

- 0, qui décrit le cluster correspondant comme étant disponible pour l’allocation

- 1, qui décrit le cluster correspondant comme n’étant pas disponible pour l’allocation (une allocation de cluster peut déjà consommer le cluster correspondant ou la FAT active peut décrire le cluster correspondant comme étant incorrecte)

### <a name="72-up-case-table-directory-entry"></a>7,2 entrée du répertoire de la table de cas

La table up-case définit la conversion des caractères minuscules en majuscules. Cela est important en raison de l’entrée de répertoire de nom de fichier (voir la section 7,7) en utilisant des caractères Unicode et le système de fichiers exFAT qui ne respecte pas la casse et conserve la casse. La table de cas existe dans le segment de mémoire du cluster (voir la [section 7.2.5](#725-up-case-table)) et a une entrée d’annuaire principale critique correspondante dans le répertoire racine (voir le [tableau 23](#table-23-up-case-table-directoryentry-structure)). Le nombre valide d’entrées du répertoire de la table de cas d’usage est de 1.

En raison de la relation entre les noms de table et de fichier, les implémentations ne doivent pas modifier la table de cas, sauf suite à des opérations de format.

<div id="table-23-up-case-table-directoryentry-structure" />

**Tableau 23 structure de la table de cas**

<table>
<thead>
<tr class="header">
<th><strong>Nom du champ</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>poids</strong></p></th>
<th><p><strong>Taille</strong></p>
<p><strong>poids</strong></p></th>
<th><strong>Commentaires</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#721-entrytype-field">section 7.2.1</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>Reserved1</td>
<td>1</td>
<td>3</td>
<td>Ce champ est obligatoire et son contenu est réservé.</td>
</tr>
<tr class="odd">
<td>TableChecksum</td>
<td>4</td>
<td>4</td>
<td>Ce champ est obligatoire et la <a href="#722-tablechecksum-field">section 7.2.2</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>Reserved2</td>
<td>8</td>
<td>12</td>
<td>Ce champ est obligatoire et son contenu est réservé.</td>
</tr>
<tr class="odd">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Ce champ est obligatoire et la <a href="#723-firstcluster-field">section 7.2.3</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Ce champ est obligatoire et la <a href="#724-datalength-field">section 7.2.4</a> définit son contenu.</td>
</tr>
</tbody>
</table>

#### <a name="721-entrytype-field"></a>7.2.1 champ EntryType

Le champ EntryType doit être conforme à la définition fournie dans le modèle DirectoryEntry principal générique (voir la [section 6.3.1](#631-entrytype-field)).

##### <a name="7211-typecode-field"></a>Champ TypeCode 7.2.1.1

Le champ TypeCode doit se conformer à la définition fournie dans le modèle DirectoryEntry principal générique (voir la [section 6.3.1.1](#6311-typecode-field)).

Pour l’entrée d’annuaire de la table de cas, la valeur valide pour ce champ est
2.

##### <a name="7212-typeimportance-field"></a>Champ TypeImportance 7.2.1.2.

Le champ TypeImportance doit être conforme à la définition fournie dans le modèle DirectoryEntry principal générique (voir la [section 6.3.1.2](#6312-typeimportance-field)).

Pour l’entrée d’annuaire de la table de cas, la valeur valide pour ce champ est
0.

##### <a name="7213-typecategory-field"></a>Champ 7.2.1.3 TypeCategory

Le champ TypeCategory doit être conforme à la définition fournie dans le modèle DirectoryEntry principal générique (voir la [section 6.3.1.3](#6313-typecategory-field)).

##### <a name="7214-inuse-field"></a>Champ 7.2.1.4 InUse

Le champ InUse doit se conformer à la définition fournie dans le modèle DirectoryEntry principal générique (voir la [section 6.3.1.4](#6314-inuse-field)).

#### <a name="722-tablechecksum-field"></a>7.2.2 champ TableChecksum

Le champ TableChecksum contient la somme de contrôle de la table up-case (les champs FirstCluster et DataLength décrivent). Les implémentations doivent vérifier que le contenu de ce champ est valide avant d’utiliser la table de cas.

<div id="figure-3-tablechecksum-computation" />

**Figure 3 calcul TableChecksum**

```C
UInt32 TableChecksum
(
    UCHAR  * Table,    // points to an in-memory copy of the up-case table
    UInt64   DataLength
)
{
    UInt32 Checksum = 0;
    UInt64 Index;

    for (Index = 0; Index < DataLength; Index++)
    {
        Checksum = ((Checksum&1) ? 0x80000000 : 0) + (Checksum>>1) + (UInt32)Table[Index];
    }

    return Checksum;
}
```

#### <a name="723-firstcluster-field"></a>7.2.3 champ FirstCluster

Le champ FirstCluster doit être conforme à la définition fournie dans le modèle DirectoryEntry principal générique (voir la [section 6.3.5](#635-firstcluster-field)).

Ce champ contient l’index du premier cluster de la chaîne de cluster, comme décrit dans le FAT, qui héberge la table de cas.

#### <a name="724-datalength-field"></a>7.2.4 champ DataLength

Le champ DataCluster doit être conforme à la définition fournie dans le modèle DirectoryEntry principal générique (voir la [section 6.3.6](#636-datalength-field)).

#### <a name="725-up-case-table"></a>7.2.5-table de cas

Une table de cas est une série de mappages de caractères Unicode. Un mappage de caractères se compose d’un champ de 2 octets, avec l’index du champ dans la table de cas, qui représente le caractère Unicode à faire figurer, et le champ de 2 octets représentant le caractère Unicode en cours.

Les 128 premiers caractères Unicode ont des mappages obligatoires (voir le [tableau 24](#table-24-mandatory-first-128-up-case-table-entries)).
Une table de cas qui a un autre mappage de caractères pour l’un des 128 premiers caractères Unicode n’est pas valide.

Les implémentations qui ne prennent en charge que les caractères de la plage de mappage obligatoire peuvent ignorer les mappages du reste de la table de cas. Ces implémentations utilisent uniquement des caractères de la plage de mappage obligatoire lors de la création ou de la modification des noms de fichiers (via l’entrée de répertoire de nom de fichier, consultez la [Section 7,7](#77-file-name-directory-entry)). Lors de la mise en majuscule des noms de fichiers existants, ces implémentations ne doivent pas respecter les caractères de la plage de mappage non obligatoire, mais les laissent intactes dans le nom de fichier résultant (il s’agit d’une casse partielle). Lors de la comparaison des noms de fichiers, ces implémentations traitent les noms de fichiers qui diffèrent du nom sous la comparaison uniquement par les caractères Unicode de la plage de mappage non obligatoire comme équivalent. Bien que ces noms de fichiers soient uniquement équivalents, ces implémentations ne peuvent pas garantir que le nom de fichier entièrement en fonction de la casse n’entre pas en conflit avec le nom sous la comparaison.

<div id="table-24-mandatory-first-128-up-case-table-entries" />

**Tableau 24 premières entrées de table de cas de première 128 obligatoires**

| Index de table | + 0 | + 1 | + 2 | + 3 | + 4 | + 5 | + 6 | + 7 |
|-----------------|-------------------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|
| **0000h**       | 0000h             | 0001h     | 0002h     | 0003h     | 0004h     | 0005h     | 0006h     | 0007h     |
| **0008h**       | 0008h             | 0009h     | 000Ah     | 000Bh     | 000Ch     | 000Dh     | 000Eh     | 000Fh     |
| **0010h**       | 0010h             | 0011h     | 0012h     | 0013h     | 0014h     | 0015h     | 0016h     | 0017h     |
| **0018h**       | 0018h             | 0019h     | 001Ah     | 001Bh     | 001Ch     | 001Dh     | 001Eh     | 001Fh     |
| **0020h**       | 0020h             | 0021h     | 0022h     | 0023h     | 0024h     | 0025h     | 0026h     | 0027h     |
| **0028h**       | 0028h             | 0029h     | 002Ah     | 002Bh     | 002Ch     | 002Dh     | 002Eh     | 002Fh     |
| **0030h**       | 0030h             | 0031h     | 0032h     | 0033h     | 0034h     | 0035h     | 0036h     | 0037h     |
| **0038h**       | 0038h             | 0039h     | 003Ah     | 003Bh     | 003Ch     | 003Dh     | 003Eh     | 003Fh     |
| **0040h**       | 0040h             | 0041h     | 0042h     | 0043h     | 0044h     | 0045h     | 0046h     | 0047h     |
| **0048h**       | 0048h             | 0049h     | 004Ah     | 004Bh     | 004Ch     | 004Dh     | 004Eh     | 004Fh     |
| **0050h**       | 0050h             | 0051h     | 0052h     | 0053h     | 0054h     | 0055h     | 0056h     | 0057h     |
| **0058h**       | 0058h             | 0059h     | 005Ah     | 005Bh     | 005Ch     | 005Dh     | 005Eh     | 005Fh     |
| **0060h**       | 0060h             | **0041h** | **0042h** | **0043h** | **0044h** | **0045h** | **0046h** | **0047h** |
| **0068h**       | **0048h**         | **0049h** | **004Ah** | **004Bh** | **004Ch** | **004Dh** | **004Eh** | **004Fh** |
| **0070h**       | **0050h**         | **0051h** | **0052h** | **0053h** | **0054h** | **0055h** | **0056h** | **0057h** |
| **0078h**       | **0058h**         | **0059h** | **005Ah** | 007Bh     | 007Ch     | 007Dh     | 007Eh     | 007Fh     |

**(Remarque : les entrées avec des mappages de cas de non-identité sont en gras)**

Lors de la mise en forme d’un volume, les implémentations peuvent générer une table de cas dans un format compressé à l’aide de la compression de mappage d’identité, car une grande partie de l’espace de caractères Unicode n’a pas de concept de casse (ce qui signifie que les caractères minuscules et majuscules sont équivalents).
Les implémentations compressent une table de cas en représentant une série de mappages d’identité avec la valeur FFFFh suivi du nombre de mappages d’identité.

Par exemple, une implémentation peut représenter les premiers mappages de caractères 100 (64h) avec les huit entrées suivantes d’une table de cas compressée :

> FFFFh, 0061h, 0041h, 0042h, 0043h

Les deux premières entrées indiquent que les 97 premiers caractères (61h) (de 0000h à 0060h) ont des mappages d’identité. Les caractères suivants, 0061h à 0063h, sont mappés aux caractères 0041h à 0043h, respectivement.

La possibilité de fournir une table de cas compressée lors de la mise en forme d’un volume est facultative. Toutefois, la possibilité d’interpréter à la fois une table non compressée et une table de cas compressée est obligatoire. La valeur du champ TableChecksum est toujours conforme à la façon dont la table de cas existe sur le volume, qui peut être au format compressé ou non compressé.

##### <a name="7251-recommended-up-case-table"></a>7.2.5.1, table de cas recommandée

Lors de la mise en forme d’un volume, les implémentations doivent enregistrer la table de cas recommandée au format compressé (voir le [tableau 25](#table-25-recommended-up-case-table-in-compressed-format)), pour lequel la valeur du champ TableChecksum est E619D30Dh.

Si une implémentation définit sa propre table de cas, compressée ou non, cette table couvre la plage de caractères Unicode complète (des codes de caractères 0000h à FFFFh inclus).

<div id="table-25-recommended-up-case-table-in-compressed-format" />

**Tableau 25 : table de cas recommandée au format compressé**

| Décalage brut | + 0 |  + 1       |  + 2       |  + 3       |  + 4       | + 5        |  + 6       | + 7        |
|----------------|------------------------------|---------|---------|---------|---------|---------|---------|---------|
| **0000h**      | 0000h                        | 0001h   | 0002h   | 0003h   | 0004h   | 0005h   | 0006h   | 0007h   |
| **0008h**      | 0008h                        | 0009h   | 000Ah   | 000Bh   | 000Ch   | 000Dh   | 000Eh   | 000Fh   |
| **0010h**      | 0010h                        | 0011h   | 0012h   | 0013h   | 0014h   | 0015h   | 0016h   | 0017h   |
| **0018h**      | 0018h                        | 0019h   | 001Ah   | 001Bh   | 001Ch   | 001Dh   | 001Eh   | 001Fh   |
| **0020h**      | 0020h                        | 0021h   | 0022h   | 0023h   | 0024h   | 0025h   | 0026h   | 0027h   |
| **0028h**      | 0028h                        | 0029h   | 002Ah   | 002Bh   | 002Ch   | 002Dh   | 002Eh   | 002Fh   |
| **0030h**      | 0030h                        | 0031h   | 0032h   | 0033h   | 0034h   | 0035h   | 0036h   | 0037h   |
| **0038h**      | 0038h                        | 0039h   | 003Ah   | 003Bh   | 003Ch   | 003Dh   | 003Eh   | 003Fh   |
| **0040h**      | 0040h                        | 0041h   | 0042h   | 0043h   | 0044h   | 0045h   | 0046h   | 0047h   |
| **0048h**      | 0048h                        | 0049h   | 004Ah   | 004Bh   | 004Ch   | 004Dh   | 004Eh   | 004Fh   |
| **0050h**      | 0050h                        | 0051h   | 0052h   | 0053h   | 0054h   | 0055h   | 0056h   | 0057h   |
| **0058h**      | 0058h                        | 0059h   | 005Ah   | 005Bh   | 005Ch   | 005Dh   | 005Eh   | 005Fh   |
| **0060h**      | 0060h                        | 0041h   | 0042h   | 0043h   | 0044h   | 0045h   | 0046h   | 0047h   |
| **0068h**      | 0048h                        | 0049h   | 004Ah   | 004Bh   | 004Ch   | 004Dh   | 004Eh   | 004Fh   |
| **0070h**      | 0050h                        | 0051h   | 0052h   | 0053h   | 0054h   | 0055h   | 0056h   | 0057h   |
| **0078h**      | 0058h                        | 0059h   | 005Ah   | 007Bh   | 007Ch   | 007Dh   | 007Eh   | 007Fh   |
| **0080h**      | 0080h                        | 0081h   | 0082h   | 0083h   | 0084h   | 0085h   | 0086h   | 0087h   |
| **0088h**      | 0088h                        | 0089h   | 008Ah   | 008Bh   | 008Ch   | 008Dh   | 008Eh   | 008Fh   |
| **0090h**      | 0090h                        | 0091h   | 0092h   | 0093h   | 0094h   | 0095h   | 0096h   | 0097h   |
| **0098h**      | 0098h                        | 0099h   | 009Ah   | 009Bh   | 009Ch   | 009Dh   | 009Eh   | 009Fh   |
| **00A0h**      | 00A0h                        | 00A1h   | 00A2h   | 00A3h   | 00A4h   | 00A5h   | 00A6h   | 00A7h   |
| **00A8h**      | 00A8h                        | 00A9h   | 00AAh   | 00ABh   | 00ACh   | 00ADh   | 00AEh   | 00AFh   |
| **00B0h**      | 00B0h                        | 00B1h   | 00B2h   | 00B3h   | 00B4h   | 00B5h   | 00B6h   | 00B7h   |
| **00B8h**      | 00B8h                        | 00B9h   | 00BAh   | 00BBh   | 00BCh   | 00BDh   | 00BEh   | 00BFh   |
| **00C0h**      | 00C0h                        | 00C1h   | 00C2h   | 00C3h   | 00C4h   | 00C5h   | 00C6h   | 00C7h   |
| **00C8h**      | 00C8h                        | 00C9h   | 00CAh   | 00CBh   | 00CCh   | 00CDh   | 00CEh   | 00CFh   |
| **00D0h**      | 00D0h                        | 00D1h   | 00D2h   | 00D3h   | 00D4h   | 00D5h   | 00D6h   | 00D7h   |
| **00D8h**      | 00D8h                        | 00D9h   | 00DAh   | 00DBh   | 00DCh   | 00DDh   | 00DEh   | 00DFh   |
| **00E0h**      | 00C0h                        | 00C1h   | 00C2h   | 00C3h   | 00C4h   | 00C5h   | 00C6h   | 00C7h   |
| **00E8h**      | 00C8h                        | 00C9h   | 00CAh   | 00CBh   | 00CCh   | 00CDh   | 00CEh   | 00CFh   |
| **00F0h**      | 00D0h                        | 00D1h   | 00D2h   | 00D3h   | 00D4h   | 00D5h   | 00D6h   | 00F7h   |
| **00F8h**      | 00D8h                        | 00D9h   | 00DAh   | 00DBh   | 00DCh   | 00DDh   | 00DEh   | 0178h   |
| **0100h**      | 0100h                        | 0100h   | 0102h   | 0102h   | 0104h   | 0104h   | 0106h   | 0106h   |
| **0108h**      | 0108h                        | 0108h   | 010Ah   | 010Ah   | 010Ch   | 010Ch   | 010Eh   | 010Eh   |
| **0110h**      | 0110h                        | 0110h   | 0112h   | 0112h   | 0114h   | 0114h   | 0116h   | 0116h   |
| **0118h**      | 0118h                        | 0118h   | 011Ah   | 011Ah   | 011Ch   | 011Ch   | 011Eh   | 011Eh   |
| **0120h**      | 0120h                        | 0120h   | 0122h   | 0122h   | 0124h   | 0124h   | 0126h   | 0126h   |
| **0128h**      | 0128h                        | 0128h   | 012Ah   | 012Ah   | 012Ch   | 012Ch   | 012Eh   | 012Eh   |
| **0130h**      | 0130h                        | 0131h   | 0132h   | 0132h   | 0134h   | 0134h   | 0136h   | 0136h   |
| **0138h**      | 0138h                        | 0139h   | 0139h   | 013Bh   | 013Bh   | 013Dh   | 013Dh   | 013Fh   |
| **0140h**      | 013Fh                        | 0141h   | 0141h   | 0143h   | 0143h   | 0145h   | 0145h   | 0147h   |
| **0148h**      | 0147h                        | 0149h   | 014Ah   | 014Ah   | 014Ch   | 014Ch   | 014Eh   | 014Eh   |
| **0150h**      | 0150h                        | 0150h   | 0152h   | 0152h   | 0154h   | 0154h   | 0156h   | 0156h   |
| **0158h**      | 0158h                        | 0158h   | 015Ah   | 015Ah   | 015Ch   | 015Ch   | 015Eh   | 015Eh   |
| **0160h**      | 0160h                        | 0160h   | 0162h   | 0162h   | 0164h   | 0164h   | 0166h   | 0166h   |
| **0168h**      | 0168h                        | 0168h   | 016Ah   | 016Ah   | 016Ch   | 016Ch   | 016Eh   | 016Eh   |
| **0170h**      | 0170h                        | 0170h   | 0172h   | 0172h   | 0174h   | 0174h   | 0176h   | 0176h   |
| **0178h**      | 0178h                        | 0179h   | 0179h   | 017Bh   | 017Bh   | 017Dh   | 017Dh   | 017Fh   |
| **0180h**      | 0243h                        | 0181h   | 0182h   | 0182h   | 0184h   | 0184h   | 0186h   | 0187h   |
| **0188h**      | 0187h                        | 0189h   | 018Ah   | 018Bh   | 018Bh   | 018Dh   | 018Eh   | 018Fh   |
| **0190h**      | 0190h                        | 0191h   | 0191h   | 0193h   | 0194h   | 01F6h   | 0196h   | 0197h   |
| **0198h**      | 0198h                        | 0198h   | 023Dh   | 019Bh   | 019Ch   | 019Dh   | 0220h   | 019Fh   |
| **01A0h**      | 01A0h                        | 01A0h   | 01A2h   | 01A2h   | 01A4h   | 01A4h   | 01A6h   | 01A7h   |
| **01A8h**      | 01A7h                        | 01A9h   | 01AAh   | 01ABh   | 01ACh   | 01ACh   | 01AEh   | 01AFh   |
| **01B0h**      | 01AFh                        | 01B1h   | 01B2h   | 01B3h   | 01B3h   | 01B5h   | 01B5h   | 01B7h   |
| **01B8h**      | 01B8h                        | 01B8h   | 01BAh   | 01BBh   | 01BCh   | 01BCh   | 01BEh   | 01F7h   |
| **01C0h**      | 01C0h                        | 01C1h   | 01C2h   | 01C3h   | 01C4h   | 01C5h   | 01C4h   | 01C7h   |
| **01C8h**      | 01C8h                        | 01C7h   | 01CAh   | 01CBh   | 01CAh   | 01CDh   | 01CDh   | 01CFh   |
| **01D0h**      | 01CFh                        | 01D1h   | 01D1h   | 01D3h   | 01D3h   | 01D5h   | 01D5h   | 01D7h   |
| **01D8h**      | 01D7h                        | 01D9h   | 01D9h   | 01DBh   | 01DBh   | 018Eh   | 01DEh   | 01DEh   |
| **01E0h**      | 01E0h                        | 01E0h   | 01E2h   | 01E2h   | 01E4h   | 01E4h   | 01E6h   | 01E6h   |
| **01E8h**      | 01E8h                        | 01E8h   | 01EAh   | 01EAh   | 01ECh   | 01ECh   | 01EEh   | 01EEh   |
| **01F0h**      | 01F0h                        | 01F1h   | 01F2h   | 01F1h   | 01F4h   | 01F4h   | 01F6h   | 01F7h   |
| **01F8h**      | 01F8h                        | 01F8h   | 01FAh   | 01FAh   | 01FCh   | 01FCh   | 01FEh   | 01FEh   |
| **0200h**      | 0200h                        | 0200h   | 0202h   | 0202h   | 0204h   | 0204h   | 0206h   | 0206h   |
| **0208h**      | 0208h                        | 0208h   | 020Ah   | 020Ah   | 020Ch   | 020Ch   | 020Eh   | 020Eh   |
| **0210h**      | 0210h                        | 0210h   | 0212h   | 0212h   | 0214h   | 0214h   | 0216h   | 0216h   |
| **0218h**      | 0218h                        | 0218h   | 021Ah   | 021Ah   | 021Ch   | 021Ch   | 021Eh   | 021Eh   |
| **0220h**      | 0220h                        | 0221h   | 0222h   | 0222h   | 0224h   | 0224h   | 0226h   | 0226h   |
| **0228h**      | 0228h                        | 0228h   | 022Ah   | 022Ah   | 022Ch   | 022Ch   | 022Eh   | 022Eh   |
| **0230h**      | 0230h                        | 0230h   | 0232h   | 0232h   | 0234h   | 0235h   | 0236h   | 0237h   |
| **0238h**      | 0238h                        | 0239h   | 2C65h   | 023Bh   | 023Bh   | 023Dh   | 2C66h   | 023Fh   |
| **0240h**      | 0240h                        | 0241h   | 0241h   | 0243h   | 0244h   | 0245h   | 0246h   | 0246h   |
| **0248h**      | 0248h                        | 0248h   | 024Ah   | 024Ah   | 024Ch   | 024Ch   | 024Eh   | 024Eh   |
| **0250h**      | 0250h                        | 0251h   | 0252h   | 0181h   | 0186h   | 0255h   | 0189h   | 018Ah   |
| **0258h**      | 0258h                        | 018Fh   | 025Ah   | 0190h   | 025Ch   | 025Dh   | 025Eh   | 025Fh   |
| **0260h**      | 0193h                        | 0261h   | 0262h   | 0194h   | 0264h   | 0265h   | 0266h   | 0267h   |
| **0268h**      | 0197h                        | 0196h   | 026Ah   | 2C62h   | 026Ch   | 026Dh   | 026Eh   | 019Ch   |
| **0270h**      | 0270h                        | 0271h   | 019Dh   | 0273h   | 0274h   | 019Fh   | 0276h   | 0277h   |
| **0278h**      | 0278h                        | 0279h   | 027Ah   | 027Bh   | 027Ch   | 2C64h   | 027Eh   | 027Fh   |
| **0280h**      | 01A6h                        | 0281h   | 0282h   | 01A9h   | 0284h   | 0285h   | 0286h   | 0287h   |
| **0288h**      | 01AEh                        | 0244h   | 01B1h   | 01B2h   | 0245h   | 028Dh   | 028Eh   | 028Fh   |
| **0290h**      | 0290h                        | 0291h   | 01B7h   | 0293h   | 0294h   | 0295h   | 0296h   | 0297h   |
| **0298h**      | 0298h                        | 0299h   | 029Ah   | 029Bh   | 029Ch   | 029Dh   | 029Eh   | 029Fh   |
| **02A0h**      | 02A0h                        | 02A1h   | 02A2h   | 02A3h   | 02A4h   | 02A5h   | 02A6h   | 02A7h   |
| **02A8h**      | 02A8h                        | 02A9h   | 02AAh   | 02ABh   | 02ACh   | 02ADh   | 02AEh   | 02AFh   |
| **02B0h**      | 02B0h                        | 02B1h   | 02B2h   | 02B3h   | 02B4h   | 02B5h   | 02B6h   | 02B7h   |
| **02B8h**      | 02B8h                        | 02B9h   | 02BAh   | 02BBh   | 02BCh   | 02BDh   | 02BEh   | 02BFh   |
| **02C0h**      | 02C0h                        | 02C1h   | 02C2h   | 02C3h   | 02C4h   | 02C5h   | 02C6h   | 02C7h   |
| **02C8h**      | 02C8h                        | 02C9h   | 02CAh   | 02CBh   | 02CCh   | 02CDh   | 02CEh   | 02CFh   |
| **02D0h**      | 02D0h                        | 02D1h   | 02D2h   | 02D3h   | 02D4h   | 02D5h   | 02D6h   | 02D7h   |
| **02D8h**      | 02D8h                        | 02D9h   | 02DAh   | 02DBh   | 02DCh   | 02DDh   | 02DEh   | 02DFh   |
| **02E0h**      | 02E0h                        | 02E1h   | 02E2h   | 02E3h   | 02E4h   | 02E5h   | 02E6h   | 02E7h   |
| **02E8h**      | 02E8h                        | 02E9h   | 02EAh   | 02EBh   | 02ECh   | 02EDh   | 02EEh   | 02EFh   |
| **02F0h**      | 02F0h                        | 02F1h   | 02F2h   | 02F3h   | 02F4h   | 02F5h   | 02F6h   | 02F7h   |
| **02F8h**      | 02F8h                        | 02F9h   | 02FAh   | 02FBh   | 02FCh   | 02FDh   | 02FEh   | 02FFh   |
| **0300h**      | 0300h                        | 0301h   | 0302h   | 0303h   | 0304h   | 0305h   | 0306h   | 0307h   |
| **0308h**      | 0308h                        | 0309h   | 030Ah   | 030Bh   | 030Ch   | 030Dh   | 030Eh   | 030Fh   |
| **0310h**      | 0310h                        | 0311h   | 0312h   | 0313h   | 0314h   | 0315h   | 0316h   | 0317h   |
| **0318h**      | 0318h                        | 0319h   | 031Ah   | 031Bh   | 031Ch   | 031Dh   | 031Eh   | 031Fh   |
| **0320h**      | 0320h                        | 0321h   | 0322h   | 0323h   | 0324h   | 0325h   | 0326h   | 0327h   |
| **0328h**      | 0328h                        | 0329h   | 032Ah   | 032Bh   | 032Ch   | 032Dh   | 032Eh   | 032Fh   |
| **0330h**      | 0330h                        | 0331h   | 0332h   | 0333h   | 0334h   | 0335h   | 0336h   | 0337h   |
| **0338h**      | 0338h                        | 0339h   | 033Ah   | 033Bh   | 033Ch   | 033Dh   | 033Eh   | 033Fh   |
| **0340h**      | 0340h                        | 0341h   | 0342h   | 0343h   | 0344h   | 0345h   | 0346h   | 0347h   |
| **0348h**      | 0348h                        | 0349h   | 034Ah   | 034Bh   | 034Ch   | 034Dh   | 034Eh   | 034Fh   |
| **0350h**      | 0350h                        | 0351h   | 0352h   | 0353h   | 0354h   | 0355h   | 0356h   | 0357h   |
| **0358h**      | 0358h                        | 0359h   | 035Ah   | 035Bh   | 035Ch   | 035Dh   | 035Eh   | 035Fh   |
| **0360h**      | 0360h                        | 0361h   | 0362h   | 0363h   | 0364h   | 0365h   | 0366h   | 0367h   |
| **0368h**      | 0368h                        | 0369h   | 036Ah   | 036Bh   | 036Ch   | 036Dh   | 036Eh   | 036Fh   |
| **0370h**      | 0370h                        | 0371h   | 0372h   | 0373h   | 0374h   | 0375h   | 0376h   | 0377h   |
| **0378h**      | 0378h                        | 0379h   | 037Ah   | 03FDh   | 03FEh   | 03FFh   | 037Eh   | 037Fh   |
| **0380h**      | 0380h                        | 0381h   | 0382h   | 0383h   | 0384h   | 0385h   | 0386h   | 0387h   |
| **0388h**      | 0388h                        | 0389h   | 038Ah   | 038Bh   | 038Ch   | 038Dh   | 038Eh   | 038Fh   |
| **0390h**      | 0390h                        | 0391h   | 0392h   | 0393h   | 0394h   | 0395h   | 0396h   | 0397h   |
| **0398h**      | 0398h                        | 0399h   | 039Ah   | 039Bh   | 039Ch   | 039Dh   | 039Eh   | 039Fh   |
| **03A0h**      | 03A0h                        | 03A1h   | 03A2h   | 03A3h   | 03A4h   | 03A5h   | 03A6h   | 03A7h   |
| **03A8h**      | 03A8h                        | 03A9h   | 03AAh   | 03ABh   | 0386h   | 0388h   | 0389h   | 038Ah   |
| **03B0h**      | 03B0h                        | 0391h   | 0392h   | 0393h   | 0394h   | 0395h   | 0396h   | 0397h   |
| **03B8h**      | 0398h                        | 0399h   | 039Ah   | 039Bh   | 039Ch   | 039Dh   | 039Eh   | 039Fh   |
| **03C0h**      | 03A0h                        | 03A1h   | 03A3h   | 03A3h   | 03A4h   | 03A5h   | 03A6h   | 03A7h   |
| **03C8h**      | 03A8h                        | 03A9h   | 03AAh   | 03ABh   | 038Ch   | 038Eh   | 038Fh   | 03CFh   |
| **03D0h**      | 03D0h                        | 03D1h   | 03D2h   | 03D3h   | 03D4h   | 03D5h   | 03D6h   | 03D7h   |
| **03D8h**      | 03D8h                        | 03D8h   | 03DAh   | 03DAh   | 03DCh   | 03DCh   | 03DEh   | 03DEh   |
| **03E0h**      | 03E0h                        | 03E0h   | 03E2h   | 03E2h   | 03E4h   | 03E4h   | 03E6h   | 03E6h   |
| **03E8h**      | 03E8h                        | 03E8h   | 03EAh   | 03EAh   | 03ECh   | 03ECh   | 03EEh   | 03EEh   |
| **03F0h**      | 03F0h                        | 03F1h   | 03F9h   | 03F3h   | 03F4h   | 03F5h   | 03F6h   | 03F7h   |
| **03F8h**      | 03F7h                        | 03F9h   | 03FAh   | 03FAh   | 03FCh   | 03FDh   | 03FEh   | 03FFh   |
| **0400h**      | 0400h                        | 0401h   | 0402h   | 0403h   | 0404h   | 0405h   | 0406h   | 0407h   |
| **0408h**      | 0408h                        | 0409h   | 040Ah   | 040Bh   | 040Ch   | 040Dh   | 040Eh   | 040Fh   |
| **0410h**      | 0410h                        | 0411h   | 0412h   | 0413h   | 0414h   | 0415h   | 0416h   | 0417h   |
| **0418h**      | 0418h                        | 0419h   | 041Ah   | 041Bh   | 041Ch   | 041Dh   | 041Eh   | 041Fh   |
| **0420h**      | 0420h                        | 0421h   | 0422h   | 0423h   | 0424h   | 0425h   | 0426h   | 0427h   |
| **0428h**      | 0428h                        | 0429h   | 042Ah   | 042Bh   | 042Ch   | 042Dh   | 042Eh   | 042Fh   |
| **0430h**      | 0410h                        | 0411h   | 0412h   | 0413h   | 0414h   | 0415h   | 0416h   | 0417h   |
| **0438h**      | 0418h                        | 0419h   | 041Ah   | 041Bh   | 041Ch   | 041Dh   | 041Eh   | 041Fh   |
| **0440h**      | 0420h                        | 0421h   | 0422h   | 0423h   | 0424h   | 0425h   | 0426h   | 0427h   |
| **0448h**      | 0428h                        | 0429h   | 042Ah   | 042Bh   | 042Ch   | 042Dh   | 042Eh   | 042Fh   |
| **0450h**      | 0400h                        | 0401h   | 0402h   | 0403h   | 0404h   | 0405h   | 0406h   | 0407h   |
| **0458h**      | 0408h                        | 0409h   | 040Ah   | 040Bh   | 040Ch   | 040Dh   | 040Eh   | 040Fh   |
| **0460h**      | 0460h                        | 0460h   | 0462h   | 0462h   | 0464h   | 0464h   | 0466h   | 0466h   |
| **0468h**      | 0468h                        | 0468h   | 046Ah   | 046Ah   | 046Ch   | 046Ch   | 046Eh   | 046Eh   |
| **0470h**      | 0470h                        | 0470h   | 0472h   | 0472h   | 0474h   | 0474h   | 0476h   | 0476h   |
| **0478h**      | 0478h                        | 0478h   | 047Ah   | 047Ah   | 047Ch   | 047Ch   | 047Eh   | 047Eh   |
| **0480h**      | 0480h                        | 0480h   | 0482h   | 0483h   | 0484h   | 0485h   | 0486h   | 0487h   |
| **0488h**      | 0488h                        | 0489h   | 048Ah   | 048Ah   | 048Ch   | 048Ch   | 048Eh   | 048Eh   |
| **0490h**      | 0490h                        | 0490h   | 0492h   | 0492h   | 0494h   | 0494h   | 0496h   | 0496h   |
| **0498h**      | 0498h                        | 0498h   | 049Ah   | 049Ah   | 049Ch   | 049Ch   | 049Eh   | 049Eh   |
| **04A0h**      | 04A0h                        | 04A0h   | 04A2h   | 04A2h   | 04A4h   | 04A4h   | 04A6h   | 04A6h   |
| **04A8h**      | 04A8h                        | 04A8h   | 04AAh   | 04AAh   | 04ACh   | 04ACh   | 04AEh   | 04AEh   |
| **04B0h**      | 04B0h                        | 04B0h   | 04B2h   | 04B2h   | 04B4h   | 04B4h   | 04B6h   | 04B6h   |
| **04B8h**      | 04B8h                        | 04B8h   | 04BAh   | 04BAh   | 04BCh   | 04BCh   | 04BEh   | 04BEh   |
| **04C0h**      | 04C0h                        | 04C1h   | 04C1h   | 04C3h   | 04C3h   | 04C5h   | 04C5h   | 04C7h   |
| **04C8h**      | 04C7h                        | 04C9h   | 04C9h   | 04CBh   | 04CBh   | 04CDh   | 04CDh   | 04C0h   |
| **04D0h**      | 04D0h                        | 04D0h   | 04D2h   | 04D2h   | 04D4h   | 04D4h   | 04D6h   | 04D6h   |
| **04D8h**      | 04D8h                        | 04D8h   | 04DAh   | 04DAh   | 04DCh   | 04DCh   | 04DEh   | 04DEh   |
| **04E0h**      | 04E0h                        | 04E0h   | 04E2h   | 04E2h   | 04E4h   | 04E4h   | 04E6h   | 04E6h   |
| **04E8h**      | 04E8h                        | 04E8h   | 04EAh   | 04EAh   | 04ECh   | 04ECh   | 04EEh   | 04EEh   |
| **04F0h**      | 04F0h                        | 04F0h   | 04F2h   | 04F2h   | 04F4h   | 04F4h   | 04F6h   | 04F6h   |
| **04F8h**      | 04F8h                        | 04F8h   | 04FAh   | 04FAh   | 04FCh   | 04FCh   | 04FEh   | 04FEh   |
| **0500h**      | 0500h                        | 0500h   | 0502h   | 0502h   | 0504h   | 0504h   | 0506h   | 0506h   |
| **0508h**      | 0508h                        | 0508h   | 050Ah   | 050Ah   | 050Ch   | 050Ch   | 050Eh   | 050Eh   |
| **0510h**      | 0510h                        | 0510h   | 0512h   | 0512h   | 0514h   | 0515h   | 0516h   | 0517h   |
| **0518h**      | 0518h                        | 0519h   | 051Ah   | 051Bh   | 051Ch   | 051Dh   | 051Eh   | 051Fh   |
| **0520h**      | 0520h                        | 0521h   | 0522h   | 0523h   | 0524h   | 0525h   | 0526h   | 0527h   |
| **0528h**      | 0528h                        | 0529h   | 052Ah   | 052Bh   | 052Ch   | 052Dh   | 052Eh   | 052Fh   |
| **0530h**      | 0530h                        | 0531h   | 0532h   | 0533h   | 0534h   | 0535h   | 0536h   | 0537h   |
| **0538h**      | 0538h                        | 0539h   | 053Ah   | 053Bh   | 053Ch   | 053Dh   | 053Eh   | 053Fh   |
| **0540h**      | 0540h                        | 0541h   | 0542h   | 0543h   | 0544h   | 0545h   | 0546h   | 0547h   |
| **0548h**      | 0548h                        | 0549h   | 054Ah   | 054Bh   | 054Ch   | 054Dh   | 054Eh   | 054Fh   |
| **0550h**      | 0550h                        | 0551h   | 0552h   | 0553h   | 0554h   | 0555h   | 0556h   | 0557h   |
| **0558h**      | 0558h                        | 0559h   | 055Ah   | 055Bh   | 055Ch   | 055Dh   | 055Eh   | 055Fh   |
| **0560h**      | 0560h                        | 0531h   | 0532h   | 0533h   | 0534h   | 0535h   | 0536h   | 0537h   |
| **0568h**      | 0538h                        | 0539h   | 053Ah   | 053Bh   | 053Ch   | 053Dh   | 053Eh   | 053Fh   |
| **0570h**      | 0540h                        | 0541h   | 0542h   | 0543h   | 0544h   | 0545h   | 0546h   | 0547h   |
| **0578h**      | 0548h                        | 0549h   | 054Ah   | 054Bh   | 054Ch   | 054Dh   | 054Eh   | 054Fh   |
| **0580h**      | 0550h                        | 0551h   | 0552h   | 0553h   | 0554h   | 0555h   | 0556h   | FFFFh   |
| **0588h**      | 17F6h                        | 2C63h   | 1D7Eh   | 1D7Fh   | 1D80h   | 1D81h   | 1D82h   | 1D83h   |
| **0590h**      | 1D84h                        | 1D85h   | 1D86h   | 1D87h   | 1D88h   | 1D89h   | 1D8Ah   | 1D8Bh   |
| **0598h**      | 1D8Ch                        | 1D8Dh   | 1D8Eh   | 1D8Fh   | 1D90h   | 1D91h   | 1D92h   | 1D93h   |
| **05A0h**      | 1D94h                        | 1D95h   | 1D96h   | 1D97h   | 1D98h   | 1D99h   | 1D9Ah   | 1D9Bh   |
| **05A8h**      | 1D9Ch                        | 1D9Dh   | 1D9Eh   | 1D9Fh   | 1DA0h   | 1DA1h   | 1DA2h   | 1DA3h   |
| **05B0h**      | 1DA4h                        | 1DA5h   | 1DA6h   | 1DA7h   | 1DA8h   | 1DA9h   | 1DAAh   | 1DABh   |
| **05B8h**      | 1DACh                        | 1DADh   | 1DAEh   | 1DAFh   | 1DB0h   | 1DB1h   | 1DB2h   | 1DB3h   |
| **05C0h**      | 1DB4h                        | 1DB5h   | 1DB6h   | 1DB7h   | 1DB8h   | 1DB9h   | 1DBAh   | 1DBBh   |
| **05C8h**      | 1DBCh                        | 1DBDh   | 1DBEh   | 1DBFh   | 1DC0h   | 1DC1h   | 1DC2h   | 1DC3h   |
| **05D0h**      | 1DC4h                        | 1DC5h   | 1DC6h   | 1DC7h   | 1DC8h   | 1DC9h   | 1DCAh   | 1DCBh   |
| **05D8h**      | 1DCCh                        | 1DCDh   | 1DCEh   | 1DCFh   | 1DD0h   | 1DD1h   | 1DD2h   | 1DD3h   |
| **05E0h**      | 1DD4h                        | 1DD5h   | 1DD6h   | 1DD7h   | 1DD8h   | 1DD9h   | 1DDAh   | 1DDBh   |
| **05E8h**      | 1DDCh                        | 1DDDh   | 1DDEh   | 1DDFh   | 1DE0h   | 1DE1h   | 1DE2h   | 1DE3h   |
| **05F0h**      | 1DE4h                        | 1DE5h   | 1DE6h   | 1DE7h   | 1DE8h   | 1DE9h   | 1DEAh   | 1DEBh   |
| **05F8h**      | 1DECh                        | 1DEDh   | 1DEEh   | 1DEFh   | 1DF0h   | 1DF1h   | 1DF2h   | 1DF3h   |
| **0600h**      | 1DF4h                        | 1DF5h   | 1DF6h   | 1DF7h   | 1DF8h   | 1DF9h   | 1DFAh   | 1DFBh   |
| **0608h**      | 1DFCh                        | 1DFDh   | 1DFEh   | 1DFFh   | 1E00h   | 1E00h   | 1E02h   | 1E02h   |
| **0610h**      | 1E04h                        | 1E04h   | 1E06h   | 1E06h   | 1E08h   | 1E08h   | 1E0Ah   | 1E0Ah   |
| **0618h**      | 1E0Ch                        | 1E0Ch   | 1E0Eh   | 1E0Eh   | 1E10h   | 1E10h   | 1E12h   | 1E12h   |
| **0620h**      | 1E14h                        | 1E14h   | 1E16h   | 1E16h   | 1E18h   | 1E18h   | 1E1Ah   | 1E1Ah   |
| **0628h**      | 1E1Ch                        | 1E1Ch   | 1E1Eh   | 1E1Eh   | 1E20h   | 1E20h   | 1E22h   | 1E22h   |
| **0630h**      | 1E24h                        | 1E24h   | 1E26h   | 1E26h   | 1E28h   | 1E28h   | 1E2Ah   | 1E2Ah   |
| **0638h**      | 1E2Ch                        | 1E2Ch   | 1E2Eh   | 1E2Eh   | 1E30h   | 1E30h   | 1E32h   | 1E32h   |
| **0640h**      | 1E34h                        | 1E34h   | 1E36h   | 1E36h   | 1E38h   | 1E38h   | 1E3Ah   | 1E3Ah   |
| **0648h**      | 1E3Ch                        | 1E3Ch   | 1E3Eh   | 1E3Eh   | 1E40h   | 1E40h   | 1E42h   | 1E42h   |
| **0650h**      | 1E44h                        | 1E44h   | 1E46h   | 1E46h   | 1E48h   | 1E48h   | 1E4Ah   | 1E4Ah   |
| **0658h**      | 1E4Ch                        | 1E4Ch   | 1E4Eh   | 1E4Eh   | 1E50h   | 1E50h   | 1E52h   | 1E52h   |
| **0660h**      | 1E54h                        | 1E54h   | 1E56h   | 1E56h   | 1E58h   | 1E58h   | 1E5Ah   | 1E5Ah   |
| **0668h**      | 1E5Ch                        | 1E5Ch   | 1E5Eh   | 1E5Eh   | 1E60h   | 1E60h   | 1E62h   | 1E62h   |
| **0670h**      | 1E64h                        | 1E64h   | 1E66h   | 1E66h   | 1E68h   | 1E68h   | 1E6Ah   | 1E6Ah   |
| **0678h**      | 1E6Ch                        | 1E6Ch   | 1E6Eh   | 1E6Eh   | 1E70h   | 1E70h   | 1E72h   | 1E72h   |
| **0680h**      | 1E74h                        | 1E74h   | 1E76h   | 1E76h   | 1E78h   | 1E78h   | 1E7Ah   | 1E7Ah   |
| **0688h**      | 1E7Ch                        | 1E7Ch   | 1E7Eh   | 1E7Eh   | 1E80h   | 1E80h   | 1E82h   | 1E82h   |
| **0690h**      | 1E84h                        | 1E84h   | 1E86h   | 1E86h   | 1E88h   | 1E88h   | 1E8Ah   | 1E8Ah   |
| **0698h**      | 1E8Ch                        | 1E8Ch   | 1E8Eh   | 1E8Eh   | 1E90h   | 1E90h   | 1E92h   | 1E92h   |
| **06A0h**      | 1E94h                        | 1E94h   | 1E96h   | 1E97h   | 1E98h   | 1E99h   | 1E9Ah   | 1E9Bh   |
| **06A8h**      | 1E9Ch                        | 1E9Dh   | 1E9Eh   | 1E9Fh   | 1EA0h   | 1EA0h   | 1EA2h   | 1EA2h   |
| **06B0h**      | 1EA4h                        | 1EA4h   | 1EA6h   | 1EA6h   | 1EA8h   | 1EA8h   | 1EAAh   | 1EAAh   |
| **06B8h**      | 1EACh                        | 1EACh   | 1EAEh   | 1EAEh   | 1EB0h   | 1EB0h   | 1EB2h   | 1EB2h   |
| **06C0h**      | 1EB4h                        | 1EB4h   | 1EB6h   | 1EB6h   | 1EB8h   | 1EB8h   | 1EBAh   | 1EBAh   |
| **06C8h**      | 1EBCh                        | 1EBCh   | 1EBEh   | 1EBEh   | 1EC0h   | 1EC0h   | 1EC2h   | 1EC2h   |
| **06D0h**      | 1EC4h                        | 1EC4h   | 1EC6h   | 1EC6h   | 1EC8h   | 1EC8h   | 1ECAh   | 1ECAh   |
| **06D8h**      | 1ECCh                        | 1ECCh   | 1ECEh   | 1ECEh   | 1ED0h   | 1ED0h   | 1ED2h   | 1ED2h   |
| **06E0h**      | 1ED4h                        | 1ED4h   | 1ED6h   | 1ED6h   | 1ED8h   | 1ED8h   | 1EDAh   | 1EDAh   |
| **06E8h**      | 1EDCh                        | 1EDCh   | 1EDEh   | 1EDEh   | 1EE0h   | 1EE0h   | 1EE2h   | 1EE2h   |
| **06F0h**      | 1EE4h                        | 1EE4h   | 1EE6h   | 1EE6h   | 1EE8h   | 1EE8h   | 1EEAh   | 1EEAh   |
| **06F8h**      | 1EECh                        | 1EECh   | 1EEEh   | 1EEEh   | 1EF0h   | 1EF0h   | 1EF2h   | 1EF2h   |
| **0700h**      | 1EF4h                        | 1EF4h   | 1EF6h   | 1EF6h   | 1EF8h   | 1EF8h   | 1EFAh   | 1EFBh   |
| **0708h**      | 1EFCh                        | 1EFDh   | 1EFEh   | 1EFFh   | 1F08h   | 1F09h   | 1F0Ah   | 1F0Bh   |
| **0710h**      | 1F0Ch                        | 1F0Dh   | 1F0Eh   | 1F0Fh   | 1F08h   | 1F09h   | 1F0Ah   | 1F0Bh   |
| **0718h**      | 1F0Ch                        | 1F0Dh   | 1F0Eh   | 1F0Fh   | 1F18h   | 1F19h   | 1F1Ah   | 1F1Bh   |
| **0720h**      | 1F1Ch                        | 1F1Dh   | 1F16h   | 1F17h   | 1F18h   | 1F19h   | 1F1Ah   | 1F1Bh   |
| **0728h**      | 1F1Ch                        | 1F1Dh   | 1F1Eh   | 1F1Fh   | 1F28h   | 1F29h   | 1F2Ah   | 1F2Bh   |
| **0730h**      | 1F2Ch                        | 1F2Dh   | 1F2Eh   | 1F2Fh   | 1F28h   | 1F29h   | 1F2Ah   | 1F2Bh   |
| **0738h**      | 1F2Ch                        | 1F2Dh   | 1F2Eh   | 1F2Fh   | 1F38h   | 1F39h   | 1F3Ah   | 1F3Bh   |
| **0740h**      | 1F3Ch                        | 1F3Dh   | 1F3Eh   | 1F3Fh   | 1F38h   | 1F39h   | 1F3Ah   | 1F3Bh   |
| **0748h**      | 1F3Ch                        | 1F3Dh   | 1F3Eh   | 1F3Fh   | 1F48h   | 1F49h   | 1F4Ah   | 1F4Bh   |
| **0750h**      | 1F4Ch                        | 1F4Dh   | 1F46h   | 1F47h   | 1F48h   | 1F49h   | 1F4Ah   | 1F4Bh   |
| **0758h**      | 1F4Ch                        | 1F4Dh   | 1F4Eh   | 1F4Fh   | 1F50h   | 1F59h   | 1F52h   | 1F5Bh   |
| **0760h**      | 1F54h                        | 1F5Dh   | 1F56h   | 1F5Fh   | 1F58h   | 1F59h   | 1F5Ah   | 1F5Bh   |
| **0768h**      | 1F5Ch                        | 1F5Dh   | 1F5Eh   | 1F5Fh   | 1F68h   | 1F69h   | 1F6Ah   | 1F6Bh   |
| **0770h**      | 1F6Ch                        | 1F6Dh   | 1F6Eh   | 1F6Fh   | 1F68h   | 1F69h   | 1F6Ah   | 1F6Bh   |
| **0778h**      | 1F6Ch                        | 1F6Dh   | 1F6Eh   | 1F6Fh   | 1FBAh   | 1FBBh   | 1FC8h   | 1FC9h   |
| **0780h**      | 1FCAh                        | 1FCBh   | 1FDAh   | 1FDBh   | 1FF8h   | 1FF9h   | 1FEAh   | 1FEBh   |
| **0788h**      | 1FFAh                        | 1FFBh   | 1F7Eh   | 1F7Fh   | 1F88h   | 1F89h   | 1F8Ah   | 1F8Bh   |
| **0790h**      | 1F8Ch                        | 1F8Dh   | 1F8Eh   | 1F8Fh   | 1F88h   | 1F89h   | 1F8Ah   | 1F8Bh   |
| **0798h**      | 1F8Ch                        | 1F8Dh   | 1F8Eh   | 1F8Fh   | 1F98h   | 1F99h   | 1F9Ah   | 1F9Bh   |
| **07A0h**      | 1F9Ch                        | 1F9Dh   | 1F9Eh   | 1F9Fh   | 1F98h   | 1F99h   | 1F9Ah   | 1F9Bh   |
| **07A8h**      | 1F9Ch                        | 1F9Dh   | 1F9Eh   | 1F9Fh   | 1FA8h   | 1FA9h   | 1FAAh   | 1FABh   |
| **07B0h**      | 1FACh                        | 1FADh   | 1FAEh   | 1FAFh   | 1FA8h   | 1FA9h   | 1FAAh   | 1FABh   |
| **07B8h**      | 1FACh                        | 1FADh   | 1FAEh   | 1FAFh   | 1FB8h   | 1FB9h   | 1FB2h   | 1FBCh   |
| **07C0h**      | 1FB4h                        | 1FB5h   | 1FB6h   | 1FB7h   | 1FB8h   | 1FB9h   | 1FBAh   | 1FBBh   |
| **07C8h**      | 1FBCh                        | 1FBDh   | 1FBEh   | 1FBFh   | 1FC0h   | 1FC1h   | 1FC2h   | 1FC3h   |
| **07D0h**      | 1FC4h                        | 1FC5h   | 1FC6h   | 1FC7h   | 1FC8h   | 1FC9h   | 1FCAh   | 1FCBh   |
| **07D8h**      | 1FC3h                        | 1FCDh   | 1FCEh   | 1FCFh   | 1FD8h   | 1FD9h   | 1FD2h   | 1FD3h   |
| **07E0h**      | 1FD4h                        | 1FD5h   | 1FD6h   | 1FD7h   | 1FD8h   | 1FD9h   | 1FDAh   | 1FDBh   |
| **07E8h**      | 1FDCh                        | 1FDDh   | 1FDEh   | 1FDFh   | 1FE8h   | 1FE9h   | 1FE2h   | 1FE3h   |
| **07F0h**      | 1FE4h                        | 1FECh   | 1FE6h   | 1FE7h   | 1FE8h   | 1FE9h   | 1FEAh   | 1FEBh   |
| **07F8h**      | 1FECh                        | 1FEDh   | 1FEEh   | 1FEFh   | 1FF0h   | 1FF1h   | 1FF2h   | 1FF3h   |
| **0800h**      | 1FF4h                        | 1FF5h   | 1FF6h   | 1FF7h   | 1FF8h   | 1FF9h   | 1FFAh   | 1FFBh   |
| **0808h**      | 1FF3h                        | 1FFDh   | 1FFEh   | 1FFFh   | 2000h   | 2001h   | 2002h   | 2003h   |
| **0810h**      | 2004h                        | 2005h   | 2006h   | 2007h   | 2008h   | 2009h   | 200Ah   | 200Bh   |
| **0818h**      | 200Ch                        | 200Dh   | 200Eh   | 200Fh   | 2010h   | 2011h   | 2012h   | 2013h   |
| **0820h**      | 2014h                        | 2015h   | 2016h   | 2017h   | 2018h   | 2019h   | 201Ah   | 201Bh   |
| **0828h**      | 201Ch                        | 201Dh   | 201Eh   | 201Fh   | 2020h   | 2021h   | 2022h   | 2023h   |
| **0830h**      | 2024h                        | 2025h   | 2026h   | 2027h   | 2028h   | 2029h   | 202Ah   | 202Bh   |
| **0838h**      | 202Ch                        | 202Dh   | 202Eh   | 202Fh   | 2030h   | 2031h   | 2032h   | 2033h   |
| **0840h**      | 2034h                        | 2035h   | 2036h   | 2037h   | 2038h   | 2039h   | 203Ah   | 203Bh   |
| **0848h**      | 203Ch                        | 203Dh   | 203Eh   | 203Fh   | 2040h   | 2041h   | 2042h   | 2043h   |
| **0850h**      | 2044h                        | 2045h   | 2046h   | 2047h   | 2048h   | 2049h   | 204Ah   | 204Bh   |
| **0858h**      | 204Ch                        | 204Dh   | 204Eh   | 204Fh   | 2050h   | 2051h   | 2052h   | 2053h   |
| **0860h**      | 2054h                        | 2055h   | 2056h   | 2057h   | 2058h   | 2059h   | 205Ah   | 205Bh   |
| **0868h**      | 205Ch                        | 205Dh   | 205Eh   | 205Fh   | 2060h   | 2061h   | 2062h   | 2063h   |
| **0870h**      | 2064h                        | 2065h   | 2066h   | 2067h   | 2068h   | 2069h   | 206Ah   | 206Bh   |
| **0878h**      | 206Ch                        | 206Dh   | 206Eh   | 206Fh   | 2070h   | 2071h   | 2072h   | 2073h   |
| **0880h**      | 2074h                        | 2075h   | 2076h   | 2077h   | 2078h   | 2079h   | 207Ah   | 207Bh   |
| **0888h**      | 207Ch                        | 207Dh   | 207Eh   | 207Fh   | 2080h   | 2081h   | 2082h   | 2083h   |
| **0890h**      | 2084h                        | 2085h   | 2086h   | 2087h   | 2088h   | 2089h   | 208Ah   | 208Bh   |
| **0898h**      | 208Ch                        | 208Dh   | 208Eh   | 208Fh   | 2090h   | 2091h   | 2092h   | 2093h   |
| **08A0h**      | 2094h                        | 2095h   | 2096h   | 2097h   | 2098h   | 2099h   | 209Ah   | 209Bh   |
| **08A8h**      | 209Ch                        | 209Dh   | 209Eh   | 209Fh   | 20A0h   | 20A1h   | 20A2h   | 20A3h   |
| **08B0h**      | 20A4h                        | 20A5h   | 20A6h   | 20A7h   | 20A8h   | 20A9h   | 20AAh   | 20ABh   |
| **08B8h**      | 20ACh                        | 20ADh   | 20AEh   | 20AFh   | 20B0h   | 20B1h   | 20B2h   | 20B3h   |
| **08C0h**      | 20B4h                        | 20B5h   | 20B6h   | 20B7h   | 20B8h   | 20B9h   | 20BAh   | 20BBh   |
| **08C8h**      | 20BCh                        | 20BDh   | 20BEh   | 20BFh   | 20C0h   | 20C1h   | 20C2h   | 20C3h   |
| **08D0h**      | 20C4h                        | 20C5h   | 20C6h   | 20C7h   | 20C8h   | 20C9h   | 20CAh   | 20CBh   |
| **08D8h**      | 20CCh                        | 20CDh   | 20CEh   | 20CFh   | 20D0h   | 20D1h   | 20D2h   | 20D3h   |
| **08E0h**      | 20D4h                        | 20D5h   | 20D6h   | 20D7h   | 20D8h   | 20D9h   | 20DAh   | 20DBh   |
| **08E8h**      | 20DCh                        | 20DDh   | 20DEh   | 20DFh   | 20E0h   | 20E1h   | 20E2h   | 20E3h   |
| **08F0h**      | 20E4h                        | 20E5h   | 20E6h   | 20E7h   | 20E8h   | 20E9h   | 20EAh   | 20EBh   |
| **08F8h**      | 20ECh                        | 20EDh   | 20EEh   | 20EFh   | 20F0h   | 20F1h   | 20F2h   | 20F3h   |
| **0900h**      | 20F4h                        | 20F5h   | 20F6h   | 20F7h   | 20F8h   | 20F9h   | 20FAh   | 20FBh   |
| **0908h**      | 20FCh                        | 20FDh   | 20FEh   | 20FFh   | 2100h   | 2101h   | 2102h   | 2103h   |
| **0910h**      | 2104h                        | 2105h   | 2106h   | 2107h   | 2108h   | 2109h   | 210Ah   | 210Bh   |
| **0918h**      | 210Ch                        | 210Dh   | 210Eh   | 210Fh   | 2110h   | 2111h   | 2112h   | 2113h   |
| **0920h**      | 2114h                        | 2115h   | 2116h   | 2117h   | 2118h   | 2119h   | 211Ah   | 211Bh   |
| **0928h**      | 211Ch                        | 211Dh   | 211Eh   | 211Fh   | 2120h   | 2121h   | 2122h   | 2123h   |
| **0930h**      | 2124h                        | 2125h   | 2126h   | 2127h   | 2128h   | 2129h   | 212Ah   | 212Bh   |
| **0938h**      | 212Ch                        | 212Dh   | 212Eh   | 212Fh   | 2130h   | 2131h   | 2132h   | 2133h   |
| **0940h**      | 2134h                        | 2135h   | 2136h   | 2137h   | 2138h   | 2139h   | 213Ah   | 213Bh   |
| **0948h**      | 213Ch                        | 213Dh   | 213Eh   | 213Fh   | 2140h   | 2141h   | 2142h   | 2143h   |
| **0950h**      | 2144h                        | 2145h   | 2146h   | 2147h   | 2148h   | 2149h   | 214Ah   | 214Bh   |
| **0958h**      | 214Ch                        | 214Dh   | 2132h   | 214Fh   | 2150h   | 2151h   | 2152h   | 2153h   |
| **0960h**      | 2154h                        | 2155h   | 2156h   | 2157h   | 2158h   | 2159h   | 215Ah   | 215Bh   |
| **0968h**      | 215Ch                        | 215Dh   | 215Eh   | 215Fh   | 2160h   | 2161h   | 2162h   | 2163h   |
| **0970h**      | 2164h                        | 2165h   | 2166h   | 2167h   | 2168h   | 2169h   | 216Ah   | 216Bh   |
| **0978h**      | 216Ch                        | 216Dh   | 216Eh   | 216Fh   | 2160h   | 2161h   | 2162h   | 2163h   |
| **0980h**      | 2164h                        | 2165h   | 2166h   | 2167h   | 2168h   | 2169h   | 216Ah   | 216Bh   |
| **0988h**      | 216Ch                        | 216Dh   | 216Eh   | 216Fh   | 2180h   | 2181h   | 2182h   | 2183h   |
| **0990h**      | 2183h                        | FFFFh   | 034Bh   | 24B6h   | 24B7h   | 24B8h   | 24B9h   | 24BAh   |
| **0998h**      | 24BBh                        | 24BCh   | 24BDh   | 24BEh   | 24BFh   | 24C0h   | 24C1h   | 24C2h   |
| **09A0h**      | 24C3h                        | 24C4h   | 24C5h   | 24C6h   | 24C7h   | 24C8h   | 24C9h   | 24CAh   |
| **09A8h**      | 24CBh                        | 24CCh   | 24CDh   | 24CEh   | 24CFh   | FFFFh   | 0746h   | 2C00h   |
| **09B0h**      | 2C01h                        | 2C02h   | 2C03h   | 2C04h   | 2C05h   | 2C06h   | 2C07h   | 2C08h   |
| **09B8h**      | 2C09h                        | 2C0Ah   | 2C0Bh   | 2C0Ch   | 2C0Dh   | 2C0Eh   | 2C0Fh   | 2C10h   |
| **09C0h**      | 2C11h                        | 2C12h   | 2C13h   | 2C14h   | 2C15h   | 2C16h   | 2C17h   | 2C18h   |
| **09C8h**      | 2C19h                        | 2C1Ah   | 2C1Bh   | 2C1Ch   | 2C1Dh   | 2C1Eh   | 2C1Fh   | 2C20h   |
| **09D0h**      | 2C21h                        | 2C22h   | 2C23h   | 2C24h   | 2C25h   | 2C26h   | 2C27h   | 2C28h   |
| **09D8h**      | 2C29h                        | 2C2Ah   | 2C2Bh   | 2C2Ch   | 2C2Dh   | 2C2Eh   | 2C5Fh   | 2C60h   |
| **09E0h**      | 2C60h                        | 2C62h   | 2C63h   | 2C64h   | 2C65h   | 2C66h   | 2C67h   | 2C67h   |
| **09E8h**      | 2C69h                        | 2C69h   | 2C6Bh   | 2C6Bh   | 2C6Dh   | 2C6Eh   | 2C6Fh   | 2C70h   |
| **09F0h**      | 2C71h                        | 2C72h   | 2C73h   | 2C74h   | 2C75h   | 2C75h   | 2C77h   | 2C78h   |
| **09F8h**      | 2C79h                        | 2C7Ah   | 2C7Bh   | 2C7Ch   | 2C7Dh   | 2C7Eh   | 2C7Fh   | 2C80h   |
| **0A00h**      | 2C80h                        | 2C82h   | 2C82h   | 2C84h   | 2C84h   | 2C86h   | 2C86h   | 2C88h   |
| **0A08h**      | 2C88h                        | 2C8Ah   | 2C8Ah   | 2C8Ch   | 2C8Ch   | 2C8Eh   | 2C8Eh   | 2C90h   |
| **0A10h**      | 2C90h                        | 2C92h   | 2C92h   | 2C94h   | 2C94h   | 2C96h   | 2C96h   | 2C98h   |
| **0A18h**      | 2C98h                        | 2C9Ah   | 2C9Ah   | 2C9Ch   | 2C9Ch   | 2C9Eh   | 2C9Eh   | 2CA0h   |
| **0A20h**      | 2CA0h                        | 2CA2h   | 2CA2h   | 2CA4h   | 2CA4h   | 2CA6h   | 2CA6h   | 2CA8h   |
| **0A28h**      | 2CA8h                        | 2CAAh   | 2CAAh   | 2CACh   | 2CACh   | 2CAEh   | 2CAEh   | 2CB0h   |
| **0A30h**      | 2CB0h                        | 2CB2h   | 2CB2h   | 2CB4h   | 2CB4h   | 2CB6h   | 2CB6h   | 2CB8h   |
| **0A38h**      | 2CB8h                        | 2CBAh   | 2CBAh   | 2CBCh   | 2CBCh   | 2CBEh   | 2CBEh   | 2CC0h   |
| **0A40h**      | 2CC0h                        | 2CC2h   | 2CC2h   | 2CC4h   | 2CC4h   | 2CC6h   | 2CC6h   | 2CC8h   |
| **0A48h**      | 2CC8h                        | 2CCAh   | 2CCAh   | 2CCCh   | 2CCCh   | 2CCEh   | 2CCEh   | 2CD0h   |
| **0A50h**      | 2CD0h                        | 2CD2h   | 2CD2h   | 2CD4h   | 2CD4h   | 2CD6h   | 2CD6h   | 2CD8h   |
| **0A58h**      | 2CD8h                        | 2CDAh   | 2CDAh   | 2CDCh   | 2CDCh   | 2CDEh   | 2CDEh   | 2CE0h   |
| **0A60h**      | 2CE0h                        | 2CE2h   | 2CE2h   | 2CE4h   | 2CE5h   | 2CE6h   | 2CE7h   | 2CE8h   |
| **0A68h**      | 2CE9h                        | 2CEAh   | 2CEBh   | 2CECh   | 2CEDh   | 2CEEh   | 2CEFh   | 2CF0h   |
| **0A70h**      | 2CF1h                        | 2CF2h   | 2CF3h   | 2CF4h   | 2CF5h   | 2CF6h   | 2CF7h   | 2CF8h   |
| **0A78h**      | 2CF9h                        | 2CFAh   | 2CFBh   | 2CFCh   | 2CFDh   | 2CFEh   | 2CFFh   | 10A0h   |
| **0A80h**      | 10A1h                        | 10A2h   | 10A3h   | 10A4h   | 10A5h   | 10A6h   | 10A7h   | 10A8h   |
| **0A88h**      | 10A9h                        | 10AAh   | 10ABh   | 10ACh   | 10ADh   | 10AEh   | 10AFh   | 10B0h   |
| **0A90h**      | 10B1h                        | 10B2h   | 10B3h   | 10B4h   | 10B5h   | 10B6h   | 10B7h   | 10B8h   |
| **0A98h**      | 10B9h                        | 10BAh   | 10BBh   | 10BCh   | 10BDh   | 10BEh   | 10BFh   | 10C0h   |
| **0AA0h**      | 10C1h                        | 10C2h   | 10C3h   | 10C4h   | 10C5h   | FFFFh   | D21Bh   | FF21h   |
| **0AA8h**      | FF22h                        | FF23h   | FF24h   | FF25h   | FF26h   | FF27h   | FF28h   | FF29h   |
| **0AB0h**      | FF2Ah                        | FF2Bh   | FF2Ch   | FF2Dh   | FF2Eh   | FF2Fh   | FF30h   | FF31h   |
| **0AB8h**      | FF32h                        | FF33h   | FF34h   | FF35h   | FF36h   | FF37h   | FF38h   | FF39h   |
| **0AC0h**      | FF3Ah                        | FF5Bh   | FF5Ch   | FF5Dh   | FF5Eh   | FF5Fh   | FF60h   | FF61h   |
| **0AC8h**      | FF62h                        | FF63h   | FF64h   | FF65h   | FF66h   | FF67h   | FF68h   | FF69h   |
| **0AD0h**      | FF6Ah                        | FF6Bh   | FF6Ch   | FF6Dh   | FF6Eh   | FF6Fh   | FF70h   | FF71h   |
| **0AD8h**      | FF72h                        | FF73h   | FF74h   | FF75h   | FF76h   | FF77h   | FF78h   | FF79h   |
| **0AE0h**      | FF7Ah                        | FF7Bh   | FF7Ch   | FF7Dh   | FF7Eh   | FF7Fh   | FF80h   | FF81h   |
| **0AE8h**      | FF82h                        | FF83h   | FF84h   | FF85h   | FF86h   | FF87h   | FF88h   | FF89h   |
| **0AF0h**      | FF8Ah                        | FF8Bh   | FF8Ch   | FF8Dh   | FF8Eh   | FF8Fh   | FF90h   | FF91h   |
| **0AF8h**      | FF92h                        | FF93h   | FF94h   | FF95h   | FF96h   | FF97h   | FF98h   | FF99h   |
| **0B00h**      | FF9Ah                        | FF9Bh   | FF9Ch   | FF9Dh   | FF9Eh   | FF9Fh   | FFA0h   | FFA1h   |
| **0B08h**      | FFA2h                        | FFA3h   | FFA4h   | FFA5h   | FFA6h   | FFA7h   | FFA8h   | FFA9h   |
| **0B10h**      | FFAAh                        | FFABh   | FFACh   | FFADh   | FFAEh   | FFAFh   | FFB0h   | FFB1h   |
| **0B18h**      | FFB2h                        | FFB3h   | FFB4h   | FFB5h   | FFB6h   | FFB7h   | FFB8h   | FFB9h   |
| **0B20h**      | FFBAh                        | FFBBh   | FFBCh   | FFBDh   | FFBEh   | FFBFh   | FFC0h   | FFC1h   |
| **0B28h**      | FFC2h                        | FFC3h   | FFC4h   | FFC5h   | FFC6h   | FFC7h   | FFC8h   | FFC9h   |
| **0B30h**      | FFCAh                        | FFCBh   | FFCCh   | FFCDh   | FFCEh   | FFCFh   | FFD0h   | FFD1h   |
| **0B38h**      | FFD2h                        | FFD3h   | FFD4h   | FFD5h   | FFD6h   | FFD7h   | FFD8h   | FFD9h   |
| **0B40h**      | FFDAh                        | FFDBh   | FFDCh   | FFDDh   | FFDEh   | FFDFh   | FFE0h   | FFE1h   |
| **0B48h**      | FFE2h                        | FFE3h   | FFE4h   | FFE5h   | FFE6h   | FFE7h   | FFE8h   | FFE9h   |
| **0B50h**      | FFEAh                        | FFEBh   | FFECh   | FFEDh   | FFEEh   | FFEFh   | FFF0h   | FFF1h   |
| **0B58h**      | FFF2h                        | FFF3h   | FFF4h   | FFF5h   | FFF6h   | FFF7h   | FFF8h   | FFF9h   |
| **0B60h**      | FFFAh                        | FFFBh   | FFFCh   | FFFDh   | FFFEh   | FFFFh   |         |         |

### <a name="73-volume-label-directory-entry"></a>Entrée de répertoire de l’étiquette de volume 7,3

Le nom de volume est une chaîne Unicode qui permet aux utilisateurs finaux de distinguer leurs volumes de stockage. Dans le système de fichiers exFAT, l’étiquette de volume existe comme une entrée d’annuaire principale critique dans le répertoire racine (voir le [tableau 26](#table-26-volume-label-directoryentry-structure)). Le nombre valide d’entrées de répertoire des noms de volume est compris entre 0 et 1.

<div id="table-26-volume-label-directoryentry-structure" />

**Tableau 26-structure de l’étiquette de volume**

<table>
<thead>
<tr class="header">
<th><strong>Nom du champ</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>poids</strong></p></th>
<th><p><strong>Taille</strong></p>
<p><strong>poids</strong></p></th>
<th><strong>Commentaires</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#731-entrytype-field">section 7.3.1</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>CharacterCount</td>
<td>1</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#732-charactercount-field">section 7.3.2</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>VolumeLabel</td>
<td>2</td>
<td>22</td>
<td>Ce champ est obligatoire et la <a href="#733-volumelabel-field">section 7.3.3 (</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>Réservé</td>
<td>24</td>
<td>8</td>
<td>Ce champ est obligatoire et son contenu est réservé.</td>
</tr>
</tbody>
</table>

#### <a name="731-entrytype-field"></a>7.3.1 champ EntryType

Le champ EntryType doit être conforme à la définition fournie dans le modèle DirectoryEntry principal générique (voir la [section 6.3.1](#631-entrytype-field)).

##### <a name="7311-typecode-field"></a>Champ TypeCode 7.3.1.1

Le champ TypeCode doit se conformer à la définition fournie dans le modèle DirectoryEntry principal générique (voir la [section 6.3.1.1](#6311-typecode-field)).

Pour l’entrée de répertoire de nom de volume, la valeur valide pour ce champ est
3.

##### <a name="7312-typeimportance-field"></a>Champ 7.3.1.2 TypeImportance

Le champ TypeImportance doit être conforme à la définition fournie dans le modèle DirectoryEntry principal générique (voir la [section 6.3.1.2](#6312-typeimportance-field)).

Pour l’entrée de répertoire de nom de volume, la valeur valide pour ce champ est
0.

##### <a name="7313-typecategory-field"></a>Champ 7.3.1.3 TypeCategory

Le champ TypeCategory doit être conforme à la définition fournie dans le modèle DirectoryEntry principal générique (voir la [section 6.3.1.3](#6313-typecategory-field)).

##### <a name="7314-inuse-field"></a>Champ 7.3.1.4 InUse

Le champ InUse doit se conformer à la définition fournie dans le modèle DirectoryEntry principal générique (voir la [section 6.3.1.4](#6314-inuse-field)).

#### <a name="732-charactercount-field"></a>Champ de CharacterCount 7.3.2

Le champ CharacterCount doit contenir la longueur de la chaîne Unicode contenue dans le champ VolumeLabel.

La plage de valeurs valide pour ce champ doit être :

- Au moins 0, ce qui signifie que la chaîne Unicode a une longueur de 0 caractère (ce qui est l’équivalent d’aucun nom de volume)

- Jusqu’à 11, ce qui signifie que la chaîne Unicode comporte 11 caractères

#### <a name="733-volumelabel-field"></a>Champ 7.3.3 (VolumeLabel

Le champ VolumeLabel doit contenir une chaîne Unicode, qui est le nom convivial du volume. Le champ VolumeLabel contient le même ensemble de caractères non valides que le champ nom de fichier de l’entrée répertoire du nom de fichier (voir la [section 7.7.3](#773-filename-field)).

### <a name="74-file-directory-entry"></a>Entrée de répertoire de fichiers 7,4

Les entrées de répertoire de fichiers décrivent les fichiers et les répertoires. Il s’agit d’entrées d’annuaire principales critiques et tout répertoire peut contenir zéro ou plusieurs entrées de répertoire de fichiers (voir le [tableau 27](#table-27-file-directoryentry)). Pour qu’une entrée de répertoire de fichiers soit valide, une seule entrée de répertoire d’extension de flux et au moins une entrée de répertoire de nom de fichier doit suivre immédiatement l’entrée de répertoire de fichier (voir la [section 7,6](#76-stream-extension-directory-entry) et la [section 7,7](#77-file-name-directory-entry), respectivement).

<div id="table-27-file-directoryentry" />

**Tableau 27 fichier DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nom du champ</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>poids</strong></p></th>
<th><p><strong>Taille</strong></p>
<p><strong>poids</strong></p></th>
<th><strong>Commentaires</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#741-entrytype-field">section 7.4.1</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>SecondaryCount</td>
<td>1</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#742-secondarycount-field">section 7.4.2</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>SetChecksum</td>
<td>2</td>
<td>2</td>
<td>Ce champ est obligatoire et la <a href="#743-setchecksum-field">section 7.4.3</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>FileAttributes</td>
<td>4</td>
<td>2</td>
<td>Ce champ est obligatoire et la <a href="#744-fileattributes-field">section 7.4.4</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>Reserved1</td>
<td>6</td>
<td>2</td>
<td>Ce champ est obligatoire et son contenu est réservé.</td>
</tr>
<tr class="even">
<td>CreateTimestamp</td>
<td>8</td>
<td>4</td>
<td>Ce champ est obligatoire et <a href="#745-createtimestamp-create10msincrement-and-createutcoffset-fields"> la section 7.4.5 </
a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>LastModifiedTimestamp</td>
<td>12</td>
<td>4</td>
<td>Ce champ est obligatoire et la <a href="#746-lastmodifiedtimestamp-lastmodified10msincrement-and-lastmodifiedutcoffset-fields">section 7.4.6</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>LastAccessedTimestamp</td>
<td>16</td>
<td>4</td>
<td>Ce champ est obligatoire et la <a href="#747-lastaccessedtimestamp-and-lastaccessedutcoffset-fields">section 7.4.7</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>Create10msIncrement</td>
<td>20</td>
<td>1</td>
<td>Ce champ est obligatoire et <a href="#745-createtimestamp-create10msincrement-and-createutcoffset-fields"> la section 7.4.5 </
a> définit son contenu.</td>
</tr>
<tr class="even">
<td>LastModified10msIncrement</td>
<td>21</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#746-lastmodifiedtimestamp-lastmodified10msincrement-and-lastmodifiedutcoffset-fields">section 7.4.6</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>CreateUtcOffset</td>
<td>22</td>
<td>1</td>
<td>Ce champ est obligatoire et <a href="#745-createtimestamp-create10msincrement-and-createutcoffset-fields"> la section 7.4.5 </
a> définit son contenu.</td>
</tr>
<tr class="even">
<td>LastModifiedUtcOffset</td>
<td>23</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#746-lastmodifiedtimestamp-lastmodified10msincrement-and-lastmodifiedutcoffset-fields">section 7.4.6</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>LastAccessedUtcOffset</td>
<td>24</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#747-lastaccessedtimestamp-and-lastaccessedutcoffset-fields">section 7.4.7</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>Reserved2</td>
<td>25</td>
<td>7</td>
<td>Ce champ est obligatoire et son contenu est réservé.</td>
</tr>
</tbody>
</table>

#### <a name="741-entrytype-field"></a>7.4.1 champ EntryType

Le champ EntryType doit être conforme à la définition fournie dans le modèle DirectoryEntry principal générique (voir la [section 6.3.1](#631-entrytype-field)).

##### <a name="7411-typecode-field"></a>Champ TypeCode 7.4.1.1

Le champ TypeCode doit se conformer à la définition fournie dans le modèle DirectoryEntry principal générique (voir la [section 6.3.1.1](#6311-typecode-field)).

Pour une entrée de répertoire de fichiers, la valeur valide pour ce champ est 5.

##### <a name="7412-typeimportance-field"></a>Champ 7.4.1.2 TypeImportance

Le champ TypeImportance doit être conforme à la définition fournie dans le modèle DirectoryEntry principal générique (voir la [section 6.3.1.2](#6312-typeimportance-field)).

Pour une entrée de répertoire de fichiers, la valeur valide pour ce champ est 0.

##### <a name="7413-typecategory-field"></a>Champ 7.4.1.3 TypeCategory

Le champ TypeCategory doit être conforme à la définition fournie dans le modèle DirectoryEntry principal générique (voir la [section 6.3.1.3](#6313-typecategory-field)).

##### <a name="7414-inuse-field"></a>Champ 7.4.1.4 InUse

Le champ InUse doit se conformer à la définition fournie dans le modèle DirectoryEntry principal générique (voir la [section 6.3.1.4](#6314-inuse-field)).

#### <a name="742-secondarycount-field"></a>7.4.2 SecondaryCount champ)

Le champ SecondaryCount doit être conforme à la définition fournie dans le modèle DirectoryEntry principal générique (voir la [section 6.3.2](#632-secondarycount-field)).

#### <a name="743-setchecksum-field"></a>7.4.3 champ SetCheckSum,

Le champ SetCheckSum, doit être conforme à la définition fournie dans le modèle DirectoryEntry principal générique (voir la [section 6.3.3](#633-setchecksum-field)).

#### <a name="744-fileattributes-field"></a>Champ FileAttributes 7.4.4

Le champ FileAttributes contient des indicateurs (voir le [tableau 28](#table-28-fileattributes-field-structure)).

<div id="table-28-fileattributes-field-structure" />

**Tableau 28, structure de champ FileAttributes**

<table>
<thead>
<tr class="header">
<th><strong>Nom du champ</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>64bits</strong></p></th>
<th><p><strong>Taille</strong></p>
<p><strong>bits</strong></p></th>
<th><strong>Commentaires</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Lecture seule</td>
<td>0</td>
<td>1</td>
<td>Ce champ est obligatoire et est conforme à la définition MS-DOS.</td>
</tr>
<tr class="even">
<td>Hidden</td>
<td>1</td>
<td>1</td>
<td>Ce champ est obligatoire et est conforme à la définition MS-DOS.</td>
</tr>
<tr class="odd">
<td>Système</td>
<td>2</td>
<td>1</td>
<td>Ce champ est obligatoire et est conforme à la définition MS-DOS.</td>
</tr>
<tr class="even">
<td>Reserved1</td>
<td>3</td>
<td>1</td>
<td>Ce champ est obligatoire et son contenu est réservé.</td>
</tr>
<tr class="odd">
<td>Répertoire</td>
<td>4</td>
<td>1</td>
<td>Ce champ est obligatoire et est conforme à la définition MS-DOS.</td>
</tr>
<tr class="even">
<td>Archive</td>
<td>5</td>
<td>1</td>
<td>Ce champ est obligatoire et est conforme à la définition MS-DOS.</td>
</tr>
<tr class="odd">
<td>Reserved2</td>
<td>6</td>
<td>10</td>
<td>Ce champ est obligatoire et son contenu est réservé.</td>
</tr>
</tbody>
</table>

#### <a name="745-createtimestamp-create10msincrement-and-createutcoffset-fields"></a>Champs 7.4.5 CreateTimestamp, Create10msIncrement et CreateUtcOffset

En combinaison, les champs CreateTimestamp et CreateTime10msIncrement décrivent la date et l’heure locales auxquelles le fichier/répertoire donné a été créé. Le champ CreateUtcOffset décrit l’offset de la date et de l’heure locales par rapport à l’heure UTC. Les implémentations doivent définir ces champs lors de la création du jeu d’entrées de répertoire donné.

Ces champs doivent être conformes aux définitions des champs timestamp, 10msIncrement et UtcOffset (consultez la [section 7.4.8](#748-timestamp-fields), [section 7.4.9](#749-10msincrement-fields)et [section 7.4.10](#7410-utcoffset-fields), respectivement).

#### <a name="746-lastmodifiedtimestamp-lastmodified10msincrement-and-lastmodifiedutcoffset-fields"></a>Champs 7.4.6 LastModifiedTimestamp, LastModified10msIncrement et LastModifiedUtcOffset

En combinaison, les champs LastModifiedTimestamp et LastModifiedTime10msIncrement décrivent la date et l’heure locales de la dernière modification du contenu de l’un des clusters associés à l’entrée de répertoire de l’extension de flux donnée. Le champ LastModifiedUtcOffset décrit l’offset de la date et de l’heure locales par rapport à l’heure UTC. Les implémentations doivent mettre à jour les champs suivants :

1. Après la modification du contenu de l’un des clusters associés à l’entrée de répertoire de l’extension de flux donnée (à l’exception du contenu qui se trouve au-delà du point indiqué par le champ ValidDataLength)

2. Lors de la modification des valeurs des champs ValidDataLength ou DataLength

Ces champs doivent être conformes aux définitions des champs timestamp, 10msIncrement et UtcOffset (consultez la [section 7.4.8](#748-timestamp-fields), [section 7.4.9](#749-10msincrement-fields)et [section 7.4.10](#7410-utcoffset-fields), respectivement).

#### <a name="747-lastaccessedtimestamp-and-lastaccessedutcoffset-fields"></a>Champs 7.4.7 LastAccessedTimestamp et LastAccessedUtcOffset

Le champ LastAccessedTimestamp doit décrire la date et l’heure locales auxquelles le contenu de l’un des clusters associés à l’entrée de répertoire de l’extension de flux donnée a été accédé pour la dernière fois. Le champ LastAccessedUtcOffset décrit l’offset de la date et de l’heure locales par rapport à l’heure UTC.
Les implémentations doivent mettre à jour les champs suivants :

1. Après la modification du contenu de l’un des clusters associés à l’entrée de répertoire de l’extension de flux donnée (à l’exception du contenu qui se trouve au-delà du ValidDataLength)

2. Lors de la modification des valeurs des champs ValidDataLength ou DataLength

Les implémentations doivent mettre à jour ces champs après avoir lu le contenu de l’un des clusters associés à l’entrée de répertoire de l’extension de flux donnée.

Ces champs doivent être conformes aux définitions des champs timestamp et UtcOffset (consultez la [section 7.4.8](#748-timestamp-fields) et la [section 7.4.10](#7410-utcoffset-fields), respectivement).

#### <a name="748-timestamp-fields"></a>Champs horodateur 7.4.8

Les champs d’horodatage décrivent à la fois la date et l’heure locales, jusqu’à une résolution de deux secondes (voir le [Tableau 29](#table-29-timestamp-field-structure)).

<div id="table-29-timestamp-field-structure" />

**Tableau 29-structure de champs d’horodatage**

<table>
<thead>
<tr class="header">
<th><strong>Nom du champ</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>64bits</strong></p></th>
<th><p><strong>Taille</strong></p>
<p><strong>bits</strong></p></th>
<th><strong>Commentaires</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DoubleSeconds</td>
<td>0</td>
<td>5</td>
<td>Ce champ est obligatoire et la <a href="#7481-doubleseconds-field">section 7.4.8.1</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>Minute</td>
<td>5</td>
<td>6</td>
<td>Ce champ est obligatoire et la <a href="#7482-minute-field">section 7.4.8.2</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>Heure</td>
<td>11</td>
<td>5</td>
<td>Ce champ est obligatoire et la <a href="#7483-hour-field">section 7.4.8.3</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>Jour</td>
<td>16</td>
<td>5</td>
<td>Ce champ est obligatoire et la <a href="#7484-day-field">section 7.4.8.4</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>Month (Mois)</td>
<td>21</td>
<td>4</td>
<td>Ce champ est obligatoire et la <a href="#7485-month-field">section 7.4.8.5</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>Year</td>
<td>25</td>
<td>7</td>
<td>Ce champ est obligatoire et la <a href="#7486-year-field">section 7.4.8.6</a> définit son contenu.</td>
</tr>
</tbody>
</table>

##### <a name="7481-doubleseconds-field"></a>Champ 7.4.8.1 DoubleSeconds

Le champ DoubleSeconds décrit la partie secondes du champ d’horodatage, en multiples de deux secondes.

La plage de valeurs valide pour ce champ doit être :

- 0, qui représente 0 seconde

- 29, qui représente 58 secondes

##### <a name="7482-minute-field"></a>Champ 7.4.8.2 minute

Le champ minute doit décrire la partie minutes du champ d’horodatage.

La plage de valeurs valide pour ce champ doit être :

- 0, qui représente 0 minute

- 59, qui représente 59 minutes

##### <a name="7483-hour-field"></a>Champ 7.4.8.3 hour

Le champ heure doit décrire la partie heures du champ horodateur.

La plage de valeurs valide pour ce champ doit être :

- 0, qui représente 00:00 heures

- 23, qui représente 23:00 heures

##### <a name="7484-day-field"></a>Champ jour de 7.4.8.4

Le champ jour doit décrire la partie jour du champ d’horodatage.

La plage de valeurs valide pour ce champ doit être :

- 1, qui est le premier jour du mois donné

- Dernier jour du mois donné (le mois donné définit le nombre de jours valides)

##### <a name="7485-month-field"></a>Champ 7.4.8.5 month

Le champ month doit décrire la partie mois du champ TIMESTAMP.

La plage de valeurs valide pour ce champ doit être :

- Au moins 1, qui représente janvier

- Au maximum 12, qui représente décembre

##### <a name="7486-year-field"></a>Champ 7.4.8.6 Year

Le champ Year doit décrire la partie Year du champ TIMESTAMP, par rapport à l’année 1980. Ce champ représente l’année 1980 avec la valeur 0 et l’année 2107 avec la valeur 127.

Toutes les valeurs possibles pour ce champ sont valides.

#### <a name="749-10msincrement-fields"></a>Champs 7.4.9 10msIncrement

les champs 10msIncrement fournissent une résolution de temps supplémentaire à leurs champs d’horodatage correspondants dans des multiples de dix millisecondes.

La plage valide de valeurs pour ces champs doit être :

- Au moins 0, qui représente 0 milliseconde

- Au plus 199, qui représente 1990 millisecondes

#### <a name="7410-utcoffset-fields"></a>Champs 7.4.10 UtcOffset

Les champs UtcOffset (voir le [tableau 30](#table-30-utcoffset-field-structure)) décrivent le décalage par rapport à l’heure UTC et la date et l’heure auxquelles leurs champs timestamp et 10msIncrement correspondants décrivent. Le décalage par rapport à l’heure UTC et à la date et à l’heure locales comprend les effets des fuseaux horaires et autres ajustements de date et d’heure, tels que l’heure d’été et les modifications de l’heure d’été régionale.

<div id="table-30-utcoffset-field-structure" />

**Tableau 30 UtcOffset, structure de champs**

<table>
<thead>
<tr class="header">
<th><strong>Nom du champ</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>64bits</strong></p></th>
<th><p><strong>Taille</strong></p>
<p><strong>bits</strong></p></th>
<th><strong>Commentaires</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>OffsetFromUtc</td>
<td>0</td>
<td>7</td>
<td>Ce champ est obligatoire et la <a href="#74101-offsetfromutc-field">section 7.4.10.1</a>définit son contenu.</td>
</tr>
<tr class="even">
<td>OffsetValid</td>
<td>7</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#74102-offsetvalid-field">section 7.4.10.2</a> définit son contenu.</td>
</tr>
</tbody>
</table>

##### <a name="74101-offsetfromutc-field"></a>Champ 7.4.10.1 OffsetFromUtc

Le champ OffsetFromUtc doit décrire le décalage par rapport à l’heure UTC de la date et de l’heure locales que contient l’horodatage et les champs 10msIncrement associés.
Ce champ décrit le décalage par rapport à l’heure UTC, en intervalles de 15 minutes (voir tableau 31).

<div id="table-31-meaning-of-the-values-of-the-offsetfromutc-field" />

**Tableau 31 signification des valeurs du champ OffsetFromUtc**

<table>
<thead>
<tr class="header">
<th><strong>Valeur</strong></th>
<th><strong>Équivalent décimal signé</strong></th>
<th><strong>Description</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>3Fh</td>
<td>63</td>
<td>La date et l’heure locales sont UTC + 15:45</td>
</tr>
<tr class="even">
<td>3Eh</td>
<td>62</td>
<td>La date et l’heure locales sont UTC + 15:30</td>
</tr>
<tr class="odd">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="even">
<td>01h</td>
<td>1</td>
<td>La date et l’heure locales sont UTC + 00:15</td>
</tr>
<tr class="odd">
<td>00h</td>
<td>0</td>
<td>La date et l’heure locales sont UTC</td>
</tr>
<tr class="even">
<td>7Fh</td>
<td>-1</td>
<td>La date et l’heure locales sont UTC – 00:15</td>
</tr>
<tr class="odd">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="even">
<td>41h</td>
<td>-63</td>
<td>La date et l’heure locales sont UTC – 15:45</td>
</tr>
<tr class="odd">
<td>40h</td>
<td>-64</td>
<td>La date et l’heure locales sont UTC – 16:00</td>
</tr>
</tbody>
</table>

Comme le montre le tableau ci-dessus, toutes les valeurs possibles pour ce champ sont valides. Toutefois, les implémentations doivent enregistrer uniquement la valeur 00h pour ce champ dans les cas suivants :

1. La date et l’heure locales sont en fait les mêmes que le temps universel coordonné (UTC), auquel cas la valeur du champ OffsetValid est 1

2. La date et l’heure locales ne sont pas connues, auquel cas la valeur du champ OffsetValid est 1 et les implémentations considèrent que la date et l’heure locales sont UTC

3. L’heure UTC n’est pas connue, auquel cas la valeur du champ OffsetValid doit être 0

Si le décalage de date et d’heure local par rapport à l’heure UTC n’est pas un multiple d’intervalles de 15 minutes, les implémentations enregistrent 00h dans le champ OffsetFromUtc et considèrent l’heure UTC comme une date et une heure locales.

##### <a name="74102-offsetvalid-field"></a>Champ 7.4.10.2 OffsetValid

Le champ OffsetValid indique si le contenu du champ OffsetFromUtc est valide ou non, comme suit :

- 0, ce qui signifie que le contenu du champ OffsetFromUtc n’est pas valide
    > et doit être 00h

- 1, ce qui signifie que le contenu du champ OffsetFromUtc est valide

Les implémentations doivent uniquement définir ce champ à la valeur 0 lorsque l’heure UTC n’est pas disponible pour le calcul de la valeur du champ OffsetFromUtc. Si ce champ contient la valeur 0, les implémentations traitent les champs timestamp et 10msIncrement comme ayant le même décalage UTC que la date et l’heure locales actuelles.

### <a name="75-volume-guid-directory-entry"></a>Entrée de répertoire du GUID de volume 7,5

L’entrée de répertoire GUID du volume contient un GUID qui permet aux implémentations de distinguer les volumes de manière unique et par programmation.
Le GUID du volume existe en tant qu’entrée de répertoire principal Bénin dans le répertoire racine (voir le [tableau 32](#table-32-volume-guid-directoryentry)). Le nombre valide d’entrées de répertoire du GUID de volume est compris entre 0 et 1.

<div id="table-32-volume-guid-directoryentry" />

**Tableau 32 GUID de volume, DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nom du champ</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>poids</strong></p></th>
<th><p><strong>Taille</strong></p>
<p><strong>poids</strong></p></th>
<th><strong>Commentaires</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#751-entrytype-field">section 7.5.1</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>SecondaryCount</td>
<td>1</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#752-secondarycount-field">section 7.5.2</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>SetChecksum</td>
<td>2</td>
<td>2</td>
<td>Ce champ est obligatoire et la <a href="#753-setchecksum-field">section 7.5.3</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>GeneralPrimaryFlags</td>
<td>4</td>
<td>2</td>
<td>Ce champ est obligatoire et la <a href="#754-generalprimaryflags-field">section 7.5.4</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>VolumeGuid</td>
<td>6</td>
<td>16</td>
<td>Ce champ est obligatoire et la <a href="#755-volumeguid-field">section 7.5.5</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>Réservé</td>
<td>22</td>
<td>10</td>
<td>Ce champ est obligatoire et son contenu est réservé.</td>
</tr>
</tbody>
</table>

#### <a name="751-entrytype-field"></a>7.5.1 champ EntryType

Le champ EntryType doit être conforme à la définition fournie dans le modèle DirectoryEntry principal générique (voir la [section 6.3.1](#631-entrytype-field)).

##### <a name="7511-typecode-field"></a>Champ TypeCode 7.5.1.1

Le champ TypeCode doit se conformer à la définition fournie dans le modèle DirectoryEntry principal générique (voir la [section 6.3.1.1](#6311-typecode-field)).

Pour l’entrée de répertoire GUID du volume, la valeur valide pour ce champ est
0.

##### <a name="7512-typeimportance-field"></a>Champ 7.5.1.2 TypeImportance

Le champ TypeImportance doit être conforme à la définition fournie dans le modèle DirectoryEntry principal générique (voir la [section 6.3.1.2](#6312-typeimportance-field)).

Pour l’entrée de répertoire GUID du volume, la valeur valide pour ce champ est
1.

##### <a name="7513-typecategory-field"></a>Champ 7.5.1.3 TypeCategory

Le champ TypeCategory doit être conforme à la définition fournie dans le modèle DirectoryEntry principal générique (voir la [section 6.3.1.3](#6313-typecategory-field)).

##### <a name="7514-inuse-field"></a>Champ 7.5.1.4 InUse

Le champ InUse doit se conformer à la définition fournie dans le modèle DirectoryEntry principal générique (voir la [section 6.3.1.4](#6314-inuse-field)).

#### <a name="752-secondarycount-field"></a>7.5.2 champ SecondaryCount

Le champ SecondaryCount doit être conforme à la définition fournie dans le modèle DirectoryEntry principal générique (voir la [section 6.3.2](#632-secondarycount-field)).

Pour l’entrée de répertoire GUID du volume, la valeur valide pour ce champ est
0.

#### <a name="753-setchecksum-field"></a>Champ 7.5.3 SetCheckSum,

Le champ SetCheckSum, doit être conforme à la définition fournie dans le modèle DirectoryEntry principal générique (voir la [section 6.3.3](#633-setchecksum-field)).

#### <a name="754-generalprimaryflags-field"></a>7.5.4 GeneralPrimaryFlags, champ

Le champ GeneralPrimaryFlags doit être conforme à la définition fournie dans le modèle DirectoryEntry principal générique (voir la [section 6.3.4](#634-generalprimaryflags-field)) et définit le contenu du champ CustomDefined à réserver.

##### <a name="7541-allocationpossible-field"></a>Champ 7.5.4.1 AllocationPossible

Le champ AllocationPossible doit être conforme à la définition fournie dans le modèle DirectoryEntry principal générique (voir la [section 6.3.4.1](#6341-allocationpossible-field)).

Pour l’entrée de répertoire GUID du volume, la valeur valide pour ce champ est
0.

##### <a name="7542-nofatchain-field"></a>Champ 7.5.4.2 NoFatChain

Le champ NoFatChain doit être conforme à la définition fournie dans le modèle DirectoryEntry principal générique (voir la [section 6.3.4.2](#6342-nofatchain-field)).

#### <a name="755-volumeguid-field"></a>Champ 7.5.5 VolumeGuid

Le champ VolumeGuid doit contenir un GUID qui identifie de façon unique le volume donné.

Toutes les valeurs possibles pour ce champ sont valides, à l’exception du GUID null, qui est {00000000-0000-0000-0000-000000000000} .

### <a name="76-stream-extension-directory-entry"></a>Entrée de répertoire de l’extension de flux 7,6

L’entrée de répertoire de l’extension de flux est une entrée d’annuaire secondaire critique dans les jeux d’entrées de répertoire de fichiers (voir le [tableau 33](#table-33-stream-extension-directoryentry)). Le nombre valide d’entrées de répertoire d’extension de flux dans un jeu d’entrée de répertoire de fichiers est 1.
En outre, cette entrée de répertoire est valide uniquement si elle suit immédiatement l’entrée de répertoire du fichier.

<div id="table-33-stream-extension-directoryentry" />

**Tableau 33 extension de flux DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nom du champ</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>poids</strong></p></th>
<th><p><strong>Taille</strong></p>
<p><strong>poids</strong></p></th>
<th><strong>Commentaires</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#761-entrytype-field">section 7.6.1</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#762-generalsecondaryflags-field">section 7.6.2</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>Reserved1</td>
<td>2</td>
<td>1</td>
<td>Ce champ est obligatoire et son contenu est réservé.</td>
</tr>
<tr class="even">
<td>NameLength</td>
<td>3</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#763-namelength-field">section 7.6.3</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>NameHash</td>
<td>4</td>
<td>2</td>
<td>Ce champ est obligatoire et la <a href="#764-namehash-field">section 7.6.4</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>Reserved2</td>
<td>6</td>
<td>2</td>
<td>Ce champ est obligatoire et son contenu est réservé.</td>
</tr>
<tr class="odd">
<td>ValidDataLength</td>
<td>8</td>
<td>8</td>
<td>Ce champ est obligatoire et la <a href="#765-validdatalength-field">section 7.6.5</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>Reserved3</td>
<td>16</td>
<td>4</td>
<td>Ce champ est obligatoire et son contenu est réservé.</td>
</tr>
<tr class="odd">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Ce champ est obligatoire et la <a href="#766-firstcluster-field">section 7.6.6</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Ce champ est obligatoire et la <a href="#767-datalength-field">section 7.6.7</a> définit son contenu.</td>
</tr>
</tbody>
</table>

#### <a name="761-entrytype-field"></a>7.6.1 champ EntryType

Le champ EntryType doit être conforme à la définition fournie dans le modèle DirectoryEntry secondaire générique (voir la [section 6.4.1](#641-entrytype-field)).

##### <a name="7611-typecode-field"></a>Champ TypeCode 7.6.1.1

Le champ TypeCode est conforme à la définition fournie dans le modèle DirectoryEntry secondaire générique (voir la [section 6.4.1.1](#6411-typecode-field)).

Pour l’entrée de répertoire de l’extension de flux, la valeur valide pour ce champ est 0.

##### <a name="7612-typeimportance-field"></a>Champ 7.6.1.2 TypeImportance

Le champ TypeImportance doit être conforme à la définition fournie dans le modèle DirectoryEntry secondaire générique (voir la [section 6.4.1.2](#6412-typeimportance-field)).

Pour l’entrée de répertoire de l’extension de flux, la valeur valide pour ce champ est 0.

##### <a name="7613-typecategory-field"></a>Champ 7.6.1.3 TypeCategory

Le champ TypeCategory doit être conforme à la définition fournie dans le modèle DirectoryEntry secondaire générique (voir la [section 6.4.1.3](#6413-typecategory-field)).

##### <a name="7614-inuse-field"></a>Champ 7.6.1.4 InUse

Le champ InUse doit se conformer à la définition fournie dans le modèle DirectoryEntry secondaire générique (voir la [section 6.4.1.4](#6414-inuse-field)).

#### <a name="762-generalsecondaryflags-field"></a>7.6.2 champ GeneralSecondaryFlags

Le champ GeneralSecondaryFlags doit être conforme à la définition fournie dans le modèle DirectoryEntry secondaire générique (voir la [section 6.4.2](#642-generalsecondaryflags-field)) et définit le contenu du champ CustomDefined à réserver.

##### <a name="7621-allocationpossible-field"></a>Champ 7.6.2.1 AllocationPossible

Le champ AllocationPossible doit être conforme à la définition fournie dans le modèle DirectoryEntry secondaire générique (voir la [section 6.4.2.1](#6421-allocationpossible-field)).

Pour l’entrée de répertoire de l’extension de flux, la valeur valide pour ce champ est 1.

##### <a name="7622-nofatchain-field"></a>Champ 7.6.2.2 NoFatChain

Le champ NoFatChain doit être conforme à la définition fournie dans le modèle DirectoryEntry secondaire générique (voir la [section 6.4.2.2](#6422-nofatchain-field)).

#### <a name="763-namelength-field"></a>Champ 7.6.3 NameLength

Le champ NameLength doit contenir la longueur de la chaîne Unicode dans laquelle les entrées de répertoire de nom de fichier suivantes (voir la [Section 7,7](#77-file-name-directory-entry)) contiennent collectivement.

La plage de valeurs valide pour ce champ doit être :

- Au moins 1, qui est le nom de fichier le plus bref possible

- Au plus 255, qui est le nom de fichier le plus long possible

La valeur du champ NameLength affecte également le nombre d’entrées de répertoire du nom de fichier (voir la [Section 7,7](#77-file-name-directory-entry)).

#### <a name="764-namehash-field"></a>Champ 7.6.4 NameHash

Le champ NameHash doit contenir un hachage de 2 octets (voir [figure 4](#figure-4-namehash-computation)) du nom de fichier dans la casse. Cela permet aux implémentations d’effectuer une comparaison rapide lors de la recherche d’un fichier par nom. Plus important encore, le NameHash fournit une vérification de la non-concordance. Les implémentations vérifient toutes les correspondances NameHash avec une comparaison du nom de fichier dans la casse.

<div id="figure-4-namehash-computation" />

**Figure 4 calcul NameHash**

```C
UInt16 NameHash
(
    WCHAR * FileName,    // points to an in-memory copy of the up-cased file name
    UCHAR   NameLength
)
{
    UCHAR  * Buffer = (UCHAR *)FileName;
    UInt16   NumberOfBytes = (UInt16)NameLength * 2;
    UInt16   Hash = 0;
    UInt16   Index;

    for (Index = 0; Index < NumberOfBytes; Index++)
    {
        Hash = ((Hash&1) ? 0x8000 : 0) + (Hash>>1) + (UInt16)Buffer[Index];
    }
    return Hash;
}
```

#### <a name="765-validdatalength-field"></a>7.6.5 ValidDataLength, champ

Le champ ValidDataLength décrira le nombre de fois où les données utilisateur du flux de données ont été écrites. Les implémentations doivent mettre à jour ce champ au fur et à mesure qu’elles écrivent des données dans le flux de données. Sur le support de stockage, les données comprises entre la longueur de données valide et la longueur des données du flux de données ne sont pas définies. Les implémentations retournent des zéros pour les opérations de lecture au-delà de la longueur des données valides.

Si l’entrée d’annuaire de fichiers correspondante décrit un répertoire, la seule valeur valide pour ce champ est égale à la valeur du champ DataLength. Dans le cas contraire, la plage de valeurs valides pour ce champ doit être :

- Au moins 0, ce qui signifie qu’aucune donnée utilisateur n’a été écrite dans le flux de données

- Au plus de DataLength, ce qui signifie que les données utilisateur ont été écrites à la longueur totale du flux de données

#### <a name="766-firstcluster-field"></a>7.6.6, champ FirstCluster

Le champ FirstCluster doit être conforme à la définition fournie dans le modèle DirectoryEntry secondaire générique (voir la [section 6.4.3](#643-firstcluster-field)).

Ce champ doit contenir l’index du premier cluster du flux de données, qui héberge les données utilisateur.

#### <a name="767-datalength-field"></a>Champ 7.6.7 DataLength

Le champ DataLength doit se conformer à la définition fournie dans le modèle DirectoryEntry secondaire générique (voir la [section 6.4.4](#644-datalength-field)).

Si l’entrée d’annuaire de fichiers correspondante décrit un répertoire, la valeur valide pour ce champ correspond à la taille totale de l’allocation associée, en octets, qui peut être 0. En outre, pour les répertoires, la valeur maximale de ce champ est de 256 Mo.

### <a name="77-file-name-directory-entry"></a>7,7 entrée de répertoire de nom de fichier

Les entrées de répertoire de nom de fichier sont des entrées de répertoire secondaire critiques dans les jeux d’entrées de répertoires de fichiers (voir le [tableau 34](#table-34-file-name-directoryentry)). Le nombre valide d’entrées de répertoires de noms de fichiers dans une entrée de répertoire de fichiers est NameLength/15, arrondi à l’entier le plus proche. En outre, les entrées de répertoire de nom de fichier ne sont valides que si elles suivent immédiatement l’entrée de répertoire de l’extension de flux en tant que série consécutive. Les entrées de répertoire de nom de fichier s’associent pour former le nom de fichier de l’ensemble d’entrées de répertoires de fichiers.

Tous les enfants d’une entrée de répertoire donnée doivent avoir des ensembles d’entrées de répertoire de nom de fichier uniques. Autrement dit, il ne peut y avoir aucun nom de fichier ou de répertoire en double après la casse dans un répertoire.

<div id="table-34-file-name-directoryentry" />

**Tableau 34 nom de fichier DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nom du champ</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>poids</strong></p></th>
<th><p><strong>Taille</strong></p>
<p><strong>poids</strong></p></th>
<th><strong>Commentaires</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#771-entrytype-field">section 7.7.1</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#772-generalsecondaryflags-field">section 7.7.2</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>FileName</td>
<td>2</td>
<td>30</td>
<td>Ce champ est obligatoire et la <a href="#773-filename-field">section 7.7.3</a> définit son contenu.</td>
</tr>
</tbody>
</table>

#### <a name="771-entrytype-field"></a>EntryType, champ

Le champ EntryType doit être conforme à la définition fournie dans le modèle DirectoryEntry secondaire générique (voir la [section 6.4.1](#641-entrytype-field)).

##### <a name="7711-typecode-field"></a>Champ TypeCode 7.7.1.1

Le champ TypeCode est conforme à la définition fournie dans le modèle DirectoryEntry secondaire générique (voir la [section 6.4.1.1](#6411-typecode-field)).

Pour l’entrée de répertoire de l’extension de flux, la valeur valide pour ce champ est 1.

##### <a name="7712-typeimportance-field"></a>Champ 7.7.1.2 TypeImportance

Le champ TypeImportance doit être conforme à la définition fournie dans le modèle DirectoryEntry secondaire générique (voir la [section 6.4.1.2](#6412-typeimportance-field)).

Pour l’entrée de répertoire de l’extension de flux, la valeur valide pour ce champ est 0.

##### <a name="7713-typecategory-field"></a>Champ 7.7.1.3 TypeCategory

Le champ TypeCategory doit être conforme à la définition fournie dans le modèle DirectoryEntry secondaire générique (voir la [section 6.4.1.3](#6413-typecategory-field)).

##### <a name="7714-inuse-field"></a>Champ 7.7.1.4 InUse

Le champ InUse doit se conformer à la définition fournie dans le modèle DirectoryEntry secondaire générique (voir la [section 6.4.1.4](#6414-inuse-field)).

#### <a name="772-generalsecondaryflags-field"></a>Champ 7.7.2 GeneralSecondaryFlags

Le champ GeneralSecondaryFlags doit être conforme à la définition fournie dans le modèle DirectoryEntry secondaire générique (voir la [section 6.4.2](#642-generalsecondaryflags-field)) et définit le contenu du champ CustomDefined à réserver.

##### <a name="7721-allocationpossible-field"></a>Champ 7.7.2.1 AllocationPossible

Le champ AllocationPossible doit être conforme à la définition fournie dans le modèle DirectoryEntry secondaire générique (voir la [section 6.4.2.1](#6421-allocationpossible-field)).

Pour l’entrée de répertoire de l’extension de flux, la valeur valide pour ce champ est 0.

##### <a name="7722-nofatchain-field"></a>Champ 7.7.2.2 NoFatChain

Le champ NoFatChain doit être conforme à la définition fournie dans le modèle DirectoryEntry secondaire générique (voir la [section 6.4.2.2](#6422-nofatchain-field)).

#### <a name="773-filename-field"></a>Champ nom du fichier 7.7.3

Le champ de nom de fichier doit contenir une chaîne Unicode, qui est une partie du nom de fichier. Dans l’ordre, les entrées de répertoire existent dans un jeu d’entrées de répertoires de fichiers. les champs de nom de fichier sont concaténés pour former le nom de fichier de l’ensemble d’entrées de répertoires de fichiers. Compte tenu de la longueur du champ de nom de fichier, de 15 caractères et du nombre maximal d’entrées de répertoires de noms de fichiers, 17, la longueur maximale du nom de fichier final est
255.

Le nom de fichier concaténé contient le même jeu de caractères non autorisés que les autres systèmes de fichiers FAT (voir le [tableau 35](#table-35-invalid-filename-characters)). Les implémentations doivent définir les caractères inutilisés des champs de nom de fichier sur la valeur 0000h.

<div id="table-35-invalid-filename-characters" />

**Tableau 35 caractères de nom de fichier non valides**

| **Code de caractère** | **Description** | **Code de caractère** | **Description**   | **Code de caractère** | **Description** |
|--------------------|-----------------|--------------------|-------------------|--------------------|-----------------|
| 0000h              | Code de contrôle    | 0001h              | Code de contrôle      | 0002h              | Code de contrôle    |
| 0003h              | Code de contrôle    | 0004h              | Code de contrôle      | 0005h              | Code de contrôle    |
| 0006h              | Code de contrôle    | 0007h              | Code de contrôle      | 0008h              | Code de contrôle    |
| 0009h              | Code de contrôle    | 000Ah              | Code de contrôle      | 000Bh              | Code de contrôle    |
| 000Ch              | Code de contrôle    | 000Dh              | Code de contrôle      | 000Eh              | Code de contrôle    |
| 000Fh              | Code de contrôle    | 0010h              | Code de contrôle      | 0011h              | Code de contrôle    |
| 0012h              | Code de contrôle    | 0013h              | Code de contrôle      | 0014h              | Code de contrôle    |
| 0015h              | Code de contrôle    | 0016h              | Code de contrôle      | 0017h              | Code de contrôle    |
| 0018h              | Code de contrôle    | 0019h              | Code de contrôle      | 001Ah              | Code de contrôle    |
| 001Bh              | Code de contrôle    | 001Ch              | Code de contrôle      | 001Dh              | Code de contrôle    |
| 001Eh              | Code de contrôle    | 001Fh              | Code de contrôle      | 0022h              | Guillemets  |
| 002Ah              | Astérisque        | 002Fh              | Barre oblique     | 003Ah              | Deux-points           |
| 003Ch              | Signe Inférieur à  | 003Eh              | Signe Supérieur à | 003Fh              | Point d'interrogation   |
| 005Ch              | Barre oblique inverse      | 007Ch              | Barre verticale      |                    |                 |

Les noms de fichiers « . » et « .. » ont la signification spéciale « ce répertoire » et « répertoire conteneur », respectivement. Les implémentations ne doivent pas enregistrer l’un de ces noms de fichiers réservés dans le champ nom de fichier.
Toutefois, les implémentations peuvent générer ces deux noms de fichiers dans des listes de répertoires pour faire référence au répertoire répertorié et au répertoire qui le contient.

Les implémentations peuvent souhaiter limiter les noms de fichiers et de répertoires uniquement au jeu de caractères ASCII. Si c’est le cas, ils doivent limiter leur utilisation de caractères à la plage de caractères valides dans les 128 premières entrées Unicode. Ils doivent toujours stocker les noms de fichiers et de répertoires en Unicode sur le volume et les traduire vers/depuis ASCII/Unicode lors de l’interfaçage avec l’utilisateur.

### <a name="78-vendor-extension-directory-entry"></a>Entrée de répertoire d’extension de fournisseur 7,8

L’entrée de répertoire de l’extension de fournisseur est une entrée d’annuaire secondaire bénigne dans les jeux d’entrées de répertoire de fichiers (voir le [tableau 36](#table-36-vendor-extension-directoryentry)). Un jeu d’entrée de répertoire de fichiers peut contenir un nombre quelconque d’entrées de répertoire d’extension de fournisseur, jusqu’à la limite des entrées de répertoire secondaire, moins le nombre d’autres entrées de répertoire secondaires. En outre, les entrées de répertoire d’extension de fournisseur ne sont valides que si elles ne précèdent pas l’extension de flux et les entrées de répertoire de nom de fichier requises.

Les entrées de répertoire d’extension de fournisseur permettent aux fournisseurs d’avoir des entrées d’annuaire uniques et spécifiques au fournisseur dans des ensembles d’entrées de répertoires de fichiers individuels via le champ VendorGuid (voir [tableau 36](#table-36-vendor-extension-directoryentry)). Les entrées d’annuaire uniques permettent effectivement aux fournisseurs d’étendre le système de fichiers exFAT. Les fournisseurs peuvent définir le contenu du champ VendorDefined (voir le [tableau 36](#table-36-vendor-extension-directoryentry)). Les implémentations de fournisseur peuvent gérer le contenu du champ VendorDefined et peuvent fournir des fonctionnalités spécifiques au fournisseur.

Les implémentations qui ne reconnaissent pas le GUID d’une entrée de répertoire d’extension de fournisseur doivent traiter l’entrée de répertoire de la même façon que toute autre entrée de répertoire secondaire non reconnue (voir la [Section 8,2](#82-implications-of-unrecognized-directory-entries)).

<div id="table-36-vendor-extension-directoryentry" />

**Tableau 36 extension de fournisseur DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nom du champ</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>poids</strong></p></th>
<th><p><strong>Taille</strong></p>
<p><strong>poids</strong></p></th>
<th><strong>Commentaires</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#781-entrytype-field">section 7.8.1</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#782-generalsecondaryflags-field">section 7.8.2</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>VendorGuid</td>
<td>2</td>
<td>16</td>
<td>Ce champ est obligatoire et la <a href="#783-vendorguid-field">section 7.8.3</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>VendorDefined</td>
<td>18</td>
<td>14</td>
<td>Ce champ est obligatoire et les fournisseurs peuvent définir son contenu.</td>
</tr>
</tbody>
</table>

#### <a name="781-entrytype-field"></a>Champ 7.8.1 EntryType

Le champ EntryType doit être conforme à la définition fournie dans le modèle DirectoryEntry secondaire générique (voir la [section 6.4.1](#641-entrytype-field)).

##### <a name="7811-typecode-field"></a>Champ TypeCode 7.8.1.1

Le champ TypeCode est conforme à la définition fournie dans le modèle DirectoryEntry secondaire générique (voir la [section 6.4.1.1](#6411-typecode-field)).

Pour l’entrée du répertoire de l’extension du fournisseur, la valeur valide pour ce champ est 0.

##### <a name="7812-typeimportance-field"></a>Champ 7.8.1.2 TypeImportance

Le champ TypeImportance doit être conforme à la définition fournie dans le modèle DirectoryEntry secondaire générique (voir la [section 6.4.1.2](#6412-typeimportance-field)).

Pour l’entrée du répertoire de l’extension du fournisseur, la valeur valide pour ce champ est 1.

##### <a name="7813-typecategory-field"></a>Champ 7.8.1.3 TypeCategory

Le champ TypeCategory doit être conforme à la définition fournie dans le modèle DirectoryEntry secondaire générique (voir la [section 6.4.1.3](#6413-typecategory-field)).

##### <a name="7814-inuse-field"></a>Champ 7.8.1.4 InUse

Le champ InUse doit se conformer à la définition fournie dans le modèle DirectoryEntry secondaire générique (voir la [section 6.4.1.4](#6414-inuse-field)).

#### <a name="782-generalsecondaryflags-field"></a>Champ 7.8.2 GeneralSecondaryFlags

Le champ GeneralSecondaryFlags doit être conforme à la définition fournie dans le modèle DirectoryEntry secondaire générique (voir la [section 6.4.2](#642-generalsecondaryflags-field)) et définit le contenu du champ CustomDefined à réserver.

##### <a name="7821-allocationpossible-field"></a>Champ 7.8.2.1 AllocationPossible

Le champ AllocationPossible doit être conforme à la définition fournie dans le modèle DirectoryEntry secondaire générique (voir la [section 6.4.2.1](#6421-allocationpossible-field)).

Pour l’entrée du répertoire de l’extension du fournisseur, la valeur valide pour ce champ est 0.

##### <a name="7822-nofatchain-field"></a>Champ 7.8.2.2 NoFatChain

Le champ NoFatChain doit être conforme à la définition fournie dans le modèle DirectoryEntry secondaire générique (voir la [section 6.4.2.2](#6422-nofatchain-field)).

#### <a name="783-vendorguid-field"></a>Champ 7.8.3 VendorGuid

Le champ VendorGuid doit contenir un GUID qui identifie de façon unique l’extension de fournisseur donnée.

Toutes les valeurs possibles pour ce champ sont valides, à l’exception du GUID null, qui est {00000000-0000-0000-0000-000000000000} . Toutefois, les fournisseurs doivent utiliser un outil de génération de GUID, tel que GuidGen.exe, pour sélectionner un GUID lors de la définition de leurs extensions.

La valeur de ce champ détermine la structure spécifique au fournisseur du champ VendorDefined.

### <a name="79-vendor-allocation-directory-entry"></a>Entrée de répertoire d’allocation de fournisseurs 7,9

L’entrée Directory allocation Directory est une entrée d’annuaire secondaire bénigne dans les jeux d’entrées de répertoires de fichiers (voir le [tableau 37](#table-37-vendor-allocation-directoryentry)). Un jeu d’entrée de répertoire de fichiers peut contenir un nombre quelconque d’entrées de répertoire d’allocation de fournisseurs, jusqu’à la limite des entrées de répertoire secondaire, moins le nombre d’autres entrées de répertoire secondaires. En outre, les entrées de répertoire d’allocation de fournisseur ne sont valides que si elles ne précèdent pas les entrées d’extension de flux et de nom de fichier requises.

Les entrées de répertoire d’allocation de fournisseur permettent aux fournisseurs d’avoir des entrées d’annuaire uniques et spécifiques au fournisseur dans des ensembles d’entrées de répertoires de fichiers individuels via le champ VendorGuid (voir [tableau 37](#table-37-vendor-allocation-directoryentry)). Les entrées d’annuaire uniques permettent effectivement aux fournisseurs d’étendre le système de fichiers exFAT. Les fournisseurs peuvent définir le contenu des clusters associés, le cas échéant. Les implémentations de fournisseurs peuvent gérer le contenu des clusters associés, le cas échéant, et peuvent fournir des fonctionnalités spécifiques au fournisseur.

Les implémentations qui ne reconnaissent pas le GUID d’une entrée de répertoire d’allocation de fournisseur doivent traiter l’entrée de répertoire de la même façon que toute autre entrée de répertoire secondaire non reconnue (voir la [Section 8,2](#82-implications-of-unrecognized-directory-entries)).

<div id="table-37-vendor-allocation-directoryentry" />

**Tableau 37 allocation des fournisseurs DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nom du champ</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>poids</strong></p></th>
<th><p><strong>Taille</strong></p>
<p><strong>poids</strong></p></th>
<th><strong>Commentaires</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#791-entrytype-field">section 7.9.1</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>Ce champ est obligatoire et la <a href="#792-generalsecondaryflags-field">section 7.9.2</a> définit son contenu.</td>
</tr>
<tr class="odd">
<td>VendorGuid</td>
<td>2</td>
<td>16</td>
<td>Ce champ est obligatoire et la <a href="#793-vendorguid-field">section 7.9.3</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>VendorDefined</td>
<td>18</td>
<td>2</td>
<td>Ce champ est obligatoire et les fournisseurs peuvent définir son contenu.</td>
</tr>
<tr class="odd">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Ce champ est obligatoire et la <a href="#794-firstcluster-field">section 7.9.4</a> définit son contenu.</td>
</tr>
<tr class="even">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Ce champ est obligatoire et la <a href="#795-datalength-field">section 7.9.5</a> définit son contenu.</td>
</tr>
</tbody>
</table>

#### <a name="791-entrytype-field"></a>Champ 7.9.1 EntryType

Le champ EntryType doit être conforme à la définition fournie dans le modèle DirectoryEntry secondaire générique (voir la [section 6.4.1](#641-entrytype-field)).

##### <a name="7911-typecode-field"></a>Champ TypeCode 7.9.1.1

Le champ TypeCode est conforme à la définition fournie dans le modèle DirectoryEntry secondaire générique (voir la [section 6.4.1.1](#6411-typecode-field)).

Pour l’entrée de répertoire d’allocation du fournisseur, la valeur valide pour ce champ est 1.

##### <a name="7912-typeimportance-field"></a>Champ 7.9.1.2 TypeImportance

Le champ TypeImportance doit être conforme à la définition fournie dans le modèle DirectoryEntry secondaire générique (voir la [section 6.4.1.2](#6412-typeimportance-field)).

Pour l’entrée de répertoire d’allocation du fournisseur, la valeur valide pour ce champ est 1.

##### <a name="7913-typecategory-field"></a>Champ 7.9.1.3 TypeCategory

Le champ TypeCategory doit être conforme à la définition fournie dans le modèle DirectoryEntry secondaire générique (voir la [section 6.4.1.3](#6413-typecategory-field)).

##### <a name="7914-inuse-field"></a>Champ 7.9.1.4 InUse

Le champ InUse doit se conformer à la définition fournie dans le modèle DirectoryEntry secondaire générique (voir la [section 6.4.1.4](#6414-inuse-field)).

#### <a name="792-generalsecondaryflags-field"></a>Champ 7.9.2 GeneralSecondaryFlags

Le champ GeneralSecondaryFlags doit être conforme à la définition fournie dans le modèle DirectoryEntry secondaire générique (voir la [section 6.4.2](#642-generalsecondaryflags-field)) et définit le contenu du champ CustomDefined à réserver.

##### <a name="7921-allocationpossible-field"></a>Champ 7.9.2.1 AllocationPossible

Le champ AllocationPossible doit être conforme à la définition fournie dans le modèle DirectoryEntry secondaire générique (voir la [section 6.4.2.1](#6421-allocationpossible-field)).

Pour l’entrée de répertoire d’allocation du fournisseur, la valeur valide pour ce champ est 1.

##### <a name="7922-nofatchain-field"></a>Champ 7.9.2.2 NoFatChain

Le champ NoFatChain doit être conforme à la définition fournie dans le modèle DirectoryEntry secondaire générique (voir la [section 6.4.2.2](#6422-nofatchain-field)).

#### <a name="793-vendorguid-field"></a>Champ 7.9.3 VendorGuid

Le champ VendorGuid doit contenir un GUID qui identifie de façon unique l’allocation de fournisseur donnée.

Toutes les valeurs possibles pour ce champ sont valides, à l’exception du GUID null, qui est {00000000-0000-0000-0000-000000000000} . Toutefois, les fournisseurs doivent utiliser un outil de génération de GUID, tel que GuidGen.exe, pour sélectionner un GUID lors de la définition de leurs extensions.

La valeur de ce champ détermine la structure spécifique au fournisseur du contenu des clusters associés, le cas échéant.

#### <a name="794-firstcluster-field"></a>Champ 7.9.4 FirstCluster

Le champ FirstCluster doit être conforme à la définition fournie dans le modèle DirectoryEntry secondaire générique (voir la [section 6.4.3](#643-firstcluster-field)).

#### <a name="795-datalength-field"></a>Champ 7.9.5 DataLength

Le champ DataLength doit se conformer à la définition fournie dans le modèle DirectoryEntry secondaire générique (voir la [section 6.4.4](#644-datalength-field)).

### <a name="710-texfat-padding-directory-entry"></a>Entrée de répertoire de remplissage 7,10 TexFAT

Cette spécification, version de base du système de fichiers de la révision 1,00, ne définit pas l’entrée de répertoire de remplissage TexFAT. Toutefois, son code de type est 1 et son type d’importance est 1. Les implémentations de cette spécification traitent les entrées de répertoire de remplissage TexFAT comme n’importe quelle autre entrée de répertoire primaire non reconnue, les implémentations ne doivent pas déplacer les entrées de répertoire de remplissage TexFAT.

## <a name="8-implementation-notes"></a>8 remarques sur l’implémentation

### <a name="81-recommended-write-ordering"></a>8,1 ordre des écritures recommandé

Les implémentations doivent garantir que le volume est aussi résilient que possible pour les pannes de courant et d’autres défaillances inévitables. Lorsque vous créez de nouvelles entrées de répertoire ou modifiez des allocations de cluster, les implémentations doivent généralement respecter cet ordre d’écriture :

1. Définissez la valeur du champ VolumeDirty sur 1.

2. Mettre à jour la FAT active, si nécessaire

3. Mettre à jour la bitmap d’allocation active

4. Créer ou mettre à jour l’entrée d’annuaire, si nécessaire

5. Désactivez la valeur du champ VolumeDirty à 0, si sa valeur avant la première étape était 0

Lors de la suppression des entrées de répertoire ou de la libération des allocations de cluster, les implémentations doivent respecter cet ordre d’écriture :

1. Définissez la valeur du champ VolumeDirty sur 1.

2. Supprimer ou mettre à jour l’entrée d’annuaire, si nécessaire

3. Mettre à jour la FAT active, si nécessaire

4. Mettre à jour la bitmap d’allocation active

5. Désactivez la valeur du champ VolumeDirty à 0, si sa valeur avant la première étape était 0

### <a name="82-implications-of-unrecognized-directory-entries"></a>8,2 implications des entrées de répertoire non reconnues

Les futures spécifications exFAT du même numéro de révision majeure, 1 et un numéro de révision mineur supérieur à 0, peuvent définir de nouvelles entrées de répertoire secondaire, critique et secondaire bénignes. Seules les spécifications exFAT d’un numéro de révision majeure plus élevé peuvent définir de nouvelles entrées de répertoire principales critiques. Les implémentations de cette spécification, version 1,00 du système de fichiers de la révision exFAT, doivent être en mesure de monter et d’accéder à un volume exFAT de numéro de révision majeur 1 et à un numéro de révision mineur. Cela présente des scénarios dans lesquels une implémentation peut rencontrer des entrées de répertoire qu’elle ne reconnaît pas. Les éléments suivants décrivent les implications de ces scénarios :

1. La présence d’entrées d’annuaire principales critiques non reconnues dans le répertoire racine rend le volume non valide. La présence d’une entrée d’annuaire principale critique, à l’exception des entrées de répertoire de fichiers, dans n’importe quel répertoire non racine, rend le répertoire d’hébergement non valide.

2. Les implémentations ne doivent pas modifier les entrées de répertoire principal bénignes non reconnues ou les allocations de cluster associées. Toutefois, lors de la suppression d’un répertoire, et uniquement lors de la suppression d’un répertoire, les implémentations doivent supprimer les entrées de répertoire primaire non reconnues et libérer toutes les allocations de cluster associées, le cas échéant.

3. Les implémentations ne doivent pas modifier les entrées de répertoire secondaires critiques non reconnues ou les allocations de cluster associées. La présence d’une ou de plusieurs entrées d’annuaire secondaires critiques non reconnues dans un jeu d’entrées de répertoire rend le jeu d’entrées de répertoire entier non reconnu. Lors de la suppression d’un jeu d’entrées de répertoire qui contient une ou plusieurs entrées de répertoire secondaires critiques non reconnues, les implémentations doivent libérer toutes les allocations de cluster, le cas échéant, associées à des entrées d’annuaire secondaires critiques non reconnues.
   En outre, si le jeu d’entrées de répertoire décrit un répertoire, les implémentations peuvent :

   - Parcourir le répertoire

   - Énumérer les entrées d’annuaire qu’il contient

   - Supprimer les entrées de répertoire contenues

   - Déplacer les entrées de répertoire contenu dans un autre répertoire

   Toutefois, les implémentations ne doivent pas :

   - Modifiez les entrées de répertoire contenues, à l’exception de supprimer, comme indiqué

   - Créer des entrées de répertoire contenues

   - Ouvrir les entrées de répertoire contenues, sauf traverser et énumérer, comme indiqué

4. Les implémentations ne doivent pas modifier les entrées de répertoire secondaires bénignes non reconnues ou les allocations de cluster associées.
   Les implémentations doivent ignorer les entrées de répertoire secondaire non reconnues. Lors de la suppression d’un jeu d’entrées de répertoire, les implémentations doivent libérer toutes les allocations de cluster, le cas échéant, associées à des entrées d’annuaire secondaire non reconnues.

## <a name="9-file-system-limits"></a>9 limites du système de fichiers

### <a name="91-sector-size-limits"></a>9,1 limites de taille de secteur

Le champ BytesPerSectorShift définit les limites de taille de secteur inférieures et supérieures (qui prend la valeur **limite inférieure : 512 octets ; limite supérieure : 4 096 octets**).

### <a name="92-cluster-size-limits"></a>9,2 limites de taille de cluster

Le champ SectorsPerClusterShift définit les limites inférieures et supérieures de la taille du cluster (**limite inférieure : 1 secteur ; limite supérieure : 25--BytesPerSectorShift secteurs**, qui prend la valeur 32 Mo).

### <a name="93-cluster-heap-size-limits"></a>Limites de taille du tas de cluster 9,3

Le segment de mémoire du cluster doit contenir au moins assez d’espace pour héberger les structures de système de fichiers de base suivantes : le répertoire racine, toutes les bitmaps d’allocation et la table de cas.

La limite inférieure de la taille du tas de cluster est une fonction de la limite de taille inférieure de chacune des structures de système de fichiers de base qui résident dans le segment de mémoire du cluster. Même en fonction du plus petit cluster possible (512 octets), chacune des structures de système de fichiers de base n’a besoin que d’un seul cluster. Par conséquent, la **limite inférieure est : 2 + clusters NumberOfFats**, qui correspond à 3 ou 4 clusters, en fonction de la valeur du champ NumberOfFats.

La limite supérieure de la taille du segment de mémoire est une fonction simple du nombre maximal possible de clusters, que le champ Clustercount, définit (**limite supérieure : 2 <sup>32</sup>à 11 clusters**). Quelle que soit la taille du cluster, un tel segment de mémoire a suffisamment d’espace pour au moins héberger les structures de système de fichiers de base.

### <a name="94-volume-size-limits"></a>9,4 limites de taille de volume

Le champ VolumeLength définit les limites de taille de volume inférieures et supérieures (limite inférieure : **2 <sup>20</sup>/2 secteurs <sup>BytesPerSectorShift</sup>**, qui prend la valeur 1 Mo ; **limite supérieure : 2 <sup>64</sup>-1 secteurs**, qui, étant donné la plus grande taille de secteur possible, est évalué à environ 64ZB). Toutefois, cette spécification ne recommande pas plus de deux clusters de<sup>24</sup>-2 dans le segment de mémoire du cluster (voir la [section 3.1.9](#319-clustercount-field)). Par conséquent, la limite supérieure recommandée pour un volume est : ClusterHeapOffset + (2<sup>24</sup>-2) \* 2<sup>SectorsPerClusterShift</sup>. Étant donné la plus grande taille de cluster possible, 32 Mo et en supposant que ClusterHeapOffset est 96 Mo (espace suffisant pour les régions de démarrage principales et de sauvegarde et uniquement pour le premier système FAT), la limite supérieure recommandée d’un volume est égale à environ 512TB.

### <a name="95-directory-size-limits"></a>9,5 limites de taille de répertoire

Le champ DataLength de l’entrée de répertoire de l’extension de flux définit les limites de taille de répertoire inférieure et supérieure (**limite inférieure : 0 octets ; limite supérieure : 256 Mo**). Cela signifie qu’un répertoire peut héberger jusqu’à 8 388 608 entrées d’annuaire (chaque entrée de répertoire consomme 32 octets). Étant donné le plus petit ensemble d’entrées de répertoires de fichiers possible, trois entrées de répertoire, un répertoire peut héberger jusqu’à 2 796 202 fichiers.

## <a name="10-appendix"></a>10 Annexe

### <a name="101-globally-unique-identifiers-guids"></a>10,1 identificateurs globaux uniques (GUID)

Un GUID est l’implémentation Microsoft d’un identificateur universellement unique. Un GUID est une valeur 128 bits composée d’un groupe de 8 chiffres hexadécimaux, suivi de trois groupes de 4 chiffres hexadécimaux chacun, suivis d’un groupe de 12 chiffres hexadécimaux, par exemple {6B29FC40-CA47-1067-B31D-00DD010662DA}, (voir la [Table 38](#table-38-guid-structure)).

<div id="table-38-guid-structure" />

**Table 38 structure GUID**

<table>
<thead>
<tr class="header">
<th><strong>Nom du champ</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>poids</strong></p></th>
<th><p><strong>Taille</strong></p>
<p><strong>bits</strong></p></th>
<th><strong>Commentaires</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Data1</td>
<td>0</td>
<td>4</td>
<td>Ce champ est obligatoire et contient les quatre octets du premier groupe du GUID (6B29FC40h de l’exemple).</td>
</tr>
<tr class="even">
<td>Data2</td>
<td>4</td>
<td>2</td>
<td>Ce champ est obligatoire et contient les deux octets du deuxième groupe du GUID (CA47h de l’exemple).</td>
</tr>
<tr class="odd">
<td>Data3</td>
<td>6</td>
<td>2</td>
<td>Ce champ est obligatoire et contient les deux octets du troisième groupe du GUID (1067h de l’exemple).</td>
</tr>
<tr class="even">
<td>Data4 [0]</td>
<td>8</td>
<td>1</td>
<td>Ce champ est obligatoire et contient l’octet le plus significatif du quatrième groupe du GUID (B3h de l’exemple).</td>
</tr>
<tr class="odd">
<td>Data4 [1]</td>
<td>9</td>
<td>1</td>
<td>Ce champ est obligatoire et contient l’octet le moins significatif du quatrième groupe du GUID (1Dh de l’exemple).</td>
</tr>
<tr class="even">
<td>Data4 [2]</td>
<td>10</td>
<td>1</td>
<td>Ce champ est obligatoire et contient le premier octet du cinquième groupe du GUID (00h de l’exemple).</td>
</tr>
<tr class="odd">
<td>Data4 [3]</td>
<td>11</td>
<td>1</td>
<td>Ce champ est obligatoire et contient le deuxième octet du cinquième groupe du GUID (DDh de l’exemple).</td>
</tr>
<tr class="even">
<td>Data4 [4]</td>
<td>12</td>
<td>1</td>
<td>Ce champ est obligatoire et contient le troisième octet du cinquième groupe du GUID (01H de l’exemple).</td>
</tr>
<tr class="odd">
<td>Data4 [5]</td>
<td>13</td>
<td>1</td>
<td>Ce champ est obligatoire et contient le quatrième octet du cinquième groupe du GUID (06h de l’exemple).</td>
</tr>
<tr class="even">
<td>Data4 [6]</td>
<td>14</td>
<td>1</td>
<td>Ce champ est obligatoire et contient le cinquième octet du cinquième groupe du GUID (62h de l’exemple).</td>
</tr>
<tr class="odd">
<td>Data4 [7]</td>
<td>15</td>
<td>1</td>
<td>Ce champ est obligatoire et contient le sixième octet du cinquième groupe du GUID (DAh de l’exemple).</td>
</tr>
</tbody>
</table>

### <a name="102-partition-tables"></a>10,2 tables de partition

Pour garantir l’interopérabilité des volumes exFAT dans un large éventail de scénarios d’utilisation, les implémentations doivent utiliser le type de partition 07h pour le stockage partitionné MBR et le GUID de partition {EBD0A0A2-B9E5-4433-87C0-68B6B72699C7} pour le stockage partitionné GPT.

## <a name="11-documentation-change-history"></a>11 historique des modifications de la documentation

Le tableau 39 décrit l’historique des versions, les corrections, les ajouts, les suppressions et les clarifications de ce document.

<div id="table-39-documentation-change-history" />

**Tableau 39 historique des modifications de la documentation**

<table>
<thead>
<tr class="header">
<th><strong>Date</strong></th>
<th><strong>Description de la modification</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>08-Jan-2008</td>
<td><p>Première version de la spécification de base, qui comprend :</p>
<blockquote>
<p>Section 1, présentation</p>
<p>Section 2,<br />
Structure du volume</p>
<p>Section 3, régions de démarrage principales et de sauvegarde</p>
<p>Section 4, zone de table d’allocation de fichiers</p>
<p>Section 5, région de données</p>
<p>Section 6, structure de répertoires</p>
<p>Section 7, définitions d’entrée de répertoire</p>
<p>Section 8, remarques sur l’implémentation</p>
<p>Section 9, limites du système de fichiers</p>
<p>Section 10, annexe</p>
</blockquote></td>
</tr>
<tr class="even">
<td>08-juin-2008</td>
<td><p>Deuxième version de la spécification de base, qui comprend les modifications suivantes :</p>
<blockquote>
<p>Ajout de la section 11,<br />
Historique des modifications de la documentation</p>
<p>Ajout des entrées de l’extension de fournisseur et des répertoires d’allocation des fournisseurs dans les sections 7,8 et 7,9</p>
<p>Ajout de la table de cas recommandée dans les sections 7.2.5 et 7.2.5.1</p>
<p>Ajout des champs UtcOffset dans la section 7,4 et ajout de l’acronyme UTC dans la section 1,3</p>
<p>Correction de la taille du champ CustomDefined dans la table 19</p>
<p>Correction de la plage valide de valeurs NameLength dans la section 7.6.3</p>
<p>Correction et clarification des champs timestamp et 10msIncrement dans la section 7,4</p>
<p>Clarification de la structure de paramètres null dans la section 3,3</p>
<p>Clarification de la signification des valeurs du champ NoFatChain dans la section 6.3.4.2</p>
<p>Clarification de la signification des valeurs du champ DataLength dans la section 6.2.3</p>
<p>Clarification du champ VolumeDirty dans la section 3.1.13.2 et ordre recommandé des écritures dans la section 8,1</p>
<p>Clarification du champ MediaFailure dans la section 3.1.13.3</p>
</blockquote></td>
</tr>
<tr class="odd">
<td>01-Oct-2008</td>
<td><p>Troisième version de la spécification de base, qui comprend les modifications suivantes :</p>
<blockquote>
<p>L’ajout de doit et peut avoir des explications sur les champs</p>
<p>Ajout de la définition UTC dans le tableau 2, section 1,3</p>
<p>Modification des sections 1,5 pour garantir l’alignement avec le document de spécification TexFAT.</p>
<p>Clarification de la restriction selon laquelle seul Microsoft peut définir la disposition des entrées d’annuaire dans la section 6,2</p>
<p>Ajout de clarification indiquant que le champ FirstCluster doit être égal à zéro si DataLength est égal à zéro et NoFatChain est défini sur la section 6.3.5 et la section 6.4.3</p>
<p>Clarification de la configuration requise pour les entrées d’annuaire de fichiers valides dans la section 7,4</p>
<p>Ajout de la spécification de noms de fichiers et de répertoires uniques à la section 7,7</p>
<p>Ajout de la note d’implémentation pour ASCII à la fin de la section 7.7.3</p>
</blockquote></td>
</tr>
<tr class="even">
<td>01-Jan-2009</td>
<td><p>Quatrième version de la spécification de base, qui comprend les modifications suivantes :</p>
<blockquote>
<p>Suppression des références aux entrées de Windows CE Access Control</p>
<p>Ajout de clarifications à la section 7.2.5.1 pour exiger explicitement une table de cas complète</p>
</blockquote></td>
</tr>
<tr class="odd">
<td>02-Sep-2009</td>
<td><p>Cinquième version de la spécification de base, qui comprend les modifications suivantes :</p>
<blockquote>
<p>Modification de la mise en forme des documents pour permettre une meilleure conversion PDF</p>
</blockquote></td>
</tr>
<tr class="even">
<td>24-fév-2010</td>
<td><p>Sixième version de la spécification de base, qui comprend les modifications suivantes :</p>
<blockquote>
<p>Instruction incorrecte modifiée : « le champ FirstCluster doit être égal à zéro si DataLength est égal à zéro et NoFatChain est défini » dans la section 6.3.5 et la section 6.4.3 sur « si le bit NoFatChain est 1, alors FirstCluster doit pointer vers un cluster valide dans le tas de cluster » pour préciser qu’il doit y avoir une allocation valide si le bit NoFatChain est défini.</p>
<p>Ajout de «si le bit NoFatChain est 1, DataLength ne doit pas être égal à zéro. Si le champ FirstCluster est égal à zéro, DataLength doit également avoir la valeur zéro» pour la section 6.3.6 et la section 6.4.4 pour clarifier la validité de l’allocation si le bit NoFatChain est défini.</p>
<p>Mention de droits d’auteur mise à jour 2010</p>
</blockquote></td>
</tr>
<tr class="odd">
<td>26-août-2019</td>
<td><p>Septième version de la spécification de base, qui comprend les modifications suivantes :</p>
<blockquote>
<p>Mise à jour des conditions juridiques relatives à la spécification, notamment :</p>
<p>Suppression de l’avis confidentiel Microsoft</p>
<p>Section de contrat de licence de la documentation technique de Microsoft Corporation</p>
<p>Mention de droits d’auteur mise à jour 2019</p>
</blockquote></td>
</tr>
</tbody>
</table>
