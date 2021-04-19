---
description: Le tableau de cases à cocher répertorie les valeurs des cases à cocher.
ms.assetid: 6881f358-74af-4160-ac69-36e848865ac0
title: Table de cases à cocher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3600b741543a88e7ded71cd385a56b499c8ef516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544809"
---
# <a name="checkbox-table"></a><span data-ttu-id="27485-103">Table de cases à cocher</span><span class="sxs-lookup"><span data-stu-id="27485-103">CheckBox Table</span></span>

<span data-ttu-id="27485-104">Le tableau de cases à cocher répertorie les valeurs des cases à cocher.</span><span class="sxs-lookup"><span data-stu-id="27485-104">The CheckBox table lists the values for the check boxes.</span></span>

<span data-ttu-id="27485-105">La table de cases à cocher contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="27485-105">The CheckBox table has the following columns.</span></span>



| <span data-ttu-id="27485-106">Colonne</span><span class="sxs-lookup"><span data-stu-id="27485-106">Column</span></span>   | <span data-ttu-id="27485-107">Type</span><span class="sxs-lookup"><span data-stu-id="27485-107">Type</span></span>                         | <span data-ttu-id="27485-108">Clé</span><span class="sxs-lookup"><span data-stu-id="27485-108">Key</span></span> | <span data-ttu-id="27485-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="27485-109">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="27485-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="27485-110">Property</span></span> | [<span data-ttu-id="27485-111">Identificateur</span><span class="sxs-lookup"><span data-stu-id="27485-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="27485-112">O</span><span class="sxs-lookup"><span data-stu-id="27485-112">Y</span></span>   | <span data-ttu-id="27485-113">N</span><span class="sxs-lookup"><span data-stu-id="27485-113">N</span></span>        |
| <span data-ttu-id="27485-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="27485-114">Value</span></span>    | [<span data-ttu-id="27485-115">Correct</span><span class="sxs-lookup"><span data-stu-id="27485-115">Formatted</span></span>](formatted.md)   | <span data-ttu-id="27485-116">N</span><span class="sxs-lookup"><span data-stu-id="27485-116">N</span></span>   | <span data-ttu-id="27485-117">O</span><span class="sxs-lookup"><span data-stu-id="27485-117">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="27485-118">Colonnes</span><span class="sxs-lookup"><span data-stu-id="27485-118">Columns</span></span>

<dl> <dt>

<span data-ttu-id="27485-119"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propriété</span><span class="sxs-lookup"><span data-stu-id="27485-119"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="27485-120">Propriété nommée à être liée à cet élément.</span><span class="sxs-lookup"><span data-stu-id="27485-120">A named property to be tied to this item.</span></span>

</dd> <dt>

<span data-ttu-id="27485-121"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Ajoutée</span><span class="sxs-lookup"><span data-stu-id="27485-121"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="27485-122">Chaîne de valeur associée à cet élément.</span><span class="sxs-lookup"><span data-stu-id="27485-122">The value string associated with this item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="27485-123">Notes</span><span class="sxs-lookup"><span data-stu-id="27485-123">Remarks</span></span>

<span data-ttu-id="27485-124">Si la case à cocher est activée, la propriété correspondante est définie sur la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="27485-124">If the check box is selected, then the corresponding property is set to the specified value.</span></span> <span data-ttu-id="27485-125">Si aucune valeur n’est spécifiée ou si cette table n’existe pas, la propriété est définie sur sa valeur d’origine lorsque la case à cocher est activée.</span><span class="sxs-lookup"><span data-stu-id="27485-125">If there is no value specified or this table does not exist, then the property is set to its original value when the check box is selected.</span></span> <span data-ttu-id="27485-126">Si la valeur d’origine est null, la propriété a la valeur « 1 ».</span><span class="sxs-lookup"><span data-stu-id="27485-126">If the original value is null, the property is set to "1".</span></span>

<span data-ttu-id="27485-127">Le contenu de la colonne de valeur est mis en forme par la fonction [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) lorsque le contrôle est créé.</span><span class="sxs-lookup"><span data-stu-id="27485-127">The contents of the Value column are formatted by the [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) function when the control is created.</span></span> <span data-ttu-id="27485-128">Par conséquent, il peut contenir n’importe quelle expression que la fonction **MsiFormatRecord** peut interpréter.</span><span class="sxs-lookup"><span data-stu-id="27485-128">Therefore, it can contain any expression that the **MsiFormatRecord** function can interpret.</span></span> <span data-ttu-id="27485-129">La colonne de valeur est mise en forme uniquement lorsque le contrôle est créé et n’est pas mise à jour si une propriété impliquée dans une expression est modifiée pendant la durée de vie du contrôle.</span><span class="sxs-lookup"><span data-stu-id="27485-129">The Value column is formatted only when the control is created, and it is not updated if a property involved in an expression is modified during the life of the control.</span></span>

## <a name="validation"></a><span data-ttu-id="27485-130">Validation</span><span class="sxs-lookup"><span data-stu-id="27485-130">Validation</span></span>

<dl>

[<span data-ttu-id="27485-131">ICE03</span><span class="sxs-lookup"><span data-stu-id="27485-131">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="27485-132">ICE06</span><span class="sxs-lookup"><span data-stu-id="27485-132">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="27485-133">ICE46</span><span class="sxs-lookup"><span data-stu-id="27485-133">ICE46</span></span>](ice46.md)  
</dl>

 

 



