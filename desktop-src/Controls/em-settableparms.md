---
title: Message EM_SETTABLEPARMS (RichEdit. h)
description: Modifie les paramètres des lignes d’une table.
ms.assetid: 6CE9B8D1-68C9-4692-8454-24BC81E9038F
keywords:
- EM_SETTABLEPARMS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETTABLEPARMS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86fa77774bd7fcf461fc74b479a57304a5f8ee3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941959"
---
# <a name="em_settableparms-message"></a><span data-ttu-id="78dc7-104">\_Message SETTABLEPARMS em</span><span class="sxs-lookup"><span data-stu-id="78dc7-104">EM\_SETTABLEPARMS message</span></span>

<span data-ttu-id="78dc7-105">Modifie les paramètres des lignes d’une table.</span><span class="sxs-lookup"><span data-stu-id="78dc7-105">Changes the parameters of rows in a table.</span></span>

## <a name="parameters"></a><span data-ttu-id="78dc7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="78dc7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78dc7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="78dc7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78dc7-108">Pointeur vers une structure [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) .</span><span class="sxs-lookup"><span data-stu-id="78dc7-108">A pointer to a [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure.</span></span>

</dd> <dt>

<span data-ttu-id="78dc7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="78dc7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78dc7-110">Pointeur vers une structure [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) .</span><span class="sxs-lookup"><span data-stu-id="78dc7-110">A pointer to a [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78dc7-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="78dc7-111">Return value</span></span>

<span data-ttu-id="78dc7-112">Retourne S \_ OK en cas de réussite, ou l’un des codes d’erreur suivants.</span><span class="sxs-lookup"><span data-stu-id="78dc7-112">Returns S\_OK if successful, or one of the following error codes.</span></span>



| <span data-ttu-id="78dc7-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="78dc7-113">Return code</span></span>                                                                                    | <span data-ttu-id="78dc7-114">Description</span><span class="sxs-lookup"><span data-stu-id="78dc7-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="78dc7-115"><dt>**E \_ ÉCHEC**</dt></span><span class="sxs-lookup"><span data-stu-id="78dc7-115"><dt>**E\_FAIL** </dt></span></span> </dl>        | <span data-ttu-id="78dc7-116">Les modifications ne peuvent pas être effectuées.</span><span class="sxs-lookup"><span data-stu-id="78dc7-116">Changes cannot be made.</span></span> <span data-ttu-id="78dc7-117">Cela peut se produire si le contrôle est un contrôle de texte brut ou une seule ligne, ou si le point d’insertion se trouve à l’intérieur d’un objet mathématique.</span><span class="sxs-lookup"><span data-stu-id="78dc7-117">This can occur if the control is a plain-text or single-line control, or if the insertion point is inside a math object.</span></span> <span data-ttu-id="78dc7-118">Elle se produit également si les tables sont désactivées, ou si le message [**\_ SETEDITSTYLEEX em**](em-seteditstyleex.md) définit la valeur sa **\_ ex \_ table** .</span><span class="sxs-lookup"><span data-stu-id="78dc7-118">It also occurs if tables are disabled, or if the [**EM\_SETEDITSTYLEEX**](em-seteditstyleex.md) message sets the **SES\_EX\_NOTABLE** value.</span></span> <br/>                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="78dc7-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="78dc7-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="78dc7-120">*WParam* ou *lParam* a la valeur null ou pointe vers une structure non valide.</span><span class="sxs-lookup"><span data-stu-id="78dc7-120">The *wParam* or *lParam* is NULL or points to an invalid structure.</span></span> <span data-ttu-id="78dc7-121">Le membre **cCell** de la structure [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) doit être au moins égal à 1 et inférieur à 63.</span><span class="sxs-lookup"><span data-stu-id="78dc7-121">The **cCell** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure must be at least 1 and not more than 63.</span></span> <span data-ttu-id="78dc7-122">Le membre **cbRow** doit être égal à `sizeof(TABLEROWPARMS)` ou `sizeof(TABLEROWPARMS)   2*sizeof(long)` .</span><span class="sxs-lookup"><span data-stu-id="78dc7-122">The **cbRow** member must equal `sizeof(TABLEROWPARMS)` or `sizeof(TABLEROWPARMS)   2*sizeof(long)`.</span></span> <span data-ttu-id="78dc7-123">La dernière valeur est la taille de la structure **TABLEROWPARMS** RichEdit 4,1.</span><span class="sxs-lookup"><span data-stu-id="78dc7-123">The latter value is the size of the RichEdit 4.1 **TABLEROWPARMS** structure.</span></span> <span data-ttu-id="78dc7-124">Le membre **cbCell** de **TABLEROWPARMS** doit être égal à `sizeof(TABLECELLPARMS)` .</span><span class="sxs-lookup"><span data-stu-id="78dc7-124">The **cbCell** member of **TABLEROWPARMS** must equal `sizeof(TABLECELLPARMS)`.</span></span> <span data-ttu-id="78dc7-125">Le point d’insertion doit être au début d’une table ou à l’intérieur d’une ligne de table, et le nombre de cellules ne peut être modifié que par un seul.</span><span class="sxs-lookup"><span data-stu-id="78dc7-125">The insertion point must be at the start of a table or inside a table row, and the number of cells can only change by one.</span></span> |
| <dl> <span data-ttu-id="78dc7-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="78dc7-126"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl> | <span data-ttu-id="78dc7-127">La mémoire disponible est insuffisante.</span><span class="sxs-lookup"><span data-stu-id="78dc7-127">Insufficient memory is available.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="78dc7-128">Notes</span><span class="sxs-lookup"><span data-stu-id="78dc7-128">Remarks</span></span>

<span data-ttu-id="78dc7-129">Ce message modifie les paramètres du nombre de lignes spécifié par le membre **cRow** de la structure [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) , si la table contient ce nombre de lignes consécutives.</span><span class="sxs-lookup"><span data-stu-id="78dc7-129">This message changes the parameters of the number of rows specified by the **cRow** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure, if the table has that many consecutive rows.</span></span> <span data-ttu-id="78dc7-130">Si **cRow** est inférieur à 0, le message itère jusqu’à la fin de la table.</span><span class="sxs-lookup"><span data-stu-id="78dc7-130">If **cRow** is less than 0, the message iterates until the end of the table.</span></span> <span data-ttu-id="78dc7-131">Si le nombre de cellules diffère du nombre de cellules actuel par + 1 ou 1, il insère ou supprime la cellule à l’index spécifié par le membre **iCell** de **TABLEROWPARMS**.</span><span class="sxs-lookup"><span data-stu-id="78dc7-131">If the new cell count differs from the current cell count by +1 or  1, it inserts or deletes the cell at the index specified by the **iCell** member of **TABLEROWPARMS**.</span></span> <span data-ttu-id="78dc7-132">La ligne de départ du tableau est identifiée par une position de caractère.</span><span class="sxs-lookup"><span data-stu-id="78dc7-132">The starting table row is identified by a character position.</span></span> <span data-ttu-id="78dc7-133">Cette position est spécifiée par les membres **cpStartRow** dont les valeurs sont supérieures ou égales à zéro.</span><span class="sxs-lookup"><span data-stu-id="78dc7-133">This position is specified by **cpStartRow** members with values that are greater than or equal to zero.</span></span> <span data-ttu-id="78dc7-134">La position doit se trouver à l’intérieur de la ligne de la table, mais pas à l’intérieur d’une table imbriquée, sauf si vous souhaitez modifier les paramètres de la table s.</span><span class="sxs-lookup"><span data-stu-id="78dc7-134">The position should be inside the table row, but not inside a nested table, unless you want to change that table s parameters.</span></span> <span data-ttu-id="78dc7-135">Si le membre **cpStartRow** est 1, la position du caractère est donnée par la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="78dc7-135">If the **cpStartRow** member is  1, the character position is given by the current selection.</span></span> <span data-ttu-id="78dc7-136">Pour ce faire, placez la sélection n’importe où dans la ligne de la table ou sélectionnez la ligne contenant l’extrémité active de la sélection à la fin de la ligne du tableau.</span><span class="sxs-lookup"><span data-stu-id="78dc7-136">For this, position the selection anywhere inside the table row, or select the row with the active end of the selection at the end of the table row.</span></span>

## <a name="requirements"></a><span data-ttu-id="78dc7-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="78dc7-137">Requirements</span></span>



| <span data-ttu-id="78dc7-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="78dc7-138">Requirement</span></span> | <span data-ttu-id="78dc7-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="78dc7-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="78dc7-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78dc7-140">Minimum supported client</span></span><br/> | <span data-ttu-id="78dc7-141">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="78dc7-141">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="78dc7-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78dc7-142">Minimum supported server</span></span><br/> | <span data-ttu-id="78dc7-143">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="78dc7-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="78dc7-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="78dc7-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="78dc7-145"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="78dc7-145"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78dc7-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78dc7-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78dc7-147">**\_GETTABLEPARMS em**</span><span class="sxs-lookup"><span data-stu-id="78dc7-147">**EM\_GETTABLEPARMS**</span></span>](em-gettableparms.md)
</dt> </dl>

 

 





