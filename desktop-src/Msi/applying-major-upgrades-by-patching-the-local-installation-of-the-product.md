---
description: Une mise à niveau majeure peut être appliquée à une application en corrigeant l’installation locale de l’application à partir de la ligne de commande ou à l’aide d’un fichier exécutable.
ms.assetid: be651457-5c66-478b-89d5-3d7607702b8e
title: Application de mises à niveau majeures en appliquant des correctifs à l’installation locale du produit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 043d106ed9f8d6455ab4412959b70854a526a4e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864482"
---
# <a name="applying-major-upgrades-by-patching-the-local-installation-of-the-product"></a><span data-ttu-id="c4a3c-103">Application de mises à niveau majeures en appliquant des correctifs à l’installation locale du produit</span><span class="sxs-lookup"><span data-stu-id="c4a3c-103">Applying Major Upgrades by Patching the Local Installation of the Product</span></span>

<span data-ttu-id="c4a3c-104">Une mise à niveau majeure peut être appliquée à une application en corrigeant l’installation locale de l’application à partir de la ligne de commande ou à l’aide d’un fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="c4a3c-104">A major upgrade can be applied to an application by patching the local installation of the application from the command line or by using an executable.</span></span>

> [!Note]  
> <span data-ttu-id="c4a3c-105">Il n’est pas recommandé de fournir une mise à niveau majeure en tant que package de correctifs, car un package correctif de mise à niveau majeure ne peut pas être séquencé avec d’autres mises à jour et parce que le correctif n’est pas un [correctif non installable](uninstallable-patches.md).</span><span class="sxs-lookup"><span data-stu-id="c4a3c-105">Providing a major upgrade as a patch package is not recommended because a major upgrade patch package cannot be sequenced with other updates and because the patch is not an [uninstallable patch](uninstallable-patches.md).</span></span> <span data-ttu-id="c4a3c-106">L’utilitaire [Msimsp.exe](msimsp-exe.md) ne peut pas être utilisé pour générer un package correctif qui applique une mise à niveau majeure.</span><span class="sxs-lookup"><span data-stu-id="c4a3c-106">The [Msimsp.exe](msimsp-exe.md) utility cannot be used to generate a patch package that applies a major upgrade.</span></span> <span data-ttu-id="c4a3c-107">Au lieu de cela, appliquez les mises à niveau majeures comme décrit dans [application des mises à niveau majeures en installant le produit](applying-major-upgrades-by-installing-the-product.md).</span><span class="sxs-lookup"><span data-stu-id="c4a3c-107">Instead, apply major upgrades as described in [Applying Major Upgrades by Installing the Product](applying-major-upgrades-by-installing-the-product.md).</span></span>

 

<span data-ttu-id="c4a3c-108">**Pour appliquer un correctif de mise à niveau majeur à une installation locale du produit**</span><span class="sxs-lookup"><span data-stu-id="c4a3c-108">**To apply a major upgrade patch to a local installation of the product**</span></span>

1.  <span data-ttu-id="c4a3c-109">Lancez l’installation du correctif à partir de la ligne de commande ou à l’aide d’un fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="c4a3c-109">Launch the installation of the patch from the command line or by using an executable.</span></span> <span data-ttu-id="c4a3c-110">Pour lancer à partir de la ligne de commande, utilisez msiexec/p patch. msp.</span><span class="sxs-lookup"><span data-stu-id="c4a3c-110">To launch from the command line, use msiexec /p patch.msp.</span></span> <span data-ttu-id="c4a3c-111">Pour lancer à partir d’un exécutable, appelez [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) ou la [**méthode ApplyPatch**](installer-applypatch.md) et fournissez les mêmes arguments de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="c4a3c-111">To launch from an executable, call [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) or the [**ApplyPatch Method**](installer-applypatch.md) and provide the same command line arguments.</span></span>
2.  <span data-ttu-id="c4a3c-112">Lors de la mise à jour corrective d’une installation du client, le programme d’installation ignore la source d’installation et poursuit la mise à jour corrective des fichiers déjà installés sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c4a3c-112">When patching a client installation, the installer ignores the installation source and proceeds to patch the files that are already installed on the user's computer.</span></span>
3.  <span data-ttu-id="c4a3c-113">Le programme d’installation modifie tous les composants corrigés marqués en tant que code d’exécution à partir de la source pour s’exécuter localement.</span><span class="sxs-lookup"><span data-stu-id="c4a3c-113">The installer changes any patched components marked as run-from-source to run-locally.</span></span> <span data-ttu-id="c4a3c-114">Les utilisateurs ne peuvent pas exécuter ces composants à partir de la source tant que le correctif reste sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c4a3c-114">Users are unable to run these components from the source as long as the patch remains on the computer.</span></span>
4.  <span data-ttu-id="c4a3c-115">Le programme d’installation ajoute toutes les transformations utilisées pour mettre à jour le fichier. msi ou ajoute des informations spécifiques aux correctifs au profil de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c4a3c-115">The installer adds any transforms used to update the .msi file or adds patch-specific information to the user's profile.</span></span>
5.  <span data-ttu-id="c4a3c-116">Le programme d’installation met en cache le fichier. msi sur l’ordinateur de l’utilisateur afin qu’il puisse effectuer une installation à la demande, une réinstallation et une réparation de l’application.</span><span class="sxs-lookup"><span data-stu-id="c4a3c-116">The installer caches the .msi file on the user's computer so that it can perform installation-on-demand, reinstall, and repair of the application.</span></span> <span data-ttu-id="c4a3c-117">Après l’application d’un correctif à une installation autonome, le programme d’installation référence deux listes sources ou plus dans des fichiers externes : une pour la source d’origine et une pour chaque correctif appliqué.</span><span class="sxs-lookup"><span data-stu-id="c4a3c-117">After a patch is applied to a stand alone installation, the installer references two or more source lists to external files: one for the original source and one for each patch that has been applied.</span></span>

 

 



