---
description: Les sections suivantes présentent un exemple de création d’un package de mise à niveau pour l’application décrite dans un exemple d’installation.
ms.assetid: 233302ea-abc3-4879-b868-425f2b10e02e
title: Exemple de mise à niveau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d1e19173a98f3ddee49c19d0ec10aca7994e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527855"
---
# <a name="an-upgrade-example"></a><span data-ttu-id="72e40-103">Exemple de mise à niveau</span><span class="sxs-lookup"><span data-stu-id="72e40-103">An Upgrade Example</span></span>

<span data-ttu-id="72e40-104">Les sections suivantes présentent un exemple de création d’un package de mise à niveau pour l’application décrite dans [un exemple d’installation](an-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="72e40-104">The following sections present an example of authoring an upgrade package for the application described in [An Installation Example](an-installation-example.md).</span></span> <span data-ttu-id="72e40-105">Un exemple d’interface utilisateur minimale pour cet exemple est fourni dans les [composants SDK Windows pour Windows Installer les développeurs](platform-sdk-components-for-windows-installer-developers.md) comme Uisample.msi de fichier.</span><span class="sxs-lookup"><span data-stu-id="72e40-105">An example of a minimal user interface for this sample is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md) as the file Uisample.msi.</span></span> <span data-ttu-id="72e40-106">Si vous avez le kit de développement logiciel (SDK), vous avez accès à tous les outils et données nécessaires pour reproduire l’exemple de package d’installation, l’interface utilisateur et le package de mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="72e40-106">If you have the SDK, you have access to all the tools and data necessary to reproduce the sample installation package, user interface, and sample upgrade package.</span></span>

<span data-ttu-id="72e40-107">Cet exemple montre comment créer un package Windows Installer qui met à niveau le produit hypothétique MNP2000 vers un nouveau produit appelé MNP2001.</span><span class="sxs-lookup"><span data-stu-id="72e40-107">This example illustrates how to create a Windows Installer package that upgrades the hypothetical product MNP2000 to a new product called MNP2001.</span></span> <span data-ttu-id="72e40-108">L’exemple de package de mise à niveau applique une mise à niveau majeure au produit qui nécessite la modification du code du produit.</span><span class="sxs-lookup"><span data-stu-id="72e40-108">The example upgrade package applies a major upgrade to the product which requires changing the product code.</span></span> <span data-ttu-id="72e40-109">Pour plus d’informations sur les mises à niveau majeures, consultez la rubrique sur les [principales mises à](major-upgrades.md) niveau dans la section [correctifs et mises à niveau](patching-and-upgrades.md) .</span><span class="sxs-lookup"><span data-stu-id="72e40-109">For more information about major upgrades, see the topic on [Major Upgrades](major-upgrades.md) in the [Patching and Upgrades](patching-and-upgrades.md) section.</span></span>

<span data-ttu-id="72e40-110">L’exemple de package de mise à niveau présente les spécifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="72e40-110">The sample upgrade package has the following specifications:</span></span>

-   <span data-ttu-id="72e40-111">Pour bénéficier de cette mise à niveau vers MNP2001, un utilisateur doit avoir préalablement installé les versions 1,0 à 1,4 (inclusive) de la langue anglaise MNP2000 à l’aide de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="72e40-111">To qualify to receive this upgrade to MNP2001, a user must have previously installed the 1.0 to 1.4 (inclusive) versions of English language MNP2000 using Windows Installer.</span></span>
-   <span data-ttu-id="72e40-112">Lorsqu’un utilisateur tente d’installer le package de mise à niveau, la fonctionnalité de mise à niveau de Windows Installer recherche sur l’ordinateur de l’utilisateur tous les produits qui sont éligibles à la mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="72e40-112">When a user attempts to install the upgrade package, the upgrade functionality of Windows Installer searches the user's computer for any products that qualify for the upgrade.</span></span>
-   <span data-ttu-id="72e40-113">Windows Installer migre tous les paramètres de fonctionnalité du produit d’origine vers le produit mis à niveau.</span><span class="sxs-lookup"><span data-stu-id="72e40-113">Windows Installer migrates all the of the original product's feature settings to the upgraded product.</span></span>
-   <span data-ttu-id="72e40-114">Le programme d’installation supprime toutes les fonctionnalités obsolètes de l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="72e40-114">The installer removes all obsolete features from the user's computer.</span></span>
-   <span data-ttu-id="72e40-115">Le programme d’installation installe toutes les nouvelles fonctionnalités appartenant à la mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="72e40-115">The installer installs all new features belonging to the upgrade.</span></span>
-   <span data-ttu-id="72e40-116">Une désinstallation du package de mise à niveau supprime le produit de l’ordinateur de l’utilisateur et ne restaure pas la version antérieure du produit.</span><span class="sxs-lookup"><span data-stu-id="72e40-116">An uninstall of the upgrade package removes the product from the user's computer, and does not restore the earlier version of the product.</span></span>
-   <span data-ttu-id="72e40-117">L’exemple de mise à niveau met à jour les raccourcis vers les nouveaux fichiers et fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="72e40-117">The sample upgrade updates shortcuts to new files and features.</span></span>

    [<span data-ttu-id="72e40-118">Planification d’une mise à niveau majeure</span><span class="sxs-lookup"><span data-stu-id="72e40-118">Planning a Major Upgrade</span></span>](planning-a-major-upgrade.md)

    [<span data-ttu-id="72e40-119">Importation de la base de données d’installation d’origine</span><span class="sxs-lookup"><span data-stu-id="72e40-119">Importing Original Installation Database</span></span>](importing-original-installation-database.md)

    [<span data-ttu-id="72e40-120">Mise à jour de la structure de répertoires pour une mise à niveau</span><span class="sxs-lookup"><span data-stu-id="72e40-120">Updating Directory Structure for an Upgrade</span></span>](updating-directory-structure-for-an-upgrade.md)

    [<span data-ttu-id="72e40-121">Mise à jour des fichiers et des attributs de fichier pour une mise à niveau</span><span class="sxs-lookup"><span data-stu-id="72e40-121">Updating Files and File Attributes for an Upgrade</span></span>](updating-files-and-file-attributes-for-an-upgrade.md)

    [<span data-ttu-id="72e40-122">Mise à jour des composants d’une mise à niveau</span><span class="sxs-lookup"><span data-stu-id="72e40-122">Updating Components for an Upgrade</span></span>](updating-components-for-an-upgrade.md)

    [<span data-ttu-id="72e40-123">Mise à jour des fonctionnalités pour une mise à niveau</span><span class="sxs-lookup"><span data-stu-id="72e40-123">Updating Features for an Upgrade</span></span>](updating-features-for-an-upgrade.md)

    [<span data-ttu-id="72e40-124">Mise à jour des raccourcis pour une mise à niveau</span><span class="sxs-lookup"><span data-stu-id="72e40-124">Updating Shortcuts for an Upgrade</span></span>](updating-shortcuts-for-an-upgrade.md)

    [<span data-ttu-id="72e40-125">Mise à jour de la table de mise à niveau pour une mise à niveau</span><span class="sxs-lookup"><span data-stu-id="72e40-125">Updating Upgrade Table for an Upgrade</span></span>](updating-upgrade-table-for-an-upgrade.md)

    [<span data-ttu-id="72e40-126">Mise à jour des propriétés d’une mise à niveau</span><span class="sxs-lookup"><span data-stu-id="72e40-126">Updating Properties for an Upgrade</span></span>](updating-properties-for-an-upgrade.md)

    [<span data-ttu-id="72e40-127">Mise à jour des tables de séquences pour une mise à niveau</span><span class="sxs-lookup"><span data-stu-id="72e40-127">Updating Sequence Tables for an Upgrade</span></span>](updating-sequence-tables-for-an-upgrade.md)

    [<span data-ttu-id="72e40-128">Mise à jour des informations récapitulatives pour une mise à niveau</span><span class="sxs-lookup"><span data-stu-id="72e40-128">Updating Summary Information for an Upgrade</span></span>](updating-summary-information-for-an-upgrade.md)

    [<span data-ttu-id="72e40-129">Validation de la mise à niveau d’une installation</span><span class="sxs-lookup"><span data-stu-id="72e40-129">Validating an Installation Upgrade</span></span>](validating-an-installation-upgrade.md)

 

 



