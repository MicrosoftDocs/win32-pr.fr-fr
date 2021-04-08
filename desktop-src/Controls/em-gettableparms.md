---
title: Message EM_GETTABLEPARMS (RichEdit. h)
description: Récupère les paramètres de table pour une ligne de table et les paramètres de cellule pour le nombre spécifié de cellules.
ms.assetid: 36ADA41B-735B-4D6E-92B1-33260C71DF73
keywords:
- EM_GETTABLEPARMS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETTABLEPARMS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7eb244b64258b1cf83559e21affea51b1d0c5d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843482"
---
# <a name="em_gettableparms-message"></a><span data-ttu-id="42c98-104">\_Message GETTABLEPARMS em</span><span class="sxs-lookup"><span data-stu-id="42c98-104">EM\_GETTABLEPARMS message</span></span>

<span data-ttu-id="42c98-105">Récupère les paramètres de table pour une ligne de table et les paramètres de cellule pour le nombre spécifié de cellules.</span><span class="sxs-lookup"><span data-stu-id="42c98-105">Retrieves the table parameters for a table row and the cell parameters for the specified number of cells.</span></span>


```C++
#define EM_GETTABLEPARMS       (WM_USER + 265)
```



## <a name="parameters"></a><span data-ttu-id="42c98-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="42c98-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42c98-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="42c98-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42c98-108">Pointeur vers une structure [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) .</span><span class="sxs-lookup"><span data-stu-id="42c98-108">A pointer to a [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure.</span></span>

</dd> <dt>

<span data-ttu-id="42c98-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="42c98-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42c98-110">Pointeur vers une structure [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) .</span><span class="sxs-lookup"><span data-stu-id="42c98-110">A pointer to a [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42c98-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="42c98-111">Return value</span></span>

<span data-ttu-id="42c98-112">Retourne S \_ OK en cas de réussite, ou l’un des codes d’erreur suivants.</span><span class="sxs-lookup"><span data-stu-id="42c98-112">Returns S\_OK if successful, or one of the following error codes.</span></span>



| <span data-ttu-id="42c98-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="42c98-113">Return code</span></span>                                                                                    | <span data-ttu-id="42c98-114">Description</span><span class="sxs-lookup"><span data-stu-id="42c98-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="42c98-115"><dt>**E \_ ÉCHEC**</dt></span><span class="sxs-lookup"><span data-stu-id="42c98-115"><dt>**E\_FAIL** </dt></span></span> </dl>        | <span data-ttu-id="42c98-116">Les modifications ne peuvent pas être effectuées.</span><span class="sxs-lookup"><span data-stu-id="42c98-116">Changes cannot be made.</span></span> <span data-ttu-id="42c98-117">Cela peut se produire si le contrôle est un contrôle de texte brut ou une seule ligne, ou si le point d’insertion se trouve à l’intérieur d’un objet mathématique.</span><span class="sxs-lookup"><span data-stu-id="42c98-117">This can occur if the control is a plain-text or single-line control, or if the insertion point is inside a math object.</span></span> <span data-ttu-id="42c98-118">Elle se produit également si les tables sont désactivées si le message [**\_ SETEDITSTYLEEX em**](em-seteditstyleex.md) définit la valeur sa **\_ ex \_ table** .</span><span class="sxs-lookup"><span data-stu-id="42c98-118">It also occurs if tables are disabled if the [**EM\_SETEDITSTYLEEX**](em-seteditstyleex.md) message sets the **SES\_EX\_NOTABLE** value.</span></span> <br/>                                                                                                                                                                     |
| <dl> <span data-ttu-id="42c98-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="42c98-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="42c98-120">*WParam* ou *lParam* a la valeur null ou pointe vers une structure non valide.</span><span class="sxs-lookup"><span data-stu-id="42c98-120">The *wParam* or *lParam* is NULL or points to an invalid structure.</span></span> <span data-ttu-id="42c98-121">Le membre **cbRow** de la structure [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) doit être égal à `sizeof(TABLEROWPARMS)` ou sizeof (TABLEROWPARMS) 2 \* sizeof (long).</span><span class="sxs-lookup"><span data-stu-id="42c98-121">The **cbRow** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure must equal `sizeof(TABLEROWPARMS)` or sizeof(TABLEROWPARMS)   2\*sizeof(long).</span></span> <span data-ttu-id="42c98-122">La dernière valeur est la taille de la structure **TABLEROWPARMS** RichEdit 4,1.</span><span class="sxs-lookup"><span data-stu-id="42c98-122">The latter value is the size of the RichEdit 4.1 **TABLEROWPARMS** structure.</span></span> <span data-ttu-id="42c98-123">Le membre **cbCell** de la structure **TABLEROWPARMS** doit être égal à `sizeof(TABLECELLPARMS)` .</span><span class="sxs-lookup"><span data-stu-id="42c98-123">The **cbCell** member of the **TABLEROWPARMS** structure must equal `sizeof(TABLECELLPARMS)`.</span></span> <span data-ttu-id="42c98-124">La position du caractère de requête doit être au niveau d’un délimiteur de ligne de table.</span><span class="sxs-lookup"><span data-stu-id="42c98-124">The query character position must be at a table row delimiter.</span></span> |
| <dl> <span data-ttu-id="42c98-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="42c98-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl> | <span data-ttu-id="42c98-126">La mémoire disponible est insuffisante.</span><span class="sxs-lookup"><span data-stu-id="42c98-126">Insufficient memory is available.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="42c98-127">Notes</span><span class="sxs-lookup"><span data-stu-id="42c98-127">Remarks</span></span>

<span data-ttu-id="42c98-128">Ce message obtient les paramètres de table pour la ligne à la position de caractère spécifiée par le membre **cpStartRow** de la structure [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) , ainsi que le nombre de cellules spécifié par le membre **cCells** de la structure [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) .</span><span class="sxs-lookup"><span data-stu-id="42c98-128">This message gets the table parameters for the row at the character position specified by the **cpStartRow** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure, and the number of cells specified by the **cCells** member of the [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) structure.</span></span>

<span data-ttu-id="42c98-129">La position du caractère spécifiée par le membre **cpStartRow** de la structure [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) doit se trouver au début de la ligne de la table ou au délimiteur de fin de la ligne de la table.</span><span class="sxs-lookup"><span data-stu-id="42c98-129">The character position specified by the **cpStartRow** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure should be at the start of the table row, or at the end delimiter of the table row.</span></span> <span data-ttu-id="42c98-130">Si **cpStartRow** a la valeur 1, la position du caractère est donnée par la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="42c98-130">If **cpStartRow** is set to  1, the character position is given by the current selection.</span></span> <span data-ttu-id="42c98-131">Dans ce cas, positionnez la sélection à la fin de la ligne (entre la marque de cellule et le délimiteur de fin de la ligne de table), ou sélectionnez la ligne.</span><span class="sxs-lookup"><span data-stu-id="42c98-131">In this case, position the selection at the end of the row (between the cell mark and the end delimiter of the table row), or select the row.</span></span>

## <a name="requirements"></a><span data-ttu-id="42c98-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42c98-132">Requirements</span></span>



| <span data-ttu-id="42c98-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42c98-133">Requirement</span></span> | <span data-ttu-id="42c98-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="42c98-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="42c98-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42c98-135">Minimum supported client</span></span><br/> | <span data-ttu-id="42c98-136">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42c98-136">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="42c98-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42c98-137">Minimum supported server</span></span><br/> | <span data-ttu-id="42c98-138">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42c98-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="42c98-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="42c98-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="42c98-140"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="42c98-140"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42c98-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42c98-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42c98-142">**\_SETTABLEPARMS em**</span><span class="sxs-lookup"><span data-stu-id="42c98-142">**EM\_SETTABLEPARMS**</span></span>](em-settableparms.md)
</dt> </dl>

 

 





