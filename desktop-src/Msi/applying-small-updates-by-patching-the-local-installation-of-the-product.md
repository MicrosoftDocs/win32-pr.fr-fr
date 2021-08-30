---
description: Une petite mise à jour peut être appliquée à une application en corrigeant l’installation locale de l’application.
ms.assetid: 2a04ffd0-d5b6-44f3-bef2-73f59179aed1
title: Application de petites mises à jour en appliquant des correctifs à l’installation locale du produit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4519a8e9e5f50968e9b11bc8154cd73254c3fb81e4a7f4e4a69bb3136033df3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078099"
---
# <a name="applying-small-updates-by-patching-the-local-installation-of-the-product"></a>Application de petites mises à jour en appliquant des correctifs à l’installation locale du produit

Une petite mise à jour peut être appliquée à une application en corrigeant l’installation locale de l’application.

**Pour appliquer un correctif de mise à jour de petite taille à une installation locale du produit**

1.  Lancez l’installation du correctif à partir de la ligne de commande ou à l’aide d’un fichier exécutable. Pour lancer à partir de la ligne de commande, utilisez **msiexec/p patch. \[ MSP REINSTALL =**_Feature List_ *_\] REINSTALLMODE = omus_*. Pour lancer à partir d’un exécutable, appelez [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) ou la [**méthode ApplyPatch**](installer-applypatch.md) et fournissez les mêmes arguments de ligne de commande.
2.  Lors de la mise à jour corrective d’une installation du client, le programme d’installation ignore la source d’installation et poursuit la mise à jour corrective des fichiers déjà installés sur l’ordinateur de l’utilisateur.
3.  Le programme d’installation modifie tous les composants corrigés marqués en tant que code d’exécution à partir de la source pour s’exécuter localement. Les utilisateurs ne peuvent pas exécuter ces composants à partir de la source tant que le correctif reste sur l’ordinateur.
4.  Le programme d’installation ajoute toutes les transformations utilisées pour mettre à jour le fichier .msi ou ajoute des informations spécifiques aux correctifs dans le profil de l’utilisateur.
5.  Le programme d’installation met en cache le fichier .msi sur l’ordinateur de l’utilisateur afin qu’il puisse effectuer l’installation à la demande, la réinstallation et la réparation de l’application. Après l’application d’un correctif à une installation autonome, le programme d’installation référence deux listes sources ou plus dans des fichiers externes : une pour la source d’origine et une pour chaque correctif appliqué.

 

 



