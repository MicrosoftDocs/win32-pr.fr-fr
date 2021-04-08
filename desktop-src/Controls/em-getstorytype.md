---
title: Message EM_GETSTORYTYPE (RichEdit. h)
description: Obtient le type d’histoire.
ms.assetid: 06D87AA1-5AA3-4235-AC1D-045CE9975384
keywords:
- EM_GETSTORYTYPE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETSTORYTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fed85183f292bd1c69e3bbebdadb4b38f9f3bdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843485"
---
# <a name="em_getstorytype-message"></a><span data-ttu-id="6da19-104">\_Message GETSTORYTYPE em</span><span class="sxs-lookup"><span data-stu-id="6da19-104">EM\_GETSTORYTYPE message</span></span>

<span data-ttu-id="6da19-105">Obtient le type d’histoire.</span><span class="sxs-lookup"><span data-stu-id="6da19-105">Gets the story type.</span></span>


```C++
#define EM_GETSTORYTYPE       (WM_USER + 290)
```



## <a name="parameters"></a><span data-ttu-id="6da19-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6da19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6da19-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6da19-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6da19-108">Index de l’histoire.</span><span class="sxs-lookup"><span data-stu-id="6da19-108">The story index.</span></span>

</dd> <dt>

<span data-ttu-id="6da19-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6da19-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6da19-110">Réservé doit être égal à 0.</span><span class="sxs-lookup"><span data-stu-id="6da19-110">Reserved; must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6da19-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6da19-111">Return value</span></span>

<span data-ttu-id="6da19-112">Retourne le type d’histoire, qui peut être une valeur personnalisée définie par le client, ou l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="6da19-112">Returns the story type, which can be a client-defined custom value, or one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="6da19-113">**[**tomCommentsStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="6da19-113">**[**tomCommentsStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="6da19-114">**[**tomEndnotesStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="6da19-114">**[**tomEndnotesStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="6da19-115">**[**tomEvenPagesFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="6da19-115">**[**tomEvenPagesFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="6da19-116">**[**tomEvenPagesHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="6da19-116">**[**tomEvenPagesHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="6da19-117">**[**tomFindStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="6da19-117">**[**tomFindStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="6da19-118">**[**tomFirstPageFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="6da19-118">**[**tomFirstPageFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="6da19-119">**[**tomFirstPageHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="6da19-119">**[**tomFirstPageHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="6da19-120">**[**tomFootnotesStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="6da19-120">**[**tomFootnotesStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="6da19-121">**[**tomMainTextStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="6da19-121">**[**tomMainTextStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="6da19-122">**[**tomPrimaryFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="6da19-122">**[**tomPrimaryFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="6da19-123">**[**tomPrimaryHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="6da19-123">**[**tomPrimaryHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="6da19-124">**[**tomReplaceStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="6da19-124">**[**tomReplaceStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="6da19-125">**[**tomScratchStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="6da19-125">**[**tomScratchStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="6da19-126">**[**tomTextFrameStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="6da19-126">**[**tomTextFrameStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="6da19-127">**[**tomUnknownStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="6da19-127">**[**tomUnknownStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6da19-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6da19-128">Requirements</span></span>



| <span data-ttu-id="6da19-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6da19-129">Requirement</span></span> | <span data-ttu-id="6da19-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="6da19-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6da19-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6da19-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6da19-132">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6da19-132">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="6da19-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6da19-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6da19-134">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6da19-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6da19-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="6da19-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="6da19-136"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6da19-136"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6da19-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6da19-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6da19-138">**\_SETSTORYTYPE em**</span><span class="sxs-lookup"><span data-stu-id="6da19-138">**EM\_SETSTORYTYPE**</span></span>](em-setstorytype.md)
</dt> <dt>

[<span data-ttu-id="6da19-139">**ITextStoryRanges :: Item**</span><span class="sxs-lookup"><span data-stu-id="6da19-139">**ITextStoryRanges::Item**</span></span>](/windows/desktop/api/Tom/nf-tom-itextstoryranges-item)
</dt> </dl>

 

 





