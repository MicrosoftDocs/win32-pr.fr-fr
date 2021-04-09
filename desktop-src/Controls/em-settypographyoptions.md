---
title: Message EM_SETTYPOGRAPHYOPTIONS (RichEdit. h)
description: Définit l’état actuel des options typographiques d’un contrôle RichEdit.
ms.assetid: 000e72a6-3f8c-4735-8190-3ac06a2206ac
keywords:
- EM_SETTYPOGRAPHYOPTIONS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETTYPOGRAPHYOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0528e19aacec394c5af6250536fdc4f693e60ece
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942293"
---
# <a name="em_settypographyoptions-message"></a><span data-ttu-id="56503-104">\_Message SETTYPOGRAPHYOPTIONS em</span><span class="sxs-lookup"><span data-stu-id="56503-104">EM\_SETTYPOGRAPHYOPTIONS message</span></span>

<span data-ttu-id="56503-105">Définit l’état actuel des options typographiques d’un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="56503-105">Sets the current state of the typography options of a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="56503-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56503-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56503-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="56503-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56503-108">Spécifie l’une des valeurs suivantes ou les deux.</span><span class="sxs-lookup"><span data-stu-id="56503-108">Specifies one or both of the following values.</span></span>



| <span data-ttu-id="56503-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="56503-109">Value</span></span>                                                                                                                                                                                    | <span data-ttu-id="56503-110">Signification</span><span class="sxs-lookup"><span data-stu-id="56503-110">Meaning</span></span>                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="TO_ADVANCEDTYPOGRAPHY_"></span><span id="to_advancedtypography_"></span><dl> <span data-ttu-id="56503-111"><dt>**À \_ ADVANCEDTYPOGRAPHY**</dt></span><span class="sxs-lookup"><span data-stu-id="56503-111"><dt>**TO\_ADVANCEDTYPOGRAPHY** </dt></span></span> </dl> | <span data-ttu-id="56503-112">Le saut de ligne avancé et la mise en forme de ligne sont activés.</span><span class="sxs-lookup"><span data-stu-id="56503-112">Advanced line breaking and line formatting is turned on.</span></span> <br/>                    |
| <span id="TO_SIMPLELINEBREAK"></span><span id="to_simplelinebreak"></span><dl> <span data-ttu-id="56503-113"><dt>**à \_ SIMPLELINEBREAK**</dt></span><span class="sxs-lookup"><span data-stu-id="56503-113"><dt>**TO\_SIMPLELINEBREAK**</dt></span></span> </dl>             | <span data-ttu-id="56503-114">Saut de ligne plus rapide pour le texte simple (requiert **\_ ADVANCEDTYPOGRAPHY**).</span><span class="sxs-lookup"><span data-stu-id="56503-114">Faster line breaking for simple text (requires **TO\_ADVANCEDTYPOGRAPHY**).</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="56503-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="56503-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56503-116">Masque constitué d’un ou plusieurs indicateurs dans *wParam*.</span><span class="sxs-lookup"><span data-stu-id="56503-116">A mask consisting of one or more of the flags in *wParam*.</span></span> <span data-ttu-id="56503-117">Seuls les indicateurs définis dans ce masque seront définis ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="56503-117">Only the flags that are set in this mask will be set or cleared.</span></span> <span data-ttu-id="56503-118">Cela permet de définir ou d’effacer un seul indicateur sans lire les États de l’indicateur actuel.</span><span class="sxs-lookup"><span data-stu-id="56503-118">This allows a single flag to be set or cleared without reading the current flag states.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56503-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="56503-119">Return value</span></span>

<span data-ttu-id="56503-120">Retourne la **valeur true** si *wParam* est valide, sinon **false**.</span><span class="sxs-lookup"><span data-stu-id="56503-120">Returns **TRUE** if *wParam* is valid, otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="56503-121">Notes</span><span class="sxs-lookup"><span data-stu-id="56503-121">Remarks</span></span>

<span data-ttu-id="56503-122">Le saut de ligne avancé est activé automatiquement par le contrôle RichEdit si nécessaire, par exemple pour la gestion de scripts complexes tels que l’arabe et l’hébreu, ainsi que pour les mathématiques.</span><span class="sxs-lookup"><span data-stu-id="56503-122">Advanced line breaking is turned on automatically by the rich edit control when needed, such as for handling complex scripts like Arabic and Hebrew, and for mathematics.</span></span> <span data-ttu-id="56503-123">Elle est également nécessaire pour les paragraphes justifiés, la césure et d’autres fonctionnalités typographiques.</span><span class="sxs-lookup"><span data-stu-id="56503-123">It s also needed for justified paragraphs, hyphenation, and other typographic features.</span></span>

## <a name="requirements"></a><span data-ttu-id="56503-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56503-124">Requirements</span></span>



| <span data-ttu-id="56503-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56503-125">Requirement</span></span> | <span data-ttu-id="56503-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="56503-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56503-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56503-127">Minimum supported client</span></span><br/> | <span data-ttu-id="56503-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56503-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="56503-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56503-129">Minimum supported server</span></span><br/> | <span data-ttu-id="56503-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56503-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="56503-131">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="56503-131">Redistributable</span></span><br/>          | <span data-ttu-id="56503-132">Édition enrichie 3,0</span><span class="sxs-lookup"><span data-stu-id="56503-132">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="56503-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="56503-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="56503-134"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="56503-134"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56503-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56503-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56503-136">**\_GETTYPOGRAPHYOPTIONS em**</span><span class="sxs-lookup"><span data-stu-id="56503-136">**EM\_GETTYPOGRAPHYOPTIONS**</span></span>](em-gettypographyoptions.md)
</dt> </dl>

 

 





