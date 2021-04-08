---
description: La table AdminExecuteSequence répertorie les actions exécutées par le programme d’installation lorsqu’il appelle l’action d’administration de niveau supérieur. Consultez le groupe tables de procédures d’installation, à l’aide d’une table de séquences et de l’exemple de table de séquence détaillé.
ms.assetid: 8b1da4a3-0b82-4b71-8a32-59e90025cbfa
title: Importation du AdminExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60e5cfef89ada780d9ce647f45667fdc34cc5b01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752781"
---
# <a name="importing-the-adminexecutesequence"></a><span data-ttu-id="4bda3-104">Importation du AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="4bda3-104">Importing the AdminExecuteSequence</span></span>

<span data-ttu-id="4bda3-105">La [table AdminExecuteSequence](adminexecutesequence-table.md) répertorie les actions exécutées par le programme d’installation lorsqu’il appelle l' [action d’administration](admin-action.md)de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="4bda3-105">The [AdminExecuteSequence table](adminexecutesequence-table.md) lists actions that the installer executes when it calls the top-level [ADMIN action](admin-action.md).</span></span> <span data-ttu-id="4bda3-106">Consultez le [groupe tables de procédures d’installation](installation-procedure-tables-group.md), [à l’aide d’une table de séquences](using-a-sequence-table.md)et de l' [exemple de table de séquence détaillé](sequence-table-detailed-example.md).</span><span class="sxs-lookup"><span data-stu-id="4bda3-106">See [Installation Procedure Tables Group](installation-procedure-tables-group.md), [Using a Sequence Table](using-a-sequence-table.md), and the [Sequence Table Detailed Example](sequence-table-detailed-example.md).</span></span>

<span data-ttu-id="4bda3-107">Si, dans la section, vous avez [importé une base de données vide](importing-a-blank-database.md) que vous avez utilisée uisample.msi du kit de développement logiciel (SDK) Windows Installer, les tables de séquence de votre copie de MNP2000.msi contiennent déjà les séquences d’action suggérées décrites dans [utilisation d’une table de séquences](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="4bda3-107">If in the section [Importing a Blank Database](importing-a-blank-database.md) you used uisample.msi from the Windows Installer SDK, the sequence tables in your copy of MNP2000.msi already contains the suggested action sequences described in [Using a Sequence Table](using-a-sequence-table.md).</span></span> <span data-ttu-id="4bda3-108">Aucune modification de ces séquences ne doit être nécessaire pour créer l’exemple de package d’installation du bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="4bda3-108">No changes to these sequences should be necessary to author the Notepad sample installation package.</span></span>

<span data-ttu-id="4bda3-109">Utilisez votre éditeur de base de données pour ouvrir MNP2000.msi et entrez les données suivantes dans la table AdminExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="4bda3-109">Use your database editor to open MNP2000.msi and enter the following data into the AdminExecuteSequence table.</span></span>

[<span data-ttu-id="4bda3-110">Table AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="4bda3-110">AdminExecuteSequence Table</span></span>](adminexecutesequence-table.md)



| <span data-ttu-id="4bda3-111">Action</span><span class="sxs-lookup"><span data-stu-id="4bda3-111">Action</span></span>              | <span data-ttu-id="4bda3-112">Condition</span><span class="sxs-lookup"><span data-stu-id="4bda3-112">Condition</span></span> | <span data-ttu-id="4bda3-113">Séquence</span><span class="sxs-lookup"><span data-stu-id="4bda3-113">Sequence</span></span> |
|---------------------|-----------|----------|
| <span data-ttu-id="4bda3-114">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="4bda3-114">CostFinalize</span></span>        |           | <span data-ttu-id="4bda3-115">1 000</span><span class="sxs-lookup"><span data-stu-id="4bda3-115">1000</span></span>     |
| <span data-ttu-id="4bda3-116">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="4bda3-116">CostInitialize</span></span>      |           | <span data-ttu-id="4bda3-117">800</span><span class="sxs-lookup"><span data-stu-id="4bda3-117">800</span></span>      |
| <span data-ttu-id="4bda3-118">FileCost</span><span class="sxs-lookup"><span data-stu-id="4bda3-118">FileCost</span></span>            |           | <span data-ttu-id="4bda3-119">900</span><span class="sxs-lookup"><span data-stu-id="4bda3-119">900</span></span>      |
| <span data-ttu-id="4bda3-120">InstallAdminPackage</span><span class="sxs-lookup"><span data-stu-id="4bda3-120">InstallAdminPackage</span></span> |           | <span data-ttu-id="4bda3-121">3900</span><span class="sxs-lookup"><span data-stu-id="4bda3-121">3900</span></span>     |
| <span data-ttu-id="4bda3-122">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="4bda3-122">InstallFiles</span></span>        |           | <span data-ttu-id="4bda3-123">4000</span><span class="sxs-lookup"><span data-stu-id="4bda3-123">4000</span></span>     |
| <span data-ttu-id="4bda3-124">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="4bda3-124">InstallFinalize</span></span>     |           | <span data-ttu-id="4bda3-125">6600</span><span class="sxs-lookup"><span data-stu-id="4bda3-125">6600</span></span>     |
| <span data-ttu-id="4bda3-126">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="4bda3-126">InstallInitialize</span></span>   |           | <span data-ttu-id="4bda3-127">1500</span><span class="sxs-lookup"><span data-stu-id="4bda3-127">1500</span></span>     |
| <span data-ttu-id="4bda3-128">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="4bda3-128">InstallValidate</span></span>     |           | <span data-ttu-id="4bda3-129">1400</span><span class="sxs-lookup"><span data-stu-id="4bda3-129">1400</span></span>     |



 

[<span data-ttu-id="4bda3-130">Continuer</span><span class="sxs-lookup"><span data-stu-id="4bda3-130">Continue</span></span>](importing-the-adminuisequence.md)

 

 



