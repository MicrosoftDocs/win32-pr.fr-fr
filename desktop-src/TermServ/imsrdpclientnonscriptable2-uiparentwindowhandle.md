---
title: IMsRdpClientNonScriptable2 propriété UIParentWindowHandle
description: Définit ou récupère le handle de fenêtre comme fenêtre parente pour toutes les boîtes de dialogue affichées par le contrôle. Cela permet aux fenêtres affichées par le contrôle d’être correctement modales par rapport à toutes les fenêtres affichées par l’application parente.
ms.assetid: 5ecf1fc3-492e-4faf-89c5-7f7abb3778a0
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété UIParentWindowHandle
- Services Bureau à distance de la propriété UIParentWindowHandle, interface IMsRdpClientNonScriptable2
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable2, propriété UIParentWindowHandle
- Services Bureau à distance de la propriété UIParentWindowHandle, interface IMsRdpClientNonScriptable3
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable3, propriété UIParentWindowHandle
- Services Bureau à distance de la propriété UIParentWindowHandle, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété UIParentWindowHandle
- Services Bureau à distance de la propriété UIParentWindowHandle, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété UIParentWindowHandle
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable2.UIParentWindowHandle
- IMsRdpClientNonScriptable2.get_UIParentWindowHandle
- IMsRdpClientNonScriptable2.put_UIParentWindowHandle
- IMsRdpClientNonScriptable3.UIParentWindowHandle
- IMsRdpClientNonScriptable3.get_UIParentWindowHandle
- IMsRdpClientNonScriptable3.put_UIParentWindowHandle
- IMsRdpClientNonScriptable4.UIParentWindowHandle
- IMsRdpClientNonScriptable4.get_UIParentWindowHandle
- IMsRdpClientNonScriptable4.put_UIParentWindowHandle
- IMsRdpClientNonScriptable5.UIParentWindowHandle
- IMsRdpClientNonScriptable5.get_UIParentWindowHandle
- IMsRdpClientNonScriptable5.put_UIParentWindowHandle
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5526fd1a699c87e32c6acadd238c2144d00a10be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464314"
---
# <a name="imsrdpclientnonscriptable2uiparentwindowhandle-property"></a><span data-ttu-id="d8365-113">IMsRdpClientNonScriptable2 :: UIParentWindowHandle, propriété</span><span class="sxs-lookup"><span data-stu-id="d8365-113">IMsRdpClientNonScriptable2::UIParentWindowHandle property</span></span>

<span data-ttu-id="d8365-114">Définit ou récupère le handle de fenêtre comme fenêtre parente pour toutes les boîtes de dialogue affichées par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="d8365-114">Sets or retrieves the window handle to be the parent window for any dialog boxes displayed by the control.</span></span> <span data-ttu-id="d8365-115">Cela permet aux fenêtres affichées par le contrôle d’être correctement modales par rapport à toutes les fenêtres affichées par l’application parente.</span><span class="sxs-lookup"><span data-stu-id="d8365-115">This allows any windows displayed by the control to be properly modal with respect to any windows displayed by the parent application.</span></span>

<span data-ttu-id="d8365-116">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="d8365-116">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8365-117">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8365-117">Syntax</span></span>


```C++
HRESULT put_UIParentWindowHandle(
  [in]  HWND hwndUIParentWindowHandle
);

HRESULT get_UIParentWindowHandle(
  [out] HWND *phwndUIParentWindowHandle
);
```



## <a name="property-value"></a><span data-ttu-id="d8365-118">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d8365-118">Property value</span></span>

<span data-ttu-id="d8365-119">Nouveau handle de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d8365-119">The new window handle.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d8365-120">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="d8365-120">Error codes</span></span>

<span data-ttu-id="d8365-121">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="d8365-121">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8365-122">Notes</span><span class="sxs-lookup"><span data-stu-id="d8365-122">Remarks</span></span>

<span data-ttu-id="d8365-123">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="d8365-123">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d8365-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8365-124">Requirements</span></span>



| <span data-ttu-id="d8365-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8365-125">Requirement</span></span> | <span data-ttu-id="d8365-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8365-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8365-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8365-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d8365-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d8365-128">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="d8365-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8365-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d8365-130">Windows Server 2008, Windows Server 2008 avec SP1</span><span class="sxs-lookup"><span data-stu-id="d8365-130">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                                  |
| <span data-ttu-id="d8365-131">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="d8365-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="d8365-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8365-132"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="d8365-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d8365-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8365-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8365-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="d8365-135">IID</span><span class="sxs-lookup"><span data-stu-id="d8365-135">IID</span></span><br/>                      | <span data-ttu-id="d8365-136">IID \_ IMsRdpClientNonScriptable2 est défini en tant que 17a5e535-4072-4FA4-AF32-c8d0d47345e9</span><span class="sxs-lookup"><span data-stu-id="d8365-136">IID\_IMsRdpClientNonScriptable2 is defined as 17a5e535-4072-4fa4-af32-c8d0d47345e9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d8365-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8365-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8365-138">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="d8365-138">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="d8365-139">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="d8365-139">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="d8365-140">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="d8365-140">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="d8365-141">**OnAuthenticationWarningDisplayed**</span><span class="sxs-lookup"><span data-stu-id="d8365-141">**OnAuthenticationWarningDisplayed**</span></span>](imstscaxevents-onauthenticationwarningdisplayed.md)
</dt> <dt>

[<span data-ttu-id="d8365-142">**OnAuthenticationWarningDismissed**</span><span class="sxs-lookup"><span data-stu-id="d8365-142">**OnAuthenticationWarningDismissed**</span></span>](imstscaxevents-onauthenticationwarningdismissed.md)
</dt> <dt>

[<span data-ttu-id="d8365-143">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="d8365-143">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> </dl>

 

 





