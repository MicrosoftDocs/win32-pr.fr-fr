---
title: Message EM_FINDTEXTW (RichEdit. h)
description: Recherche du texte Unicode dans un contrôle RichEdit.
ms.assetid: 0c1579f5-3b37-4e28-86a2-f4e03e195f38
keywords:
- EM_FINDTEXTW les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_FINDTEXTW
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73e8bae60269ab3ddb84a17c285c243e00d8117c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742828"
---
# <a name="em_findtextw-message"></a><span data-ttu-id="38c64-104">\_Message FINDTEXTW em</span><span class="sxs-lookup"><span data-stu-id="38c64-104">EM\_FINDTEXTW message</span></span>

<span data-ttu-id="38c64-105">Recherche du texte Unicode dans un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="38c64-105">Finds Unicode text within a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="38c64-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="38c64-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38c64-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="38c64-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38c64-108">Spécifie les paramètres de l’opération de recherche.</span><span class="sxs-lookup"><span data-stu-id="38c64-108">Specifies the parameters of the search operation.</span></span> <span data-ttu-id="38c64-109">Ce paramètre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="38c64-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="38c64-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="38c64-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="38c64-111">Signification</span><span class="sxs-lookup"><span data-stu-id="38c64-111">Meaning</span></span>                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <span data-ttu-id="38c64-112"><dt>**FR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="38c64-112"><dt>**FR\_DOWN**</dt></span></span> </dl>                               | <span data-ttu-id="38c64-113">Si cette option est définie, l’opération recherche à partir de la fin de la sélection actuelle jusqu’à la fin du document.</span><span class="sxs-lookup"><span data-stu-id="38c64-113">If set, the operation searches from the end of the current selection to the end of the document.</span></span> <span data-ttu-id="38c64-114">Si la valeur n’est pas définie, l’opération recherche à partir de la fin de la sélection actuelle jusqu’au début du document.</span><span class="sxs-lookup"><span data-stu-id="38c64-114">If not set, the operation searches from the end of the current selection to the beginning of the document.</span></span><br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <span data-ttu-id="38c64-115"><dt>**le \_ MATCHALEFHAMZA**</dt></span><span class="sxs-lookup"><span data-stu-id="38c64-115"><dt>**FR\_MATCHALEFHAMZA**</dt></span></span> </dl> | <span data-ttu-id="38c64-116">Par défaut, les alefs arabe et hébreu avec des accents différents sont tous mis en correspondance par le caractère Alef.</span><span class="sxs-lookup"><span data-stu-id="38c64-116">By default, Arabic and Hebrew alefs with different accents are all matched by the alef character.</span></span> <span data-ttu-id="38c64-117">Définissez cet indicateur si vous souhaitez que la recherche fasse la distinction entre les alefs et les accents différents.</span><span class="sxs-lookup"><span data-stu-id="38c64-117">Set this flag if you want the search to differentiate between alefs with different accents.</span></span><br/>               |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <span data-ttu-id="38c64-118"><dt>**FR \_ RespecterCasse**</dt></span><span class="sxs-lookup"><span data-stu-id="38c64-118"><dt>**FR\_MATCHCASE**</dt></span></span> </dl>                | <span data-ttu-id="38c64-119">Si cette valeur est définie, l’opération de recherche respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="38c64-119">If set, the search operation is case-sensitive.</span></span> <span data-ttu-id="38c64-120">Si la valeur n’est pas définie, l’opération de recherche n’est pas sensible à la casse.</span><span class="sxs-lookup"><span data-stu-id="38c64-120">If not set, the search operation is case-insensitive.</span></span><br/>                                                                                                       |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <span data-ttu-id="38c64-121"><dt>**\_MATCHDIAC fr**</dt></span><span class="sxs-lookup"><span data-stu-id="38c64-121"><dt>**FR\_MATCHDIAC**</dt></span></span> </dl>                | <span data-ttu-id="38c64-122">Par défaut, les marques diacritiques arabe et hébreu sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="38c64-122">By default, Arabic and Hebrew diacritical marks are ignored.</span></span> <span data-ttu-id="38c64-123">Définissez cet indicateur si vous souhaitez que l’opération de recherche examine les signes diacritiques.</span><span class="sxs-lookup"><span data-stu-id="38c64-123">Set this flag if you want the search operation to consider diacritical marks.</span></span><br/>                                                                  |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <span data-ttu-id="38c64-124"><dt>**FR \_ MATCHKASHIDA**</dt></span><span class="sxs-lookup"><span data-stu-id="38c64-124"><dt>**FR\_MATCHKASHIDA**</dt></span></span> </dl>       | <span data-ttu-id="38c64-125">Par défaut, les kachidés arabe et hébreu sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="38c64-125">By default, Arabic and Hebrew kashidas are ignored.</span></span> <span data-ttu-id="38c64-126">Définissez cet indicateur si vous souhaitez que l’opération de recherche examine les signes kachidé.</span><span class="sxs-lookup"><span data-stu-id="38c64-126">Set this flag if you want the search operation to consider kashidas.</span></span><br/>                                                                                    |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <span data-ttu-id="38c64-127"><dt>**\_WHOLEWORD fr**</dt></span><span class="sxs-lookup"><span data-stu-id="38c64-127"><dt>**FR\_WHOLEWORD**</dt></span></span> </dl>                | <span data-ttu-id="38c64-128">Si elle est définie, l’opération recherche uniquement les mots entiers qui correspondent à la chaîne recherchée.</span><span class="sxs-lookup"><span data-stu-id="38c64-128">If set, the operation searches only for whole words that match the search string.</span></span> <span data-ttu-id="38c64-129">Si la valeur n’est pas définie, l’opération recherche également des fragments de mot qui correspondent à la chaîne recherchée.</span><span class="sxs-lookup"><span data-stu-id="38c64-129">If not set, the operation also searches for word fragments that match the search string.</span></span><br/>                                  |



 

</dd> <dt>

<span data-ttu-id="38c64-130">*lParam*</span><span class="sxs-lookup"><span data-stu-id="38c64-130">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38c64-131">Structure [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) contenant des informations sur l’opération de recherche.</span><span class="sxs-lookup"><span data-stu-id="38c64-131">A [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) structure containing information about the find operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38c64-132">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="38c64-132">Return value</span></span>

<span data-ttu-id="38c64-133">Si la chaîne cible est trouvée, la valeur de retour est la position de base zéro du premier caractère de la correspondance.</span><span class="sxs-lookup"><span data-stu-id="38c64-133">If the target string is found, the return value is the zero-based position of the first character of the match.</span></span> <span data-ttu-id="38c64-134">Si la cible est introuvable, la valeur de retour est-1.</span><span class="sxs-lookup"><span data-stu-id="38c64-134">If the target is not found, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="38c64-135">Notes</span><span class="sxs-lookup"><span data-stu-id="38c64-135">Remarks</span></span>

<span data-ttu-id="38c64-136">**Em \_ FINDTEXTW** utilise la structure [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) , tandis que [**em \_ FINDTEXTEXW**](em-findtextexw.md) utilise la structure [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) .</span><span class="sxs-lookup"><span data-stu-id="38c64-136">**EM\_FINDTEXTW** uses the [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) structure, while [**EM\_FINDTEXTEXW**](em-findtextexw.md) uses the [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure.</span></span> <span data-ttu-id="38c64-137">La différence est que **FINDTEXTEXW** renvoie la plage de texte qui a été trouvée.</span><span class="sxs-lookup"><span data-stu-id="38c64-137">The difference is that **FINDTEXTEXW** reports back the range of text that was found.</span></span>

## <a name="requirements"></a><span data-ttu-id="38c64-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="38c64-138">Requirements</span></span>



| <span data-ttu-id="38c64-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="38c64-139">Requirement</span></span> | <span data-ttu-id="38c64-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="38c64-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="38c64-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38c64-141">Minimum supported client</span></span><br/> | <span data-ttu-id="38c64-142">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="38c64-142">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="38c64-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38c64-143">Minimum supported server</span></span><br/> | <span data-ttu-id="38c64-144">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="38c64-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="38c64-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="38c64-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="38c64-146"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="38c64-146"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38c64-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38c64-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38c64-148">**\_FINDTEXTEXW em**</span><span class="sxs-lookup"><span data-stu-id="38c64-148">**EM\_FINDTEXTEXW**</span></span>](em-findtextexw.md)
</dt> </dl>

 

 





