---
description: Windows Installer est la solution recommandée pour l’installation et la configuration d’applications sur Windows.
ms.assetid: 13f41020-5275-44cd-b26b-f45483700d8a
title: Guide basé sur les rôles pour Windows Installer la documentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc8a2138e963b6d29bd161df5e09144cf0cfd36b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034196"
---
# <a name="role-based-guide-to-windows-installer-documentation"></a><span data-ttu-id="d4c7b-103">Guide basé sur les rôles pour Windows Installer la documentation</span><span class="sxs-lookup"><span data-stu-id="d4c7b-103">Role-based Guide to Windows Installer Documentation</span></span>

<span data-ttu-id="d4c7b-104">Windows Installer est la solution recommandée pour l’installation et la configuration d’applications sur Windows.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-104">Windows Installer is the recommended solution for the installation and setup of applications on Windows.</span></span> <span data-ttu-id="d4c7b-105">Par conséquent, certaines des informations contenues dans ce kit de développement logiciel (SDK) présentent un intérêt pour un large éventail de développeurs de logiciels et de professionnels de l’informatique.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-105">Therefore, some of the information contained in this SDK will be of interest to a wide range of software development and IT professionals.</span></span> <span data-ttu-id="d4c7b-106">Cette section est fournie à titre de guide pour les lecteurs qui préfèrent voir des liens vers des rubriques organisées par rôle professionnel et les scénarios de tâches courantes.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-106">This section is provided as a guide to readers who prefer to see links to topics organized by professional role and common task scenarios.</span></span> <span data-ttu-id="d4c7b-107">Étant donné que les rôles peuvent varier d’une organisation à l’autre, le regroupement suivant doit être considéré comme un guide d’un emplacement pour commencer à rechercher les informations dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-107">Because roles can differ greatly between organizations, the following grouping should only be considered as a guide to a location to start searching for the information you need.</span></span>

-   [<span data-ttu-id="d4c7b-108">Développeurs d’applications</span><span class="sxs-lookup"><span data-stu-id="d4c7b-108">Application Developers</span></span>](#application-developers)
-   [<span data-ttu-id="d4c7b-109">Auteurs d’installation</span><span class="sxs-lookup"><span data-stu-id="d4c7b-109">Setup Authors</span></span>](#setup-authors)
-   [<span data-ttu-id="d4c7b-110">Professionnels de l’informatique</span><span class="sxs-lookup"><span data-stu-id="d4c7b-110">IT Professionals</span></span>](#it-professionals)
-   [<span data-ttu-id="d4c7b-111">Développeurs d’infrastructure</span><span class="sxs-lookup"><span data-stu-id="d4c7b-111">Infrastructure Developers</span></span>](#infrastructure-developers)

<span data-ttu-id="d4c7b-112">Cette documentation est destinée aux développeurs de logiciels qui souhaitent créer des applications qui utilisent Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-112">This documentation is intended for software developers who want to make applications that use Windows Installer.</span></span> <span data-ttu-id="d4c7b-113">En tant que principale source de documentation de référence pour le programme d’installation, le kit de développement logiciel (SDK) fournit des informations sur les packages d’installation et le service d’installation.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-113">As the primary source of reference material for the installer, the SDK provides information about installation packages and the installer service.</span></span> <span data-ttu-id="d4c7b-114">Elle contient des descriptions complètes de l’interface de programmation d’applications (API) et des éléments de la base de données du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-114">It contains complete descriptions of the application programming interface (API) and the elements of the installer database.</span></span>

<span data-ttu-id="d4c7b-115">Pour plus d’informations, consultez [autres sources d’informations sur les Windows Installer](other-sources-of-windows-installer-information.md).</span><span class="sxs-lookup"><span data-stu-id="d4c7b-115">For more information, see [Other Sources of Windows Installer Information](other-sources-of-windows-installer-information.md).</span></span>

## <a name="application-developers"></a><span data-ttu-id="d4c7b-116">Développeurs d’applications</span><span class="sxs-lookup"><span data-stu-id="d4c7b-116">Application Developers</span></span>

<span data-ttu-id="d4c7b-117">Les développeurs d’applications créent des applications qui appellent l’interface de programmation d’applications Windows Installer et installent des packages Windows Installer au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-117">Application developers create applications that call the Windows Installer application programming interface and install Windows installer packages at run time.</span></span> <span data-ttu-id="d4c7b-118">La Windows Installer peut faire fonctionner dans une application telle que la réparation automatique et l’installation à la demande.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-118">The Windows Installer can do work in an application such as self-repair and installation-on-demand.</span></span> <span data-ttu-id="d4c7b-119">En règle générale, les développeurs d’applications effectuent les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-119">Typically, application Developers do the following:</span></span>

-   <span data-ttu-id="d4c7b-120">Activer l’installation à la demande des applications au moment de l’exécution à partir d’une autre application.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-120">Enable installation-on-demand of applications at run time from within another application.</span></span>

    <span data-ttu-id="d4c7b-121">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-121">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-122">Utilisation des fonctions de programme d’installation</span><span class="sxs-lookup"><span data-stu-id="d4c7b-122">Using Installer Functions</span></span>](using-installer-functions.md)
    -   [<span data-ttu-id="d4c7b-123">Référence des fonctions du programme d’installation</span><span class="sxs-lookup"><span data-stu-id="d4c7b-123">Installer Function Reference</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="d4c7b-124">Installation à la demande</span><span class="sxs-lookup"><span data-stu-id="d4c7b-124">Installation-On-Demand</span></span>](installation-on-demand.md)
    -   [<span data-ttu-id="d4c7b-125">Gestion des composants</span><span class="sxs-lookup"><span data-stu-id="d4c7b-125">Component Management</span></span>](component-management.md)
    -   [<span data-ttu-id="d4c7b-126">Modification des raccourcis du programme d’installation</span><span class="sxs-lookup"><span data-stu-id="d4c7b-126">Editing Installer Shortcuts</span></span>](editing-installer-shortcuts.md)
    -   [<span data-ttu-id="d4c7b-127">**Propriété OLEAdvtSupport**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-127">**OLEAdvtSupport Property**</span></span>](oleadvtsupport.md)
    -   [<span data-ttu-id="d4c7b-128">Prise en charge des plateformes de la publication</span><span class="sxs-lookup"><span data-stu-id="d4c7b-128">Platform Support of Advertisement</span></span>](platform-support-of-advertisement.md)

-   <span data-ttu-id="d4c7b-129">Activez la réparation automatique des applications en réinstallant les composants en fonction des besoins au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-129">Enable self-repair of applications by reinstalling components as needed at run time.</span></span>

    <span data-ttu-id="d4c7b-130">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-130">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-131">Utilisation des fonctions de programme d’installation</span><span class="sxs-lookup"><span data-stu-id="d4c7b-131">Using Installer Functions</span></span>](using-installer-functions.md)
    -   [<span data-ttu-id="d4c7b-132">Référence des fonctions du programme d’installation</span><span class="sxs-lookup"><span data-stu-id="d4c7b-132">Installer Function Reference</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="d4c7b-133">Résilience</span><span class="sxs-lookup"><span data-stu-id="d4c7b-133">Resiliency</span></span>](resiliency.md)
    -   [<span data-ttu-id="d4c7b-134">Résilience source</span><span class="sxs-lookup"><span data-stu-id="d4c7b-134">Source Resiliency</span></span>](source-resiliency.md)
    -   [<span data-ttu-id="d4c7b-135">Recherche d’une fonctionnalité ou d’un composant endommagé</span><span class="sxs-lookup"><span data-stu-id="d4c7b-135">Searching for a Broken Feature or Component</span></span>](searching-for-a-broken-feature-or-component.md)
    -   [<span data-ttu-id="d4c7b-136">Remplacement des fichiers existants</span><span class="sxs-lookup"><span data-stu-id="d4c7b-136">Replacing Existing Files</span></span>](replacing-existing-files.md)

-   <span data-ttu-id="d4c7b-137">Affichez une interface utilisateur pour collecter des informations sur l’utilisateur et des préférences de configuration la première fois qu’une application est installée ou exécutée.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-137">Display a user interface to collect user information and configuration preferences the first time an application is installed or run.</span></span> <span data-ttu-id="d4c7b-138">L’interface utilisateur doit être ajoutée par l’auteur du programme d’installation du Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-138">The user interface must be added by the Setup Author of the Windows Installer package.</span></span>

    <span data-ttu-id="d4c7b-139">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-139">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-140">Utilisation des fonctions de programme d’installation</span><span class="sxs-lookup"><span data-stu-id="d4c7b-140">Using Installer Functions</span></span>](using-installer-functions.md)
    -   [<span data-ttu-id="d4c7b-141">Initialisation d’une application</span><span class="sxs-lookup"><span data-stu-id="d4c7b-141">Initializing an Application</span></span>](initializing-an-application.md)
    -   [<span data-ttu-id="d4c7b-142">Boîte de dialogue FirstRun</span><span class="sxs-lookup"><span data-stu-id="d4c7b-142">FirstRun Dialog</span></span>](firstrun-dialog.md)
    -   [<span data-ttu-id="d4c7b-143">À propos de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="d4c7b-143">About the User Interface</span></span>](about-the-user-interface.md)

-   <span data-ttu-id="d4c7b-144">Créez des applications qui utilisent un modèle d’indirection pour faire référence aux composants avec des fonctionnalités parallèles.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-144">Create applications that use an indirection model to refer to components with parallel functionality.</span></span> <span data-ttu-id="d4c7b-145">Les catégories de composants qualifiés doivent être ajoutées par l’auteur du programme d’installation du Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-145">The qualified component categories must be added by the Setup Author of the Windows Installer package.</span></span>

    <span data-ttu-id="d4c7b-146">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-146">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-147">Composants qualifiés</span><span class="sxs-lookup"><span data-stu-id="d4c7b-147">Qualified Components</span></span>](qualified-components.md)
    -   [<span data-ttu-id="d4c7b-148">Utilisation des composants qualifiés</span><span class="sxs-lookup"><span data-stu-id="d4c7b-148">Using Qualified Components</span></span>](using-qualified-components.md)

-   <span data-ttu-id="d4c7b-149">Utilisez des assemblys privés et côte à côte pour isoler les applications et réduire les conflits de DLL.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-149">Use private and side-by-side assemblies to isolate applications and reduce DLL conflicts.</span></span>

    <span data-ttu-id="d4c7b-150">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-150">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-151">Assemblys</span><span class="sxs-lookup"><span data-stu-id="d4c7b-151">Assemblies</span></span>](assemblies.md)
    -   [<span data-ttu-id="d4c7b-152">Clés de registre de l’assembly écrites par Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d4c7b-152">Assembly Registry Keys Written by Windows Installer</span></span>](assembly-registry-keys-written-by-windows-installer-.md)
    -   [<span data-ttu-id="d4c7b-153">Installation d’assemblys Win32 pour le partage côte à côte sur Windows XP</span><span class="sxs-lookup"><span data-stu-id="d4c7b-153">Installing Win32 Assemblies for Side-by-Side Sharing on Windows XP</span></span>](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
    -   [<span data-ttu-id="d4c7b-154">Installation d’assemblys Win32 pour l’utilisation privée d’une application sur Windows XP</span><span class="sxs-lookup"><span data-stu-id="d4c7b-154">Installing Win32 Assemblies for the Private Use of an Application on Windows XP</span></span>](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)
    -   [<span data-ttu-id="d4c7b-155">Table MsiAssembly</span><span class="sxs-lookup"><span data-stu-id="d4c7b-155">MsiAssembly Table</span></span>](msiassembly-table.md)
    -   [<span data-ttu-id="d4c7b-156">Table MsiAssemblyName</span><span class="sxs-lookup"><span data-stu-id="d4c7b-156">MsiAssemblyName Table</span></span>](msiassemblyname-table.md)
    -   [<span data-ttu-id="d4c7b-157">**MsiProvideAssembly**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-157">**MsiProvideAssembly**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)
    -   [<span data-ttu-id="d4c7b-158">**Propriété MsiWin32AssemblySupport**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-158">**MsiWin32AssemblySupport Property**</span></span>](msiwin32assemblysupport.md)
    -   [<span data-ttu-id="d4c7b-159">**Propriété MsiNetAssemblySupport**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-159">**MsiNetAssemblySupport Property**</span></span>](msinetassemblysupport.md)
    -   [<span data-ttu-id="d4c7b-160">**Composants isolés**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-160">**Isolated Components**</span></span>](isolated-components.md)

-   <span data-ttu-id="d4c7b-161">Préparez l’application pour installer ses propres mises à niveau majeures complètes.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-161">Prepare the application to install its own comprehensive major upgrades.</span></span>

    <span data-ttu-id="d4c7b-162">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-162">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-163">Correctifs et mises à niveau</span><span class="sxs-lookup"><span data-stu-id="d4c7b-163">Patching and Upgrades</span></span>](patching-and-upgrades.md)
    -   [<span data-ttu-id="d4c7b-164">Mises à niveau majeures</span><span class="sxs-lookup"><span data-stu-id="d4c7b-164">Major Upgrades</span></span>](major-upgrades.md)
    -   [<span data-ttu-id="d4c7b-165">**UpgradeCode, propriété**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-165">**UpgradeCode Property**</span></span>](upgradecode.md)
    -   [<span data-ttu-id="d4c7b-166">**Utilisation d’un UpgradeCode**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-166">**Using an UpgradeCode**</span></span>](using-an-upgradecode.md)
    -   [<span data-ttu-id="d4c7b-167">Empêcher l’installation d’un ancien package sur une version plus récente</span><span class="sxs-lookup"><span data-stu-id="d4c7b-167">Preventing an Old Package from Installing Over a Newer Version</span></span>](preventing-an-old-package-from-installing-over-a-newer-version.md)

-   <span data-ttu-id="d4c7b-168">Préparez l’application pour installer ses propres mises à niveau mineures, petites mises à jour ou correctifs.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-168">Prepare the application to install its own minor upgrades, small updates, or fixes.</span></span>

    <span data-ttu-id="d4c7b-169">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-169">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-170">Correctifs et mises à niveau</span><span class="sxs-lookup"><span data-stu-id="d4c7b-170">Patching and Upgrades</span></span>](patching-and-upgrades.md)
    -   [<span data-ttu-id="d4c7b-171">Petites mises à jour</span><span class="sxs-lookup"><span data-stu-id="d4c7b-171">Small Updates</span></span>](small-updates.md)
    -   [<span data-ttu-id="d4c7b-172">Mises à niveau mineures</span><span class="sxs-lookup"><span data-stu-id="d4c7b-172">Minor Upgrades</span></span>](minor-upgrades.md)

-   <span data-ttu-id="d4c7b-173">Organisez les ressources d’application en composants pouvant fonctionner avec l’Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-173">Organize application resources into components that can work with the Windows Installer.</span></span>

    <span data-ttu-id="d4c7b-174">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-174">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-175">Composants Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d4c7b-175">Windows Installer Components</span></span>](windows-installer-components.md)
    -   [<span data-ttu-id="d4c7b-176">Utilisation des fonctionnalités et des composants</span><span class="sxs-lookup"><span data-stu-id="d4c7b-176">Working with Features and Components</span></span>](working-with-features-and-components.md)
    -   [<span data-ttu-id="d4c7b-177">Utilisation de composants transitifs</span><span class="sxs-lookup"><span data-stu-id="d4c7b-177">Using Transitive Components</span></span>](using-transitive-components.md)
    -   [<span data-ttu-id="d4c7b-178">Que se passe-t-il si les règles des composants sont rompues ?</span><span class="sxs-lookup"><span data-stu-id="d4c7b-178">What happens if the component rules are broken?</span></span>](what-happens-if-the-component-rules-are-broken.md)
    -   [<span data-ttu-id="d4c7b-179">Organisation des applications en composants</span><span class="sxs-lookup"><span data-stu-id="d4c7b-179">Organizing Applications into Components</span></span>](organizing-applications-into-components.md)
    -   [<span data-ttu-id="d4c7b-180">Composants isolés</span><span class="sxs-lookup"><span data-stu-id="d4c7b-180">Isolated Components</span></span>](isolated-components.md)
    -   [<span data-ttu-id="d4c7b-181">Composants qualifiés</span><span class="sxs-lookup"><span data-stu-id="d4c7b-181">Qualified Components</span></span>](qualified-components.md)

## <a name="setup-authors"></a><span data-ttu-id="d4c7b-182">Auteurs d’installation</span><span class="sxs-lookup"><span data-stu-id="d4c7b-182">Setup Authors</span></span>

<span data-ttu-id="d4c7b-183">Le programme d’installation crée des packages de Windows Installer (fichiers. msi) qui contiennent la logique d’installation et les informations nécessaires pour installer une application.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-183">Setup Authors create Windows Installer packages (.msi files) that contain the setup logic and information needed to install an application.</span></span> <span data-ttu-id="d4c7b-184">Ils utilisent généralement des outils de création tels que [Orca.exe](orca-exe.md) pour remplir la base de données Windows Installer avec la logique d’installation et des informations.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-184">They typically use authoring tools such as [Orca.exe](orca-exe.md) to populate the Windows Installer database with the setup logic and information.</span></span> <span data-ttu-id="d4c7b-185">En règle générale, les auteurs d’installation effectuent les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-185">Typically, Setup Authors do the following:</span></span>

-   <span data-ttu-id="d4c7b-186">Déterminer les fonctionnalités disponibles avec différentes versions de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-186">Determine the functionality available with different Windows Installer versions.</span></span>

    <span data-ttu-id="d4c7b-187">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-187">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-188">Détermination de la version de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d4c7b-188">Determining the Windows Installer Version</span></span>](determining-the-windows-installer-version.md)
    -   [<span data-ttu-id="d4c7b-189">Versions commercialisées de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d4c7b-189">Released Versions of Windows Installer</span></span>](released-versions-of-windows-installer.md)
    -   [<span data-ttu-id="d4c7b-190">Nouveautés de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d4c7b-190">What's New in Windows Installer</span></span>](what-s-new-in-windows-installer.md)

-   <span data-ttu-id="d4c7b-191">Organisez les ressources d’application en composants Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-191">Organize application resources into Windows Installer components.</span></span>

    <span data-ttu-id="d4c7b-192">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-192">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-193">Composants Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d4c7b-193">Windows Installer Components</span></span>](windows-installer-components.md)
    -   [<span data-ttu-id="d4c7b-194">Organisation des applications en composants</span><span class="sxs-lookup"><span data-stu-id="d4c7b-194">Organizing Applications into Components</span></span>](organizing-applications-into-components.md)
    -   [<span data-ttu-id="d4c7b-195">Modification du code du composant</span><span class="sxs-lookup"><span data-stu-id="d4c7b-195">Changing the Component Code</span></span>](changing-the-component-code.md)
    -   [<span data-ttu-id="d4c7b-196">Que se passe-t-il si les règles des composants sont rompues ?</span><span class="sxs-lookup"><span data-stu-id="d4c7b-196">What happens if the component rules are broken?</span></span>](what-happens-if-the-component-rules-are-broken.md)
    -   [<span data-ttu-id="d4c7b-197">Exemples de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d4c7b-197">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="d4c7b-198">Utilisez des outils de création de packages tiers Windows Installer ou des outils du kit de développement logiciel (SDK) tels que [Orca.exe](orca-exe.md) pour remplir une base de données d’installation et créer un package de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-198">Use third-party Windows Installer package authoring tools or SDK tools such as [Orca.exe](orca-exe.md) to populate an installation database and create a Windows Installer package.</span></span>

    <span data-ttu-id="d4c7b-199">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-199">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-200">Outils de développement Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d4c7b-200">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
    -   [<span data-ttu-id="d4c7b-201">Package d’installation, à propos de la base de données du programme d’installation</span><span class="sxs-lookup"><span data-stu-id="d4c7b-201">Installation Package, About the Installer Database</span></span>](installation-package.md)
    -   [<span data-ttu-id="d4c7b-202">Extensions de fichier Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d4c7b-202">Windows Installer File Extensions</span></span>](windows-installer-file-extensions.md)
    -   [<span data-ttu-id="d4c7b-203">Tables de base de données</span><span class="sxs-lookup"><span data-stu-id="d4c7b-203">Database Tables</span></span>](database-tables.md)
    -   [<span data-ttu-id="d4c7b-204">Codes de package</span><span class="sxs-lookup"><span data-stu-id="d4c7b-204">Package Codes</span></span>](package-codes.md)
    -   [<span data-ttu-id="d4c7b-205">Création d’un package volumineux</span><span class="sxs-lookup"><span data-stu-id="d4c7b-205">Authoring a Large Package</span></span>](authoring-a-large-package.md)
    -   [<span data-ttu-id="d4c7b-206">Windows Installer sur les systèmes d’exploitation 64 bits</span><span class="sxs-lookup"><span data-stu-id="d4c7b-206">Windows Installer on 64-bit Operating Systems</span></span>](windows-installer-on-64-bit-operating-systems.md)
    -   [<span data-ttu-id="d4c7b-207">Attribution d’un nom aux tables, propriétés et actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="d4c7b-207">Naming Custom Tables, Properties, and Actions</span></span>](naming-custom-tables-properties-and-actions.md)
    -   [<span data-ttu-id="d4c7b-208">Limitations OLE sur les flux</span><span class="sxs-lookup"><span data-stu-id="d4c7b-208">OLE Limitations on Streams</span></span>](ole-limitations-on-streams.md)
    -   [<span data-ttu-id="d4c7b-209">Format de définition de colonne</span><span class="sxs-lookup"><span data-stu-id="d4c7b-209">Column Definition Format</span></span>](column-definition-format.md)
    -   [<span data-ttu-id="d4c7b-210">Réduction de la taille d’un fichier. msi</span><span class="sxs-lookup"><span data-stu-id="d4c7b-210">Reducing the Size of an .msi File</span></span>](reducing-the-size-of-an--msi-file.md)

-   <span data-ttu-id="d4c7b-211">Créez la base de données Windows Installer pour installer des fichiers.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-211">Author the Windows Installer database to install files.</span></span>

    <span data-ttu-id="d4c7b-212">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-212">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-213">Groupe de tables principales</span><span class="sxs-lookup"><span data-stu-id="d4c7b-213">Core Tables Group</span></span>](core-tables-group.md)
    -   [<span data-ttu-id="d4c7b-214">Groupe de tables de fichiers</span><span class="sxs-lookup"><span data-stu-id="d4c7b-214">File Tables Group</span></span>](file-tables-group.md)
    -   [<span data-ttu-id="d4c7b-215">Table de fichier</span><span class="sxs-lookup"><span data-stu-id="d4c7b-215">File Table</span></span>](file-table.md)
    -   [<span data-ttu-id="d4c7b-216">Recherche de fichiers</span><span class="sxs-lookup"><span data-stu-id="d4c7b-216">File Searching</span></span>](file-searching.md)
    -   [<span data-ttu-id="d4c7b-217">Coût des fichiers</span><span class="sxs-lookup"><span data-stu-id="d4c7b-217">File Costing</span></span>](file-costing.md)
    -   [<span data-ttu-id="d4c7b-218">Installation du fichier</span><span class="sxs-lookup"><span data-stu-id="d4c7b-218">File Installation</span></span>](file-installation.md)
    -   [<span data-ttu-id="d4c7b-219">Fichiers auxiliaires</span><span class="sxs-lookup"><span data-stu-id="d4c7b-219">Companion Files</span></span>](companion-files.md)
    -   [<span data-ttu-id="d4c7b-220">Règles de contrôle de version des fichiers</span><span class="sxs-lookup"><span data-stu-id="d4c7b-220">File Versioning Rules</span></span>](file-versioning-rules.md)
    -   [<span data-ttu-id="d4c7b-221">Contrôle de version de fichier par défaut</span><span class="sxs-lookup"><span data-stu-id="d4c7b-221">Default File Versioning</span></span>](default-file-versioning.md)
    -   [<span data-ttu-id="d4c7b-222">Remplacement des fichiers existants</span><span class="sxs-lookup"><span data-stu-id="d4c7b-222">Replacing Existing Files</span></span>](replacing-existing-files.md)
    -   [<span data-ttu-id="d4c7b-223">Utilisation d’armoires et de sources compressées</span><span class="sxs-lookup"><span data-stu-id="d4c7b-223">Using Cabinets and Compressed Sources</span></span>](using-cabinets-and-compressed-sources.md)
    -   [<span data-ttu-id="d4c7b-224">Suppression des fichiers bloqués</span><span class="sxs-lookup"><span data-stu-id="d4c7b-224">Removing Stranded Files</span></span>](removing-stranded-files.md)
    -   [<span data-ttu-id="d4c7b-225">Installation des composants permanents, des fichiers, des polices, des clés de Registre</span><span class="sxs-lookup"><span data-stu-id="d4c7b-225">Installing Permanent Components, Files, Fonts, Registry Keys</span></span>](installing-permanent-components-files-fonts-registry-keys.md)
    -   [<span data-ttu-id="d4c7b-226">Table FileSFPCatalog</span><span class="sxs-lookup"><span data-stu-id="d4c7b-226">FileSFPCatalog Table</span></span>](filesfpcatalog-table.md)
    -   [<span data-ttu-id="d4c7b-227">Recherche d’un fichier et création d’une propriété contenant le chemin d’accès du fichier</span><span class="sxs-lookup"><span data-stu-id="d4c7b-227">Searching for a File and Creating a Property Holding the File's Path</span></span>](searching-for-a-file-and-creating-a-property-holding-the-file-s-path.md)
    -   [<span data-ttu-id="d4c7b-228">Recherche d’un répertoire et d’un fichier dans le répertoire</span><span class="sxs-lookup"><span data-stu-id="d4c7b-228">Searching for a Directory and a File in the Directory</span></span>](searching-for-a-directory-and-a-file-in-the-directory.md)
    -   [<span data-ttu-id="d4c7b-229">Exemples de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d4c7b-229">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="d4c7b-230">Créer une base de données Windows Installer qui installe une structure de répertoires et des dossiers.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-230">Author a Windows Installer database that installs a directory structure and folders.</span></span>

    <span data-ttu-id="d4c7b-231">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-231">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-232">Groupe de tables principales</span><span class="sxs-lookup"><span data-stu-id="d4c7b-232">Core Tables Group</span></span>](core-tables-group.md)
    -   [<span data-ttu-id="d4c7b-233">Groupe de tables de fichiers</span><span class="sxs-lookup"><span data-stu-id="d4c7b-233">File Tables Group</span></span>](file-tables-group.md)
    -   [<span data-ttu-id="d4c7b-234">Table des composants</span><span class="sxs-lookup"><span data-stu-id="d4c7b-234">Component Table</span></span>](component-table.md)
    -   [<span data-ttu-id="d4c7b-235">Table de répertoire</span><span class="sxs-lookup"><span data-stu-id="d4c7b-235">Directory Table</span></span>](directory-table.md)
    -   [<span data-ttu-id="d4c7b-236">Utilisation de la table Directory</span><span class="sxs-lookup"><span data-stu-id="d4c7b-236">Using the Directory Table</span></span>](using-the-directory-table.md)
    -   [<span data-ttu-id="d4c7b-237">Utilisation d’une propriété de répertoire dans un chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="d4c7b-237">Using a Directory Property in a Path</span></span>](using-a-directory-property-in-a-path.md)
    -   [<span data-ttu-id="d4c7b-238">Propriétés du dossier système</span><span class="sxs-lookup"><span data-stu-id="d4c7b-238">System Folder Properties</span></span>](property-reference.md)
    -   [<span data-ttu-id="d4c7b-239">Table CreateFolder</span><span class="sxs-lookup"><span data-stu-id="d4c7b-239">CreateFolder Table</span></span>](createfolder-table.md)
    -   [<span data-ttu-id="d4c7b-240">Table LockPermissions</span><span class="sxs-lookup"><span data-stu-id="d4c7b-240">LockPermissions Table</span></span>](lockpermissions-table.md)
    -   [<span data-ttu-id="d4c7b-241">Table MsiLockPermissionsEx</span><span class="sxs-lookup"><span data-stu-id="d4c7b-241">MsiLockPermissionsEx Table</span></span>](msilockpermissionsex-table.md)
    -   [<span data-ttu-id="d4c7b-242">Modification de l’emplacement cible d’un répertoire</span><span class="sxs-lookup"><span data-stu-id="d4c7b-242">Changing the Target Location for a Directory</span></span>](changing-the-target-location-for-a-directory.md)
    -   [<span data-ttu-id="d4c7b-243">Exemples de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d4c7b-243">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="d4c7b-244">Créer une base de données Windows Installer qui installe des clés de registre.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-244">Author a Windows Installer database that installs registry keys.</span></span>

    <span data-ttu-id="d4c7b-245">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-245">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-246">Groupe de tables principales</span><span class="sxs-lookup"><span data-stu-id="d4c7b-246">Core Tables Group</span></span>](core-tables-group.md)
    -   [<span data-ttu-id="d4c7b-247">Groupe de tables de Registre</span><span class="sxs-lookup"><span data-stu-id="d4c7b-247">Registry Tables Group</span></span>](registry-tables-group.md)
    -   [<span data-ttu-id="d4c7b-248">Table du Registre</span><span class="sxs-lookup"><span data-stu-id="d4c7b-248">Registry Table</span></span>](registry-table.md)
    -   [<span data-ttu-id="d4c7b-249">Modification du Registre</span><span class="sxs-lookup"><span data-stu-id="d4c7b-249">Modifying the Registry</span></span>](modifying-the-registry.md)
    -   [<span data-ttu-id="d4c7b-250">Ajout ou suppression de clés de registre lors de l’installation ou de la suppression de composants</span><span class="sxs-lookup"><span data-stu-id="d4c7b-250">Adding or Removing Registry Keys on the Installation or Removal of Components</span></span>](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md)
    -   [<span data-ttu-id="d4c7b-251">Ajout et suppression d’une application et absence de trace dans le registre</span><span class="sxs-lookup"><span data-stu-id="d4c7b-251">Adding and Removing an Application and Leaving No Trace in the Registry</span></span>](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)
    -   [<span data-ttu-id="d4c7b-252">Installation des composants permanents, des fichiers, des polices, des clés de Registre</span><span class="sxs-lookup"><span data-stu-id="d4c7b-252">Installing Permanent Components, Files, Fonts, Registry Keys</span></span>](installing-permanent-components-files-fonts-registry-keys.md)
    -   [<span data-ttu-id="d4c7b-253">Recherche d’applications, de fichiers, d’entrées de registre ou d’entrées de fichier. ini existants</span><span class="sxs-lookup"><span data-stu-id="d4c7b-253">Searching for Existing Applications, Files, Registry Entries or .ini File Entries</span></span>](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
    -   [<span data-ttu-id="d4c7b-254">Recherche d’une entrée de Registre et création d’une propriété contenant la valeur du Registre</span><span class="sxs-lookup"><span data-stu-id="d4c7b-254">Searching for a Registry Entry and Creating a Property Holding the Value of the Registry</span></span>](searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry.md)
    -   [<span data-ttu-id="d4c7b-255">Clés de registre de l’assembly écrites par l’Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d4c7b-255">Assembly Registry Keys Written by the Windows Installer</span></span>](assembly-registry-keys-written-by-windows-installer-.md)
    -   [<span data-ttu-id="d4c7b-256">Désinstaller la clé de Registre</span><span class="sxs-lookup"><span data-stu-id="d4c7b-256">Uninstall Registry Key</span></span>](uninstall-registry-key.md)
    -   [<span data-ttu-id="d4c7b-257">Table SelfReg</span><span class="sxs-lookup"><span data-stu-id="d4c7b-257">SelfReg Table</span></span>](selfreg-table.md)
    -   [<span data-ttu-id="d4c7b-258">Spécification de l’ordre d’inscription automatique</span><span class="sxs-lookup"><span data-stu-id="d4c7b-258">Specifying the Order of Self Registration</span></span>](specifying-the-order-of-self-registration.md)
    -   [<span data-ttu-id="d4c7b-259">Exemples de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d4c7b-259">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="d4c7b-260">Créer une base de données Windows Installer qui installe les services.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-260">Author a Windows Installer database that installs services.</span></span>

    <span data-ttu-id="d4c7b-261">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-261">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-262">Table ServiceInstall</span><span class="sxs-lookup"><span data-stu-id="d4c7b-262">ServiceInstall Table</span></span>](serviceinstall-table.md)
    -   [<span data-ttu-id="d4c7b-263">Table ServiceControl</span><span class="sxs-lookup"><span data-stu-id="d4c7b-263">ServiceControl Table</span></span>](servicecontrol-table.md)
    -   [<span data-ttu-id="d4c7b-264">Table des composants</span><span class="sxs-lookup"><span data-stu-id="d4c7b-264">Component Table</span></span>](component-table.md)

-   <span data-ttu-id="d4c7b-265">Créer une base de données Windows Installer qui installe des composants isolés ou des composants COM.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-265">Author a Windows Installer database that installs isolated components or COM components.</span></span>

    <span data-ttu-id="d4c7b-266">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-266">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-267">Groupe de tables de Registre</span><span class="sxs-lookup"><span data-stu-id="d4c7b-267">Registry Tables Group</span></span>](registry-tables-group.md)
    -   [<span data-ttu-id="d4c7b-268">Table de classe</span><span class="sxs-lookup"><span data-stu-id="d4c7b-268">Class Table</span></span>](class-table.md)
    -   [<span data-ttu-id="d4c7b-269">Table ComPlus</span><span class="sxs-lookup"><span data-stu-id="d4c7b-269">Complus Table</span></span>](complus-table.md)
    -   [<span data-ttu-id="d4c7b-270">Composants isolés</span><span class="sxs-lookup"><span data-stu-id="d4c7b-270">Isolated Components</span></span>](isolated-components.md)
    -   [<span data-ttu-id="d4c7b-271">Utilisation des composants isolés</span><span class="sxs-lookup"><span data-stu-id="d4c7b-271">Using Isolated Components</span></span>](using-isolated-components.md)
    -   [<span data-ttu-id="d4c7b-272">Installation de composants isolés</span><span class="sxs-lookup"><span data-stu-id="d4c7b-272">Installation of Isolated Components</span></span>](installation-of-isolated-components.md)
    -   [<span data-ttu-id="d4c7b-273">Réinstallation de composants isolés</span><span class="sxs-lookup"><span data-stu-id="d4c7b-273">Reinstallation of Isolated Components</span></span>](reinstallation-of-isolated-components.md)
    -   [<span data-ttu-id="d4c7b-274">Suppression de composants isolés</span><span class="sxs-lookup"><span data-stu-id="d4c7b-274">Removal of Isolated Components</span></span>](removal-of-isolated-components.md)
    -   [<span data-ttu-id="d4c7b-275">Installation d’un composant COM dans un emplacement privé</span><span class="sxs-lookup"><span data-stu-id="d4c7b-275">Installing a COM Component to a Private Location</span></span>](installing-a-com-component-to-a-private-location.md)
    -   [<span data-ttu-id="d4c7b-276">Rendre un composant COM dans un package existant privé</span><span class="sxs-lookup"><span data-stu-id="d4c7b-276">Make a COM Component in an Existing Package Private</span></span>](make-a-com-component-in-an-existing-package-private.md)
    -   [<span data-ttu-id="d4c7b-277">Installation d’une application COM+ avec la Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d4c7b-277">Installing a COM+ Application with the Windows Installer</span></span>](installing-a-com--application-with-the-windows-installer.md)
    -   [<span data-ttu-id="d4c7b-278">Installation d’un composant non-COM dans un emplacement privé</span><span class="sxs-lookup"><span data-stu-id="d4c7b-278">Installing a non-COM Component to a Private Location</span></span>](installing-a-non-com-component-to-a-private-location.md)
    -   [<span data-ttu-id="d4c7b-279">Rendre un composant non-COM dans un package existant privé</span><span class="sxs-lookup"><span data-stu-id="d4c7b-279">Make a non-COM Component in an Existing Package Private</span></span>](make-a-non-com-component-in-an-existing-package-private.md)

-   <span data-ttu-id="d4c7b-280">Créer une base de données Windows Installer qui installe les assemblys.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-280">Author a Windows Installer database that installs assemblies.</span></span>

    <span data-ttu-id="d4c7b-281">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-281">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-282">Table MsiAssembly</span><span class="sxs-lookup"><span data-stu-id="d4c7b-282">MsiAssembly Table</span></span>](msiassembly-table.md)
    -   [<span data-ttu-id="d4c7b-283">Table MsiAssemblyName</span><span class="sxs-lookup"><span data-stu-id="d4c7b-283">MsiAssemblyName Table</span></span>](msiassemblyname-table.md)
    -   [<span data-ttu-id="d4c7b-284">Assemblys</span><span class="sxs-lookup"><span data-stu-id="d4c7b-284">Assemblies</span></span>](assemblies.md)
    -   [<span data-ttu-id="d4c7b-285">Clés de registre de l’assembly écrites par l’Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d4c7b-285">Assembly Registry Keys Written by the Windows Installer</span></span>](assembly-registry-keys-written-by-windows-installer-.md)
    -   [<span data-ttu-id="d4c7b-286">Installation d’assemblys Win32</span><span class="sxs-lookup"><span data-stu-id="d4c7b-286">Installation of Win32 Assemblies</span></span>](installation-of-win32-assemblies.md)

-   <span data-ttu-id="d4c7b-287">Créer une base de données Windows Installer qui installe les pilotes ODBC et les traducteurs.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-287">Author a Windows Installer database that installs ODBC drivers and translators.</span></span>

    <span data-ttu-id="d4c7b-288">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-288">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-289">Table ODBCAttribute</span><span class="sxs-lookup"><span data-stu-id="d4c7b-289">ODBCAttribute Table</span></span>](odbcattribute-table.md)
    -   [<span data-ttu-id="d4c7b-290">Table ODBCDriver</span><span class="sxs-lookup"><span data-stu-id="d4c7b-290">ODBCDriver Table</span></span>](odbcdriver-table.md)
    -   [<span data-ttu-id="d4c7b-291">Table ODBCTranslator</span><span class="sxs-lookup"><span data-stu-id="d4c7b-291">ODBCTranslator Table</span></span>](odbctranslator-table.md)
    -   [<span data-ttu-id="d4c7b-292">Table ODBCDataSource</span><span class="sxs-lookup"><span data-stu-id="d4c7b-292">ODBCDataSource Table</span></span>](odbcdatasource-table.md)
    -   [<span data-ttu-id="d4c7b-293">Table ODBCSourceAttribute</span><span class="sxs-lookup"><span data-stu-id="d4c7b-293">ODBCSourceAttribute Table</span></span>](odbcsourceattribute-table.md)

-   <span data-ttu-id="d4c7b-294">Créer une base de données Windows Installer qui installe le protocole MIME.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-294">Author a Windows Installer database that installs MIME.</span></span>

    <span data-ttu-id="d4c7b-295">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-295">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-296">Table MIME</span><span class="sxs-lookup"><span data-stu-id="d4c7b-296">MIME Table</span></span>](mime-table.md)
    -   [<span data-ttu-id="d4c7b-297">Table d’extension</span><span class="sxs-lookup"><span data-stu-id="d4c7b-297">Extension Table</span></span>](extension-table.md)
    -   [<span data-ttu-id="d4c7b-298">Modification du Registre</span><span class="sxs-lookup"><span data-stu-id="d4c7b-298">Modifying the Registry</span></span>](modifying-the-registry.md)

-   <span data-ttu-id="d4c7b-299">Créer une base de données Windows Installer qui installe les variables d’environnement.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-299">Author a Windows Installer database that installs environment variables.</span></span>

    <span data-ttu-id="d4c7b-300">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-300">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-301">Table d’environnement</span><span class="sxs-lookup"><span data-stu-id="d4c7b-301">Environment Table</span></span>](environment-table.md)

-   <span data-ttu-id="d4c7b-302">Créer une base de données Windows Installer qui installe les raccourcis.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-302">Author a Windows Installer database that installs shortcuts.</span></span>

    <span data-ttu-id="d4c7b-303">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-303">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-304">Tableau de raccourcis</span><span class="sxs-lookup"><span data-stu-id="d4c7b-304">Shortcut Table</span></span>](shortcut-table.md)
    -   [<span data-ttu-id="d4c7b-305">Table MsiShortcutProperty</span><span class="sxs-lookup"><span data-stu-id="d4c7b-305">MsiShortcutProperty Table</span></span>](msishortcutproperty-table.md)
    -   [<span data-ttu-id="d4c7b-306">Modification des raccourcis du programme d’installation</span><span class="sxs-lookup"><span data-stu-id="d4c7b-306">Editing Installer Shortcuts</span></span>](editing-installer-shortcuts.md)
    -   [<span data-ttu-id="d4c7b-307">Exemples de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d4c7b-307">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="d4c7b-308">Créer une base de données Windows Installer qui installe plusieurs instances d’applications.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-308">Author a Windows Installer database that installs multiple instances of applications.</span></span>

    <span data-ttu-id="d4c7b-309">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-309">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-310">Installation de plusieurs instances de produits et correctifs</span><span class="sxs-lookup"><span data-stu-id="d4c7b-310">Installing Multiple Instances of Products and Patches</span></span>](installing-multiple-instances-of-products-and-patches.md)
    -   [<span data-ttu-id="d4c7b-311">Création de plusieurs instances à l’aide de transformations d’instance</span><span class="sxs-lookup"><span data-stu-id="d4c7b-311">Authoring Multiple Instances with Instance Transforms</span></span>](authoring-multiple-instances-with-instance-transforms.md)
    -   [<span data-ttu-id="d4c7b-312">Installation de plusieurs instances à l’aide de transformations d’instance</span><span class="sxs-lookup"><span data-stu-id="d4c7b-312">Installing Multiple Instances with Instance Transforms</span></span>](installing-multiple-instances-with-instance-transforms.md)

-   <span data-ttu-id="d4c7b-313">Spécifiez les options et les États de sélection des fonctionnalités par défaut.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-313">Specify default feature selection states and options.</span></span>

    <span data-ttu-id="d4c7b-314">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-314">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-315">Groupe de tables principales</span><span class="sxs-lookup"><span data-stu-id="d4c7b-315">Core Tables Group</span></span>](core-tables-group.md)
    -   [<span data-ttu-id="d4c7b-316">Table des composants</span><span class="sxs-lookup"><span data-stu-id="d4c7b-316">Component Table</span></span>](component-table.md)
    -   [<span data-ttu-id="d4c7b-317">Tableau des fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="d4c7b-317">Feature Table</span></span>](feature-table.md)
    -   [<span data-ttu-id="d4c7b-318">Table FeatureComponents</span><span class="sxs-lookup"><span data-stu-id="d4c7b-318">FeatureComponents Table</span></span>](featurecomponents-table.md)
    -   [<span data-ttu-id="d4c7b-319">Contrôle des États de sélection des fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="d4c7b-319">Controlling Feature Selection States</span></span>](controlling-feature-selection-states.md)
    -   [<span data-ttu-id="d4c7b-320">Propriétés options d’installation de la fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="d4c7b-320">Feature Installation Options Properties</span></span>](property-reference.md)

-   <span data-ttu-id="d4c7b-321">Spécifiez les conditions qui doivent être remplies pour installer une application ou des composants sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-321">Specify conditions that must be met to install an application or selected components.</span></span>

    <span data-ttu-id="d4c7b-322">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-322">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-323">Table de conditions</span><span class="sxs-lookup"><span data-stu-id="d4c7b-323">Condition Table</span></span>](condition-table.md)
    -   [<span data-ttu-id="d4c7b-324">Table LaunchCondition</span><span class="sxs-lookup"><span data-stu-id="d4c7b-324">LaunchCondition Table</span></span>](launchcondition-table.md)
    -   [<span data-ttu-id="d4c7b-325">Table des composants</span><span class="sxs-lookup"><span data-stu-id="d4c7b-325">Component Table</span></span>](component-table.md)
    -   [<span data-ttu-id="d4c7b-326">Utilisation des propriétés dans les instructions conditionnelles</span><span class="sxs-lookup"><span data-stu-id="d4c7b-326">Using Properties in Conditional Statements</span></span>](using-properties-in-conditional-statements.md)
    -   [<span data-ttu-id="d4c7b-327">Syntaxe d’instruction conditionnelle</span><span class="sxs-lookup"><span data-stu-id="d4c7b-327">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
    -   [<span data-ttu-id="d4c7b-328">Mesures de conditionnement à exécuter pendant la suppression</span><span class="sxs-lookup"><span data-stu-id="d4c7b-328">Conditioning Actions to Run During Removal</span></span>](conditioning-actions-to-run-during-removal.md)
    -   [<span data-ttu-id="d4c7b-329">Exemples de syntaxe d’instruction conditionnelle</span><span class="sxs-lookup"><span data-stu-id="d4c7b-329">Examples of Conditional Statement Syntax</span></span>](examples-of-conditional-statement-syntax.md)

-   <span data-ttu-id="d4c7b-330">Créez la séquence d’actions utilisée pour installer l’application.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-330">Author the sequence of actions used to install the application.</span></span>

    <span data-ttu-id="d4c7b-331">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-331">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-332">Utilisation d’une table de séquences</span><span class="sxs-lookup"><span data-stu-id="d4c7b-332">Using a Sequence Table</span></span>](using-a-sequence-table.md)
    -   [<span data-ttu-id="d4c7b-333">Groupe de tables de procédure d’installation</span><span class="sxs-lookup"><span data-stu-id="d4c7b-333">Installation Procedure Tables Group</span></span>](installation-procedure-tables-group.md)
    -   [<span data-ttu-id="d4c7b-334">Exemple de table de séquence détaillé</span><span class="sxs-lookup"><span data-stu-id="d4c7b-334">Sequence Table Detailed Example</span></span>](sequence-table-detailed-example.md)
    -   [<span data-ttu-id="d4c7b-335">Actions avec restrictions de séquencement</span><span class="sxs-lookup"><span data-stu-id="d4c7b-335">Actions with Sequencing Restrictions</span></span>](actions-with-sequencing-restrictions.md)
    -   [<span data-ttu-id="d4c7b-336">Actions sans restrictions de séquencement</span><span class="sxs-lookup"><span data-stu-id="d4c7b-336">Actions without Sequencing Restrictions</span></span>](actions-without-sequencing-restrictions.md)
    -   [<span data-ttu-id="d4c7b-337">Utilisation des propriétés dans les instructions conditionnelles</span><span class="sxs-lookup"><span data-stu-id="d4c7b-337">Using Properties in Conditional Statements</span></span>](using-properties-in-conditional-statements.md)
    -   [<span data-ttu-id="d4c7b-338">Syntaxe d’instruction conditionnelle</span><span class="sxs-lookup"><span data-stu-id="d4c7b-338">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
    -   [<span data-ttu-id="d4c7b-339">Exemples de syntaxe d’instruction conditionnelle</span><span class="sxs-lookup"><span data-stu-id="d4c7b-339">Examples of Conditional Statement Syntax</span></span>](examples-of-conditional-statement-syntax.md)
    -   [<span data-ttu-id="d4c7b-340">Mesures de conditionnement à exécuter pendant la suppression</span><span class="sxs-lookup"><span data-stu-id="d4c7b-340">Conditioning Actions to Run During Removal</span></span>](conditioning-actions-to-run-during-removal.md)
    -   [<span data-ttu-id="d4c7b-341">Actions standard</span><span class="sxs-lookup"><span data-stu-id="d4c7b-341">Standard Actions</span></span>](standard-actions.md)
    -   [<span data-ttu-id="d4c7b-342">Exemples de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d4c7b-342">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="d4c7b-343">Préparez le package d’installation de l’application pour les futures mises à niveau de l’application par le service Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-343">Prepare the installation package of the application for future upgrades of the application by the Windows Installer service.</span></span>

    <span data-ttu-id="d4c7b-344">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-344">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-345">Correctifs et mises à niveau</span><span class="sxs-lookup"><span data-stu-id="d4c7b-345">Patching and Upgrades</span></span>](patching-and-upgrades.md)
    -   [<span data-ttu-id="d4c7b-346">Préparation d’une application pour les futures mises à niveau majeures</span><span class="sxs-lookup"><span data-stu-id="d4c7b-346">Preparing an Application for Future Major Upgrades</span></span>](preparing-an-application-for-future-major-upgrades.md)
    -   [<span data-ttu-id="d4c7b-347">Utilisation d’un UpgradeCode</span><span class="sxs-lookup"><span data-stu-id="d4c7b-347">Using an UpgradeCode</span></span>](using-an-upgradecode.md)
    -   [<span data-ttu-id="d4c7b-348">Mettre à niveau la table</span><span class="sxs-lookup"><span data-stu-id="d4c7b-348">Upgrade Table</span></span>](upgrade-table.md)
    -   [<span data-ttu-id="d4c7b-349">**UpgradeCode, propriété**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-349">**UpgradeCode Property**</span></span>](upgradecode.md)
    -   [<span data-ttu-id="d4c7b-350">Empêcher l’installation d’un ancien package sur une version plus récente</span><span class="sxs-lookup"><span data-stu-id="d4c7b-350">Preventing an Old Package from Installing Over a Newer Version</span></span>](preventing-an-old-package-from-installing-over-a-newer-version.md)
    -   [<span data-ttu-id="d4c7b-351">Modification du code du produit</span><span class="sxs-lookup"><span data-stu-id="d4c7b-351">Changing the Product Code</span></span>](changing-the-product-code.md)
    -   [<span data-ttu-id="d4c7b-352">Mise à jour des assemblys</span><span class="sxs-lookup"><span data-stu-id="d4c7b-352">Updating Assemblies</span></span>](updating-assemblies.md)
    -   [<span data-ttu-id="d4c7b-353">Exemples de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d4c7b-353">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="d4c7b-354">Résolvez les problèmes Windows Installer packages en cours de développement.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-354">Troubleshoot Windows Installer packages under development.</span></span>

    <span data-ttu-id="d4c7b-355">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-355">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-356">Validations de package</span><span class="sxs-lookup"><span data-stu-id="d4c7b-356">Package Validation</span></span>](package-validation.md)
    -   [<span data-ttu-id="d4c7b-357">Évaluateurs de cohérence internes-CIEM</span><span class="sxs-lookup"><span data-stu-id="d4c7b-357">Internal Consistency Evaluators - ICEs</span></span>](internal-consistency-evaluators-ices.md)
    -   [<span data-ttu-id="d4c7b-358">Journalisation Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d4c7b-358">Windows Installer Logging</span></span>](windows-installer-logging.md)
    -   [<span data-ttu-id="d4c7b-359">Vérification de l’installation des fonctionnalités, des composants, des fichiers</span><span class="sxs-lookup"><span data-stu-id="d4c7b-359">Checking the Installation of Features, Components, Files</span></span>](checking-the-installation-of-features-components-files.md)
    -   [<span data-ttu-id="d4c7b-360">Création d’un package volumineux</span><span class="sxs-lookup"><span data-stu-id="d4c7b-360">Authoring a Large Package</span></span>](authoring-a-large-package.md)
    -   [<span data-ttu-id="d4c7b-361">Wilogutl.exe</span><span class="sxs-lookup"><span data-stu-id="d4c7b-361">Wilogutl.exe</span></span>](wilogutl-exe.md)
    -   [<span data-ttu-id="d4c7b-362">Outils de développement Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d4c7b-362">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
    -   [<span data-ttu-id="d4c7b-363">Validation des modules de fusion</span><span class="sxs-lookup"><span data-stu-id="d4c7b-363">Validating Merge Modules</span></span>](validating-merge-modules.md)
    -   [<span data-ttu-id="d4c7b-364">Validation d’une base de données d’installation</span><span class="sxs-lookup"><span data-stu-id="d4c7b-364">Validating an Installation Database</span></span>](validating-an-installation-database.md)
    -   [<span data-ttu-id="d4c7b-365">Validation de la mise à niveau d’une installation</span><span class="sxs-lookup"><span data-stu-id="d4c7b-365">Validating an Installation Upgrade</span></span>](validating-an-installation-upgrade.md)
    -   [<span data-ttu-id="d4c7b-366">Recherche d’une fonctionnalité ou d’un composant endommagé</span><span class="sxs-lookup"><span data-stu-id="d4c7b-366">Searching for a Broken Feature or Component</span></span>](searching-for-a-broken-feature-or-component.md)
    -   [<span data-ttu-id="d4c7b-367">Windows Installer des messages d’erreur</span><span class="sxs-lookup"><span data-stu-id="d4c7b-367">Windows Installer Error Messages</span></span>](windows-installer-error-messages.md)
    -   [<span data-ttu-id="d4c7b-368">Journalisation des demandes de redémarrage</span><span class="sxs-lookup"><span data-stu-id="d4c7b-368">Logging of Reboot Requests</span></span>](logging-of-reboot-requests.md)

-   <span data-ttu-id="d4c7b-369">Assurez une configuration et une installation sécurisées de l’application.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-369">Ensure a secure setup and installation of the application.</span></span>

    <span data-ttu-id="d4c7b-370">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-370">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-371">Instructions pour la création d’installations sécurisées</span><span class="sxs-lookup"><span data-stu-id="d4c7b-371">Guidelines for Authoring Secure Installations</span></span>](guidelines-for-authoring-secure-installations.md)
    -   [<span data-ttu-id="d4c7b-372">Instructions pour la sécurisation des actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="d4c7b-372">Guidelines for Securing Custom Actions</span></span>](guidelines-for-securing-custom-actions.md)
    -   [<span data-ttu-id="d4c7b-373">Sécurité des actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="d4c7b-373">Custom Action Security</span></span>](custom-action-security.md)
    -   [<span data-ttu-id="d4c7b-374">Instructions pour la sécurisation des packages sur les ordinateurs verrouillés</span><span class="sxs-lookup"><span data-stu-id="d4c7b-374">Guidelines for Securing Packages on Locked-Down Computers</span></span>](guidelines-for-securing-packages-on-locked-down-computers.md)
    -   [<span data-ttu-id="d4c7b-375">Création d’une installation signée entièrement vérifiée à l’aide d’Automation</span><span class="sxs-lookup"><span data-stu-id="d4c7b-375">Authoring a Fully Verified Signed Installation Using Automation</span></span>](authoring-a-fully-verified-signed-installation-using-automation.md)
    -   [<span data-ttu-id="d4c7b-376">Exemple d’installation de Windows Installer basée sur une URL</span><span class="sxs-lookup"><span data-stu-id="d4c7b-376">A URL-Based Windows Installer Installation Example</span></span>](a-url-based-windows-installer-installation-example.md)
    -   [<span data-ttu-id="d4c7b-377">Création de l’interface utilisateur pour l’entrée de mot de passe</span><span class="sxs-lookup"><span data-stu-id="d4c7b-377">Authoring the User Interface for Password Input</span></span>](authoring-the-user-interface-for-password-input.md)
    -   [<span data-ttu-id="d4c7b-378">Signatures numériques et Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d4c7b-378">Digital Signatures and Windows Installer</span></span>](digital-signatures-and-windows-installer.md)
    -   [<span data-ttu-id="d4c7b-379">Utilisation de Windows Installer avec UAC</span><span class="sxs-lookup"><span data-stu-id="d4c7b-379">Using Windows Installer with UAC</span></span>](using-windows-installer-with-uac.md)
    -   [<span data-ttu-id="d4c7b-380">Mise à jour corrective du contrôle de compte d’utilisateur (UAC)</span><span class="sxs-lookup"><span data-stu-id="d4c7b-380">User Account Control (UAC) Patching</span></span>](user-account-control--uac--patching.md)
    -   [<span data-ttu-id="d4c7b-381">Msicert.exe</span><span class="sxs-lookup"><span data-stu-id="d4c7b-381">Msicert.exe</span></span>](msicert-exe.md)
    -   [<span data-ttu-id="d4c7b-382">**Propriété AdminUser**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-382">**AdminUser property**</span></span>](adminuser.md)
    -   [<span data-ttu-id="d4c7b-383">**Privileged, propriété**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-383">**Privileged property**</span></span>](privileged.md)
    -   [<span data-ttu-id="d4c7b-384">**Propriété SecureCustomProperties**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-384">**SecureCustomProperties property**</span></span>](securecustomproperties.md)

-   <span data-ttu-id="d4c7b-385">Créez une interface utilisateur pour présenter les options permettant de configurer l’installation et d’obtenir des informations de l’utilisateur sur le processus d’installation en attente.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-385">Create a user interface to present options to configure the installation and obtain information from the user about the pending installation process.</span></span>

    <span data-ttu-id="d4c7b-386">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-386">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-387">À propos de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="d4c7b-387">About the User Interface</span></span>](about-the-user-interface.md)
    -   [<span data-ttu-id="d4c7b-388">Ajout de contrôles et de texte</span><span class="sxs-lookup"><span data-stu-id="d4c7b-388">Adding Controls and Text</span></span>](adding-controls-and-text.md)
    -   [<span data-ttu-id="d4c7b-389">Création d’un contrôle ProgressBar</span><span class="sxs-lookup"><span data-stu-id="d4c7b-389">Authoring a ProgressBar Control</span></span>](authoring-a-progressbar-control.md)
    -   [<span data-ttu-id="d4c7b-390">Messages d’invite de création de disque</span><span class="sxs-lookup"><span data-stu-id="d4c7b-390">Authoring Disk Prompt Messages</span></span>](authoring-disk-prompt-messages.md)
    -   [<span data-ttu-id="d4c7b-391">Création d’une condition « Veuillez patienter... » Boîte de message</span><span class="sxs-lookup"><span data-stu-id="d4c7b-391">Authoring a Conditional "Please Wait . . ." Message Box</span></span>](authoring-a-conditional-please-wait-------message-box.md)
    -   [<span data-ttu-id="d4c7b-392">Aperçu de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="d4c7b-392">Previewing the User Interface</span></span>](previewing-the-user-interface.md)
    -   [<span data-ttu-id="d4c7b-393">Ajout de texte stocké dans une propriété</span><span class="sxs-lookup"><span data-stu-id="d4c7b-393">Adding Text Stored in a Property</span></span>](adding-text-stored-in-a-property.md)
    -   [<span data-ttu-id="d4c7b-394">**MsiSetInternalUI**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-394">**MsiSetInternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

-   <span data-ttu-id="d4c7b-395">Créer une interface utilisateur externe pour présenter une interface utilisateur personnalisée afin de configurer l’installation et d’obtenir des informations de l’utilisateur sur le processus d’installation en attente.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-395">Create an external user interface to present a custom user interface to configure the installation and obtain information from the user about the pending installation process.</span></span>

    <span data-ttu-id="d4c7b-396">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-396">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-397">**MsiSetExternalUI**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-397">**MsiSetExternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
    -   [<span data-ttu-id="d4c7b-398">Surveillance d’une installation à l’aide de MsiSetExternalUIRecord</span><span class="sxs-lookup"><span data-stu-id="d4c7b-398">Monitoring an Installation Using MsiSetExternalUIRecord</span></span>](monitoring-an-installation-using-msisetexternaluirecord.md)
    -   [<span data-ttu-id="d4c7b-399">Analyse des messages de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d4c7b-399">Parsing Windows Installer Messages</span></span>](parsing-windows-installer-messages.md)
    -   [<span data-ttu-id="d4c7b-400">Retour de valeurs à partir d’un gestionnaire d’interface utilisateur externe</span><span class="sxs-lookup"><span data-stu-id="d4c7b-400">Returning Values from an External User Interface Handler</span></span>](returning-values-from-an-external-user-interface-handler.md)
    -   [<span data-ttu-id="d4c7b-401">\_Gestionnaire INSTALLUI</span><span class="sxs-lookup"><span data-stu-id="d4c7b-401">INSTALLUI\_HANDLER</span></span>](/windows/desktop/api/Msi/nc-msi-installui_handlera)
    -   [<span data-ttu-id="d4c7b-402">Gestion des messages de progression à l’aide de MsiSetExternalUI</span><span class="sxs-lookup"><span data-stu-id="d4c7b-402">Handling Progress Messages Using MsiSetExternalUI</span></span>](handling-progress-messages-using-msisetexternalui.md)
    -   [<span data-ttu-id="d4c7b-403">Surveillance d’une installation à l’aide de MsiSetExternalUI</span><span class="sxs-lookup"><span data-stu-id="d4c7b-403">Monitoring an Installation Using MsiSetExternalUI</span></span>](monitoring-an-installation-using-msisetexternalui.md)

-   <span data-ttu-id="d4c7b-404">Définissez les informations de l’application dans **Ajout/suppression de programmes** (ARP).</span><span class="sxs-lookup"><span data-stu-id="d4c7b-404">Set information for the application in **Add/Remove Programs** (ARP.)</span></span>

    <span data-ttu-id="d4c7b-405">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-405">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-406">Configuration de l’ajout/suppression de programmes avec Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d4c7b-406">Configuring Add/Remove Programs with Windows Installer</span></span>](configuring-add-remove-programs-with-windows-installer.md)
    -   [<span data-ttu-id="d4c7b-407">Ajout et suppression d’une application et absence de trace dans le registre</span><span class="sxs-lookup"><span data-stu-id="d4c7b-407">Adding and Removing an Application and Leaving No Trace in the Registry</span></span>](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)
    -   [<span data-ttu-id="d4c7b-408">Désinstaller la clé de Registre</span><span class="sxs-lookup"><span data-stu-id="d4c7b-408">Uninstall Registry Key</span></span>](uninstall-registry-key.md)

-   <span data-ttu-id="d4c7b-409">Écrivez des actions personnalisées pour gérer la logique d’installation qui n’est pas prise en charge en mode natif par Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-409">Write custom actions to handle setup logic that is not natively supported by Windows Installer.</span></span>

    <span data-ttu-id="d4c7b-410">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-410">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-411">Actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="d4c7b-411">Custom Actions</span></span>](custom-actions.md)
    -   [<span data-ttu-id="d4c7b-412">Liste récapitulative de tous les types d’actions personnalisés</span><span class="sxs-lookup"><span data-stu-id="d4c7b-412">Summary List of All Custom Action Types</span></span>](summary-list-of-all-custom-action-types.md)
    -   [<span data-ttu-id="d4c7b-413">Instructions pour la sécurisation des actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="d4c7b-413">Guidelines for Securing Custom Actions</span></span>](guidelines-for-securing-custom-actions.md)
    -   [<span data-ttu-id="d4c7b-414">Référence des actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="d4c7b-414">Custom Action Reference</span></span>](custom-action-reference.md)
    -   [<span data-ttu-id="d4c7b-415">Utilisation d’une action personnalisée pour créer des comptes d’utilisateur sur un ordinateur local</span><span class="sxs-lookup"><span data-stu-id="d4c7b-415">Using a Custom Action to Create User Accounts on a Local Computer</span></span>](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [<span data-ttu-id="d4c7b-416">Utilisation d’une action personnalisée pour lancer un fichier installé à la fin de l’installation</span><span class="sxs-lookup"><span data-stu-id="d4c7b-416">Using a Custom Action to Launch an Installed File at the End of the Installation</span></span>](using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation.md)
    -   [<span data-ttu-id="d4c7b-417">Accès à une base de données ou à une session à partir d’une action personnalisée</span><span class="sxs-lookup"><span data-stu-id="d4c7b-417">Accessing a Database or Session from Inside a Custom Action</span></span>](accessing-a-database-or-session-from-inside-a-custom-action.md)
    -   [<span data-ttu-id="d4c7b-418">Accès à la session de programme d’installation actuelle à partir d’une action personnalisée</span><span class="sxs-lookup"><span data-stu-id="d4c7b-418">Accessing the Current Installer Session from Inside a Custom Action</span></span>](accessing-the-current-installer-session-from-inside-a-custom-action.md)
    -   [<span data-ttu-id="d4c7b-419">Modification de l’état du système à l’aide d’une action personnalisée</span><span class="sxs-lookup"><span data-stu-id="d4c7b-419">Changing the System State Using a Custom Action</span></span>](changing-the-system-state-using-a-custom-action.md)

-   <span data-ttu-id="d4c7b-420">Amorcez le Windows Installer sur l’ordinateur d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-420">Bootstrap the Windows Installer onto a user's computer.</span></span>

    <span data-ttu-id="d4c7b-421">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-421">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-422">Amorçage</span><span class="sxs-lookup"><span data-stu-id="d4c7b-422">Bootstrapping</span></span>](bootstrapping.md)
    -   [<span data-ttu-id="d4c7b-423">Instmsi.exe</span><span class="sxs-lookup"><span data-stu-id="d4c7b-423">Instmsi.exe</span></span>](instmsi-exe.md)
    -   [<span data-ttu-id="d4c7b-424">Amorçage du téléchargement Internet</span><span class="sxs-lookup"><span data-stu-id="d4c7b-424">Internet Download Bootstrapping</span></span>](internet-download-bootstrapping.md)
    -   [<span data-ttu-id="d4c7b-425">Msistuff.exe</span><span class="sxs-lookup"><span data-stu-id="d4c7b-425">Msistuff.exe</span></span>](msistuff-exe.md)
    -   [<span data-ttu-id="d4c7b-426">Exemple d’installation de Windows Installer basée sur une URL</span><span class="sxs-lookup"><span data-stu-id="d4c7b-426">A URL-Based Windows Installer Installation Example</span></span>](a-url-based-windows-installer-installation-example.md)
    -   [<span data-ttu-id="d4c7b-427">Configuration des ressources Setup.exe</span><span class="sxs-lookup"><span data-stu-id="d4c7b-427">Configuring the Setup.exe Resources</span></span>](configuring-the-setup-exe-resources.md)
    -   [<span data-ttu-id="d4c7b-428">Téléchargement d’une installation à partir d’Internet</span><span class="sxs-lookup"><span data-stu-id="d4c7b-428">Downloading an Installation from the Internet</span></span>](downloading-an-installation-from-the-internet.md)

-   <span data-ttu-id="d4c7b-429">Respectez les instructions de Active Accessibility lors de l’écriture de packages Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-429">Adhere to Active Accessibility guidelines when writing Windows Installer packages.</span></span>

    <span data-ttu-id="d4c7b-430">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-430">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-431">Accessibilité</span><span class="sxs-lookup"><span data-stu-id="d4c7b-431">Accessibility</span></span>](accessibility.md)

-   <span data-ttu-id="d4c7b-432">Préparez l’internationalisation de l’installation d’une application.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-432">Prepare for the internationalization of an application setup.</span></span>

    <span data-ttu-id="d4c7b-433">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-433">For more information, see the following:</span></span>

    -   <span data-ttu-id="d4c7b-434">[Préparation d’un package de Windows Installer pour la localisation](preparing-a-windows-installer-package-for-localization.md),</span><span class="sxs-lookup"><span data-stu-id="d4c7b-434">[Preparing a Windows Installer Package for Localization](preparing-a-windows-installer-package-for-localization.md),</span></span>
    -   [<span data-ttu-id="d4c7b-435">Localisation d’un package Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d4c7b-435">Localizing a Windows Installer Package</span></span>](localizing-a-windows-installer-package.md)
    -   [<span data-ttu-id="d4c7b-436">Gestion des pages de codes (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="d4c7b-436">Code Page Handling (Windows Installer)</span></span>](code-page-handling-windows-installer-.md)
    -   [<span data-ttu-id="d4c7b-437">Ajout de ressources localisées</span><span class="sxs-lookup"><span data-stu-id="d4c7b-437">Adding Localized Resources</span></span>](adding-localized-resources.md)
    -   [<span data-ttu-id="d4c7b-438">Exemple de localisation</span><span class="sxs-lookup"><span data-stu-id="d4c7b-438">A Localization Example</span></span>](a-localization-example.md)
    -   [<span data-ttu-id="d4c7b-439">Localisation des tables Error et ActionText</span><span class="sxs-lookup"><span data-stu-id="d4c7b-439">Localizing the Error and ActionText Tables</span></span>](localizing-the-error-and-actiontext-tables.md)
    -   [<span data-ttu-id="d4c7b-440">Localiser des colonnes de base de données</span><span class="sxs-lookup"><span data-stu-id="d4c7b-440">Localizing Database Columns</span></span>](localizing-database-columns.md)
    -   [<span data-ttu-id="d4c7b-441">Création d’une base de données avec une page de codes neutre</span><span class="sxs-lookup"><span data-stu-id="d4c7b-441">Creating a Database with a Neutral Code Page</span></span>](creating-a-database-with-a-neutral-code-page.md)
    -   [<span data-ttu-id="d4c7b-442">Gestion des pages de codes des tables importées et exportées</span><span class="sxs-lookup"><span data-stu-id="d4c7b-442">Code Page Handling of Imported and Exported Tables</span></span>](code-page-handling-of-imported-and-exported-tables.md)
    -   [<span data-ttu-id="d4c7b-443">Localisation de la langue affichée par les boîtes de dialogue</span><span class="sxs-lookup"><span data-stu-id="d4c7b-443">Localizing the Language Displayed by Dialogs</span></span>](localizing-the-language-displayed-by-dialogs.md)
    -   [<span data-ttu-id="d4c7b-444">Importation de tables Error et ActionText localisées</span><span class="sxs-lookup"><span data-stu-id="d4c7b-444">Importing Localized Error and ActionText Tables</span></span>](importing-localized-error-and-actiontext-tables.md)
    -   [<span data-ttu-id="d4c7b-445">Mise à jour des propriétés ProductLanguage et ProductCode</span><span class="sxs-lookup"><span data-stu-id="d4c7b-445">Updating ProductLanguage and ProductCode Properties</span></span>](updating-productlanguage-and-productcode-properties.md)
    -   [<span data-ttu-id="d4c7b-446">Mise à jour d’un flux d’informations de synthèse</span><span class="sxs-lookup"><span data-stu-id="d4c7b-446">Updating a Summary Information Stream</span></span>](updating-a-summary-information-stream.md)
    -   [<span data-ttu-id="d4c7b-447">Composants qualifiés</span><span class="sxs-lookup"><span data-stu-id="d4c7b-447">Qualified Components</span></span>](qualified-components.md)
    -   [<span data-ttu-id="d4c7b-448">Table UIText</span><span class="sxs-lookup"><span data-stu-id="d4c7b-448">UIText Table</span></span>](uitext-table.md)
    -   [<span data-ttu-id="d4c7b-449">Gérer la langue et la page de codes</span><span class="sxs-lookup"><span data-stu-id="d4c7b-449">Manage Language and Codepage</span></span>](manage-language-and-codepage.md)
    -   [<span data-ttu-id="d4c7b-450">Vérification de la page de codes de la base de données d’installation</span><span class="sxs-lookup"><span data-stu-id="d4c7b-450">Checking the Installation Database Code Page</span></span>](checking-the-installation-database-code-page.md)

-   <span data-ttu-id="d4c7b-451">Créez des packages Windows Installer pour les plateformes 32 bits et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-451">Create Windows Installer packages for 32-bit and 64-bit platforms.</span></span>

    <span data-ttu-id="d4c7b-452">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-452">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-453">Windows Installer sur les systèmes d’exploitation 64 bits</span><span class="sxs-lookup"><span data-stu-id="d4c7b-453">Windows Installer on 64-bit Operating Systems</span></span>](windows-installer-on-64-bit-operating-systems.md)
    -   [<span data-ttu-id="d4c7b-454">Actions personnalisées 64 bits</span><span class="sxs-lookup"><span data-stu-id="d4c7b-454">64-Bit Custom Actions</span></span>](64-bit-custom-actions.md)
    -   [<span data-ttu-id="d4c7b-455">Utilisation d’actions personnalisées 64 bits</span><span class="sxs-lookup"><span data-stu-id="d4c7b-455">Using 64-bit Custom Actions</span></span>](using-64-bit-custom-actions.md)
    -   [<span data-ttu-id="d4c7b-456">Utilisation des modules de fusion 64 bits</span><span class="sxs-lookup"><span data-stu-id="d4c7b-456">Using 64-bit Merge Modules</span></span>](using-64-bit-merge-modules.md)

-   <span data-ttu-id="d4c7b-457">Redistribuer les composants de Windows Installer partagés et la logique d’installation en tant que modules de fusion.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-457">Redistribute shared Windows Installer components and setup logic as merge modules.</span></span>

    <span data-ttu-id="d4c7b-458">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-458">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-459">Modules de fusion</span><span class="sxs-lookup"><span data-stu-id="d4c7b-459">Merge Modules</span></span>](merge-modules.md)
    -   [<span data-ttu-id="d4c7b-460">Création d’une transformation de langue pour un module de fusion à plusieurs langues</span><span class="sxs-lookup"><span data-stu-id="d4c7b-460">Authoring a Language Transform for a Multiple Language Merge Module</span></span>](authoring-a-language-transform-for-a-multiple-language-merge-module.md)
    -   [<span data-ttu-id="d4c7b-461">Application d’un module de fusion configurable avec des personnalisations</span><span class="sxs-lookup"><span data-stu-id="d4c7b-461">Applying a Configurable Merge Module with Customizations</span></span>](applying-a-configurable-merge-module-with-customizations.md)

-   <span data-ttu-id="d4c7b-462">Planifiez ou supprimez les redémarrages au cours d’une installation Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-462">Schedule or suppress reboots during a Windows Installer installation.</span></span>

    <span data-ttu-id="d4c7b-463">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-463">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-464">Redémarrages du système</span><span class="sxs-lookup"><span data-stu-id="d4c7b-464">System Reboots</span></span>](system-reboots.md)
    -   [<span data-ttu-id="d4c7b-465">Journalisation des demandes de redémarrage</span><span class="sxs-lookup"><span data-stu-id="d4c7b-465">Logging of Reboot Requests</span></span>](logging-of-reboot-requests.md)

-   <span data-ttu-id="d4c7b-466">Créer des mises à jour ou des correctifs pour une application existante en créant un correctif.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-466">Create updates or fixes for an existing application by creating a patch.</span></span>

    <span data-ttu-id="d4c7b-467">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-467">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-468">Création d’un correctif de mise à jour de petite taille</span><span class="sxs-lookup"><span data-stu-id="d4c7b-468">Creating a Small Update Patch</span></span>](creating-a-small-update-patch.md)
    -   [<span data-ttu-id="d4c7b-469">Exemple de mise à jour corrective de petite taille</span><span class="sxs-lookup"><span data-stu-id="d4c7b-469">A Small Update Patching Example</span></span>](a-small-update-patching-example.md)

-   <span data-ttu-id="d4c7b-470">Créez un package à double usage qui peut installer une application uniquement pour l’utilisateur actuel ou pour tous les utilisateurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-470">Author a dual-purpose package capable of installing an application either for only the current user or for all users of the computer.</span></span>

    <span data-ttu-id="d4c7b-471">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-471">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-472">Contexte d’installation</span><span class="sxs-lookup"><span data-stu-id="d4c7b-472">Installation Context</span></span>](installation-context.md)
    -   [<span data-ttu-id="d4c7b-473">Création d’un package unique</span><span class="sxs-lookup"><span data-stu-id="d4c7b-473">Single Package Authoring</span></span>](single-package-authoring.md)
    -   [<span data-ttu-id="d4c7b-474">Exemple de création de package unique</span><span class="sxs-lookup"><span data-stu-id="d4c7b-474">Single Package Authoring Example</span></span>](single-package-authoring-example.md)

-   <span data-ttu-id="d4c7b-475">Personnalisez les services sur l’ordinateur à l’aide de l’Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-475">Customize services on the computer using the Windows Installer.</span></span>

    <span data-ttu-id="d4c7b-476">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-476">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-477">Utilisation de la configuration des services</span><span class="sxs-lookup"><span data-stu-id="d4c7b-477">Using Services Configuration</span></span>](using-services-configuration.md)

-   <span data-ttu-id="d4c7b-478">Sécurisez les ressources sur l’ordinateur à l’aide de l’Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-478">Secure resources on the computer using the Windows Installer.</span></span>

    <span data-ttu-id="d4c7b-479">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-479">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-480">Instructions pour la création d’installations sécurisées</span><span class="sxs-lookup"><span data-stu-id="d4c7b-480">Guidelines for Authoring Secure Installations</span></span>](guidelines-for-authoring-secure-installations.md)
    -   [<span data-ttu-id="d4c7b-481">Sécurisation des ressources</span><span class="sxs-lookup"><span data-stu-id="d4c7b-481">Securing Resources</span></span>](securing-resources-.md)

-   <span data-ttu-id="d4c7b-482">Énumérer tous les composants installés sur l’ordinateur et obtenir le chemin d’accès à la clé du composant.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-482">Enumerate all components installed on the computer and obtain the key path for the component.</span></span>

    <span data-ttu-id="d4c7b-483">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-483">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-484">Énumération des composants</span><span class="sxs-lookup"><span data-stu-id="d4c7b-484">Enumerating Components</span></span>](enumerating-components-.md)

-   <span data-ttu-id="d4c7b-485">Installer plusieurs packages à l’aide du [*traitement des transactions*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d4c7b-485">Install multiple packages using [*transaction processing*](t-gly.md).</span></span>

    <span data-ttu-id="d4c7b-486">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-486">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-487">Installations sur plusieurs packages</span><span class="sxs-lookup"><span data-stu-id="d4c7b-487">Multiple-Package Installations</span></span>](multiple-package-installations.md)

-   <span data-ttu-id="d4c7b-488">Incorporez une interface utilisateur personnalisée dans le package Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-488">Embed a custom user interface in the Windows Installer package.</span></span>

    <span data-ttu-id="d4c7b-489">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-489">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-490">Utilisation de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="d4c7b-490">Using the User Interface</span></span>](using-the-user-interface.md)
    -   [<span data-ttu-id="d4c7b-491">Utilisation d’une interface utilisateur incorporée</span><span class="sxs-lookup"><span data-stu-id="d4c7b-491">Using an Embedded UI</span></span>](using-an-embedded-ui.md)

## <a name="it-professionals"></a><span data-ttu-id="d4c7b-492">Professionnels de l’informatique</span><span class="sxs-lookup"><span data-stu-id="d4c7b-492">IT Professionals</span></span>

<span data-ttu-id="d4c7b-493">Les professionnels de l’informatique et les administrateurs peuvent personnaliser et déployer des packages de Windows Installer existants.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-493">IT Professionals and Administrators customize and deploy existing Windows Installer packages.</span></span> <span data-ttu-id="d4c7b-494">Ces utilisateurs reconditionnent les configurations des applications existantes dans Windows Installer des packages d’installation, et installent et gèrent les images administratives des installations Windows Installer sur les réseaux.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-494">These users repackage setups for existing applications into Windows Installer installation packages, and install and maintain administrative images of Windows Installer installations on networks.</span></span>

-   <span data-ttu-id="d4c7b-495">Personnaliser les applications et le programme d’installation en générant et en appliquant des transformations Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d4c7b-495">Customize applications and setup by generating and applying Windows Installer transforms</span></span>

    <span data-ttu-id="d4c7b-496">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-496">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-497">Personnalisation</span><span class="sxs-lookup"><span data-stu-id="d4c7b-497">Customization</span></span>](customization.md)
    -   [<span data-ttu-id="d4c7b-498">Transformations de base de données</span><span class="sxs-lookup"><span data-stu-id="d4c7b-498">Database Transforms</span></span>](database-transforms.md)
    -   [<span data-ttu-id="d4c7b-499">Exemple de transformation de personnalisation</span><span class="sxs-lookup"><span data-stu-id="d4c7b-499">A Customization Transform Example</span></span>](a-customization-transform-example.md)
    -   [<span data-ttu-id="d4c7b-500">Fusions et transformations</span><span class="sxs-lookup"><span data-stu-id="d4c7b-500">Merges and Transforms</span></span>](merges-and-transforms.md)
    -   [<span data-ttu-id="d4c7b-501">Utilisation des transformations pour ajouter des ressources</span><span class="sxs-lookup"><span data-stu-id="d4c7b-501">Using Transforms to Add Resources</span></span>](using-transforms-to-add-resources.md)
    -   [<span data-ttu-id="d4c7b-502">Générer une transformation</span><span class="sxs-lookup"><span data-stu-id="d4c7b-502">Generate a Transform</span></span>](generate-a-transform.md)
    -   [<span data-ttu-id="d4c7b-503">Options de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="d4c7b-503">Command Line Options</span></span>](command-line-options.md)
    -   [<span data-ttu-id="d4c7b-504">Msitran.exe</span><span class="sxs-lookup"><span data-stu-id="d4c7b-504">Msitran.exe</span></span>](msitran-exe.md)
    -   [<span data-ttu-id="d4c7b-505">Appliquer une transformation</span><span class="sxs-lookup"><span data-stu-id="d4c7b-505">Apply a Transform</span></span>](apply-a-transform.md)
    -   [<span data-ttu-id="d4c7b-506">Afficher une transformation</span><span class="sxs-lookup"><span data-stu-id="d4c7b-506">View a Transform</span></span>](view-a-transform.md)
    -   [<span data-ttu-id="d4c7b-507">Afficher les différences entre deux bases de données</span><span class="sxs-lookup"><span data-stu-id="d4c7b-507">View Differences Between Two Databases</span></span>](view-differences-between-two-databases.md)
    -   [<span data-ttu-id="d4c7b-508">Mise à jour corrective des applications personnalisées</span><span class="sxs-lookup"><span data-stu-id="d4c7b-508">Patching Customized Applications</span></span>](patching-customized-applications.md)

-   <span data-ttu-id="d4c7b-509">Déployez un package d’installation Windows Installer, une mise à jour ou un correctif logiciel.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-509">Deploy a Windows Installer installation package, update, or patch.</span></span>

    <span data-ttu-id="d4c7b-510">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-510">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-511">Installation d’une application</span><span class="sxs-lookup"><span data-stu-id="d4c7b-511">Installing an Application</span></span>](installing-an-application.md)
    -   [<span data-ttu-id="d4c7b-512">Correctifs et mises à niveau</span><span class="sxs-lookup"><span data-stu-id="d4c7b-512">Patching and Upgrades</span></span>](patching-and-upgrades.md)
    -   [<span data-ttu-id="d4c7b-513">Transformations</span><span class="sxs-lookup"><span data-stu-id="d4c7b-513">Transforms</span></span>](transforms.md)
    -   [<span data-ttu-id="d4c7b-514">Installation d’un package avec des privilèges élevés pour un non-administrateur</span><span class="sxs-lookup"><span data-stu-id="d4c7b-514">Installing a Package with Elevated Privileges for a Non-Admin</span></span>](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [<span data-ttu-id="d4c7b-515">Application de mises à niveau majeures en appliquant des correctifs à l’installation locale du produit</span><span class="sxs-lookup"><span data-stu-id="d4c7b-515">Applying Major Upgrades by Patching the Local Installation of the Product</span></span>](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md)
    -   [<span data-ttu-id="d4c7b-516">Application de mises à niveau majeures en installant le produit</span><span class="sxs-lookup"><span data-stu-id="d4c7b-516">Applying Major Upgrades by Installing the Product</span></span>](applying-major-upgrades-by-installing-the-product.md)
    -   [<span data-ttu-id="d4c7b-517">Application de petites mises à jour en appliquant des correctifs à l’installation locale du produit</span><span class="sxs-lookup"><span data-stu-id="d4c7b-517">Applying Small Updates by Patching the Local Installation of the Product</span></span>](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
    -   [<span data-ttu-id="d4c7b-518">Application de petites mises à jour en réinstallant le produit</span><span class="sxs-lookup"><span data-stu-id="d4c7b-518">Applying Small Updates by Reinstalling the Product</span></span>](applying-small-updates-by-reinstalling-the-product.md)
    -   [<span data-ttu-id="d4c7b-519">Application de petites mises à jour en corrigeant une image administrative</span><span class="sxs-lookup"><span data-stu-id="d4c7b-519">Applying Small Updates by Patching an Administrative Image</span></span>](applying-small-updates-by-patching-an-administrative-image.md)
    -   [<span data-ttu-id="d4c7b-520">Mise à jour corrective des installations initiales</span><span class="sxs-lookup"><span data-stu-id="d4c7b-520">Patching Initial Installations</span></span>](patching-initial-installations.md)
    -   [<span data-ttu-id="d4c7b-521">Options de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="d4c7b-521">Command Line Options</span></span>](command-line-options.md)

-   <span data-ttu-id="d4c7b-522">Résolvez les problèmes Windows Installer packages.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-522">Troubleshoot Windows Installer packages.</span></span>

    <span data-ttu-id="d4c7b-523">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-523">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-524">Journalisation Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d4c7b-524">Windows Installer Logging</span></span>](windows-installer-logging.md)
    -   [<span data-ttu-id="d4c7b-525">Vérification de l’installation des fonctionnalités, des composants, des fichiers</span><span class="sxs-lookup"><span data-stu-id="d4c7b-525">Checking the Installation of Features, Components, Files</span></span>](checking-the-installation-of-features-components-files.md)
    -   [<span data-ttu-id="d4c7b-526">Wilogutl.exe</span><span class="sxs-lookup"><span data-stu-id="d4c7b-526">Wilogutl.exe</span></span>](wilogutl-exe.md)
    -   [<span data-ttu-id="d4c7b-527">Recherche d’une fonctionnalité ou d’un composant endommagé</span><span class="sxs-lookup"><span data-stu-id="d4c7b-527">Searching for a Broken Feature or Component</span></span>](searching-for-a-broken-feature-or-component.md)
    -   [<span data-ttu-id="d4c7b-528">Windows Installer des messages d’erreur</span><span class="sxs-lookup"><span data-stu-id="d4c7b-528">Windows Installer Error Messages</span></span>](windows-installer-error-messages.md)
    -   [<span data-ttu-id="d4c7b-529">Msicert.exe</span><span class="sxs-lookup"><span data-stu-id="d4c7b-529">Msicert.exe</span></span>](msicert-exe.md)

-   <span data-ttu-id="d4c7b-530">Utilisez les scripts pour interroger des packages Windows Installer pour obtenir des informations sur un produit et modifier l’installation.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-530">Use scripting to query Windows Installer packages for information about a product and modify the installation.</span></span>

    <span data-ttu-id="d4c7b-531">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-531">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-532">Interface d’automatisation</span><span class="sxs-lookup"><span data-stu-id="d4c7b-532">Automation Interface</span></span>](automation-interface.md)
    -   [<span data-ttu-id="d4c7b-533">Exemples de scripts Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d4c7b-533">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
    -   [<span data-ttu-id="d4c7b-534">Utilisation de Windows Installer avec WMI</span><span class="sxs-lookup"><span data-stu-id="d4c7b-534">Using Windows Installer with WMI</span></span>](using-windows-installer-with-wmi.md)

-   <span data-ttu-id="d4c7b-535">Créer et gérer des installations administratives.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-535">Create and maintain administrative installations.</span></span>

    <span data-ttu-id="d4c7b-536">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-536">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-537">Installation administrative</span><span class="sxs-lookup"><span data-stu-id="d4c7b-537">Administrative Installation</span></span>](administrative-installation.md)
    -   [<span data-ttu-id="d4c7b-538">Options de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="d4c7b-538">Command Line Options</span></span>](command-line-options.md)
    -   [<span data-ttu-id="d4c7b-539">**Propriété AdminProperties**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-539">**AdminProperties Property**</span></span>](adminproperties.md)
    -   [<span data-ttu-id="d4c7b-540">Application de petites mises à jour en corrigeant une image administrative</span><span class="sxs-lookup"><span data-stu-id="d4c7b-540">Applying Small Updates by Patching an Administrative Image</span></span>](applying-small-updates-by-patching-an-administrative-image.md)
    -   [<span data-ttu-id="d4c7b-541">Application d’un package de correctifs à une installation d’administration</span><span class="sxs-lookup"><span data-stu-id="d4c7b-541">Applying a Patch Package to an Administrative Installation</span></span>](applying-a-patch-package-to-an-administrative-installation.md)
    -   [<span data-ttu-id="d4c7b-542">Ordre d’exécution des actions</span><span class="sxs-lookup"><span data-stu-id="d4c7b-542">Action Execution Order</span></span>](action-execution-order.md)
    -   [<span data-ttu-id="d4c7b-543">**Propriété IsAdminPackage**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-543">**IsAdminPackage Property**</span></span>](isadminpackage.md)
    -   [<span data-ttu-id="d4c7b-544">Ordre de priorité des propriétés</span><span class="sxs-lookup"><span data-stu-id="d4c7b-544">Order of Property Precedence</span></span>](order-of-property-precedence.md)
    -   [<span data-ttu-id="d4c7b-545">**Propriété AdminProperties**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-545">**AdminProperties Property**</span></span>](adminproperties.md)

-   <span data-ttu-id="d4c7b-546">Rendre une application accessible à tous les utilisateurs d’un ordinateur ou à un utilisateur spécifié uniquement.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-546">Make an application available to all users of a computer or to a specified user only.</span></span>

    <span data-ttu-id="d4c7b-547">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-547">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-548">Contexte d’installation</span><span class="sxs-lookup"><span data-stu-id="d4c7b-548">Installation Context</span></span>](installation-context.md)
    -   [<span data-ttu-id="d4c7b-549">**ALLUSERS, propriété**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-549">**ALLUSERS Property**</span></span>](allusers.md)

-   <span data-ttu-id="d4c7b-550">Interprétez les packages, installez les produits et configurez les options de fonctionnalité à l’aide d’une ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-550">Interpret packages, install products, and configure feature options using a command line.</span></span>

    <span data-ttu-id="d4c7b-551">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-551">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-552">Options de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="d4c7b-552">Command Line Options</span></span>](command-line-options.md)
    -   [<span data-ttu-id="d4c7b-553">Définition des valeurs de propriété publiques sur la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="d4c7b-553">Setting Public Property Values on the Command Line</span></span>](setting-public-property-values-on-the-command-line.md)
    -   [<span data-ttu-id="d4c7b-554">Obtention et définition des propriétés</span><span class="sxs-lookup"><span data-stu-id="d4c7b-554">Getting and Setting Properties</span></span>](getting-and-setting-properties.md)
    -   [<span data-ttu-id="d4c7b-555">Réinstallation d’une fonctionnalité ou d’une application</span><span class="sxs-lookup"><span data-stu-id="d4c7b-555">Reinstalling a Feature or Application</span></span>](reinstalling-a-feature-or-application.md)
    -   [<span data-ttu-id="d4c7b-556">Application de petites mises à jour en appliquant des correctifs à l’installation locale du produit</span><span class="sxs-lookup"><span data-stu-id="d4c7b-556">Applying Small Updates by Patching the Local Installation of the Product</span></span>](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
    -   [<span data-ttu-id="d4c7b-557">Application de petites mises à jour en réinstallant le produit</span><span class="sxs-lookup"><span data-stu-id="d4c7b-557">Applying Small Updates by Reinstalling the Product</span></span>](applying-small-updates-by-reinstalling-the-product.md)
    -   [<span data-ttu-id="d4c7b-558">Modification de l’emplacement cible d’un répertoire</span><span class="sxs-lookup"><span data-stu-id="d4c7b-558">Changing the Target Location for a Directory</span></span>](changing-the-target-location-for-a-directory.md)
    -   [<span data-ttu-id="d4c7b-559">Application de petites mises à jour en corrigeant une image administrative</span><span class="sxs-lookup"><span data-stu-id="d4c7b-559">Applying Small Updates by Patching an Administrative Image</span></span>](applying-small-updates-by-patching-an-administrative-image.md)
    -   [<span data-ttu-id="d4c7b-560">Application de mises à niveau majeures en installant le produit</span><span class="sxs-lookup"><span data-stu-id="d4c7b-560">Applying Major Upgrades by Installing the Product</span></span>](applying-major-upgrades-by-installing-the-product.md)
    -   [<span data-ttu-id="d4c7b-561">Propriétés de configuration</span><span class="sxs-lookup"><span data-stu-id="d4c7b-561">Configuration Properties</span></span>](property-reference.md)
    -   [<span data-ttu-id="d4c7b-562">Propriétés options d’installation de la fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="d4c7b-562">Feature Installation Options Properties</span></span>](property-reference.md)

-   <span data-ttu-id="d4c7b-563">Utilisez la stratégie pour gérer les droits d’accès et les autorisations.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-563">Work with policy to manage access rights and permissions.</span></span>

    <span data-ttu-id="d4c7b-564">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-564">For more information, see the following:</span></span>

    -   <span data-ttu-id="d4c7b-565">[Stratégies d’ordinateur](machine-policies.md),</span><span class="sxs-lookup"><span data-stu-id="d4c7b-565">[Machine Policies](machine-policies.md),</span></span>
    -   <span data-ttu-id="d4c7b-566">[Stratégies d’utilisateur](user-policies.md),</span><span class="sxs-lookup"><span data-stu-id="d4c7b-566">[User Policies](user-policies.md),</span></span>
    -   [<span data-ttu-id="d4c7b-567">Installation d’un package avec des privilèges élevés pour un non-administrateur</span><span class="sxs-lookup"><span data-stu-id="d4c7b-567">Installing a Package with Elevated Privileges for a Non-Admin</span></span>](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [<span data-ttu-id="d4c7b-568">Publication d’une application Per-User à installer avec des privilèges élevés</span><span class="sxs-lookup"><span data-stu-id="d4c7b-568">Advertising a Per-User Application To Be Installed with Elevated Privileges</span></span>](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
    -   [<span data-ttu-id="d4c7b-569">Utilisation d’une action personnalisée pour créer des comptes d’utilisateur sur un ordinateur local</span><span class="sxs-lookup"><span data-stu-id="d4c7b-569">Using a Custom Action to Create User Accounts on a Local Computer</span></span>](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [<span data-ttu-id="d4c7b-570">**Propriété AdminUser**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-570">**AdminUser Property**</span></span>](adminuser.md)
    -   [<span data-ttu-id="d4c7b-571">**Privileged, propriété**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-571">**Privileged Property**</span></span>](privileged.md)
    -   [<span data-ttu-id="d4c7b-572">**Propriété EnableUserControl**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-572">**EnableUserControl Property**</span></span>](enableusercontrol.md)
    -   [<span data-ttu-id="d4c7b-573">**UserSID, propriété**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-573">**UserSID Property**</span></span>](usersid.md)
    -   [<span data-ttu-id="d4c7b-574">**Propriété SecureCustomProperties**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-574">**SecureCustomProperties Property**</span></span>](securecustomproperties.md)

-   <span data-ttu-id="d4c7b-575">Installer plusieurs packages à l’aide du [*traitement des transactions*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d4c7b-575">Install multiple packages using [*transaction processing*](t-gly.md).</span></span>

    <span data-ttu-id="d4c7b-576">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-576">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-577">Installations sur plusieurs packages</span><span class="sxs-lookup"><span data-stu-id="d4c7b-577">Multiple-Package Installations</span></span>](multiple-package-installations.md)

-   <span data-ttu-id="d4c7b-578">Incorporez une interface utilisateur personnalisée dans un package Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-578">Embed a custom user interface within a Windows Installer package..</span></span>

    <span data-ttu-id="d4c7b-579">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-579">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-580">Utilisation de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="d4c7b-580">Using the User Interface</span></span>](using-the-user-interface.md)
    -   [<span data-ttu-id="d4c7b-581">Utilisation d’une interface utilisateur incorporée</span><span class="sxs-lookup"><span data-stu-id="d4c7b-581">Using an Embedded UI</span></span>](using-an-embedded-ui.md)

## <a name="infrastructure-developers"></a><span data-ttu-id="d4c7b-582">Développeurs d’infrastructure</span><span class="sxs-lookup"><span data-stu-id="d4c7b-582">Infrastructure Developers</span></span>

<span data-ttu-id="d4c7b-583">Les développeurs d’infrastructure peuvent créer des plateformes unifiées pour le déploiement et la gestion de logiciels qui utilisent le service Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-583">Infrastructure Developers can create unified platforms for the deployment and management of software that uses the Windows Installer service.</span></span> <span data-ttu-id="d4c7b-584">Ils peuvent utiliser l’interface de programmation Windows Installer pour interroger, gérer et distribuer des applications, des correctifs et des sources sur un système.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-584">They can use the Windows Installer programming interface to query, manage, and distribute applications, patches, and sources on a system.</span></span>

-   <span data-ttu-id="d4c7b-585">Localisez, stockez et interrogez l’État, les informations et les clients des composants.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-585">Locate, inventory and query for the state, information, and clients of components.</span></span>

    <span data-ttu-id="d4c7b-586">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-586">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-587">Fonctions spécifiques au composant</span><span class="sxs-lookup"><span data-stu-id="d4c7b-587">Component-Specific Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="d4c7b-588">Fonctions d’État du système</span><span class="sxs-lookup"><span data-stu-id="d4c7b-588">System Status Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="d4c7b-589">Objet installer</span><span class="sxs-lookup"><span data-stu-id="d4c7b-589">Installer Object</span></span>](installer-object.md)
    -   [<span data-ttu-id="d4c7b-590">Product, objet</span><span class="sxs-lookup"><span data-stu-id="d4c7b-590">Product Object</span></span>](product-object.md)
    -   [<span data-ttu-id="d4c7b-591">Objet patch</span><span class="sxs-lookup"><span data-stu-id="d4c7b-591">Patch Object</span></span>](patch-object.md)

-   <span data-ttu-id="d4c7b-592">Inventorier et interroger pour obtenir des informations et l’état des produits et des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-592">Inventory and query for information and the state of products and features.</span></span>

    <span data-ttu-id="d4c7b-593">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-593">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-594">Inventaire des produits et des correctifs</span><span class="sxs-lookup"><span data-stu-id="d4c7b-594">Inventory products and patches</span></span>](inventory-products-and-patches-.md)
    -   [<span data-ttu-id="d4c7b-595">Fonctions d’État du système</span><span class="sxs-lookup"><span data-stu-id="d4c7b-595">System Status Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="d4c7b-596">Fonctions de requête de produit</span><span class="sxs-lookup"><span data-stu-id="d4c7b-596">Product Query Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="d4c7b-597">Objet installer</span><span class="sxs-lookup"><span data-stu-id="d4c7b-597">Installer Object</span></span>](installer-object.md)
    -   [<span data-ttu-id="d4c7b-598">Product, objet</span><span class="sxs-lookup"><span data-stu-id="d4c7b-598">Product Object</span></span>](product-object.md)
    -   [<span data-ttu-id="d4c7b-599">Objet patch</span><span class="sxs-lookup"><span data-stu-id="d4c7b-599">Patch Object</span></span>](patch-object.md)

-   <span data-ttu-id="d4c7b-600">Améliorez la résilience de la source à l’aide de la Windows Installer pour inventorier, interroger et modifier la liste source des applications, des mises à niveau et des correctifs.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-600">Improve source resiliency by using the Windows Installer to inventory, query, and modify the source list of applications, upgrades, and patches.</span></span>

    <span data-ttu-id="d4c7b-601">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-601">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-602">**SOURCELIST, propriété**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-602">**SOURCELIST Property**</span></span>](sourcelist.md)
    -   [<span data-ttu-id="d4c7b-603">**Résilience source**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-603">**Source Resiliency**</span></span>](source-resiliency.md)
    -   [<span data-ttu-id="d4c7b-604">Fonctions d’installation et de configuration</span><span class="sxs-lookup"><span data-stu-id="d4c7b-604">Installation and Configuration Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="d4c7b-605">Objet installer</span><span class="sxs-lookup"><span data-stu-id="d4c7b-605">Installer Object</span></span>](installer-object.md)
    -   [<span data-ttu-id="d4c7b-606">Product, objet</span><span class="sxs-lookup"><span data-stu-id="d4c7b-606">Product Object</span></span>](product-object.md)
    -   [<span data-ttu-id="d4c7b-607">Objet patch</span><span class="sxs-lookup"><span data-stu-id="d4c7b-607">Patch Object</span></span>](patch-object.md)

-   <span data-ttu-id="d4c7b-608">Améliorez la résilience de la source à l’aide de la Windows Installer pour inventorier, interroger et modifier des sources multimédias.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-608">Improve source resiliency by using the Windows Installer to inventory, query, and modify media sources.</span></span>

    <span data-ttu-id="d4c7b-609">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-609">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-610">**SOURCELIST, propriété**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-610">**SOURCELIST Property**</span></span>](sourcelist.md)
    -   [<span data-ttu-id="d4c7b-611">Résilience source</span><span class="sxs-lookup"><span data-stu-id="d4c7b-611">Source Resiliency</span></span>](source-resiliency.md)
    -   [<span data-ttu-id="d4c7b-612">Fonctions d’installation et de configuration</span><span class="sxs-lookup"><span data-stu-id="d4c7b-612">Installation and Configuration Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="d4c7b-613">Product, objet</span><span class="sxs-lookup"><span data-stu-id="d4c7b-613">Product Object</span></span>](product-object.md)
    -   [<span data-ttu-id="d4c7b-614">Objet patch</span><span class="sxs-lookup"><span data-stu-id="d4c7b-614">Patch Object</span></span>](patch-object.md)

-   <span data-ttu-id="d4c7b-615">Inventaire et requête pour obtenir des informations et l’état des correctifs.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-615">Inventory and query for information and the state of patches.</span></span>

    <span data-ttu-id="d4c7b-616">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-616">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-617">Inventaire des produits et des correctifs</span><span class="sxs-lookup"><span data-stu-id="d4c7b-617">Inventory products and patches</span></span>](inventory-products-and-patches-.md)
    -   [<span data-ttu-id="d4c7b-618">Référence des fonctions du programme d’installation</span><span class="sxs-lookup"><span data-stu-id="d4c7b-618">Installer Function Reference</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="d4c7b-619">Objet patch</span><span class="sxs-lookup"><span data-stu-id="d4c7b-619">Patch Object</span></span>](patch-object.md)

-   <span data-ttu-id="d4c7b-620">Utilisez la stratégie pour gérer les droits d’accès et les autorisations.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-620">Work with policy to manage access rights and permissions.</span></span>

    <span data-ttu-id="d4c7b-621">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c7b-621">For more information, see the following:</span></span>

    -   [<span data-ttu-id="d4c7b-622">Stratégies d’ordinateur</span><span class="sxs-lookup"><span data-stu-id="d4c7b-622">Machine Policies</span></span>](machine-policies.md)
    -   [<span data-ttu-id="d4c7b-623">Stratégies utilisateur</span><span class="sxs-lookup"><span data-stu-id="d4c7b-623">User Policies</span></span>](user-policies.md)
    -   [<span data-ttu-id="d4c7b-624">Installation d’un package avec des privilèges élevés pour un non-administrateur</span><span class="sxs-lookup"><span data-stu-id="d4c7b-624">Installing a Package with Elevated Privileges for a Non-Admin</span></span>](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [<span data-ttu-id="d4c7b-625">Publication d’une application Per-User à installer avec des privilèges élevés</span><span class="sxs-lookup"><span data-stu-id="d4c7b-625">Advertising a Per-User Application To Be Installed with Elevated Privileges</span></span>](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
    -   [<span data-ttu-id="d4c7b-626">Utilisation d’une action personnalisée pour créer des comptes d’utilisateur sur un ordinateur local</span><span class="sxs-lookup"><span data-stu-id="d4c7b-626">Using a Custom Action to Create User Accounts on a Local Computer</span></span>](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [<span data-ttu-id="d4c7b-627">**Propriété AdminUser**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-627">**AdminUser Property**</span></span>](adminuser.md)
    -   [<span data-ttu-id="d4c7b-628">**Privileged, propriété**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-628">**Privileged Property**</span></span>](privileged.md)
    -   [<span data-ttu-id="d4c7b-629">**Propriété EnableUserControl**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-629">**EnableUserControl Property**</span></span>](enableusercontrol.md)
    -   [<span data-ttu-id="d4c7b-630">**UserSID, propriété**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-630">**UserSID Property**</span></span>](usersid.md)
    -   [<span data-ttu-id="d4c7b-631">**Propriété SecureCustomProperties**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-631">**SecureCustomProperties Property**</span></span>](securecustomproperties.md)

 

 



