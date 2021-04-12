---
title: Message EM_INSERTTABLE (RichEdit. h)
description: Insère une ou plusieurs lignes de table identiques avec des cellules vides.
ms.assetid: 7F9B2F28-1035-44AA-9DF6-57BC62886A4E
keywords:
- EM_INSERTTABLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_INSERTTABLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fea5de278df98e412f219d246164221cfea75255
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464534"
---
# <a name="em_inserttable-message"></a><span data-ttu-id="64c40-104">\_Message INSERTTABLE em</span><span class="sxs-lookup"><span data-stu-id="64c40-104">EM\_INSERTTABLE message</span></span>

<span data-ttu-id="64c40-105">Insère une ou plusieurs lignes de table identiques avec des cellules vides.</span><span class="sxs-lookup"><span data-stu-id="64c40-105">Inserts one or more identical table rows with empty cells.</span></span>


```C++
#define EM_INSERTTABLE       (WM_USER + 232)
```



## <a name="parameters"></a><span data-ttu-id="64c40-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="64c40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64c40-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="64c40-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64c40-108">Pointeur vers une structure [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) .</span><span class="sxs-lookup"><span data-stu-id="64c40-108">A pointer to a [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure.</span></span>

</dd> <dt>

<span data-ttu-id="64c40-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="64c40-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64c40-110">Pointeur vers une structure [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) .</span><span class="sxs-lookup"><span data-stu-id="64c40-110">A pointer to a [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64c40-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="64c40-111">Return value</span></span>

<span data-ttu-id="64c40-112">Retourne S \_ OK si la table est insérée ou un code d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="64c40-112">Returns S\_OK if the table is inserted, or an error code if not.</span></span>

## <a name="remarks"></a><span data-ttu-id="64c40-113">Notes</span><span class="sxs-lookup"><span data-stu-id="64c40-113">Remarks</span></span>

<span data-ttu-id="64c40-114">Si le membre **cpStartRow** du [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) est 1, ce message supprime le texte sélectionné (le cas échéant), puis insère les lignes de table vides avec les paramètres de ligne et de cellule donnés par *wParam* et *lParam*.</span><span class="sxs-lookup"><span data-stu-id="64c40-114">If the **cpStartRow** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) is  1, this message deletes the selected text (if any), and then inserts empty table rows with the row and cell parameters given by *wParam* and *lParam*.</span></span> <span data-ttu-id="64c40-115">Elle laisse la sélection pointant vers le début de la première cellule de la première ligne.</span><span class="sxs-lookup"><span data-stu-id="64c40-115">It leaves the selection pointing to the start of the first cell in the first row.</span></span> <span data-ttu-id="64c40-116">Le client peut ensuite remplir les cellules de la table en pointant la sélection (ou un [**ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange)) sur les différentes marques de fin de cellule et en insérant et en mettant en forme le texte souhaité.</span><span class="sxs-lookup"><span data-stu-id="64c40-116">The client can then populate the table cells by pointing the selection (or an [**ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange)) to the various cell end marks and inserting and formatting the desired text.</span></span> <span data-ttu-id="64c40-117">Ce type de texte peut inclure des lignes de table imbriquée.</span><span class="sxs-lookup"><span data-stu-id="64c40-117">Such text can include nested table rows.</span></span> <span data-ttu-id="64c40-118">Sinon, si le membre **cpStartRow** du **TABLEROWPARMS** est supérieur ou égal à 0, les lignes de la table sont insérées à la position de caractère donnée par **cpStartRow**.</span><span class="sxs-lookup"><span data-stu-id="64c40-118">Alternatively, if the **cpStartRow** member of the **TABLEROWPARMS** is 0 or greater, table rows are inserted at the character position given by **cpStartRow**.</span></span> <span data-ttu-id="64c40-119">Cela modifie uniquement la sélection actuelle si la table est insérée à l’intérieur du texte sélectionné.</span><span class="sxs-lookup"><span data-stu-id="64c40-119">This only changes the current selection if the table is inserted inside the selected text.</span></span>

<span data-ttu-id="64c40-120">Une table RichEdit Microsoft se compose d’une séquence de lignes de table qui, à leur tour, est composée de séquences de paragraphes.</span><span class="sxs-lookup"><span data-stu-id="64c40-120">A Microsoft Rich Edit table consists of a sequence of table rows which, in turn, consist of sequences of paragraphs.</span></span> <span data-ttu-id="64c40-121">Une ligne de table commence par le point de délimiteur de deux caractères spécial U + FFF9 U + 000D et se termine par le point d’arrêt à deux caractères U + FFFB U + 000D.</span><span class="sxs-lookup"><span data-stu-id="64c40-121">A table row starts with the special two-character delimiter paragraph U+FFF9 U+000D and ends with the two-character delimiter paragraph U+FFFB U+000D.</span></span> <span data-ttu-id="64c40-122">Chaque cellule se termine par la marque de cellule U + 0007, qui est traitée comme une marque de fin de paragraphe dure exactement comme U + 000D (CR) est.</span><span class="sxs-lookup"><span data-stu-id="64c40-122">Each cell is terminated by the cell mark U+0007, which is treated as a hard end-of-paragraph mark just as U+000D (CR) is.</span></span> <span data-ttu-id="64c40-123">Les paramètres de ligne de table et de cellule sont traités comme une mise en forme spéciale des paragraphes des séparateurs de lignes de table.</span><span class="sxs-lookup"><span data-stu-id="64c40-123">The table row and cell parameters are treated as special paragraph formatting of the table-row delimiters.</span></span> <span data-ttu-id="64c40-124">La mise en forme contient les informations dans la structure [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) .</span><span class="sxs-lookup"><span data-stu-id="64c40-124">The formatting contains the information in the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure.</span></span> <span data-ttu-id="64c40-125">Les paramètres de cellule fournis par la structure [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) sont stockés dans une version développée du tableau Tabs.</span><span class="sxs-lookup"><span data-stu-id="64c40-125">The cell parameters given by the [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) structure are stored in an expanded version of the tabs array.</span></span> <span data-ttu-id="64c40-126">Ce format permet d’imbriquer des tables dans d’autres tables, jusqu’à quinze niveaux de profondeur.</span><span class="sxs-lookup"><span data-stu-id="64c40-126">This format allows tables to be nested within other tables, up to fifteen levels deep.</span></span>

## <a name="requirements"></a><span data-ttu-id="64c40-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64c40-127">Requirements</span></span>



| <span data-ttu-id="64c40-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="64c40-128">Requirement</span></span> | <span data-ttu-id="64c40-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="64c40-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="64c40-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="64c40-130">Minimum supported client</span></span><br/> | <span data-ttu-id="64c40-131">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="64c40-131">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="64c40-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="64c40-132">Minimum supported server</span></span><br/> | <span data-ttu-id="64c40-133">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="64c40-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="64c40-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="64c40-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="64c40-135"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="64c40-135"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64c40-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64c40-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64c40-137">**\_INSERTIMAGE em**</span><span class="sxs-lookup"><span data-stu-id="64c40-137">**EM\_INSERTIMAGE**</span></span>](em-insertimage.md)
</dt> </dl>

 

 





