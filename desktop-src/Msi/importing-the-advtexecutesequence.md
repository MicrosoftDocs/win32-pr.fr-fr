---
description: La table AdvtExecuteSequence répertorie les actions que le programme d’installation appelle lorsqu’il exécute l’action de publication de niveau supérieur. Consultez le groupe tables de procédures d’installation, à l’aide d’une table de séquences et de l’exemple de table de séquence détaillé.
ms.assetid: 269bd28c-fa45-42b8-a610-1c4c5fcabc19
title: Importation du AdvtExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e4d7622670973a622b1376456ecfef445684cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757816"
---
# <a name="importing-the-advtexecutesequence"></a><span data-ttu-id="f2b98-104">Importation du AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="f2b98-104">Importing the AdvtExecuteSequence</span></span>

<span data-ttu-id="f2b98-105">La [table AdvtExecuteSequence](advtexecutesequence-table.md) répertorie les actions que le programme d’installation appelle lorsqu’il exécute l' [action de publication](advertise-action.md)de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="f2b98-105">The [AdvtExecuteSequence table](advtexecutesequence-table.md) lists actions the installer calls when it executes the top-level [ADVERTISE action](advertise-action.md).</span></span> <span data-ttu-id="f2b98-106">Consultez le [groupe tables de procédures d’installation](installation-procedure-tables-group.md), [à l’aide d’une table de séquences](using-a-sequence-table.md)et de l' [exemple de table de séquence détaillé](sequence-table-detailed-example.md).</span><span class="sxs-lookup"><span data-stu-id="f2b98-106">See [Installation Procedure Tables Group](installation-procedure-tables-group.md), [Using a Sequence Table](using-a-sequence-table.md), and the [Sequence Table Detailed Example](sequence-table-detailed-example.md).</span></span>

<span data-ttu-id="f2b98-107">Si, dans la section, vous avez [importé une base de données vide](importing-a-blank-database.md) que vous avez utilisée uisample.msi du kit de développement logiciel (SDK) Windows Installer, les tables de séquence de votre copie de MNP2000.msi contiennent déjà les séquences d’action suggérées décrites dans [utilisation d’une table de séquences](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="f2b98-107">If in the section [Importing a Blank Database](importing-a-blank-database.md) you used uisample.msi from the Windows Installer SDK, the sequence tables in your copy of MNP2000.msi already contains the suggested action sequences described in [Using a Sequence table](using-a-sequence-table.md).</span></span> <span data-ttu-id="f2b98-108">Aucune modification de ces séquences ne doit être nécessaire pour créer l’exemple de package d’installation du bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="f2b98-108">No changes to these sequences should be necessary to author the Notepad sample installation package.</span></span>

<span data-ttu-id="f2b98-109">Utilisez votre éditeur de base de données pour ouvrir MNP2000.msi et entrez les données suivantes dans la [table AdvtExecuteSequence](advtexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="f2b98-109">Use your database editor to open MNP2000.msi and enter the following data into the [AdvtExecuteSequence table](advtexecutesequence-table.md).</span></span>

[<span data-ttu-id="f2b98-110">Table AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="f2b98-110">AdvtExecuteSequence Table</span></span>](advtexecutesequence-table.md)



| <span data-ttu-id="f2b98-111">Action</span><span class="sxs-lookup"><span data-stu-id="f2b98-111">Action</span></span>                | <span data-ttu-id="f2b98-112">Condition</span><span class="sxs-lookup"><span data-stu-id="f2b98-112">Condition</span></span> | <span data-ttu-id="f2b98-113">Séquence</span><span class="sxs-lookup"><span data-stu-id="f2b98-113">Sequence</span></span> |
|-----------------------|-----------|----------|
| <span data-ttu-id="f2b98-114">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="f2b98-114">CostFinalize</span></span>          |           | <span data-ttu-id="f2b98-115">1 000</span><span class="sxs-lookup"><span data-stu-id="f2b98-115">1000</span></span>     |
| <span data-ttu-id="f2b98-116">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="f2b98-116">CostInitialize</span></span>        |           | <span data-ttu-id="f2b98-117">800</span><span class="sxs-lookup"><span data-stu-id="f2b98-117">800</span></span>      |
| <span data-ttu-id="f2b98-118">CreateShortcuts</span><span class="sxs-lookup"><span data-stu-id="f2b98-118">CreateShortcuts</span></span>       |           | <span data-ttu-id="f2b98-119">4500</span><span class="sxs-lookup"><span data-stu-id="f2b98-119">4500</span></span>     |
| <span data-ttu-id="f2b98-120">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="f2b98-120">InstallFinalize</span></span>       |           | <span data-ttu-id="f2b98-121">6600</span><span class="sxs-lookup"><span data-stu-id="f2b98-121">6600</span></span>     |
| <span data-ttu-id="f2b98-122">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="f2b98-122">InstallInitialize</span></span>     |           | <span data-ttu-id="f2b98-123">1500</span><span class="sxs-lookup"><span data-stu-id="f2b98-123">1500</span></span>     |
| <span data-ttu-id="f2b98-124">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="f2b98-124">InstallValidate</span></span>       |           | <span data-ttu-id="f2b98-125">1400</span><span class="sxs-lookup"><span data-stu-id="f2b98-125">1400</span></span>     |
| <span data-ttu-id="f2b98-126">PublishComponents</span><span class="sxs-lookup"><span data-stu-id="f2b98-126">PublishComponents</span></span>     |           | <span data-ttu-id="f2b98-127">6200</span><span class="sxs-lookup"><span data-stu-id="f2b98-127">6200</span></span>     |
| <span data-ttu-id="f2b98-128">PublishFeatures</span><span class="sxs-lookup"><span data-stu-id="f2b98-128">PublishFeatures</span></span>       |           | <span data-ttu-id="f2b98-129">6300</span><span class="sxs-lookup"><span data-stu-id="f2b98-129">6300</span></span>     |
| <span data-ttu-id="f2b98-130">PublishProduct</span><span class="sxs-lookup"><span data-stu-id="f2b98-130">PublishProduct</span></span>        |           | <span data-ttu-id="f2b98-131">6 400</span><span class="sxs-lookup"><span data-stu-id="f2b98-131">6400</span></span>     |
| <span data-ttu-id="f2b98-132">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="f2b98-132">RegisterClassInfo</span></span>     |           | <span data-ttu-id="f2b98-133">4600</span><span class="sxs-lookup"><span data-stu-id="f2b98-133">4600</span></span>     |
| <span data-ttu-id="f2b98-134">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="f2b98-134">RegisterExtensionInfo</span></span> |           | <span data-ttu-id="f2b98-135">4700</span><span class="sxs-lookup"><span data-stu-id="f2b98-135">4700</span></span>     |
| <span data-ttu-id="f2b98-136">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="f2b98-136">RegisterMIMEInfo</span></span>      |           | <span data-ttu-id="f2b98-137">4900</span><span class="sxs-lookup"><span data-stu-id="f2b98-137">4900</span></span>     |
| <span data-ttu-id="f2b98-138">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="f2b98-138">RegisterProgIdInfo</span></span>    |           | <span data-ttu-id="f2b98-139">4 800</span><span class="sxs-lookup"><span data-stu-id="f2b98-139">4800</span></span>     |



 

<span data-ttu-id="f2b98-140">La [table AdvtUISequence](advtuisequence-table.md) n’est pas utilisée par le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="f2b98-140">The [AdvtUISequence table](advtuisequence-table.md) is not used by the installer.</span></span> <span data-ttu-id="f2b98-141">Cette table ne doit pas exister ou rester vide dans la base de données d’installation.</span><span class="sxs-lookup"><span data-stu-id="f2b98-141">This table should not exist or be left empty in the installation database.</span></span>

[<span data-ttu-id="f2b98-142">Continuer</span><span class="sxs-lookup"><span data-stu-id="f2b98-142">Continue</span></span>](adding-summary-information.md)

 

 



