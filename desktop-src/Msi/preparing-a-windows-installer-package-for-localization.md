---
description: Respectez ces recommandations pour faciliter la localisation des packages Windows Installer.
ms.assetid: f00b44b4-e8ec-46d2-b329-00728a83275b
title: Préparation d’un package de Windows Installer pour la localisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa46af5259b880398aa84dc817eb201bd63456eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515962"
---
# <a name="preparing-a-windows-installer-package-for-localization"></a><span data-ttu-id="758a1-103">Préparation d’un package de Windows Installer pour la localisation</span><span class="sxs-lookup"><span data-stu-id="758a1-103">Preparing a Windows Installer Package for Localization</span></span>

<span data-ttu-id="758a1-104">La localisation d’un package Windows Installer dans plusieurs langues peut être simplifiée en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="758a1-104">Localization of a Windows Installer package into multiple languages can be greatly facilitated by doing the following:</span></span>

-   <span data-ttu-id="758a1-105">Créer une base de données d’installation de base qui est indépendante de la page de codes.</span><span class="sxs-lookup"><span data-stu-id="758a1-105">Author a base installation database that is code page neutral.</span></span> <span data-ttu-id="758a1-106">Consultez [création d’une base de données à l’aide d’une page de codes neutre](creating-a-database-with-a-neutral-code-page.md).</span><span class="sxs-lookup"><span data-stu-id="758a1-106">See [Creating a database with a neutral code page](creating-a-database-with-a-neutral-code-page.md).</span></span> <span data-ttu-id="758a1-107">La page de codes de la base de données localisée peut ensuite être définie par l’importation d’une table d’archive de texte avec une page de codes non neutre dans la base de données de base.</span><span class="sxs-lookup"><span data-stu-id="758a1-107">The code page of the localized database can then be set by importing a text archive table with a non-neutral code page into the base database.</span></span> <span data-ttu-id="758a1-108">Consultez [définition de la page de codes d’une base de données](setting-the-code-page-of-a-database.md).</span><span class="sxs-lookup"><span data-stu-id="758a1-108">See [Setting the code page of a database](setting-the-code-page-of-a-database.md).</span></span>
-   <span data-ttu-id="758a1-109">Organisez les fichiers nécessitant une localisation dans des composants distincts et installez ces fichiers dans des répertoires distincts.</span><span class="sxs-lookup"><span data-stu-id="758a1-109">Organize files requiring localization into separate components and install these files into separate directories.</span></span> <span data-ttu-id="758a1-110">Cela permet de s’assurer que deux packages localisés n’installent jamais des fichiers portant le même nom dans le même répertoire.</span><span class="sxs-lookup"><span data-stu-id="758a1-110">This ensures that two localized packages never install identically named files into the same directory.</span></span>

<span data-ttu-id="758a1-111">Par exemple, une application dans le monde entier utilisant les ressources suivantes peut avoir trois composants.</span><span class="sxs-lookup"><span data-stu-id="758a1-111">For example, a worldwide application using the following resources may have three components.</span></span>



| <span data-ttu-id="758a1-112">Composant</span><span class="sxs-lookup"><span data-stu-id="758a1-112">Component</span></span> | <span data-ttu-id="758a1-113">Ressource</span><span class="sxs-lookup"><span data-stu-id="758a1-113">Resource</span></span>                   |
|-----------|----------------------------|
| <span data-ttu-id="758a1-114">RÉELLES</span><span class="sxs-lookup"><span data-stu-id="758a1-114">WORLD</span></span>     | <span data-ttu-id="758a1-115">worldwide.exe</span><span class="sxs-lookup"><span data-stu-id="758a1-115">worldwide.exe</span></span>              |
| <span data-ttu-id="758a1-116">RÉELLES</span><span class="sxs-lookup"><span data-stu-id="758a1-116">WORLD</span></span>     | <span data-ttu-id="758a1-117">entrées de Registre mondiales</span><span class="sxs-lookup"><span data-stu-id="758a1-117">worldwide registry entries</span></span> |
| <span data-ttu-id="758a1-118">RÉELLES</span><span class="sxs-lookup"><span data-stu-id="758a1-118">WORLD</span></span>     | <span data-ttu-id="758a1-119">raccourci dans le monde entier</span><span class="sxs-lookup"><span data-stu-id="758a1-119">worldwide shortcut</span></span>         |
| <span data-ttu-id="758a1-120">FR</span><span class="sxs-lookup"><span data-stu-id="758a1-120">ENG</span></span>       | <span data-ttu-id="758a1-121">engui.dll</span><span class="sxs-lookup"><span data-stu-id="758a1-121">engui.dll</span></span>                  |
| <span data-ttu-id="758a1-122">FR</span><span class="sxs-lookup"><span data-stu-id="758a1-122">ENG</span></span>       | <span data-ttu-id="758a1-123">readme.txt</span><span class="sxs-lookup"><span data-stu-id="758a1-123">readme.txt</span></span>                 |
| <span data-ttu-id="758a1-124">FRA</span><span class="sxs-lookup"><span data-stu-id="758a1-124">FRA</span></span>       | <span data-ttu-id="758a1-125">fraui.dll</span><span class="sxs-lookup"><span data-stu-id="758a1-125">fraui.dll</span></span>                  |
| <span data-ttu-id="758a1-126">FRA</span><span class="sxs-lookup"><span data-stu-id="758a1-126">FRA</span></span>       | <span data-ttu-id="758a1-127">readme.txt</span><span class="sxs-lookup"><span data-stu-id="758a1-127">readme.txt</span></span>                 |



 

<span data-ttu-id="758a1-128">Les fichiers qui doivent être localisés peuvent être installés dans les emplacements de répertoire suivants :</span><span class="sxs-lookup"><span data-stu-id="758a1-128">The files that need to be localized may be installed into the following directory locations:</span></span>

-   <span data-ttu-id="758a1-129">\[\] \\worldwide.exe du monde de ProgramFilesFolder \\</span><span class="sxs-lookup"><span data-stu-id="758a1-129">\[ProgramFilesFolder\]\\World\\worldwide.exe</span></span>
-   <span data-ttu-id="758a1-130">\[engui.dll de l’anglais du monde de l' \] \\ \\ anglais \\</span><span class="sxs-lookup"><span data-stu-id="758a1-130">\[ProgramFilesFolder\]\\World\\English\\engui.dll</span></span>
-   <span data-ttu-id="758a1-131">\[readme.txt de l’anglais du monde de l' \] \\ \\ anglais \\</span><span class="sxs-lookup"><span data-stu-id="758a1-131">\[ProgramFilesFolder\]\\World\\English\\readme.txt</span></span>
-   <span data-ttu-id="758a1-132">\[fraui.dll de la \] \\ planète universelle de l' \\ anglais \\</span><span class="sxs-lookup"><span data-stu-id="758a1-132">\[ProgramFilesFolder\]\\World\\French\\fraui.dll</span></span>
-   <span data-ttu-id="758a1-133">\[readme.txt de la \] \\ planète universelle de l' \\ anglais \\</span><span class="sxs-lookup"><span data-stu-id="758a1-133">\[ProgramFilesFolder\]\\World\\French\\readme.txt</span></span>

 

 



