---
description: Cet exemple montre comment créer un package de correctifs qui applique une petite mise à jour de l’exemple de package d’installation abordé dans un exemple d’installation.
ms.assetid: 17dadd64-6e81-444a-985e-1b340e4f2ee5
title: Exemple de mise à jour corrective de petite taille
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0670693e9f5c6bf1c6b48c72e4b05b0f06703d69c08f46f6a2209b3d5046ea7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082969"
---
# <a name="a-small-update-patching-example"></a>Exemple de mise à jour corrective de petite taille

Cet exemple montre comment créer un package de [correctifs](patch-packages.md) qui applique une [petite mise à jour](small-updates.md) de l’exemple de package d’installation abordé dans [un exemple d’installation](an-installation-example.md). Une petite mise à jour apporte des modifications à un ou plusieurs fichiers d’application qui sont jugés trop mineurs pour justifier la modification du code du produit. Pour plus d’informations [, consultez Mise à jour corrective et mises à niveau](patching-and-upgrades.md).

cet exemple montre comment créer un package de correctifs Windows Installer qui met à jour la fonctionnalité de Concert du produit hypothétique MNP2000 pour résoudre une erreur dans le produit d’origine. L’exemple de package correctif applique une petite mise à jour du produit qui ne nécessite pas de modification du code du produit. Pour plus d’informations sur les principales mises à niveau, consultez la rubrique sur les [mises à niveau majeures](major-upgrades.md) dans la section [correctifs et mises à niveau](patching-and-upgrades.md) .

L’exemple de package de mise à niveau présente les spécifications suivantes :

-   Il corrige une erreur mineure dans la planification de concert affichée par la fonctionnalité de concert.
-   Il met à jour le code du package pour refléter la modification du package d’installation.
-   La petite mise à jour peut être appliquée en appliquant des correctifs à l’installation locale du produit.

[Continuer](planning-a-small-update-patch.md)

 

 



