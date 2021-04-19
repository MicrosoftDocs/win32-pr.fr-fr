---
description: La table LaunchCondition est utilisée par l’action LaunchConditions. Elle contient une liste de conditions qui doivent toutes être satisfaites pour que l’installation commence.
ms.assetid: 6e550cc7-c479-417e-ab89-882d8fece4e1
title: Table LaunchCondition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d67834f058575dde297454480040028ef9c5732
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514188"
---
# <a name="launchcondition-table"></a><span data-ttu-id="b4925-104">Table LaunchCondition</span><span class="sxs-lookup"><span data-stu-id="b4925-104">LaunchCondition Table</span></span>

<span data-ttu-id="b4925-105">La table LaunchCondition est utilisée par l' [action LaunchConditions](launchconditions-action.md).</span><span class="sxs-lookup"><span data-stu-id="b4925-105">The LaunchCondition table is used by the [LaunchConditions action](launchconditions-action.md).</span></span> <span data-ttu-id="b4925-106">Elle contient une liste de conditions qui doivent toutes être satisfaites pour que l’installation commence.</span><span class="sxs-lookup"><span data-stu-id="b4925-106">It contains a list of conditions that all must be satisfied for the installation to begin.</span></span>

<span data-ttu-id="b4925-107">La table LaunchCondition contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="b4925-107">The LaunchCondition table has the following columns.</span></span>



| <span data-ttu-id="b4925-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="b4925-108">Column</span></span>      | <span data-ttu-id="b4925-109">Type</span><span class="sxs-lookup"><span data-stu-id="b4925-109">Type</span></span>                       | <span data-ttu-id="b4925-110">Clé</span><span class="sxs-lookup"><span data-stu-id="b4925-110">Key</span></span> | <span data-ttu-id="b4925-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="b4925-111">Nullable</span></span> |
|-------------|----------------------------|-----|----------|
| <span data-ttu-id="b4925-112">Condition</span><span class="sxs-lookup"><span data-stu-id="b4925-112">Condition</span></span>   | [<span data-ttu-id="b4925-113">Condition</span><span class="sxs-lookup"><span data-stu-id="b4925-113">Condition</span></span>](condition.md) | <span data-ttu-id="b4925-114">O</span><span class="sxs-lookup"><span data-stu-id="b4925-114">Y</span></span>   | <span data-ttu-id="b4925-115">N</span><span class="sxs-lookup"><span data-stu-id="b4925-115">N</span></span>        |
| <span data-ttu-id="b4925-116">Description</span><span class="sxs-lookup"><span data-stu-id="b4925-116">Description</span></span> | [<span data-ttu-id="b4925-117">Correct</span><span class="sxs-lookup"><span data-stu-id="b4925-117">Formatted</span></span>](formatted.md) | <span data-ttu-id="b4925-118">N</span><span class="sxs-lookup"><span data-stu-id="b4925-118">N</span></span>   | <span data-ttu-id="b4925-119">N</span><span class="sxs-lookup"><span data-stu-id="b4925-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="b4925-120">Colonnes</span><span class="sxs-lookup"><span data-stu-id="b4925-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="b4925-121"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Etat</span><span class="sxs-lookup"><span data-stu-id="b4925-121"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="b4925-122">Expression qui doit avoir la valeur true pour que l’installation commence.</span><span class="sxs-lookup"><span data-stu-id="b4925-122">Expression that must evaluate to True for installation to begin.</span></span>

</dd> <dt>

<span data-ttu-id="b4925-123"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive</span><span class="sxs-lookup"><span data-stu-id="b4925-123"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="b4925-124">Texte localisable à afficher lorsque la condition échoue et que l’installation doit être terminée.</span><span class="sxs-lookup"><span data-stu-id="b4925-124">Localizable text to display when the condition fails and the installation must be terminated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b4925-125">Notes</span><span class="sxs-lookup"><span data-stu-id="b4925-125">Remarks</span></span>

<span data-ttu-id="b4925-126">Vous ne pouvez pas garantir l’ordre dans lequel les conditions de lancement sont évaluées en créant cette table.</span><span class="sxs-lookup"><span data-stu-id="b4925-126">You cannot guarantee the order in which the launch conditions are evaluated by authoring this table.</span></span> <span data-ttu-id="b4925-127">S’il est nécessaire de contrôler l’ordre dans lequel les conditions sont évaluées, vous devez le faire à l’aide de l’action personnalisée type 19 actions personnalisées dans votre installation.</span><span class="sxs-lookup"><span data-stu-id="b4925-127">If it is necessary to control the order in which conditions are evaluated, you should do this by using Custom Action Type 19 custom actions in your installation.</span></span>

## <a name="validation"></a><span data-ttu-id="b4925-128">Validation</span><span class="sxs-lookup"><span data-stu-id="b4925-128">Validation</span></span>

<dl>

[<span data-ttu-id="b4925-129">ICE03</span><span class="sxs-lookup"><span data-stu-id="b4925-129">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="b4925-130">ICE06</span><span class="sxs-lookup"><span data-stu-id="b4925-130">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="b4925-131">ICE46</span><span class="sxs-lookup"><span data-stu-id="b4925-131">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="b4925-132">ICE79</span><span class="sxs-lookup"><span data-stu-id="b4925-132">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="b4925-133">ICE86</span><span class="sxs-lookup"><span data-stu-id="b4925-133">ICE86</span></span>](ice86.md)  
</dl>

 

 



