---
description: Le tableau d’affichage répertorie les contrôles de tableau blanc affichés dans l’interface utilisateur complète.
ms.assetid: bb8c1d7c-aa1d-43cc-9fb4-3a0ad75c4615
title: Tableau d’panneaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a561eb629e07b25437d6e5ce12b58bb0d7dd20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951752"
---
# <a name="billboard-table"></a><span data-ttu-id="2a355-103">Tableau d’panneaux</span><span class="sxs-lookup"><span data-stu-id="2a355-103">Billboard Table</span></span>

<span data-ttu-id="2a355-104">Le tableau d’affichage répertorie les contrôles de tableau [blanc](billboard-control.md) affichés dans l’interface utilisateur complète.</span><span class="sxs-lookup"><span data-stu-id="2a355-104">The Billboard table lists the [Billboard controls](billboard-control.md) displayed in the full user interface.</span></span>

<span data-ttu-id="2a355-105">La table du tableau blanc contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="2a355-105">The Billboard table has the following columns.</span></span>



| <span data-ttu-id="2a355-106">Colonne</span><span class="sxs-lookup"><span data-stu-id="2a355-106">Column</span></span>    | <span data-ttu-id="2a355-107">Type</span><span class="sxs-lookup"><span data-stu-id="2a355-107">Type</span></span>                         | <span data-ttu-id="2a355-108">Clé</span><span class="sxs-lookup"><span data-stu-id="2a355-108">Key</span></span> | <span data-ttu-id="2a355-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="2a355-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="2a355-110">Blanc</span><span class="sxs-lookup"><span data-stu-id="2a355-110">Billboard</span></span> | [<span data-ttu-id="2a355-111">Identificateur</span><span class="sxs-lookup"><span data-stu-id="2a355-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="2a355-112">O</span><span class="sxs-lookup"><span data-stu-id="2a355-112">Y</span></span>   | <span data-ttu-id="2a355-113">N</span><span class="sxs-lookup"><span data-stu-id="2a355-113">N</span></span>        |
| <span data-ttu-id="2a355-114">Fonctionnalité\_</span><span class="sxs-lookup"><span data-stu-id="2a355-114">Feature\_</span></span> | [<span data-ttu-id="2a355-115">Identificateur</span><span class="sxs-lookup"><span data-stu-id="2a355-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="2a355-116">N</span><span class="sxs-lookup"><span data-stu-id="2a355-116">N</span></span>   | <span data-ttu-id="2a355-117">N</span><span class="sxs-lookup"><span data-stu-id="2a355-117">N</span></span>        |
| <span data-ttu-id="2a355-118">Action</span><span class="sxs-lookup"><span data-stu-id="2a355-118">Action</span></span>    | [<span data-ttu-id="2a355-119">Identificateur</span><span class="sxs-lookup"><span data-stu-id="2a355-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="2a355-120">N</span><span class="sxs-lookup"><span data-stu-id="2a355-120">N</span></span>   | <span data-ttu-id="2a355-121">O</span><span class="sxs-lookup"><span data-stu-id="2a355-121">Y</span></span>        |
| <span data-ttu-id="2a355-122">Classement</span><span class="sxs-lookup"><span data-stu-id="2a355-122">Ordering</span></span>  | [<span data-ttu-id="2a355-123">Integer</span><span class="sxs-lookup"><span data-stu-id="2a355-123">Integer</span></span>](integer.md)       | <span data-ttu-id="2a355-124">N</span><span class="sxs-lookup"><span data-stu-id="2a355-124">N</span></span>   | <span data-ttu-id="2a355-125">O</span><span class="sxs-lookup"><span data-stu-id="2a355-125">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="2a355-126">Colonnes</span><span class="sxs-lookup"><span data-stu-id="2a355-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="2a355-127"><span id="Billboard"></span><span id="billboard"></span><span id="BILLBOARD"></span>Blanc</span><span class="sxs-lookup"><span data-stu-id="2a355-127"><span id="Billboard"></span><span id="billboard"></span><span id="BILLBOARD"></span>Billboard</span></span>
</dt> <dd>

<span data-ttu-id="2a355-128">Nom du contrôle de tableau [blanc](billboard-control.md).</span><span class="sxs-lookup"><span data-stu-id="2a355-128">Name of the [Billboard control](billboard-control.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a355-129"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Fonctionnalité\_</span><span class="sxs-lookup"><span data-stu-id="2a355-129"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="2a355-130">Clé externe de la première colonne de la [table de fonctionnalités](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="2a355-130">An external key to the first column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="2a355-131">Le panneau s’affiche uniquement si cette fonctionnalité est en cours d’installation.</span><span class="sxs-lookup"><span data-stu-id="2a355-131">The billboard is displayed only if this feature is being installed.</span></span>

</dd> <dt>

<span data-ttu-id="2a355-132"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Transactionnel</span><span class="sxs-lookup"><span data-stu-id="2a355-132"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="2a355-133">Nom d’une action.</span><span class="sxs-lookup"><span data-stu-id="2a355-133">The name of an action.</span></span> <span data-ttu-id="2a355-134">Le panneau s’affiche pendant les messages de progression reçus de cette action.</span><span class="sxs-lookup"><span data-stu-id="2a355-134">The billboard is displayed during the progress messages received from this action.</span></span>

</dd> <dt>

<span data-ttu-id="2a355-135"><span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Commandé</span><span class="sxs-lookup"><span data-stu-id="2a355-135"><span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Ordering</span></span>
</dt> <dd>

<span data-ttu-id="2a355-136">Si plusieurs panneaux d’affichage correspondent à une action, ils sont affichés dans l’ordre défini par cette colonne.</span><span class="sxs-lookup"><span data-stu-id="2a355-136">If there is more than one billboard corresponding to an action, then they are displayed in the order defined by this column.</span></span> <span data-ttu-id="2a355-137">Ce nombre ne doit pas être négatif.</span><span class="sxs-lookup"><span data-stu-id="2a355-137">This number must be non-negative.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="2a355-138">Validation</span><span class="sxs-lookup"><span data-stu-id="2a355-138">Validation</span></span>

<dl>

[<span data-ttu-id="2a355-139">ICE03</span><span class="sxs-lookup"><span data-stu-id="2a355-139">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="2a355-140">ICE06</span><span class="sxs-lookup"><span data-stu-id="2a355-140">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="2a355-141">ICE32</span><span class="sxs-lookup"><span data-stu-id="2a355-141">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="2a355-142">ICE95</span><span class="sxs-lookup"><span data-stu-id="2a355-142">ICE95</span></span>](ice95.md)  
</dl>

 

 



