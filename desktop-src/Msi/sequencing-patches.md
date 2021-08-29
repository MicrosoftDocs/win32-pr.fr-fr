---
description: à partir de Windows Installer 3,0, les auteurs peuvent ajouter des informations de séquencement de correctifs à la base de données des packages de correctifs dans la table MsiPatchSequence.
ms.assetid: 9cdcb25f-2c3d-411e-9aae-bdd52df38a97
title: Mise en séquence des correctifs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f61a72c8122f9f3679cf691f88bc3d9bc952732b9d638ca838f9992068b1c24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040008"
---
# <a name="sequencing-patches"></a>Mise en séquence des correctifs

à partir de Windows Installer 3,0, les auteurs peuvent ajouter des informations de séquencement de correctifs à la base de données des packages de correctifs dans la table [MsiPatchSequence](msipatchsequence-table.md) . Le programme d’installation peut utiliser ces informations pour déterminer les correctifs applicables à un package d’installation, pour déterminer la meilleure séquence de mise à jour corrective et pour installer les correctifs dans un ordre constant, indépendamment de l’ordre dans lequel ils sont fournis au système.

**Windows Installer 2,0 :** Non pris en charge. Windows les versions du programme d’installation antérieures à Windows Installer 3,0 installent les correctifs dans l’ordre dans lequel elles sont fournies au système, qu’elles contiennent ou non une table [MsiPatchSequence](msipatchsequence-table.md) .

Les éléments suivants sont requis pour utiliser la fonctionnalité de séquencement des correctifs.

-   Les [packages de correctifs](patch-packages.md) (fichiers. msp) doivent avoir une table [MsiPatchSequence](msipatchsequence-table.md) contenant les informations de séquencement. Le programme d’installation installe les correctifs qui n’ont pas de table MsiPatchSequence dans l’ordre dans lequel ils sont fournis au système.
-   les correctifs sont installés à l’aide de Windows Installer 3,0 ou version ultérieure.

Windows La version 3,0 du programme d’installation offre les fonctions suivantes que les applications peuvent utiliser pour déterminer la meilleure séquence de mise à jour corrective.

-   La fonction [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) prend une liste de correctifs et détermine dans quelle séquence ils peuvent être appliqués à un produit installé. Cette fonction tient compte de tous les correctifs ou produits qui ont déjà été installés sur le système.
-   La fonction [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) prend une liste de correctifs et détermine dans quelle séquence ils peuvent être appliqués à un produit installé. Cette fonction ne prend pas en compte les correctifs ou les produits déjà installés sur le système.

Windows Le programme d’installation 3,0 peut appliquer plusieurs correctifs à un produit dans une seule installation de mise à jour corrective. Le groupe de correctifs peut contenir des correctifs qui incluent la mise à jour corrective des informations de séquence (une table [MsiPatchSequence](msipatchsequence-table.md) ) et les correctifs qui ne le sont pas. le Windows Installer installe les packages de correctifs sans ce tableau dans l’ordre dans lequel ils sont fournis au système. Le programme d’installation compte pour les packages de correctifs qui n’ont pas de table MsiPatchSequence, mais qui ont été marqués comme des correctifs obsolètes ou remplacés par la méthode décrite dans la section suivante.

quand Windows Installer version 3,0 installe plusieurs correctifs, elle effectue les étapes suivantes pour déterminer l’ordre dans lequel les correctifs individuels sont appliqués au produit :

1.  Les correctifs installés sans table [MsiPatchSequence](msipatchsequence-table.md) sont placés dans la séquence dans l’ordre dans lequel ils ont été appliqués au produit. Le premier correctif appliqué est placé en premier dans la séquence.
2.  Les nouveaux correctifs sans [table MsiPatchSequence](msipatchsequence-table.md) sont placés dans la séquence. Ces correctifs sont appliqués par l’installation de mise à jour corrective actuelle. Ils sont placés dans l’ordre dans lequel ils sont fournis au système et placés après tous les correctifs de l’étape 1.
3.  Les correctifs obsolètes sont éliminés de la séquence des correctifs.
    > [!Note]  
    > Un package de correctifs peut spécifier dans la propriété [**Résumé du numéro de révision**](revision-number-summary.md) une liste explicite des correctifs obsolètes à supprimer par le correctif. cette liste est destinée à être utilisée par les versions Windows Installer antérieures à la version 3,0. Windows La version 3,0 du programme d’installation supprime les correctifs marqués comme obsolètes de la séquence, uniquement si les correctifs ne disposent pas de la [table MsiPatchSequence](msipatchsequence-table.md).

     

4.  Le programme d’installation parcourt la séquence de mise à jour corrective et détermine quels correctifs sont applicables dans la séquence donnée. Lorsque plusieurs correctifs sont appliqués à un produit, chaque correctif de la séquence transforme également la base de données d’installation du produit (fichier .msi). Un correctif est applicable dans une séquence particulière uniquement si sa transformation de base de données est capable de prendre le [Code du produit](product-codes.md), la [**version**](productversion.md), la [**langue**](productlanguage.md)et la [**UpgradeCode**](upgradecode.md) qui résultent de l’application des transformations de tous les [packages de correctifs](patch-packages.md) précédents à la base de données du produit. Le programme d’installation élimine tout correctif inapplicable de la séquence.
5.  Le programme d’installation commence à placer les correctifs dont les informations de séquencement sont dans leur table [MsiPatchSequence](msipatchsequence-table.md) . Les correctifs de [mise à niveau mineurs](minor-upgrades.md) qui comportent la table MsiPatchSequence sont placés dans la séquence après les correctifs qui ont été séquencés au cours des étapes précédentes et dans l’ordre de leurs versions les plus anciennes et les plus élevées après leur mise à niveau. Windows Le programme d’installation élimine ensuite les correctifs de mise à niveau mineurs qui ne sont pas applicables dans cette séquence.
6.  Les correctifs de [petite mise à jour](small-updates.md) ciblant des [mises à niveau mineures](minor-upgrades.md) avec une table [MsiPatchSequence](msipatchsequence-table.md) sont affectés à la version la plus récente du correctif de mise à niveau mineure dans la séquence.
7.  Tous les correctifs de [mise à jour de petite taille](small-updates.md) qui ne sont pas affectés après les étapes précédentes, et qui ont la table [MsiPatchSequence](msipatchsequence-table.md) , sont placés dans la séquence avant la première [mise à niveau mineure](minor-upgrades.md) contenant la table MsiPatchSequence, et après la .msi base de données d’installation et les correctifs sans la table MsiPatchSequence. Windows Le programme d’installation élimine ensuite les correctifs de mise à jour de petite taille qui ne sont pas applicables dans cette séquence.
8.  Windows La version 3,0 du programme d’installation élimine les correctifs remplacés de la séquence. Lorsqu’un correctif remplace des correctifs qui se produisent plus tôt dans la séquence de correctifs, le correctif contient tous les correctifs des correctifs précédents. Les correctifs antérieurs ne sont plus nécessaires. le Windows Installer requiert les informations de la table [MsiPatchSequence](msipatchsequence-table.md) pour éliminer les correctifs remplacés.
    > [!Note]  
    > Les correctifs destinés à remplacer un ensemble antérieur de correctifs doivent être créés pour remplacer les correctifs antérieurs dans toutes les familles de correctifs. Les correctifs de [petite taille](small-updates.md) peuvent uniquement remplacer les petites mises à jour. Les [mises à niveau mineures](minor-upgrades.md) peuvent remplacer les petites mises à jour et les autres mises à niveau mineures.

     

9.  Les [mises à jour de petite taille](small-updates.md) qui contiennent des tables [MsiPatchSequence](msipatchsequence-table.md) sont séquencées dans les versions de produit en fonction des informations de séquencement dans leurs tables MsiPatchSequence. Cela détermine la séquence de mise à jour corrective finale.

Un correctif qui ne doit plus être utilisé peut être éliminé de la séquence de mise à jour corrective. Pour plus d’informations sur la façon d’éliminer les correctifs de la séquence de mise à jour corrective, consultez [élimination des correctifs](eliminating-patches.md).

Pour obtenir un exemple de la façon dont la table [MsiPatchSequence](msipatchsequence-table.md) peut être utilisée pour appliquer des correctifs dans l’ordre dans lequel ils sont créés, consultez l’exemple de mise à [jour corrective multiple](multiple-patching-example.md).

 

 



