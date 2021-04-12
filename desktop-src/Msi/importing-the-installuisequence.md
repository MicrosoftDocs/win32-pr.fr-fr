---
description: La séquence de l’interface utilisateur est importée dans l’exemple de base de données.
ms.assetid: 750e4dc6-91ff-4d9a-a968-abc2515e3b7c
title: Importation du InstallUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f20de59a752da6d24a5f3e7fed94e00aa4f0048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203775"
---
# <a name="importing-the-installuisequence"></a><span data-ttu-id="29fde-103">Importation du InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="29fde-103">Importing the InstallUISequence</span></span>

<span data-ttu-id="29fde-104">La [table InstallUISequence](installuisequence-table.md) répertorie les actions qui sont exécutées lorsque l' [action d’installation](install-action.md) de niveau supérieur est exécutée et que le niveau d’interface utilisateur interne est défini sur interface utilisateur complète ou réduite.</span><span class="sxs-lookup"><span data-stu-id="29fde-104">The [InstallUISequence table](installuisequence-table.md) lists actions that are executed when the top-level [INSTALL action](install-action.md) is executed and the internal user interface level is set to full UI or reduced UI.</span></span> <span data-ttu-id="29fde-105">Le programme d’installation ignore les actions dans ce tableau si le niveau de l’interface utilisateur est défini sur interface utilisateur de base ou sur aucune interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="29fde-105">The installer skips the actions in this table if the user interface level is set to basic UI or to no UI.</span></span> <span data-ttu-id="29fde-106">Consultez l' [interface utilisateur](user-interface.md) et les [niveaux d’interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="29fde-106">See [User Interface](user-interface.md) and [User Interface Levels](user-interface-levels.md).</span></span> <span data-ttu-id="29fde-107">Consultez le [groupe tables de procédures d’installation](installation-procedure-tables-group.md), [à l’aide d’une table de séquences](using-a-sequence-table.md)et de l' [exemple de table de séquence détaillé](sequence-table-detailed-example.md).</span><span class="sxs-lookup"><span data-stu-id="29fde-107">See [Installation Procedure Tables Group](installation-procedure-tables-group.md), [Using a Sequence Table](using-a-sequence-table.md), and the [Sequence Table Detailed Example](sequence-table-detailed-example.md).</span></span>

<span data-ttu-id="29fde-108">Si, dans la section, vous avez [importé une base de données vide](importing-a-blank-database.md) que vous avez utilisée uisample.msi du kit de développement logiciel (SDK) Windows Installer, les tables de séquence de votre copie de MNP2000.msi contiennent déjà les séquences d’action suggérées décrites dans [utilisation d’une table de séquences](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="29fde-108">If in the section [Importing a Blank Database](importing-a-blank-database.md) you used uisample.msi from the Windows Installer SDK, the sequence tables in your copy of MNP2000.msi already contains the suggested action sequences described in [Using a Sequence Table](using-a-sequence-table.md).</span></span> <span data-ttu-id="29fde-109">Aucune modification de ces séquences ne doit être nécessaire pour créer le package d’installation du bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="29fde-109">No changes to these sequences should be necessary to author the Notepad installation package.</span></span>

<span data-ttu-id="29fde-110">Utilisez votre éditeur de base de données pour ouvrir MNP2000.msi et entrez les données suivantes dans la table InstallUISequence.</span><span class="sxs-lookup"><span data-stu-id="29fde-110">Use your database editor to open MNP2000.msi and enter the following data into the InstallUISequence table.</span></span>

[<span data-ttu-id="29fde-111">Table InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="29fde-111">InstallUISequence Table</span></span>](installuisequence-table.md)



| <span data-ttu-id="29fde-112">Action</span><span class="sxs-lookup"><span data-stu-id="29fde-112">Action</span></span>                | <span data-ttu-id="29fde-113">Condition</span><span class="sxs-lookup"><span data-stu-id="29fde-113">Condition</span></span>                                    | <span data-ttu-id="29fde-114">Séquence</span><span class="sxs-lookup"><span data-stu-id="29fde-114">Sequence</span></span> |
|-----------------------|----------------------------------------------|----------|
| <span data-ttu-id="29fde-115">AppSearch</span><span class="sxs-lookup"><span data-stu-id="29fde-115">AppSearch</span></span>             |                                              | <span data-ttu-id="29fde-116">400</span><span class="sxs-lookup"><span data-stu-id="29fde-116">400</span></span>      |
| <span data-ttu-id="29fde-117">CCPSearch</span><span class="sxs-lookup"><span data-stu-id="29fde-117">CCPSearch</span></span>             | <span data-ttu-id="29fde-118">NON installé</span><span class="sxs-lookup"><span data-stu-id="29fde-118">NOT Installed</span></span>                                | <span data-ttu-id="29fde-119">500</span><span class="sxs-lookup"><span data-stu-id="29fde-119">500</span></span>      |
| <span data-ttu-id="29fde-120">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="29fde-120">CostFinalize</span></span>          |                                              | <span data-ttu-id="29fde-121">1 000</span><span class="sxs-lookup"><span data-stu-id="29fde-121">1000</span></span>     |
| <span data-ttu-id="29fde-122">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="29fde-122">CostInitialize</span></span>        |                                              | <span data-ttu-id="29fde-123">800</span><span class="sxs-lookup"><span data-stu-id="29fde-123">800</span></span>      |
| <span data-ttu-id="29fde-124">ExecuteAction</span><span class="sxs-lookup"><span data-stu-id="29fde-124">ExecuteAction</span></span>         |                                              | <span data-ttu-id="29fde-125">1 300</span><span class="sxs-lookup"><span data-stu-id="29fde-125">1300</span></span>     |
| <span data-ttu-id="29fde-126">ExitDlg</span><span class="sxs-lookup"><span data-stu-id="29fde-126">ExitDlg</span></span>               |                                              | <span data-ttu-id="29fde-127">-1</span><span class="sxs-lookup"><span data-stu-id="29fde-127">-1</span></span>       |
| <span data-ttu-id="29fde-128">FatalErrorDlg</span><span class="sxs-lookup"><span data-stu-id="29fde-128">FatalErrorDlg</span></span>         |                                              | <span data-ttu-id="29fde-129">-3</span><span class="sxs-lookup"><span data-stu-id="29fde-129">-3</span></span>       |
| <span data-ttu-id="29fde-130">FileCost</span><span class="sxs-lookup"><span data-stu-id="29fde-130">FileCost</span></span>              |                                              | <span data-ttu-id="29fde-131">900</span><span class="sxs-lookup"><span data-stu-id="29fde-131">900</span></span>      |
| <span data-ttu-id="29fde-132">LaunchConditions</span><span class="sxs-lookup"><span data-stu-id="29fde-132">LaunchConditions</span></span>      |                                              | <span data-ttu-id="29fde-133">100</span><span class="sxs-lookup"><span data-stu-id="29fde-133">100</span></span>      |
| <span data-ttu-id="29fde-134">MaintenanceWelcomeDlg</span><span class="sxs-lookup"><span data-stu-id="29fde-134">MaintenanceWelcomeDlg</span></span> | <span data-ttu-id="29fde-135">Installé et ne reprend pas et n’est pas présélectionné</span><span class="sxs-lookup"><span data-stu-id="29fde-135">Installed AND NOT RESUME AND NOT Preselected</span></span> | <span data-ttu-id="29fde-136">1250</span><span class="sxs-lookup"><span data-stu-id="29fde-136">1250</span></span>     |
| <span data-ttu-id="29fde-137">PrepareDlg</span><span class="sxs-lookup"><span data-stu-id="29fde-137">PrepareDlg</span></span>            |                                              | <span data-ttu-id="29fde-138">140</span><span class="sxs-lookup"><span data-stu-id="29fde-138">140</span></span>      |
| <span data-ttu-id="29fde-139">ProgressDlg</span><span class="sxs-lookup"><span data-stu-id="29fde-139">ProgressDlg</span></span>           |                                              | <span data-ttu-id="29fde-140">1 280</span><span class="sxs-lookup"><span data-stu-id="29fde-140">1280</span></span>     |
| <span data-ttu-id="29fde-141">ResumeDlg</span><span class="sxs-lookup"><span data-stu-id="29fde-141">ResumeDlg</span></span>             | <span data-ttu-id="29fde-142">Installé et (reprise ou présélection)</span><span class="sxs-lookup"><span data-stu-id="29fde-142">Installed AND (RESUME OR Preselected)</span></span>        | <span data-ttu-id="29fde-143">1240</span><span class="sxs-lookup"><span data-stu-id="29fde-143">1240</span></span>     |
| <span data-ttu-id="29fde-144">RMCCPSearch</span><span class="sxs-lookup"><span data-stu-id="29fde-144">RMCCPSearch</span></span>           | <span data-ttu-id="29fde-145">NON installé</span><span class="sxs-lookup"><span data-stu-id="29fde-145">NOT Installed</span></span>                                | <span data-ttu-id="29fde-146">600</span><span class="sxs-lookup"><span data-stu-id="29fde-146">600</span></span>      |
| <span data-ttu-id="29fde-147">UserExitDlg</span><span class="sxs-lookup"><span data-stu-id="29fde-147">UserExitDlg</span></span>           |                                              | <span data-ttu-id="29fde-148">-2</span><span class="sxs-lookup"><span data-stu-id="29fde-148">-2</span></span>       |
| <span data-ttu-id="29fde-149">WelcomeDlg</span><span class="sxs-lookup"><span data-stu-id="29fde-149">WelcomeDlg</span></span>            | <span data-ttu-id="29fde-150">NON installé</span><span class="sxs-lookup"><span data-stu-id="29fde-150">NOT Installed</span></span>                                | <span data-ttu-id="29fde-151">1230</span><span class="sxs-lookup"><span data-stu-id="29fde-151">1230</span></span>     |
| <span data-ttu-id="29fde-152">MigrateFeatureStates</span><span class="sxs-lookup"><span data-stu-id="29fde-152">MigrateFeatureStates</span></span>  |                                              | <span data-ttu-id="29fde-153">1200</span><span class="sxs-lookup"><span data-stu-id="29fde-153">1200</span></span>     |
| <span data-ttu-id="29fde-154">FindRelatedProducts</span><span class="sxs-lookup"><span data-stu-id="29fde-154">FindRelatedProducts</span></span>   |                                              | <span data-ttu-id="29fde-155">200</span><span class="sxs-lookup"><span data-stu-id="29fde-155">200</span></span>      |



 

[<span data-ttu-id="29fde-156">Continuer</span><span class="sxs-lookup"><span data-stu-id="29fde-156">Continue</span></span>](importing-the-adminexecutesequence.md)

 

 



