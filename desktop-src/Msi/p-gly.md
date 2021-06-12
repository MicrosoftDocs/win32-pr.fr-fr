---
description: En savoir plus sur les concepts de Windows Installer qui commencent par la lettre P, tels que le code du package et l’application de correctifs.
ms.assetid: 868f5ed3-b179-404b-9462-1d3a179103f8
title: P (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8923359197916a1186fe28ab0d12e4118b989bc
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011101"
---
# <a name="p-windows-installer"></a><span data-ttu-id="e86de-103">P (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="e86de-103">P (Windows Installer)</span></span>

<span data-ttu-id="e86de-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [e](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) P [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="e86de-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) P [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="e86de-105"><span id="_msi_package_using_windows_installer_gly"></span><span id="_MSI_PACKAGE_USING_WINDOWS_INSTALLER_GLY"></span>**Packages**</span><span class="sxs-lookup"><span data-stu-id="e86de-105"><span id="_msi_package_using_windows_installer_gly"></span><span id="_MSI_PACKAGE_USING_WINDOWS_INSTALLER_GLY"></span>**package**</span></span>
</dt> <dd>

<span data-ttu-id="e86de-106">[*.msi fichier*](m-gly.md) et tous les [*fichiers sources externes*](e-gly.md) pouvant être référencés par ce fichier.</span><span class="sxs-lookup"><span data-stu-id="e86de-106">[*.msi file*](m-gly.md) and any [*external source files*](e-gly.md) that may be pointed to by this file.</span></span> <span data-ttu-id="e86de-107">Un package contient donc toutes les informations dont le Windows Installer a besoin pour exécuter l’interface utilisateur et installer ou désinstaller l’application.</span><span class="sxs-lookup"><span data-stu-id="e86de-107">A package therefore contains all the information the Windows Installer needs to run the UI and to install or uninstall the application.</span></span> <span data-ttu-id="e86de-108">Pour plus d’informations, consultez également [*installer la base de données*](i-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e86de-108">For more information, see also [*installer database*](i-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="e86de-109"><span id="_msi_package_code_gly"></span><span id="_MSI_PACKAGE_CODE_GLY"></span>**Code du package**</span><span class="sxs-lookup"><span data-stu-id="e86de-109"><span id="_msi_package_code_gly"></span><span id="_MSI_PACKAGE_CODE_GLY"></span>**package code**</span></span>
</dt> <dd>

<span data-ttu-id="e86de-110">GUID qui identifie un package particulier.</span><span class="sxs-lookup"><span data-stu-id="e86de-110">GUID that identifies a particular package.</span></span> <span data-ttu-id="e86de-111">Un code de package unique est nécessaire, car certains transformations ou packages de correctifs peuvent être appliqués à plusieurs applications ou peuvent mettre à niveau une application vers une autre application ou version.</span><span class="sxs-lookup"><span data-stu-id="e86de-111">A unique package code is required because some transforms or patch packages can be applied to more than one application or can upgrade an application into another application or version.</span></span> <span data-ttu-id="e86de-112">Pour plus d’informations, consultez [codes de package](package-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e86de-112">For more information, see [Package Codes](package-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="e86de-113"><span id="_msi_patching_gly"></span><span id="_MSI_PATCHING_GLY"></span>**correctifs**</span><span class="sxs-lookup"><span data-stu-id="e86de-113"><span id="_msi_patching_gly"></span><span id="_MSI_PATCHING_GLY"></span>**patching**</span></span>
</dt> <dd>

<span data-ttu-id="e86de-114">Méthode de mise à jour d’un fichier qui remplace uniquement les bits en cours de modification, plutôt que le fichier entier.</span><span class="sxs-lookup"><span data-stu-id="e86de-114">Method of updating a file that replaces only the bits being changed, rather than the entire file.</span></span> <span data-ttu-id="e86de-115">Cela signifie que les utilisateurs peuvent télécharger un correctif de mise à niveau pour un produit qui est plus petit que l’intégralité du produit.</span><span class="sxs-lookup"><span data-stu-id="e86de-115">This means that users can download an upgrade patch for a product that is much smaller than the entire product.</span></span> <span data-ttu-id="e86de-116">Pour plus d’informations, consultez [packages de correctifs](patch-packages.md).</span><span class="sxs-lookup"><span data-stu-id="e86de-116">For more information, see [Patch Packages](patch-packages.md).</span></span>

</dd> <dt>

<span data-ttu-id="e86de-117"><span id="_msi_patch_file_gly"></span><span id="_MSI_PATCH_FILE_GLY"></span>**fichier correctif**</span><span class="sxs-lookup"><span data-stu-id="e86de-117"><span id="_msi_patch_file_gly"></span><span id="_MSI_PATCH_FILE_GLY"></span>**patch file**</span></span>
</dt> <dd>

<span data-ttu-id="e86de-118">[Package P atch](patch-packages.md) utilisé pour la mise à jour corrective.</span><span class="sxs-lookup"><span data-stu-id="e86de-118">P [atch package](patch-packages.md) used for patching.</span></span> <span data-ttu-id="e86de-119">Pour plus d’informations, consultez [mise à jour corrective et mises à niveau](patching-and-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="e86de-119">For more information, see [Patching and Upgrades](patching-and-upgrades.md).</span></span>

</dd> <dt>

<span data-ttu-id="e86de-120"><span id="_msi_preview_mode_using_windows_installer_gly"></span><span id="_MSI_PREVIEW_MODE_USING_WINDOWS_INSTALLER_GLY"></span>**mode aperçu**</span><span class="sxs-lookup"><span data-stu-id="e86de-120"><span id="_msi_preview_mode_using_windows_installer_gly"></span><span id="_MSI_PREVIEW_MODE_USING_WINDOWS_INSTALLER_GLY"></span>**preview mode**</span></span>
</dt> <dd>

<span data-ttu-id="e86de-121">Mode d’affichage de la conception de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e86de-121">Mode for viewing the design of the UI.</span></span> <span data-ttu-id="e86de-122">Pour plus d’informations, consultez [aperçu de l’interface utilisateur](previewing-the-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="e86de-122">For more information, see [Previewing the User Interface](previewing-the-user-interface.md).</span></span>

</dd> <dt>

<span data-ttu-id="e86de-123"><span id="_msi_progress_bar_gly"></span><span id="_MSI_PROGRESS_BAR_GLY"></span>**barre de progression**</span><span class="sxs-lookup"><span data-stu-id="e86de-123"><span id="_msi_progress_bar_gly"></span><span id="_MSI_PROGRESS_BAR_GLY"></span>**progress bar**</span></span>
</dt> <dd>

<span data-ttu-id="e86de-124">Contrôle que le programme d’installation peut afficher pendant l’exécution du script représentant la progression de l’installation.</span><span class="sxs-lookup"><span data-stu-id="e86de-124">Control the installer can display during script execution time representing the progress of the installation.</span></span> <span data-ttu-id="e86de-125">Pour plus d’informations, consultez [création d’un contrôle ProgressBar](authoring-a-progressbar-control.md).</span><span class="sxs-lookup"><span data-stu-id="e86de-125">For more information, see [Authoring a ProgressBar Control](authoring-a-progressbar-control.md).</span></span>

</dd> <dt>

<span data-ttu-id="e86de-126"><span id="_msi_property_gly"></span><span id="_MSI_PROPERTY_GLY"></span>**propriété**</span><span class="sxs-lookup"><span data-stu-id="e86de-126"><span id="_msi_property_gly"></span><span id="_MSI_PROPERTY_GLY"></span>**property**</span></span>
</dt> <dd>

<span data-ttu-id="e86de-127">Variables globales utilisées durant une installation.</span><span class="sxs-lookup"><span data-stu-id="e86de-127">Global variables used during an installation.</span></span> <span data-ttu-id="e86de-128">(Consultez [à propos des propriétés](about-properties.md).)</span><span class="sxs-lookup"><span data-stu-id="e86de-128">(See [About Properties](about-properties.md).)</span></span>

<span data-ttu-id="e86de-129">Le terme « propriété » fait également référence à un attribut d’un objet Automation.</span><span class="sxs-lookup"><span data-stu-id="e86de-129">The term "property" also refers to an attribute of an automation object.</span></span> <span data-ttu-id="e86de-130">(Voir [interface Automation](automation-interface.md).)</span><span class="sxs-lookup"><span data-stu-id="e86de-130">(See [Automation Interface](automation-interface.md).)</span></span>

</dd> <dt>

<span data-ttu-id="e86de-131"><span id="_msi_publishing_gly"></span><span id="_MSI_PUBLISHING_GLY"></span>**publiée**</span><span class="sxs-lookup"><span data-stu-id="e86de-131"><span id="_msi_publishing_gly"></span><span id="_MSI_PUBLISHING_GLY"></span>**publishing**</span></span>
</dt> <dd>

<span data-ttu-id="e86de-132">Méthode de [*publication*](a-gly.md) d’une fonctionnalité ou d’une application.</span><span class="sxs-lookup"><span data-stu-id="e86de-132">Method of [*advertising*](a-gly.md) a feature or application.</span></span> <span data-ttu-id="e86de-133">La publication ne remplit pas l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e86de-133">Publishing does not populate the UI.</span></span> <span data-ttu-id="e86de-134">Toutefois, si une autre application tente d’ouvrir une application publiée, il y a suffisamment d’informations pour que le programme d’installation affecte l’application publiée.</span><span class="sxs-lookup"><span data-stu-id="e86de-134">However, if another application attempts to open a published application, there is enough information present for the installer to assign the published application.</span></span> <span data-ttu-id="e86de-135">Pour plus d’informations, consultez [*Assigning*](a-gly.md) and [Components and features](components-and-features.md).</span><span class="sxs-lookup"><span data-stu-id="e86de-135">For more information, see [*assigning*](a-gly.md) and [Components and Features](components-and-features.md).</span></span>

</dd> </dl>

 

 



