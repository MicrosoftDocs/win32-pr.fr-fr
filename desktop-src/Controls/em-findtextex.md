---
title: Message EM_FINDTEXTEX (RichEdit. h)
description: EM_FINDTEXTEX message-recherche du texte dans un contrôle RichEdit.
ms.assetid: f1bf925b-2776-40b8-9d05-8484daf8d989
keywords:
- EM_FINDTEXTEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_FINDTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2158dabf9ea17d1bd4cac48454bdbb4056765752
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109837"
---
# <a name="em_findtextex-message"></a><span data-ttu-id="d66f6-104">\_Message FINDTEXTEX em</span><span class="sxs-lookup"><span data-stu-id="d66f6-104">EM\_FINDTEXTEX message</span></span>

<span data-ttu-id="d66f6-105">Recherche du texte dans un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="d66f6-105">Finds text within a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d66f6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d66f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d66f6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d66f6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d66f6-108">Spécifie le comportement de l’opération de recherche.</span><span class="sxs-lookup"><span data-stu-id="d66f6-108">Specifies the behavior of the search operation.</span></span> <span data-ttu-id="d66f6-109">Ce paramètre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="d66f6-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="d66f6-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="d66f6-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="d66f6-111">Signification</span><span class="sxs-lookup"><span data-stu-id="d66f6-111">Meaning</span></span>                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <span data-ttu-id="d66f6-112"><dt>**FR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d66f6-112"><dt>**FR\_DOWN**</dt></span></span> </dl>                               | <span data-ttu-id="d66f6-113">Microsoft Rich Edit 2,0 et versions ultérieures : si cette valeur est définie, la recherche est effectuée vers l’avant à partir de **FINDTEXTEX. frais. cpMin**; Si la valeur n’est pas définie, la recherche est vers l’arrière à partir de **FINDTEXTEX. frais. cpMin**.</span><span class="sxs-lookup"><span data-stu-id="d66f6-113">Microsoft Rich Edit 2.0 and later: If set, the search is forward from **FINDTEXTEX.chrg.cpMin**; if not set, the search is backward from **FINDTEXTEX.chrg.cpMin**.</span></span> <br/> <span data-ttu-id="d66f6-114">Édition enrichie de Microsoft 1,0 : l' \_ indicateur fr vers le PG. est ignoré.</span><span class="sxs-lookup"><span data-stu-id="d66f6-114">Microsoft Rich Edit 1.0: The FR\_DOWN flag is ignored.</span></span> <span data-ttu-id="d66f6-115">La recherche est toujours Forward.</span><span class="sxs-lookup"><span data-stu-id="d66f6-115">The search is always forward.</span></span><br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <span data-ttu-id="d66f6-116"><dt>**le \_ MATCHALEFHAMZA**</dt></span><span class="sxs-lookup"><span data-stu-id="d66f6-116"><dt>**FR\_MATCHALEFHAMZA**</dt></span></span> </dl> | <span data-ttu-id="d66f6-117">Microsoft Rich Edit 3,0 et versions ultérieures : si cette valeur est définie, la recherche fait la distinction entre les alefs arabe et hébreu avec des accents différents.</span><span class="sxs-lookup"><span data-stu-id="d66f6-117">Microsoft Rich Edit 3.0 and later: If set, the search differentiates between Arabic and Hebrew alefs with different accents.</span></span> <span data-ttu-id="d66f6-118">S’il n’est pas défini, tous les alefs sont mis en correspondance par le caractère Alef seul.</span><span class="sxs-lookup"><span data-stu-id="d66f6-118">If not set, all alefs are matched by the alef character alone.</span></span> <br/>                                                                         |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <span data-ttu-id="d66f6-119"><dt>**FR \_ RespecterCasse**</dt></span><span class="sxs-lookup"><span data-stu-id="d66f6-119"><dt>**FR\_MATCHCASE**</dt></span></span> </dl>                | <span data-ttu-id="d66f6-120">Si cette valeur est définie, l’opération de recherche respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="d66f6-120">If set, the search operation is case-sensitive.</span></span> <span data-ttu-id="d66f6-121">Si la valeur n’est pas définie, l’opération de recherche n’est pas sensible à la casse.</span><span class="sxs-lookup"><span data-stu-id="d66f6-121">If not set, the search operation is case-insensitive.</span></span> <br/>                                                                                                                                                               |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <span data-ttu-id="d66f6-122"><dt>**\_MATCHDIAC fr**</dt></span><span class="sxs-lookup"><span data-stu-id="d66f6-122"><dt>**FR\_MATCHDIAC**</dt></span></span> </dl>                | <span data-ttu-id="d66f6-123">Édition enrichie de Microsoft 3,0 et versions ultérieures : si elle est définie, l’opération de recherche prend en compte les marques diacritiques arabe et hébreu.</span><span class="sxs-lookup"><span data-stu-id="d66f6-123">Microsoft Rich Edit 3.0 and later: If set, the search operation considers Arabic and Hebrew diacritical marks.</span></span> <span data-ttu-id="d66f6-124">S’il n’est pas défini, les signes diacritiques sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="d66f6-124">If not set, diacritical marks are ignored.</span></span> <br/>                                                                                                           |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <span data-ttu-id="d66f6-125"><dt>**FR \_ MATCHKASHIDA**</dt></span><span class="sxs-lookup"><span data-stu-id="d66f6-125"><dt>**FR\_MATCHKASHIDA**</dt></span></span> </dl>       | <span data-ttu-id="d66f6-126">Édition enrichie de Microsoft 3,0 et versions ultérieures : si elle est définie, l’opération de recherche prend en compte les kachidés arabes et Hébreux.</span><span class="sxs-lookup"><span data-stu-id="d66f6-126">Microsoft Rich Edit 3.0 and later: If set, the search operation considers Arabic and Hebrew kashidas.</span></span> <span data-ttu-id="d66f6-127">Si la valeur n’est pas définie, les signes kachidé sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="d66f6-127">If not set, kashidas are ignored.</span></span> <br/>                                                                                                                             |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <span data-ttu-id="d66f6-128"><dt>**\_WHOLEWORD fr**</dt></span><span class="sxs-lookup"><span data-stu-id="d66f6-128"><dt>**FR\_WHOLEWORD**</dt></span></span> </dl>                | <span data-ttu-id="d66f6-129">Si elle est définie, l’opération recherche uniquement les mots entiers qui correspondent à la chaîne recherchée.</span><span class="sxs-lookup"><span data-stu-id="d66f6-129">If set, the operation searches only for whole words that match the search string.</span></span> <span data-ttu-id="d66f6-130">Si la valeur n’est pas définie, l’opération recherche également des fragments de mot qui correspondent à la chaîne recherchée.</span><span class="sxs-lookup"><span data-stu-id="d66f6-130">If not set, the operation also searches for word fragments that match the search string.</span></span><br/>                                                                                           |



 

</dd> <dt>

<span data-ttu-id="d66f6-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d66f6-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d66f6-132">Structure [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) contenant des informations sur l’opération de recherche.</span><span class="sxs-lookup"><span data-stu-id="d66f6-132">A [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure containing information about the find operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d66f6-133">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d66f6-133">Return value</span></span>

<span data-ttu-id="d66f6-134">Si la chaîne cible est trouvée, la valeur de retour est la position de base zéro du premier caractère de la correspondance.</span><span class="sxs-lookup"><span data-stu-id="d66f6-134">If the target string is found, the return value is the zero-based position of the first character of the match.</span></span> <span data-ttu-id="d66f6-135">Si la cible est introuvable, la valeur de retour est-1.</span><span class="sxs-lookup"><span data-stu-id="d66f6-135">If the target is not found, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="d66f6-136">Notes </span><span class="sxs-lookup"><span data-stu-id="d66f6-136">Remarks</span></span>

<span data-ttu-id="d66f6-137">Utilisez ce message pour rechercher des chaînes ANSI.</span><span class="sxs-lookup"><span data-stu-id="d66f6-137">Use this message to find ANSI strings.</span></span> <span data-ttu-id="d66f6-138">Pour Unicode, utilisez [**em \_ FINDTEXTEXW**](em-findtextexw.md).</span><span class="sxs-lookup"><span data-stu-id="d66f6-138">For Unicode, use [**EM\_FINDTEXTEXW**](em-findtextexw.md).</span></span>

<span data-ttu-id="d66f6-139">Le membre **cpMin** de **FINDTEXTEX.** frais spécifie toujours le point de départ de la recherche, tandis que **cpMax** spécifie le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="d66f6-139">The **cpMin** member of **FINDTEXTEX.chrg** always specifies the starting-point of the search, and **cpMax** specifies the end point.</span></span> <span data-ttu-id="d66f6-140">Lorsque vous effectuez une recherche vers l’arrière, **cpMin** doit être supérieur ou égal à **cpMax**.</span><span class="sxs-lookup"><span data-stu-id="d66f6-140">When searching backward, **cpMin** must be equal to or greater than **cpMax**.</span></span> <span data-ttu-id="d66f6-141">Lors d’une recherche vers l’avant, la valeur-1 dans **cpMax** étend la plage de recherche à la fin du texte.</span><span class="sxs-lookup"><span data-stu-id="d66f6-141">When searching forward, a value of -1 in **cpMax** extends the search range to the end of the text.</span></span>

<span data-ttu-id="d66f6-142">Si l’opération de recherche trouve une correspondance, le membre **chrgText** de la structure [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) retourne la plage de positions de caractères qui contient le texte correspondant.</span><span class="sxs-lookup"><span data-stu-id="d66f6-142">If the search operation finds a match, the **chrgText** member of the [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure returns the range of character positions that contains the matching text.</span></span>

## <a name="requirements"></a><span data-ttu-id="d66f6-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d66f6-143">Requirements</span></span>



| <span data-ttu-id="d66f6-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d66f6-144">Requirement</span></span> | <span data-ttu-id="d66f6-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="d66f6-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d66f6-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d66f6-146">Minimum supported client</span></span><br/> | <span data-ttu-id="d66f6-147">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d66f6-147">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d66f6-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d66f6-148">Minimum supported server</span></span><br/> | <span data-ttu-id="d66f6-149">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d66f6-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d66f6-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="d66f6-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="d66f6-151"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d66f6-151"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d66f6-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d66f6-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d66f6-153">**\_TEXTECHERCHÉ em**</span><span class="sxs-lookup"><span data-stu-id="d66f6-153">**EM\_FINDTEXT**</span></span>](em-findtext.md)
</dt> </dl>

 

 





