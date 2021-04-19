---
description: Cet exemple montre comment créer un package de correctifs qui applique une petite mise à jour de l’exemple de package d’installation abordé dans un exemple d’installation.
ms.assetid: 17dadd64-6e81-444a-985e-1b340e4f2ee5
title: Exemple de mise à jour corrective de petite taille
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d4997a326e8fea33086a75c9cf40ecef8cb997
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527857"
---
# <a name="a-small-update-patching-example"></a>Exemple de mise à jour corrective de petite taille

Cet exemple montre comment créer un package de [correctifs](patch-packages.md) qui applique une [petite mise à jour](small-updates.md) de l’exemple de package d’installation abordé dans [un exemple d’installation](an-installation-example.md). Une petite mise à jour apporte des modifications à un ou plusieurs fichiers d’application qui sont jugés trop mineurs pour justifier la modification du code du produit. Pour plus d’informations [, consultez Mise à jour corrective et mises à niveau](patching-and-upgrades.md).

Cet exemple montre comment créer un package de correctifs Windows Installer qui met à jour la fonctionnalité de concert du produit hypothétique MNP2000 pour résoudre une erreur dans le produit d’origine. L’exemple de package correctif applique une petite mise à jour du produit qui ne nécessite pas de modification du code du produit. Pour plus d’informations sur les principales mises à niveau, consultez la rubrique sur les [mises à niveau majeures](major-upgrades.md) dans la section [correctifs et mises à niveau](patching-and-upgrades.md) .

L’exemple de package de mise à niveau présente les spécifications suivantes :

-   Il corrige une erreur mineure dans la planification de concert affichée par la fonctionnalité de concert.
-   Il met à jour le code du package pour refléter la modification du package d’installation.
-   La petite mise à jour peut être appliquée en appliquant des correctifs à l’installation locale du produit.

[Continuer](planning-a-small-update-patch.md)

 

 



