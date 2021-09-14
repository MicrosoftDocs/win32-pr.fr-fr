---
description: Une mise à niveau majeure peut être appliquée à une application en corrigeant l’installation locale de l’application à partir de la ligne de commande ou à l’aide d’un fichier exécutable.
ms.assetid: be651457-5c66-478b-89d5-3d7607702b8e
title: Application de mises à niveau majeures en appliquant des correctifs à l’installation locale du produit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 043d106ed9f8d6455ab4412959b70854a526a4e3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092669"
---
# <a name="applying-major-upgrades-by-patching-the-local-installation-of-the-product"></a>Application de mises à niveau majeures en appliquant des correctifs à l’installation locale du produit

Une mise à niveau majeure peut être appliquée à une application en corrigeant l’installation locale de l’application à partir de la ligne de commande ou à l’aide d’un fichier exécutable.

> [!Note]  
> Il n’est pas recommandé de fournir une mise à niveau majeure en tant que package de correctifs, car un package correctif de mise à niveau majeure ne peut pas être séquencé avec d’autres mises à jour et parce que le correctif n’est pas un [correctif non installable](uninstallable-patches.md). L’utilitaire [Msimsp.exe](msimsp-exe.md) ne peut pas être utilisé pour générer un package correctif qui applique une mise à niveau majeure. Au lieu de cela, appliquez les mises à niveau majeures comme décrit dans [application des mises à niveau majeures en installant le produit](applying-major-upgrades-by-installing-the-product.md).

 

**Pour appliquer un correctif de mise à niveau majeur à une installation locale du produit**

1.  Lancez l’installation du correctif à partir de la ligne de commande ou à l’aide d’un fichier exécutable. Pour lancer à partir de la ligne de commande, utilisez msiexec/p patch. msp. Pour lancer à partir d’un exécutable, appelez [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) ou la [**méthode ApplyPatch**](installer-applypatch.md) et fournissez les mêmes arguments de ligne de commande.
2.  Lors de la mise à jour corrective d’une installation du client, le programme d’installation ignore la source d’installation et poursuit la mise à jour corrective des fichiers déjà installés sur l’ordinateur de l’utilisateur.
3.  Le programme d’installation modifie tous les composants corrigés marqués en tant que code d’exécution à partir de la source pour s’exécuter localement. Les utilisateurs ne peuvent pas exécuter ces composants à partir de la source tant que le correctif reste sur l’ordinateur.
4.  Le programme d’installation ajoute toutes les transformations utilisées pour mettre à jour le fichier .msi ou ajoute des informations spécifiques aux correctifs dans le profil de l’utilisateur.
5.  Le programme d’installation met en cache le fichier .msi sur l’ordinateur de l’utilisateur afin qu’il puisse effectuer l’installation à la demande, la réinstallation et la réparation de l’application. Après l’application d’un correctif à une installation autonome, le programme d’installation référence deux listes sources ou plus dans des fichiers externes : une pour la source d’origine et une pour chaque correctif appliqué.

 

 



