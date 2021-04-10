---
description: Le programme d’installation conserve les informations sur la structure du répertoire d’installation dans la table du répertoire.
ms.assetid: 31390138-b1d0-4f0b-9304-6e7c69e6a736
title: Spécification de la structure de répertoires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a87880921799158559e28fed2c6dde97c9a331
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862909"
---
# <a name="specifying-directory-structure"></a><span data-ttu-id="17907-103">Spécification de la structure de répertoires</span><span class="sxs-lookup"><span data-stu-id="17907-103">Specifying Directory Structure</span></span>

<span data-ttu-id="17907-104">Le programme d’installation conserve les informations sur la structure du répertoire d’installation dans la [table du répertoire](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="17907-104">The installer keeps information about the installation directory structure in the [Directory Table](directory-table.md).</span></span> <span data-ttu-id="17907-105">Consultez le [groupe tables principales](core-tables-group.md).</span><span class="sxs-lookup"><span data-stu-id="17907-105">See the [Core Tables Group](core-tables-group.md).</span></span> <span data-ttu-id="17907-106">Dans cette section, vous allez ajouter des informations sur la structure de répertoires de l’exemple Notepad à la base de données vide que vous avez créée lors de l' [importation d’une base de données vide](importing-a-blank-database.md).</span><span class="sxs-lookup"><span data-stu-id="17907-106">In this section you add directory structure information for the Notepad sample to the empty database you created in [Importing a Blank Database](importing-a-blank-database.md).</span></span> <span data-ttu-id="17907-107">Utilisez l’éditeur de base de données Orca fourni avec le kit de développement logiciel (SDK), ou un autre éditeur, pour ouvrir la table de répertoires dans MNP2000.msi.</span><span class="sxs-lookup"><span data-stu-id="17907-107">Use the database editor Orca that is provided with the SDK, or another editor, to open the Directory Table in MNP2000.msi.</span></span> <span data-ttu-id="17907-108">Utilisez l’éditeur pour entrer les données suivantes dans la table de répertoires vide.</span><span class="sxs-lookup"><span data-stu-id="17907-108">Use the editor to enter the following data into the blank Directory table.</span></span>

[<span data-ttu-id="17907-109">Table de répertoire</span><span class="sxs-lookup"><span data-stu-id="17907-109">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="17907-110">Répertoire</span><span class="sxs-lookup"><span data-stu-id="17907-110">Directory</span></span>                                        | <span data-ttu-id="17907-111">Répertoire \_ parent</span><span class="sxs-lookup"><span data-stu-id="17907-111">Directory\_Parent</span></span>                                | <span data-ttu-id="17907-112">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="17907-112">DefaultDir</span></span>        |
|--------------------------------------------------|--------------------------------------------------|-------------------|
| [<span data-ttu-id="17907-113">**TARGETDIR**</span><span class="sxs-lookup"><span data-stu-id="17907-113">**TARGETDIR**</span></span>](targetdir.md)                   |                                                  | <span data-ttu-id="17907-114">SourceDir</span><span class="sxs-lookup"><span data-stu-id="17907-114">SourceDir</span></span>         |
| [<span data-ttu-id="17907-115">**ProgramFilesFolder**</span><span class="sxs-lookup"><span data-stu-id="17907-115">**ProgramFilesFolder**</span></span>](programfilesfolder.md) | [<span data-ttu-id="17907-116">**TARGETDIR**</span><span class="sxs-lookup"><span data-stu-id="17907-116">**TARGETDIR**</span></span>](targetdir.md)                   | <span data-ttu-id="17907-117">.</span><span class="sxs-lookup"><span data-stu-id="17907-117">.</span></span>                 |
| <span data-ttu-id="17907-118">ARTSDIR</span><span class="sxs-lookup"><span data-stu-id="17907-118">ARTSDIR</span></span>                                          | <span data-ttu-id="17907-119">NOTEPADDIR</span><span class="sxs-lookup"><span data-stu-id="17907-119">NOTEPADDIR</span></span>                                       | <span data-ttu-id="17907-120">Arts : événements</span><span class="sxs-lookup"><span data-stu-id="17907-120">Arts:Events</span></span>       |
| <span data-ttu-id="17907-121">HOLDIR</span><span class="sxs-lookup"><span data-stu-id="17907-121">HOLDIR</span></span>                                           | <span data-ttu-id="17907-122">MONDIR</span><span class="sxs-lookup"><span data-stu-id="17907-122">MONDIR</span></span>                                           | <span data-ttu-id="17907-123">. : Jours fériés</span><span class="sxs-lookup"><span data-stu-id="17907-123">.:Holidays</span></span>        |
| <span data-ttu-id="17907-124">MENUDIR</span><span class="sxs-lookup"><span data-stu-id="17907-124">MENUDIR</span></span>                                          | <span data-ttu-id="17907-125">NOTEPADDIR</span><span class="sxs-lookup"><span data-stu-id="17907-125">NOTEPADDIR</span></span>                                       | <span data-ttu-id="17907-126">Menu</span><span class="sxs-lookup"><span data-stu-id="17907-126">Menu</span></span>              |
| <span data-ttu-id="17907-127">MONDIR</span><span class="sxs-lookup"><span data-stu-id="17907-127">MONDIR</span></span>                                           | <span data-ttu-id="17907-128">NOTEPADDIR</span><span class="sxs-lookup"><span data-stu-id="17907-128">NOTEPADDIR</span></span>                                       | <span data-ttu-id="17907-129">Transistor</span><span class="sxs-lookup"><span data-stu-id="17907-129">Gate</span></span>              |
| <span data-ttu-id="17907-130">NOTEPADDIR</span><span class="sxs-lookup"><span data-stu-id="17907-130">NOTEPADDIR</span></span>                                       | [<span data-ttu-id="17907-131">**ProgramFilesFolder**</span><span class="sxs-lookup"><span data-stu-id="17907-131">**ProgramFilesFolder**</span></span>](programfilesfolder.md) | <span data-ttu-id="17907-132">\_Parc rouge : bloc-notes</span><span class="sxs-lookup"><span data-stu-id="17907-132">Red\_Park:Notepad</span></span> |
| <span data-ttu-id="17907-133">SPORTDIR</span><span class="sxs-lookup"><span data-stu-id="17907-133">SPORTDIR</span></span>                                         | <span data-ttu-id="17907-134">NOTEPADDIR</span><span class="sxs-lookup"><span data-stu-id="17907-134">NOTEPADDIR</span></span>                                       | <span data-ttu-id="17907-135">Sports : événements</span><span class="sxs-lookup"><span data-stu-id="17907-135">Sports:Events</span></span>     |



 

<span data-ttu-id="17907-136">L’entrée de ces données dans la table Directory spécifie les structures de répertoire source et cible.</span><span class="sxs-lookup"><span data-stu-id="17907-136">Entering this data into the Directory table specifies the source and target directory structures.</span></span> <span data-ttu-id="17907-137">Consultez la [table Directory](directory-table.md) et [Utilisez les rubriques de la table Directory](using-the-directory-table.md) .</span><span class="sxs-lookup"><span data-stu-id="17907-137">See the [Directory Table](directory-table.md) and [Using the Directory Table](using-the-directory-table.md) topics.</span></span> <span data-ttu-id="17907-138">Notez que la propriété [**targetDir**](targetdir.md) doit être le nom d’une racine dans la table des répertoires de chaque installation.</span><span class="sxs-lookup"><span data-stu-id="17907-138">Note that the [**TARGETDIR**](targetdir.md) property must be the name of one root in the Directory table of every installation.</span></span>

[<span data-ttu-id="17907-139">Continuer</span><span class="sxs-lookup"><span data-stu-id="17907-139">Continue</span></span>](specifying-components.md)

 

 



