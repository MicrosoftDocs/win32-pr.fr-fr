---
description: Vous pouvez appliquer la petite mise à jour à une image source d’administration de MNP2000.msi en installant l’exemple de correctif MNP2000. msp créé lors de la génération d’un package de correctifs.
ms.assetid: 24ae9cd6-2057-4345-90ec-943da7620cb0
title: Application d’un package de correctifs à une installation d’administration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c29cbec604ae18745348a62f147d13d2ccbf06c0620b3a5dcca7c6c009045b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105439"
---
# <a name="applying-a-patch-package-to-an-administrative-installation"></a>Application d’un package de correctifs à une installation d’administration

Vous pouvez appliquer la petite mise à jour à une image source d’administration de MNP2000.msi en installant l’exemple de correctif MNP2000. msp créé lors de la [génération d’un package de correctifs](generating-a-patch-package.md). La mise à jour peut ensuite être propagée aux utilisateurs en demandant qu’ils réinstallent l’application à partir de la nouvelle image source d’administration.

Un administrateur peut utiliser la ligne de commande suivante pour mettre à jour l’image source administrative située dans//Server/MNP2000.msi vers une nouvelle image source qui est la même que celle produite par une installation d’administration à partir d’un CD-ROM entièrement mis à jour.

**msiexec/a//Server/MNP2000.msi/p MNP2000. msp**

Les membres du groupe de travail utilisant MNP2000 doivent ensuite réinstaller l’application à partir de la nouvelle image source d’administration pour recevoir la mise à jour.

Pour réinstaller complètement les applications et mettre en cache le fichier .msi mis à jour sur l’ordinateur de l’utilisateur, les utilisateurs peuvent entrer l’une ou l’autre des commandes suivantes.

**msiexec/fvomus//Server/MNP2000.msi**

**msiexec/I//Server/MNP2000.msi REINSTALL = ALL REINSTALLMODE = vomus**

Pour réinstaller uniquement la fonctionnalité de concert mise à jour et mettre en cache le fichier .msi mis à jour sur l’ordinateur de l’utilisateur, les utilisateurs peuvent entrer la commande suivante.

**msiexec/I//Server/MNP2000.msi REINSTALL = concert REINSTALLMODE = vomus**

## <a name="next-example"></a>Exemple suivant

[Exemple de localisation](a-localization-example.md)

 

 



