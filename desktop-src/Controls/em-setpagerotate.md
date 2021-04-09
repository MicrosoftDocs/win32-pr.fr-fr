---
title: Message EM_SETPAGEROTATE (RichEdit. h)
description: Définit la disposition du texte pour un contrôle RichEdit.
ms.assetid: 3c2a37fe-ee9f-4b34-87bf-7ac27d010afc
keywords:
- EM_SETPAGEROTATE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETPAGEROTATE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12eb595456bca444c92b536b0e428ee56a5903ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942027"
---
# <a name="em_setpagerotate-message"></a><span data-ttu-id="ca984-104">\_Message SETPAGEROTATE em</span><span class="sxs-lookup"><span data-stu-id="ca984-104">EM\_SETPAGEROTATE message</span></span>

<span data-ttu-id="ca984-105">\[**Em \_ SETPAGEROTATE** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="ca984-105">\[**EM\_SETPAGEROTATE** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ca984-106">Il sera peut-être modifié ou indisponible dans les versions ultérieures.\]</span><span class="sxs-lookup"><span data-stu-id="ca984-106">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="ca984-107">Définit la disposition du texte pour un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="ca984-107">Sets the text layout for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ca984-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ca984-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca984-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ca984-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ca984-110">Valeur de disposition du texte.</span><span class="sxs-lookup"><span data-stu-id="ca984-110">Text layout value.</span></span> <span data-ttu-id="ca984-111">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ca984-111">This can be one of the following values.</span></span>



| <span data-ttu-id="ca984-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca984-112">Value</span></span>                                                                                                                                       | <span data-ttu-id="ca984-113">Signification</span><span class="sxs-lookup"><span data-stu-id="ca984-113">Meaning</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="EPR_0"></span><span id="epr_0"></span><dl> <span data-ttu-id="ca984-114"><dt>**EPR \_ 0**</dt></span><span class="sxs-lookup"><span data-stu-id="ca984-114"><dt>**EPR\_0**</dt></span></span> </dl>       | <span data-ttu-id="ca984-115">Le texte est écrit de gauche à droite et de haut en bas.</span><span class="sxs-lookup"><span data-stu-id="ca984-115">Text flows from left to right and from top to bottom.</span></span><br/>                              |
| <span id="EPR_90"></span><span id="epr_90"></span><dl> <span data-ttu-id="ca984-116"><dt>**EPR \_ 90**</dt></span><span class="sxs-lookup"><span data-stu-id="ca984-116"><dt>**EPR\_90**</dt></span></span> </dl>    | <span data-ttu-id="ca984-117">Le texte est écrit de bas en haut et de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="ca984-117">Text flows from bottom to top and from left to right.</span></span><br/>                              |
| <span id="EPR_180"></span><span id="epr_180"></span><dl> <span data-ttu-id="ca984-118"><dt>**EPR \_ 180**</dt></span><span class="sxs-lookup"><span data-stu-id="ca984-118"><dt>**EPR\_180**</dt></span></span> </dl> | <span data-ttu-id="ca984-119">Le texte est écrit de droite à gauche et de bas en haut.</span><span class="sxs-lookup"><span data-stu-id="ca984-119">Text flows from right to left and from bottom to top.</span></span><br/>                              |
| <span id="EPR_270"></span><span id="epr_270"></span><dl> <span data-ttu-id="ca984-120"><dt>**EPR \_ 270**</dt></span><span class="sxs-lookup"><span data-stu-id="ca984-120"><dt>**EPR\_270**</dt></span></span> </dl> | <span data-ttu-id="ca984-121">Le texte est écrit de haut en bas et de droite à gauche.</span><span class="sxs-lookup"><span data-stu-id="ca984-121">Text flows from top to bottom and from right to left.</span></span><br/>                              |
| <span id="EPR_SE"></span><span id="epr_se"></span><dl> <span data-ttu-id="ca984-122"><dt>**\_se EPR**</dt></span><span class="sxs-lookup"><span data-stu-id="ca984-122"><dt>**EPR\_SE**</dt></span></span> </dl>    | <span data-ttu-id="ca984-123">**Windows 8 :** Les flux de texte de haut en bas et de gauche à droite (disposition du texte mongol).</span><span class="sxs-lookup"><span data-stu-id="ca984-123">**Windows 8:** Text flows top to bottom and left to right (Mongolian text layout).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ca984-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ca984-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ca984-125">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="ca984-125">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca984-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ca984-126">Return value</span></span>

<span data-ttu-id="ca984-127">La valeur de retour est la nouvelle valeur de disposition du texte.</span><span class="sxs-lookup"><span data-stu-id="ca984-127">Return value is the new text layout value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca984-128">Notes</span><span class="sxs-lookup"><span data-stu-id="ca984-128">Remarks</span></span>

<span data-ttu-id="ca984-129">Ce message définit la disposition du texte pour l’ensemble du document.</span><span class="sxs-lookup"><span data-stu-id="ca984-129">This message sets the text layout for the entire document.</span></span> <span data-ttu-id="ca984-130">Toutefois, le contenu incorporé n’est pas pivoté et doit être pivoté séparément par l’application.</span><span class="sxs-lookup"><span data-stu-id="ca984-130">However, embedded contents are not rotated and must be rotated separately by the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca984-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca984-131">Requirements</span></span>



| <span data-ttu-id="ca984-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca984-132">Requirement</span></span> | <span data-ttu-id="ca984-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca984-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca984-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca984-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ca984-135">Windows XP avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca984-135">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ca984-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca984-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ca984-137">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca984-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ca984-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="ca984-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca984-139"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca984-139"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca984-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca984-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca984-141">**\_GETPAGEROTATE em**</span><span class="sxs-lookup"><span data-stu-id="ca984-141">**EM\_GETPAGEROTATE**</span></span>](em-getpagerotate.md)
</dt> </dl>

 

 





