---
title: Message EM_FINDTEXTEXW (RichEdit. h)
description: 'EM_FINDTEXTEXW message : recherche le texte Unicode dans un contrôle RichEdit.'
ms.assetid: 7b90ef06-0395-430e-8b5d-b392481a5f70
keywords:
- EM_FINDTEXTEXW les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_FINDTEXTEXW
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5278726ca4d3e4748e96d8095a411bcebd5637ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109807"
---
# <a name="em_findtextexw-message"></a><span data-ttu-id="dd0e3-104">\_Message FINDTEXTEXW em</span><span class="sxs-lookup"><span data-stu-id="dd0e3-104">EM\_FINDTEXTEXW message</span></span>

<span data-ttu-id="dd0e3-105">Recherche du texte Unicode dans un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="dd0e3-105">Finds Unicode text within a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="dd0e3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd0e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd0e3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dd0e3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dd0e3-108">Spécifie le comportement de l’opération de recherche.</span><span class="sxs-lookup"><span data-stu-id="dd0e3-108">Specifies the behavior of the search operation.</span></span> <span data-ttu-id="dd0e3-109">Ce paramètre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="dd0e3-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="dd0e3-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd0e3-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="dd0e3-111">Signification</span><span class="sxs-lookup"><span data-stu-id="dd0e3-111">Meaning</span></span>                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <span data-ttu-id="dd0e3-112"><dt>**FR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dd0e3-112"><dt>**FR\_DOWN**</dt></span></span> </dl>                               | <span data-ttu-id="dd0e3-113">Microsoft Rich Edit 2,0 et versions ultérieures : si cette valeur est définie, la recherche est effectuée vers l’avant à partir de **FINDTEXTEX. frais. cpMin**; Si la valeur n’est pas définie, la recherche est vers l’arrière à partir de **FINDTEXTEX. frais. cpMin**.</span><span class="sxs-lookup"><span data-stu-id="dd0e3-113">Microsoft Rich Edit 2.0 and later: If set, the search is forward from **FINDTEXTEX.chrg.cpMin**; if not set, the search is backward from **FINDTEXTEX.chrg.cpMin**.</span></span> <br/> <span data-ttu-id="dd0e3-114">Édition enrichie de Microsoft 1,0 : l' \_ indicateur fr vers le PG. est ignoré.</span><span class="sxs-lookup"><span data-stu-id="dd0e3-114">Microsoft Rich Edit 1.0: The FR\_DOWN flag is ignored.</span></span> <span data-ttu-id="dd0e3-115">La recherche est toujours Forward.</span><span class="sxs-lookup"><span data-stu-id="dd0e3-115">The search is always forward.</span></span><br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <span data-ttu-id="dd0e3-116"><dt>**le \_ MATCHALEFHAMZA**</dt></span><span class="sxs-lookup"><span data-stu-id="dd0e3-116"><dt>**FR\_MATCHALEFHAMZA**</dt></span></span> </dl> | <span data-ttu-id="dd0e3-117">Si cette valeur est définie, la recherche fait la distinction entre les alefs avec des accents différents.</span><span class="sxs-lookup"><span data-stu-id="dd0e3-117">If set, the search differentiates between alefs with different accents.</span></span> <span data-ttu-id="dd0e3-118">S’il n’est pas défini, les alefs en arabe et en Hébreu avec des accents différents sont tous mis en correspondance par le caractère Alef.</span><span class="sxs-lookup"><span data-stu-id="dd0e3-118">If not set, Arabic and Hebrew alefs with different accents are all matched by the alef character.</span></span> <br/>                                                                                           |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <span data-ttu-id="dd0e3-119"><dt>**FR \_ RespecterCasse**</dt></span><span class="sxs-lookup"><span data-stu-id="dd0e3-119"><dt>**FR\_MATCHCASE**</dt></span></span> </dl>                | <span data-ttu-id="dd0e3-120">Si cette valeur est définie, l’opération de recherche respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="dd0e3-120">If set, the search operation is case-sensitive.</span></span> <span data-ttu-id="dd0e3-121">Si la valeur n’est pas définie, l’opération de recherche n’est pas sensible à la casse.</span><span class="sxs-lookup"><span data-stu-id="dd0e3-121">If not set, the search operation is case-insensitive.</span></span><br/>                                                                                                                                                                |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <span data-ttu-id="dd0e3-122"><dt>**\_MATCHDIAC fr**</dt></span><span class="sxs-lookup"><span data-stu-id="dd0e3-122"><dt>**FR\_MATCHDIAC**</dt></span></span> </dl>                | <span data-ttu-id="dd0e3-123">Si cette valeur est définie, l’opération de recherche prend en compte les signes diacritiques.</span><span class="sxs-lookup"><span data-stu-id="dd0e3-123">If set, the search operation considers diacritical marks.</span></span> <span data-ttu-id="dd0e3-124">S’il n’est pas défini, les marques diacritiques arabe et hébreu sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="dd0e3-124">If not set, Arabic and Hebrew diacritical marks are ignored.</span></span> <br/>                                                                                                                                              |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <span data-ttu-id="dd0e3-125"><dt>**FR \_ MATCHKASHIDA**</dt></span><span class="sxs-lookup"><span data-stu-id="dd0e3-125"><dt>**FR\_MATCHKASHIDA**</dt></span></span> </dl>       | <span data-ttu-id="dd0e3-126">Si cette valeur est définie, l’opération de recherche prend en compte les signes kachidé.</span><span class="sxs-lookup"><span data-stu-id="dd0e3-126">If set, the search operation considers kashidas.</span></span> <span data-ttu-id="dd0e3-127">Si ce n’est pas le cas, les signes arabe et hébreu sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="dd0e3-127">If not set, Arabic and Hebrew kashidas are ignored.</span></span> <br/>                                                                                                                                                                |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <span data-ttu-id="dd0e3-128"><dt>**\_WHOLEWORD fr**</dt></span><span class="sxs-lookup"><span data-stu-id="dd0e3-128"><dt>**FR\_WHOLEWORD**</dt></span></span> </dl>                | <span data-ttu-id="dd0e3-129">Si elle est définie, l’opération recherche uniquement les mots entiers qui correspondent à la chaîne recherchée.</span><span class="sxs-lookup"><span data-stu-id="dd0e3-129">If set, the operation searches only for whole words that match the search string.</span></span> <span data-ttu-id="dd0e3-130">Si la valeur n’est pas définie, l’opération recherche également des fragments de mot qui correspondent à la chaîne recherchée.</span><span class="sxs-lookup"><span data-stu-id="dd0e3-130">If not set, the operation also searches for word fragments that match the search string.</span></span><br/>                                                                                           |



 

</dd> <dt>

<span data-ttu-id="dd0e3-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dd0e3-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dd0e3-132">Structure [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) contenant des informations sur l’opération de recherche.</span><span class="sxs-lookup"><span data-stu-id="dd0e3-132">A [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure containing information about the find operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd0e3-133">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="dd0e3-133">Return value</span></span>

<span data-ttu-id="dd0e3-134">Si la chaîne cible est trouvée, la valeur de retour est la position de base zéro du premier caractère de la correspondance.</span><span class="sxs-lookup"><span data-stu-id="dd0e3-134">If the target string is found, the return value is the zero-based position of the first character of the match.</span></span> <span data-ttu-id="dd0e3-135">Si la cible est introuvable, la valeur de retour est-1.</span><span class="sxs-lookup"><span data-stu-id="dd0e3-135">If the target is not found, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd0e3-136">Notes </span><span class="sxs-lookup"><span data-stu-id="dd0e3-136">Remarks</span></span>

<span data-ttu-id="dd0e3-137">Utilisez ce message pour rechercher des chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="dd0e3-137">Use this message to find Unicode strings.</span></span> <span data-ttu-id="dd0e3-138">Pour ANSI ;, utilisez [**em \_ FINDTEXTEX**](em-findtextex.md).</span><span class="sxs-lookup"><span data-stu-id="dd0e3-138">For ANSI;, use [**EM\_FINDTEXTEX**](em-findtextex.md).</span></span>

<span data-ttu-id="dd0e3-139">Le membre **cpMin** de **FINDTEXTEX.** frais spécifie toujours le point de départ de la recherche, tandis que **cpMax** spécifie le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="dd0e3-139">The **cpMin** member of **FINDTEXTEX.chrg** always specifies the starting-point of the search, and **cpMax** specifies the end point.</span></span> <span data-ttu-id="dd0e3-140">Lorsque vous effectuez une recherche vers l’arrière, **cpMin** doit être supérieur ou égal à **cpMax**.</span><span class="sxs-lookup"><span data-stu-id="dd0e3-140">When searching backward, **cpMin** must be equal to or greater than **cpMax**.</span></span> <span data-ttu-id="dd0e3-141">Lors d’une recherche vers l’avant, la valeur-1 dans **cpMax** étend la plage de recherche à la fin du texte.</span><span class="sxs-lookup"><span data-stu-id="dd0e3-141">When searching forward, a value of -1 in **cpMax** extends the search range to the end of the text.</span></span>

<span data-ttu-id="dd0e3-142">Si l’opération de recherche trouve une correspondance, le membre **chrgText** de la structure [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) retourne la plage de positions de caractères qui contient le texte correspondant.</span><span class="sxs-lookup"><span data-stu-id="dd0e3-142">If the search operation finds a match, the **chrgText** member of the [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure returns the range of character positions that contains the matching text.</span></span>

<span data-ttu-id="dd0e3-143">**Em \_ FINDTEXTEXW** utilise la structure [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) , tandis que [**em \_ FINDTEXTW**](em-findtextw.md) utilise la structure [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) .</span><span class="sxs-lookup"><span data-stu-id="dd0e3-143">**EM\_FINDTEXTEXW** uses the [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure, while [**EM\_FINDTEXTW**](em-findtextw.md) uses the [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) structure.</span></span> <span data-ttu-id="dd0e3-144">La différence est que **em \_ FINDTEXTEXW** signale la plage de texte qui a été trouvée.</span><span class="sxs-lookup"><span data-stu-id="dd0e3-144">The difference is that **EM\_FINDTEXTEXW** reports the range of text that was found.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd0e3-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd0e3-145">Requirements</span></span>



| <span data-ttu-id="dd0e3-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd0e3-146">Requirement</span></span> | <span data-ttu-id="dd0e3-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd0e3-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dd0e3-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd0e3-148">Minimum supported client</span></span><br/> | <span data-ttu-id="dd0e3-149">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dd0e3-149">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dd0e3-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd0e3-150">Minimum supported server</span></span><br/> | <span data-ttu-id="dd0e3-151">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dd0e3-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dd0e3-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="dd0e3-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd0e3-153"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd0e3-153"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd0e3-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd0e3-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd0e3-155">**\_FINDTEXTW em**</span><span class="sxs-lookup"><span data-stu-id="dd0e3-155">**EM\_FINDTEXTW**</span></span>](em-findtextw.md)
</dt> </dl>

 

 





