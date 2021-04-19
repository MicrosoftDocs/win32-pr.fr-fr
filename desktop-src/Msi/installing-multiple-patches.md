---
description: À partir de Windows Installer 3,0, plusieurs correctifs peuvent être appliqués à un produit dans un ordre constant, quelle que soit l’ordre dans lequel les correctifs sont fournis au système.
ms.assetid: 10af1857-d59f-490d-9b50-49619b1e892c
title: Installation de plusieurs correctifs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d4edb8d085ede6aee81690bf67bd9c5e19780ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524516"
---
# <a name="installing-multiple-patches"></a>Installation de plusieurs correctifs

À partir de Windows Installer 3,0, plusieurs correctifs peuvent être appliqués à un produit dans un ordre constant, quelle que soit l’ordre dans lequel les correctifs sont fournis au système.

**Windows Installer 2,0 :** Non pris en charge. Windows Installer versions antérieures à la version 3,0 installent toujours les correctifs dans l’ordre dans lequel elles sont fournies au système.

**Windows Installer 3,0 et versions ultérieures :** Le programme d’installation peut utiliser les informations fournies dans le tableau [MsiPatchSequence](msipatchsequence-table.md) pour déterminer les correctifs applicables au package Windows Installer et l’ordre d’application des correctifs. Les applications peuvent utiliser les fonctions [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) et [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) .

La fonction [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) détermine les correctifs qui s’appliquent au package Windows Installer et dans quelle séquence. La fonction peut tenir compte des correctifs remplacés ou obsolètes. Cette fonction ne prend pas en compte les produits ou les correctifs installés sur le système qui ne sont pas spécifiés dans le jeu.

La fonction de séquence [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) peut déterminer la meilleure séquence d’application pour les correctifs pour un produit installé spécifié. Cette fonction compte les correctifs qui ont déjà été appliqués au produit et les comptes des correctifs obsolètes et remplacés.

Lorsque le package de correctifs n’a pas de table [MsiPatchSequence](msipatchsequence-table.md) , le programme d’installation applique toujours les correctifs dans l’ordre dans lequel ils sont fournis au système.

Lorsque le package de correctifs contient un mélange de correctifs avec des informations de séquence dans la table [MsiPatchSequence](msipatchsequence-table.md) et certains correctifs sans ces informations, la version 3,0 de Windows Installer séquence les correctifs dans l’ordre décrit dans la section suivante : séquencement des [correctifs](sequencing-patches.md).

Un package Windows Installer ne peut pas installer plus de 127 correctifs lors de l’installation ou de la mise à jour d’une application. Lorsque de nombreuses mises à jour sont nécessaires, elles doivent être combinées et les correctifs obsolètes précédents doivent être éliminés de la séquence de mise à jour corrective.

Un correctif qui ne doit pas être utilisé peut être éliminé de la séquence de mise à jour corrective. Cela empêche l’application du correctif lorsque l’application cible est corrigée. Cela est différent de la suppression d’un correctif qui a déjà été appliqué à une application. Pour plus d’informations sur la suppression des correctifs de la séquence de mise à jour corrective, consultez [élimination](eliminating-patches.md)des correctifs. Pour plus d’informations sur la suppression des correctifs appliqués, consultez [suppression des correctifs](removing-patches.md).

Pour obtenir un exemple de la façon dont Windows Installer applique plusieurs correctifs quand tous ont des tables [MsiPatchSequence](msipatchsequence-table.md) , consultez l’exemple de mise à [jour corrective multiple](multiple-patching-example.md).

 

 



