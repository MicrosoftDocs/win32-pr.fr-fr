---
description: Cet exemple montre comment créer un package Windows Installer simple qui installe une application.
ms.assetid: eee1e3e6-74e9-41d0-b732-1f792a4df423
title: Exemple d’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11eefaab2977bf7cc31e86ac7541b21b345c1aa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864493"
---
# <a name="an-installation-example"></a><span data-ttu-id="1cf06-103">Exemple d’installation</span><span class="sxs-lookup"><span data-stu-id="1cf06-103">An Installation Example</span></span>

<span data-ttu-id="1cf06-104">Cet exemple montre comment créer un package Windows Installer simple qui installe une application.</span><span class="sxs-lookup"><span data-stu-id="1cf06-104">This example illustrates how to create a simple Windows Installer package that installs an application.</span></span> <span data-ttu-id="1cf06-105">L’exemple installe le bloc-notes, un éditeur de texte inclus avec Windows et plusieurs fichiers texte qui décrivent les événements et les admissions à l’aide du parc rouge imaginaire.</span><span class="sxs-lookup"><span data-stu-id="1cf06-105">The sample installs Notepad, a text editor included with Windows, and several text files describing events and admissions at the imaginary Red Park Arena.</span></span>

<span data-ttu-id="1cf06-106">L’exemple présente les spécifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="1cf06-106">The sample has the following specifications:</span></span>

-   <span data-ttu-id="1cf06-107">L’application est fournie aux utilisateurs sous la forme d’un package de Windows Installer qui installe automatiquement tous les fichiers, raccourcis et informations de registre requis.</span><span class="sxs-lookup"><span data-stu-id="1cf06-107">The application is provided to users as a self-installing Windows Installer package that installs all the required files, shortcuts, and registry information.</span></span>
-   <span data-ttu-id="1cf06-108">Le package d’installation peut présenter à l’utilisateur un assistant d’interface utilisateur lors de l’installation afin de collecter les informations de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1cf06-108">The installation package may present a UI wizard to the user during setup to collect user information.</span></span>
-   <span data-ttu-id="1cf06-109">Pendant l’installation, les utilisateurs ont la possibilité de sélectionner des fonctionnalités individuelles à installer pour s’exécuter-localement, d’exécuter à partir de la source ou de ne pas être installées.</span><span class="sxs-lookup"><span data-stu-id="1cf06-109">During setup, users have the option of selecting individual features to be installed to run-locally, to run-from-source, or to not be installed.</span></span>
-   <span data-ttu-id="1cf06-110">L’une des fonctionnalités peut être présentée aux utilisateurs sous la forme d’une fonctionnalité d’installation à la demande.</span><span class="sxs-lookup"><span data-stu-id="1cf06-110">One of the features can be presented to users as an install-on-demand feature.</span></span>
-   <span data-ttu-id="1cf06-111">Le même package désinstalle l’application et supprime tous les fichiers d’application et les informations de registre de l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1cf06-111">The same package uninstalls the application and removes all the application files and registry information from the user's computer.</span></span>
-   <span data-ttu-id="1cf06-112">Le package est prêt à recevoir une mise à niveau majeure qui comprend la modification de son code de produit.</span><span class="sxs-lookup"><span data-stu-id="1cf06-112">The package is prepared to receive a major upgrade that includes changing its product code.</span></span>

<span data-ttu-id="1cf06-113">Pour reproduire l’exemple, vous avez besoin d’un outil logiciel apte à créer et à modifier une base de données Windows Installer vide.</span><span class="sxs-lookup"><span data-stu-id="1cf06-113">To reproduce the example, you need a software tool capable of creating and editing a blank Windows Installer database.</span></span> <span data-ttu-id="1cf06-114">Plusieurs outils de création de packages sont disponibles auprès des éditeurs de logiciels indépendants.</span><span class="sxs-lookup"><span data-stu-id="1cf06-114">Several package creation tools are available from independent software vendors.</span></span> <span data-ttu-id="1cf06-115">Un éditeur de base de données Windows Installer appelé Orca est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="1cf06-115">A Windows Installer database editor called Orca is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="1cf06-116">Pour compléter l’exemple, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="1cf06-116">To complete the example, follow these steps:</span></span>

[<span data-ttu-id="1cf06-117">Planification de l’installation</span><span class="sxs-lookup"><span data-stu-id="1cf06-117">Planning the Installation</span></span>](planning-the-installation.md)

[<span data-ttu-id="1cf06-118">Importation d’une base de données vide</span><span class="sxs-lookup"><span data-stu-id="1cf06-118">Importing a Blank Database</span></span>](importing-a-blank-database.md)

[<span data-ttu-id="1cf06-119">Spécification de la structure de répertoires</span><span class="sxs-lookup"><span data-stu-id="1cf06-119">Specifying Directory Structure</span></span>](specifying-directory-structure.md)

[<span data-ttu-id="1cf06-120">Spécification des composants</span><span class="sxs-lookup"><span data-stu-id="1cf06-120">Specifying Components</span></span>](specifying-components.md)

[<span data-ttu-id="1cf06-121">Spécification des fichiers et des attributs de fichier</span><span class="sxs-lookup"><span data-stu-id="1cf06-121">Specifying Files and File Attributes</span></span>](specifying-files-and-file-attributes.md)

[<span data-ttu-id="1cf06-122">Spécification du média source</span><span class="sxs-lookup"><span data-stu-id="1cf06-122">Specifying Source Media</span></span>](specifying-source-media.md)

[<span data-ttu-id="1cf06-123">Spécification des fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="1cf06-123">Specifying Features</span></span>](specifying-features.md)

[<span data-ttu-id="1cf06-124">Spécification des relations Feature-Component</span><span class="sxs-lookup"><span data-stu-id="1cf06-124">Specifying Feature-Component Relationships</span></span>](specifying-feature-component-relationships.md)

[<span data-ttu-id="1cf06-125">Ajout d’informations de Registre</span><span class="sxs-lookup"><span data-stu-id="1cf06-125">Adding Registry Information</span></span>](adding-registry-information.md)

[<span data-ttu-id="1cf06-126">Spécification de raccourcis</span><span class="sxs-lookup"><span data-stu-id="1cf06-126">Specifying Shortcuts</span></span>](specifying-shortcuts.md)

[<span data-ttu-id="1cf06-127">Spécification des propriétés</span><span class="sxs-lookup"><span data-stu-id="1cf06-127">Specifying Properties</span></span>](specifying-properties.md)

[<span data-ttu-id="1cf06-128">Importation du InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="1cf06-128">Importing the InstallExecuteSequence</span></span>](importing-the-installexecutesequence.md)

[<span data-ttu-id="1cf06-129">Importation du InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="1cf06-129">Importing the InstallUISequence</span></span>](importing-the-installuisequence.md)

[<span data-ttu-id="1cf06-130">Importation du AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="1cf06-130">Importing the AdminExecuteSequence</span></span>](importing-the-adminexecutesequence.md)

[<span data-ttu-id="1cf06-131">Importation du AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="1cf06-131">Importing the AdminUISequence</span></span>](importing-the-adminuisequence.md)

[<span data-ttu-id="1cf06-132">Importation du AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="1cf06-132">Importing the AdvtExecuteSequence</span></span>](importing-the-advtexecutesequence.md)

[<span data-ttu-id="1cf06-133">Ajout d’informations de résumé</span><span class="sxs-lookup"><span data-stu-id="1cf06-133">Adding Summary Information</span></span>](adding-summary-information.md)

[<span data-ttu-id="1cf06-134">Importation de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="1cf06-134">Importing the User Interface</span></span>](importing-the-user-interface.md)

[<span data-ttu-id="1cf06-135">Validation d’une base de données d’installation</span><span class="sxs-lookup"><span data-stu-id="1cf06-135">Validating an Installation Database</span></span>](validating-an-installation-database.md)

 

 



