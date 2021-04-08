---
title: Message TTM_SETTITLE (commctrl. h)
description: Ajoute une icône standard et une chaîne de titre à une info-bulle.
ms.assetid: e745a592-eef7-4e0d-8939-a48b52c4ab9f
keywords:
- TTM_SETTITLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TTM_SETTITLE
- TTM_SETTITLEA
- TTM_SETTITLEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7972a9d40347995e9d641e7fc8706f9ad4c58bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844258"
---
# <a name="ttm_settitle-message"></a><span data-ttu-id="03fb3-104">\_Message atténuation SETTITLE</span><span class="sxs-lookup"><span data-stu-id="03fb3-104">TTM\_SETTITLE message</span></span>

<span data-ttu-id="03fb3-105">Ajoute une icône standard et une chaîne de titre à une info-bulle.</span><span class="sxs-lookup"><span data-stu-id="03fb3-105">Adds a standard icon and title string to a tooltip.</span></span>

## <a name="parameters"></a><span data-ttu-id="03fb3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="03fb3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03fb3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="03fb3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03fb3-108">Affectez l’une des valeurs suivantes à *wParam* pour spécifier l’icône à afficher.</span><span class="sxs-lookup"><span data-stu-id="03fb3-108">Set *wParam* to one of the following values to specify the icon to be displayed.</span></span> <span data-ttu-id="03fb3-109">À compter de Windows XP SP2 et versions ultérieures, ce paramètre peut également contenir une valeur **HICON** .</span><span class="sxs-lookup"><span data-stu-id="03fb3-109">As of Windows XP SP2 and later, this parameter can also contain an **HICON** value.</span></span> <span data-ttu-id="03fb3-110">Toute valeur supérieure à TTI \_ erreur est supposée être un **HICON**.</span><span class="sxs-lookup"><span data-stu-id="03fb3-110">Any value greater than TTI\_ERROR is assumed to be an **HICON**.</span></span>



| <span data-ttu-id="03fb3-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="03fb3-111">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="03fb3-112">Signification</span><span class="sxs-lookup"><span data-stu-id="03fb3-112">Meaning</span></span>                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| <span id="TTI_NONE"></span><span id="tti_none"></span><dl> <span data-ttu-id="03fb3-113"><dt>**TTI \_ aucun**</dt></span><span class="sxs-lookup"><span data-stu-id="03fb3-113"><dt>**TTI\_NONE**</dt></span></span> </dl>                             | <span data-ttu-id="03fb3-114">Pas d'icône.</span><span class="sxs-lookup"><span data-stu-id="03fb3-114">No icon.</span></span><br/>         |
| <span id="TTI_INFO"></span><span id="tti_info"></span><dl> <span data-ttu-id="03fb3-115"><dt>**\_informations TTI**</dt></span><span class="sxs-lookup"><span data-stu-id="03fb3-115"><dt>**TTI\_INFO**</dt></span></span> </dl>                             | <span data-ttu-id="03fb3-116">Icône info.</span><span class="sxs-lookup"><span data-stu-id="03fb3-116">Info icon.</span></span><br/>       |
| <span id="TTI_WARNING"></span><span id="tti_warning"></span><dl> <span data-ttu-id="03fb3-117"><dt>**\_Avertissement TTI**</dt></span><span class="sxs-lookup"><span data-stu-id="03fb3-117"><dt>**TTI\_WARNING**</dt></span></span> </dl>                    | <span data-ttu-id="03fb3-118">Icône d'avertissement</span><span class="sxs-lookup"><span data-stu-id="03fb3-118">Warning icon</span></span><br/>     |
| <span id="TTI_ERROR"></span><span id="tti_error"></span><dl> <span data-ttu-id="03fb3-119"><dt>**\_erreur TTI**</dt></span><span class="sxs-lookup"><span data-stu-id="03fb3-119"><dt>**TTI\_ERROR**</dt></span></span> </dl>                          | <span data-ttu-id="03fb3-120">Icône d’erreur</span><span class="sxs-lookup"><span data-stu-id="03fb3-120">Error Icon</span></span><br/>       |
| <span id="TTI_INFO_LARGE"></span><span id="tti_info_large"></span><dl> <span data-ttu-id="03fb3-121"><dt>**TTI \_ info \_ grand**</dt></span><span class="sxs-lookup"><span data-stu-id="03fb3-121"><dt>**TTI\_INFO\_LARGE**</dt></span></span> </dl>          | <span data-ttu-id="03fb3-122">Icône d’erreur importante</span><span class="sxs-lookup"><span data-stu-id="03fb3-122">Large error Icon</span></span><br/> |
| <span id="TTI_WARNING_LARGE"></span><span id="tti_warning_large"></span><dl> <span data-ttu-id="03fb3-123"><dt>**\_Avertissement TTI \_ grand**</dt></span><span class="sxs-lookup"><span data-stu-id="03fb3-123"><dt>**TTI\_WARNING\_LARGE**</dt></span></span> </dl> | <span data-ttu-id="03fb3-124">Icône d’erreur importante</span><span class="sxs-lookup"><span data-stu-id="03fb3-124">Large error Icon</span></span><br/> |
| <span id="TTI_ERROR_LARGE"></span><span id="tti_error_large"></span><dl> <span data-ttu-id="03fb3-125"><dt>**erreur TTI de \_ \_ grande taille**</dt></span><span class="sxs-lookup"><span data-stu-id="03fb3-125"><dt>**TTI\_ERROR\_LARGE**</dt></span></span> </dl>       | <span data-ttu-id="03fb3-126">Icône d’erreur importante</span><span class="sxs-lookup"><span data-stu-id="03fb3-126">Large error Icon</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="03fb3-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="03fb3-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03fb3-128">Pointeur vers la chaîne de titre.</span><span class="sxs-lookup"><span data-stu-id="03fb3-128">Pointer to the title string.</span></span> <span data-ttu-id="03fb3-129">Vous devez assigner une valeur à *lParam*.</span><span class="sxs-lookup"><span data-stu-id="03fb3-129">You must assign a value to *lParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03fb3-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="03fb3-130">Return value</span></span>

<span data-ttu-id="03fb3-131">Retourne la **valeur true** en cas de réussite, **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="03fb3-131">Returns **TRUE** if successful, **FALSE** if not.</span></span>

## <a name="remarks"></a><span data-ttu-id="03fb3-132">Notes</span><span class="sxs-lookup"><span data-stu-id="03fb3-132">Remarks</span></span>

<span data-ttu-id="03fb3-133">Le titre d’une info-bulle s’affiche au-dessus du texte, dans une police différente.</span><span class="sxs-lookup"><span data-stu-id="03fb3-133">The title of a tooltip appears above the text, in a different font.</span></span> <span data-ttu-id="03fb3-134">Il n’est pas suffisant d’avoir un titre ; l’info-bulle doit également comporter du texte ou elle ne s’affiche pas.</span><span class="sxs-lookup"><span data-stu-id="03fb3-134">It is not sufficient to have a title; the tooltip must have text as well, or it is not displayed.</span></span>

<span data-ttu-id="03fb3-135">Lorsque *wParam* contient un **HICON**, une copie de l’icône est créée par la fenêtre d’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="03fb3-135">When *wParam* contains an **HICON**, a copy of the icon is created by the tooltip window.</span></span>

<span data-ttu-id="03fb3-136">Lors de l’appel de **atténuation \_ SETTITLE**, la chaîne vers laquelle pointe *lParam* ne doit pas dépasser 100 **TCHARs** , y compris le caractère **null** de fin.</span><span class="sxs-lookup"><span data-stu-id="03fb3-136">When calling **TTM\_SETTITLE**, the string pointed to by *lParam* must not exceed 100 **TCHARs** in length, including the terminating **NULL**.</span></span>

## <a name="examples"></a><span data-ttu-id="03fb3-137">Exemples</span><span class="sxs-lookup"><span data-stu-id="03fb3-137">Examples</span></span>

<span data-ttu-id="03fb3-138">L’exemple suivant montre comment ajouter un titre et une icône système à une info-bulle.</span><span class="sxs-lookup"><span data-stu-id="03fb3-138">The following example shows how to add a title and a system icon to a tooltip.</span></span>


```C++
// hwndTip is the handle of the tooltip window.
HICON hIcon = LoadIcon(NULL, IDI_INFORMATION);
SendMessage(hwndTip, TTM_SETTITLE, (WPARAM)hIcon, L"Title text");
DestroyIcon(hIcon);
```



## <a name="requirements"></a><span data-ttu-id="03fb3-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="03fb3-139">Requirements</span></span>



| <span data-ttu-id="03fb3-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="03fb3-140">Requirement</span></span> | <span data-ttu-id="03fb3-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="03fb3-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="03fb3-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03fb3-142">Minimum supported client</span></span><br/> | <span data-ttu-id="03fb3-143">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="03fb3-143">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="03fb3-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03fb3-144">Minimum supported server</span></span><br/> | <span data-ttu-id="03fb3-145">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="03fb3-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="03fb3-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="03fb3-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="03fb3-147"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="03fb3-147"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="03fb3-148">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="03fb3-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="03fb3-149">**Atténuation \_ SETTITLEW** (Unicode) et **atténuation \_ SETTITLEA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="03fb3-149">**TTM\_SETTITLEW** (Unicode) and **TTM\_SETTITLEA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="03fb3-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03fb3-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03fb3-151">À propos des contrôles ToolTip</span><span class="sxs-lookup"><span data-stu-id="03fb3-151">About Tooltip Controls</span></span>](tooltip-controls.md)
</dt> </dl>

 

 





