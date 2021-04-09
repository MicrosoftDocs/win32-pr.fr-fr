---
description: Une petite mise à jour peut être appliquée à une application en corrigeant l’installation locale de l’application.
ms.assetid: 2a04ffd0-d5b6-44f3-bef2-73f59179aed1
title: Application de petites mises à jour en appliquant des correctifs à l’installation locale du produit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bced3e7f69761ff3e270046718eedb9032cab8a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951781"
---
# <a name="applying-small-updates-by-patching-the-local-installation-of-the-product"></a><span data-ttu-id="e80c8-103">Application de petites mises à jour en appliquant des correctifs à l’installation locale du produit</span><span class="sxs-lookup"><span data-stu-id="e80c8-103">Applying Small Updates by Patching the Local Installation of the Product</span></span>

<span data-ttu-id="e80c8-104">Une petite mise à jour peut être appliquée à une application en corrigeant l’installation locale de l’application.</span><span class="sxs-lookup"><span data-stu-id="e80c8-104">A small update can be applied to an application by patching the local installation of the application.</span></span>

<span data-ttu-id="e80c8-105">**Pour appliquer un correctif de mise à jour de petite taille à une installation locale du produit**</span><span class="sxs-lookup"><span data-stu-id="e80c8-105">**To apply a small update patch to a local installation of the product**</span></span>

1.  <span data-ttu-id="e80c8-106">Lancez l’installation du correctif à partir de la ligne de commande ou à l’aide d’un fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="e80c8-106">Launch the installation of the patch from the command line or by using an executable.</span></span> <span data-ttu-id="e80c8-107">Pour lancer à partir de la ligne de commande, utilisez **msiexec/p patch. \[ MSP REINSTALL =**_Feature List_ *_\] REINSTALLMODE = omus_*.</span><span class="sxs-lookup"><span data-stu-id="e80c8-107">To launch from the command line, use **msiexec /p patch.msp REINSTALL=\[**_Feature list_*_\] REINSTALLMODE=omus_*.</span></span> <span data-ttu-id="e80c8-108">Pour lancer à partir d’un exécutable, appelez [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) ou la [**méthode ApplyPatch**](installer-applypatch.md) et fournissez les mêmes arguments de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="e80c8-108">To launch from an executable, call [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) or the [**ApplyPatch Method**](installer-applypatch.md) and provide the same command line arguments.</span></span>
2.  <span data-ttu-id="e80c8-109">Lors de la mise à jour corrective d’une installation du client, le programme d’installation ignore la source d’installation et poursuit la mise à jour corrective des fichiers déjà installés sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e80c8-109">When patching a client installation, the installer ignores the installation source and proceeds to patch the files that are already installed on the user's computer.</span></span>
3.  <span data-ttu-id="e80c8-110">Le programme d’installation modifie tous les composants corrigés marqués en tant que code d’exécution à partir de la source pour s’exécuter localement.</span><span class="sxs-lookup"><span data-stu-id="e80c8-110">The installer changes any patched components marked as run-from-source to run-locally.</span></span> <span data-ttu-id="e80c8-111">Les utilisateurs ne peuvent pas exécuter ces composants à partir de la source tant que le correctif reste sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e80c8-111">Users are unable to run these components from the source as long as the patch remains on the computer.</span></span>
4.  <span data-ttu-id="e80c8-112">Le programme d’installation ajoute toutes les transformations utilisées pour mettre à jour le fichier. msi ou ajoute des informations spécifiques aux correctifs au profil de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e80c8-112">The installer adds any transforms used to update the .msi file or adds patch-specific information to the user's profile.</span></span>
5.  <span data-ttu-id="e80c8-113">Le programme d’installation met en cache le fichier. msi sur l’ordinateur de l’utilisateur afin qu’il puisse effectuer une installation à la demande, une réinstallation et une réparation de l’application.</span><span class="sxs-lookup"><span data-stu-id="e80c8-113">The installer caches the .msi file on the user's computer so that it can perform installation-on-demand, reinstall, and repair of the application.</span></span> <span data-ttu-id="e80c8-114">Après l’application d’un correctif à une installation autonome, le programme d’installation référence deux listes sources ou plus dans des fichiers externes : une pour la source d’origine et une pour chaque correctif appliqué.</span><span class="sxs-lookup"><span data-stu-id="e80c8-114">After a patch is applied to a standalone installation, the installer references two or more source lists to external files: one for the original source and one for each patch that has been applied.</span></span>

 

 



