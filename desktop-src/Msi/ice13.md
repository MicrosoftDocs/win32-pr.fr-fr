---
description: ICE13 vérifie que les boîtes de dialogue des tables de séquences s’affichent dans les tables AdminUISequence ou InstallUISequence. Les boîtes de dialogue ne doivent pas figurer dans les tables InstallExecuteSequence, AdminExecuteSequence ou AdvtExecuteSequence.
ms.assetid: 51542a8f-2fb6-4021-b52d-6f7a2b0294d6
title: ICE13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fff440217ccffe41d5e4036f4ea0d03d1eabb0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952288"
---
# <a name="ice13"></a><span data-ttu-id="633f6-104">ICE13</span><span class="sxs-lookup"><span data-stu-id="633f6-104">ICE13</span></span>

<span data-ttu-id="633f6-105">ICE13 vérifie que les boîtes de dialogue des tables de séquences s’affichent dans les tables [AdminUISequence](adminuisequence-table.md)ou [InstallUISequence](installuisequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="633f6-105">ICE13 validates that dialogs in sequence tables appear in the [AdminUISequence](adminuisequence-table.md), or [InstallUISequence](installuisequence-table.md) tables.</span></span> <span data-ttu-id="633f6-106">Les boîtes de dialogue ne doivent pas figurer dans les tables [InstallExecuteSequence](installexecutesequence-table.md), [AdminExecuteSequence](adminexecutesequence-table.md)ou [AdvtExecuteSequence](advtexecutesequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="633f6-106">Dialogs must not be listed in the [InstallExecuteSequence](installexecutesequence-table.md), [AdminExecuteSequence](adminexecutesequence-table.md), or [AdvtExecuteSequence](advtexecutesequence-table.md) tables.</span></span>

## <a name="result"></a><span data-ttu-id="633f6-107">Résultats</span><span class="sxs-lookup"><span data-stu-id="633f6-107">Result</span></span>

<span data-ttu-id="633f6-108">ICE13 publie un message d’erreur si une boîte de dialogue s’affiche dans une table de séquence d’exécution.</span><span class="sxs-lookup"><span data-stu-id="633f6-108">ICE13 posts an error message if a dialog appears in an execute sequence table.</span></span>

## <a name="example"></a><span data-ttu-id="633f6-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="633f6-109">Example</span></span>

<span data-ttu-id="633f6-110">Dans l’exemple suivant, ICE13 publie un message d’erreur indiquant que « WelcomeDialog » ne peut pas être listé dans la table « InstallExecuteSequence ».</span><span class="sxs-lookup"><span data-stu-id="633f6-110">For the following example, ICE13 posts an error message stating that the 'WelcomeDialog' cannot be listed in the 'InstallExecuteSequence' table.</span></span>

<span data-ttu-id="633f6-111">[Table InstallExecuteSequence](installexecutesequence-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="633f6-111">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="633f6-112">Action</span><span class="sxs-lookup"><span data-stu-id="633f6-112">Action</span></span>          |
|-----------------|
| <span data-ttu-id="633f6-113">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="633f6-113">InstallFinalize</span></span> |
| <span data-ttu-id="633f6-114">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="633f6-114">CostFinalize</span></span>    |
| <span data-ttu-id="633f6-115">WelcomeDialog</span><span class="sxs-lookup"><span data-stu-id="633f6-115">WelcomeDialog</span></span>   |



 

<span data-ttu-id="633f6-116">[Table InstallUISequence](installuisequence-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="633f6-116">[InstallUISequence Table](installuisequence-table.md) (partial)</span></span>



| <span data-ttu-id="633f6-117">Action</span><span class="sxs-lookup"><span data-stu-id="633f6-117">Action</span></span>         |
|----------------|
| <span data-ttu-id="633f6-118">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="633f6-118">CostFinalize</span></span>   |
| <span data-ttu-id="633f6-119">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="633f6-119">CostInitialize</span></span> |
| <span data-ttu-id="633f6-120">BrowseDialog</span><span class="sxs-lookup"><span data-stu-id="633f6-120">BrowseDialog</span></span>   |



 

<span data-ttu-id="633f6-121">[Table de boîtes de dialogue](dialog-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="633f6-121">[Dialog Table](dialog-table.md) (partial)</span></span>



| <span data-ttu-id="633f6-122">Boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="633f6-122">Dialog</span></span>        |
|---------------|
| <span data-ttu-id="633f6-123">BrowseDialog</span><span class="sxs-lookup"><span data-stu-id="633f6-123">BrowseDialog</span></span>  |
| <span data-ttu-id="633f6-124">WelcomeDialog</span><span class="sxs-lookup"><span data-stu-id="633f6-124">WelcomeDialog</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="633f6-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="633f6-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="633f6-126">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="633f6-126">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



