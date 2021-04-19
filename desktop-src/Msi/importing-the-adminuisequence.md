---
description: La table AdminUISequence répertorie les actions que le programme d’installation appelle lorsqu’il exécute l’action d’administration de niveau supérieur et que le niveau d’interface utilisateur interne a la valeur interface utilisateur complète ou interface utilisateur réduite.
ms.assetid: f23bd5c2-1d7f-485f-a22b-99436dfab6bf
title: Importation du AdminUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f1b9d2a91a350097ac043c186478e4933f6e81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541862"
---
# <a name="importing-the-adminuisequence"></a><span data-ttu-id="346b3-103">Importation du AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="346b3-103">Importing the AdminUISequence</span></span>

<span data-ttu-id="346b3-104">La [table AdminUISequence](adminuisequence-table.md) répertorie les actions que le programme d’installation appelle lorsqu’il exécute l' [action d’administration](admin-action.md) de niveau supérieur et que le niveau d’interface utilisateur interne a la valeur interface utilisateur complète ou interface utilisateur réduite.</span><span class="sxs-lookup"><span data-stu-id="346b3-104">The [AdminUISequence table](adminuisequence-table.md) lists actions that the installer calls when it executes the top-level [ADMIN action](admin-action.md) and the internal user interface level is set to full UI or reduced UI.</span></span> <span data-ttu-id="346b3-105">Le programme d’installation ignore les actions dans ce tableau si le niveau de l’interface utilisateur est défini sur interface utilisateur de base ou aucune interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="346b3-105">The installer skips the actions in this table if the user interface level is set to basic UI or no UI.</span></span> <span data-ttu-id="346b3-106">Consultez l' [interface utilisateur](user-interface.md) et les [niveaux d’interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="346b3-106">See [User Interface](user-interface.md) and [User Interface Levels](user-interface-levels.md).</span></span> <span data-ttu-id="346b3-107">Consultez le [groupe tables de procédures d’installation](installation-procedure-tables-group.md), [à l’aide d’une table de séquences](using-a-sequence-table.md)et de l' [exemple de table de séquence détaillé](sequence-table-detailed-example.md).</span><span class="sxs-lookup"><span data-stu-id="346b3-107">See [Installation Procedure Tables Group](installation-procedure-tables-group.md), [Using a Sequence Table](using-a-sequence-table.md), and the [Sequence Table Detailed Example](sequence-table-detailed-example.md).</span></span>

<span data-ttu-id="346b3-108">Si, dans la section, vous avez [importé une base de données vide](importing-a-blank-database.md) que vous avez utilisée uisample.msi du kit de développement logiciel (SDK) Windows Installer, les tables de séquence de votre copie de MNP2000.msi contiennent déjà les séquences d’action suggérées décrites dans [utilisation d’une table de séquences](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="346b3-108">If in the section [Importing a Blank Database](importing-a-blank-database.md) you used uisample.msi from the Windows Installer SDK, the sequence tables in your copy of MNP2000.msi already contains the suggested action sequences described in [Using a Sequence Table](using-a-sequence-table.md).</span></span> <span data-ttu-id="346b3-109">Aucune modification de ces séquences ne doit être nécessaire pour installer l’exemple du bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="346b3-109">No changes to these sequences should be necessary to install the Notepad sample.</span></span>

<span data-ttu-id="346b3-110">Utilisez votre éditeur de base de données pour ouvrir MNP2000.msi et entrez les données suivantes dans la table AdminExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="346b3-110">Use your database editor to open MNP2000.msi and enter the following data into the AdminExecuteSequence table.</span></span>

[<span data-ttu-id="346b3-111">Table AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="346b3-111">AdminUISequence Table</span></span>](adminuisequence-table.md)



| <span data-ttu-id="346b3-112">Action</span><span class="sxs-lookup"><span data-stu-id="346b3-112">Action</span></span>          | <span data-ttu-id="346b3-113">Condition</span><span class="sxs-lookup"><span data-stu-id="346b3-113">Condition</span></span> | <span data-ttu-id="346b3-114">Séquence</span><span class="sxs-lookup"><span data-stu-id="346b3-114">Sequence</span></span> |
|-----------------|-----------|----------|
| <span data-ttu-id="346b3-115">AdminWelcomeDlg</span><span class="sxs-lookup"><span data-stu-id="346b3-115">AdminWelcomeDlg</span></span> |           | <span data-ttu-id="346b3-116">1230</span><span class="sxs-lookup"><span data-stu-id="346b3-116">1230</span></span>     |
| <span data-ttu-id="346b3-117">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="346b3-117">CostFinalize</span></span>    |           | <span data-ttu-id="346b3-118">1 000</span><span class="sxs-lookup"><span data-stu-id="346b3-118">1000</span></span>     |
| <span data-ttu-id="346b3-119">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="346b3-119">CostInitialize</span></span>  |           | <span data-ttu-id="346b3-120">800</span><span class="sxs-lookup"><span data-stu-id="346b3-120">800</span></span>      |
| <span data-ttu-id="346b3-121">ExecuteAction</span><span class="sxs-lookup"><span data-stu-id="346b3-121">ExecuteAction</span></span>   |           | <span data-ttu-id="346b3-122">1 300</span><span class="sxs-lookup"><span data-stu-id="346b3-122">1300</span></span>     |
| <span data-ttu-id="346b3-123">ExitDlg</span><span class="sxs-lookup"><span data-stu-id="346b3-123">ExitDlg</span></span>         |           | <span data-ttu-id="346b3-124">-1</span><span class="sxs-lookup"><span data-stu-id="346b3-124">-1</span></span>       |
| <span data-ttu-id="346b3-125">FatalErrorDlg</span><span class="sxs-lookup"><span data-stu-id="346b3-125">FatalErrorDlg</span></span>   |           | <span data-ttu-id="346b3-126">-3</span><span class="sxs-lookup"><span data-stu-id="346b3-126">-3</span></span>       |
| <span data-ttu-id="346b3-127">FileCost</span><span class="sxs-lookup"><span data-stu-id="346b3-127">FileCost</span></span>        |           | <span data-ttu-id="346b3-128">900</span><span class="sxs-lookup"><span data-stu-id="346b3-128">900</span></span>      |
| <span data-ttu-id="346b3-129">PrepareDlg</span><span class="sxs-lookup"><span data-stu-id="346b3-129">PrepareDlg</span></span>      |           | <span data-ttu-id="346b3-130">140</span><span class="sxs-lookup"><span data-stu-id="346b3-130">140</span></span>      |
| <span data-ttu-id="346b3-131">ProgressDlg</span><span class="sxs-lookup"><span data-stu-id="346b3-131">ProgressDlg</span></span>     |           | <span data-ttu-id="346b3-132">1 280</span><span class="sxs-lookup"><span data-stu-id="346b3-132">1280</span></span>     |
| <span data-ttu-id="346b3-133">UserExitDlg</span><span class="sxs-lookup"><span data-stu-id="346b3-133">UserExitDlg</span></span>     |           | <span data-ttu-id="346b3-134">-2</span><span class="sxs-lookup"><span data-stu-id="346b3-134">-2</span></span>       |



 

[<span data-ttu-id="346b3-135">Continuer</span><span class="sxs-lookup"><span data-stu-id="346b3-135">Continue</span></span>](importing-the-advtexecutesequence.md)

 

 



