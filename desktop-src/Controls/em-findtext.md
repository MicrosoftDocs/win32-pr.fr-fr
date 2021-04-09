---
title: Message EM_FINDTEXT (RichEdit. h)
description: Recherche du texte dans un contrôle RichEdit.
ms.assetid: f19e19a0-d8dd-4d31-b76d-f1f09577dd2d
keywords:
- EM_FINDTEXT les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_FINDTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e50034337f05d2df17af777986136881c503d05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942304"
---
# <a name="em_findtext-message"></a><span data-ttu-id="b5f54-104">\_Message du TEXTECHERCHÉ em</span><span class="sxs-lookup"><span data-stu-id="b5f54-104">EM\_FINDTEXT message</span></span>

<span data-ttu-id="b5f54-105">Recherche du texte dans un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="b5f54-105">Finds text within a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b5f54-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b5f54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5f54-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b5f54-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5f54-108">Spécifiez les paramètres de l’opération de recherche.</span><span class="sxs-lookup"><span data-stu-id="b5f54-108">Specify the parameters of the search operation.</span></span> <span data-ttu-id="b5f54-109">Ce paramètre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="b5f54-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="b5f54-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5f54-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="b5f54-111">Signification</span><span class="sxs-lookup"><span data-stu-id="b5f54-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <span data-ttu-id="b5f54-112"><dt>**FR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b5f54-112"><dt>**FR\_DOWN**</dt></span></span> </dl>                               | <span data-ttu-id="b5f54-113">Microsoft Rich Edit 2,0 et versions ultérieures : si cette option est définie, la recherche se fait à partir de la fin de la sélection actuelle jusqu’à la fin du document.</span><span class="sxs-lookup"><span data-stu-id="b5f54-113">Microsoft Rich Edit 2.0 and later: If set, the search is from the end of the current selection to the end of the document.</span></span> <span data-ttu-id="b5f54-114">S’il n’est pas défini, la recherche commence à la fin de la sélection actuelle jusqu’au début du document.</span><span class="sxs-lookup"><span data-stu-id="b5f54-114">If not set, the search is from the end of the current selection to the beginning of the document.</span></span> <br/> <span data-ttu-id="b5f54-115">Édition enrichie de Microsoft 1,0 : l' \_ indicateur fr vers le PG. est ignoré.</span><span class="sxs-lookup"><span data-stu-id="b5f54-115">Microsoft Rich Edit 1.0: The FR\_DOWN flag is ignored.</span></span> <span data-ttu-id="b5f54-116">La recherche est toujours à la fin de la sélection actuelle jusqu’à la fin du document.</span><span class="sxs-lookup"><span data-stu-id="b5f54-116">The search is always from the end of the current selection to the end of the document.</span></span><br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <span data-ttu-id="b5f54-117"><dt>**le \_ MATCHALEFHAMZA**</dt></span><span class="sxs-lookup"><span data-stu-id="b5f54-117"><dt>**FR\_MATCHALEFHAMZA**</dt></span></span> </dl> | <span data-ttu-id="b5f54-118">Microsoft Rich Edit 3,0 et versions ultérieures : si cette valeur est définie, la recherche fait la distinction entre les alefs arabes avec des accents différents.</span><span class="sxs-lookup"><span data-stu-id="b5f54-118">Microsoft Rich Edit 3.0 and later: If set, the search differentiates between Arabic alefs with different accents.</span></span> <span data-ttu-id="b5f54-119">S’il n’est pas défini, tous les alefs sont mis en correspondance par le caractère Alef seul.</span><span class="sxs-lookup"><span data-stu-id="b5f54-119">If not set, all alefs are matched by the alef character alone.</span></span> <br/>                                                                                                                                                                                                      |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <span data-ttu-id="b5f54-120"><dt>**\_MATCHDIAC fr**</dt></span><span class="sxs-lookup"><span data-stu-id="b5f54-120"><dt>**FR\_MATCHDIAC**</dt></span></span> </dl>                | <span data-ttu-id="b5f54-121">Édition enrichie de Microsoft 3,0 et versions ultérieures : si elle est définie, l’opération de recherche prend en compte les marques diacritiques arabe et hébreu.</span><span class="sxs-lookup"><span data-stu-id="b5f54-121">Microsoft Rich Edit 3.0 and later: If set, the search operation considers Arabic and Hebrew diacritical marks.</span></span> <span data-ttu-id="b5f54-122">S’il n’est pas défini, les signes diacritiques sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="b5f54-122">If not set, diacritical marks are ignored.</span></span> <br/>                                                                                                                                                                                                                             |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <span data-ttu-id="b5f54-123"><dt>**FR \_ MATCHKASHIDA**</dt></span><span class="sxs-lookup"><span data-stu-id="b5f54-123"><dt>**FR\_MATCHKASHIDA**</dt></span></span> </dl>       | <span data-ttu-id="b5f54-124">Rich Edit 3,0 et versions ultérieures de Microsoft : si cette valeur est définie, l’opération de recherche prend en compte les kachidés arabes.</span><span class="sxs-lookup"><span data-stu-id="b5f54-124">Microsoft Rich Edit 3.0 and later: If set, the search operation considers Arabic kashidas.</span></span> <span data-ttu-id="b5f54-125">Si la valeur n’est pas définie, les signes kachidé sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="b5f54-125">If not set, kashidas are ignored.</span></span> <br/>                                                                                                                                                                                                                                                          |
| <span id="FR_MATCHWIDTH"></span><span id="fr_matchwidth"></span><dl> <span data-ttu-id="b5f54-126"><dt>**\_MATCHWIDTH fr**</dt></span><span class="sxs-lookup"><span data-stu-id="b5f54-126"><dt>**FR\_MATCHWIDTH**</dt></span></span> </dl>             | <span data-ttu-id="b5f54-127">Windows 8 : si cette valeur est définie, les versions sur un octet et sur deux octets du même caractère sont considérées comme différentes.</span><span class="sxs-lookup"><span data-stu-id="b5f54-127">Windows 8: If set, single-byte and double-byte versions of the same character are considered to be not equal.</span></span><br/>                                                                                                                                                                                                                                                                          |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <span data-ttu-id="b5f54-128"><dt>**\_WHOLEWORD fr**</dt></span><span class="sxs-lookup"><span data-stu-id="b5f54-128"><dt>**FR\_WHOLEWORD**</dt></span></span> </dl>                | <span data-ttu-id="b5f54-129">Si elle est définie, l’opération recherche uniquement les mots entiers qui correspondent à la chaîne recherchée.</span><span class="sxs-lookup"><span data-stu-id="b5f54-129">If set, the operation searches only for whole words that match the search string.</span></span> <span data-ttu-id="b5f54-130">Si la valeur n’est pas définie, l’opération recherche également des fragments de mot qui correspondent à la chaîne recherchée.</span><span class="sxs-lookup"><span data-stu-id="b5f54-130">If not set, the operation also searches for word fragments that match the search string.</span></span><br/>                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="b5f54-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b5f54-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5f54-132">Structure [**TexteCherché**](/windows/win32/api/richedit/ns-richedit-findtexta) contenant des informations sur l’opération de recherche.</span><span class="sxs-lookup"><span data-stu-id="b5f54-132">A [**FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta) structure containing information about the find operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5f54-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b5f54-133">Return value</span></span>

<span data-ttu-id="b5f54-134">Si la chaîne cible est trouvée, la valeur de retour est la position de base zéro du premier caractère de la correspondance.</span><span class="sxs-lookup"><span data-stu-id="b5f54-134">If the target string is found, the return value is the zero-based position of the first character of the match.</span></span> <span data-ttu-id="b5f54-135">Si la cible est introuvable, la valeur de retour est-1.</span><span class="sxs-lookup"><span data-stu-id="b5f54-135">If the target is not found, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5f54-136">Notes</span><span class="sxs-lookup"><span data-stu-id="b5f54-136">Remarks</span></span>

<span data-ttu-id="b5f54-137">Le membre **cpMin** de **FINDTEXT.** frais spécifie toujours le point de départ de la recherche, tandis que **cpMax** spécifie le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="b5f54-137">The **cpMin** member of **FINDTEXT.chrg** always specifies the starting-point of the search, and **cpMax** specifies the end point.</span></span> <span data-ttu-id="b5f54-138">Lorsque vous effectuez une recherche vers l’arrière, **cpMin** doit être supérieur ou égal à **cpMax**.</span><span class="sxs-lookup"><span data-stu-id="b5f54-138">When searching backward, **cpMin** must be equal to or greater than **cpMax**.</span></span> <span data-ttu-id="b5f54-139">Lors d’une recherche vers l’avant, la valeur-1 dans **cpMax** étend la plage de recherche à la fin du texte.</span><span class="sxs-lookup"><span data-stu-id="b5f54-139">When searching forward, a value of -1 in **cpMax** extends the search range to the end of the text.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5f54-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5f54-140">Requirements</span></span>



| <span data-ttu-id="b5f54-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5f54-141">Requirement</span></span> | <span data-ttu-id="b5f54-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5f54-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b5f54-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5f54-143">Minimum supported client</span></span><br/> | <span data-ttu-id="b5f54-144">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5f54-144">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b5f54-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5f54-145">Minimum supported server</span></span><br/> | <span data-ttu-id="b5f54-146">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5f54-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b5f54-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="b5f54-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5f54-148"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5f54-148"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5f54-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5f54-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5f54-150">**FINDTEXT**</span><span class="sxs-lookup"><span data-stu-id="b5f54-150">**FINDTEXT**</span></span>](/windows/win32/api/richedit/ns-richedit-findtexta)
</dt> </dl>

 

 





