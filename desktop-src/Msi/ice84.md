---
description: ICE84 vérifie la table AdvtExecuteSequence, la table AdminExecuteSequence et la table InstallExecuteSequence pour vérifier que les actions standard suivantes n’ont pas été définies avec des conditions dans le champ condition.
ms.assetid: 0d1bbf4b-ffab-409e-a292-891dfa823433
title: ICE84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8960f53f5a01e9bec95a02bb3241487aa31aaae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320086"
---
# <a name="ice84"></a><span data-ttu-id="42457-103">ICE84</span><span class="sxs-lookup"><span data-stu-id="42457-103">ICE84</span></span>

<span data-ttu-id="42457-104">ICE84 vérifie la table [AdvtExecuteSequence](advtexecutesequence-table.md), la [table AdminExecuteSequence](adminexecutesequence-table.md)et la [table InstallExecuteSequence](installexecutesequence-table.md) pour vérifier que les [actions standard](standard-actions.md) suivantes n’ont pas été définies avec des conditions dans le champ condition.</span><span class="sxs-lookup"><span data-stu-id="42457-104">ICE84 checks the [AdvtExecuteSequence table](advtexecutesequence-table.md), [AdminExecuteSequence table](adminexecutesequence-table.md), and the [InstallExecuteSequence table](installexecutesequence-table.md) to verify that the following [standard actions](standard-actions.md) have not been set with conditions in the Condition field.</span></span>

-   [<span data-ttu-id="42457-105">Action CostInitialize</span><span class="sxs-lookup"><span data-stu-id="42457-105">CostInitialize action</span></span>](costinitialize-action.md)
-   [<span data-ttu-id="42457-106">Action CostFinalize</span><span class="sxs-lookup"><span data-stu-id="42457-106">CostFinalize action</span></span>](costfinalize-action.md)
-   [<span data-ttu-id="42457-107">Action FileCost</span><span class="sxs-lookup"><span data-stu-id="42457-107">FileCost action</span></span>](filecost-action.md)
-   [<span data-ttu-id="42457-108">Action InstallValidate</span><span class="sxs-lookup"><span data-stu-id="42457-108">InstallValidate action</span></span>](installvalidate-action.md)
-   [<span data-ttu-id="42457-109">Action InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="42457-109">InstallInitialize action</span></span>](installinitialize-action.md)
-   [<span data-ttu-id="42457-110">Action InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="42457-110">InstallFinalize action</span></span>](installfinalize-action.md)
-   [<span data-ttu-id="42457-111">Action ProcessComponents</span><span class="sxs-lookup"><span data-stu-id="42457-111">ProcessComponents action</span></span>](processcomponents-action.md)
-   [<span data-ttu-id="42457-112">Action PublishFeatures</span><span class="sxs-lookup"><span data-stu-id="42457-112">PublishFeatures action</span></span>](publishfeatures-action.md)
-   [<span data-ttu-id="42457-113">Action PublishProduct</span><span class="sxs-lookup"><span data-stu-id="42457-113">PublishProduct action</span></span>](publishproduct-action.md)
-   [<span data-ttu-id="42457-114">Action RegisterProduct</span><span class="sxs-lookup"><span data-stu-id="42457-114">RegisterProduct action</span></span>](registerproduct-action.md)
-   [<span data-ttu-id="42457-115">Action UnpublishFeatures</span><span class="sxs-lookup"><span data-stu-id="42457-115">UnpublishFeatures action</span></span>](unpublishfeatures-action.md)

<span data-ttu-id="42457-116">Si des conditions sont trouvées, ICE84 publie un avertissement.</span><span class="sxs-lookup"><span data-stu-id="42457-116">If conditions are found, ICE84 posts a warning.</span></span>

## <a name="result"></a><span data-ttu-id="42457-117">Résultats</span><span class="sxs-lookup"><span data-stu-id="42457-117">Result</span></span>

<span data-ttu-id="42457-118">ICE84 publie l’avertissement suivant.</span><span class="sxs-lookup"><span data-stu-id="42457-118">ICE84 posts the following warning.</span></span>



| <span data-ttu-id="42457-119">Erreur ICE84</span><span class="sxs-lookup"><span data-stu-id="42457-119">ICE84 error</span></span>                                                             | <span data-ttu-id="42457-120">Description</span><span class="sxs-lookup"><span data-stu-id="42457-120">Description</span></span>                                           |
|-------------------------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="42457-121">L’action « \[ 1 \] » trouvée dans la table% s est une action requise avec une condition.</span><span class="sxs-lookup"><span data-stu-id="42457-121">Action '\[1\]' found in %s table is a required action with a condition.</span></span> | <span data-ttu-id="42457-122">Une action requise a été créée avec une condition.</span><span class="sxs-lookup"><span data-stu-id="42457-122">A required action has been authored with a condition.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="42457-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="42457-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42457-124">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="42457-124">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



