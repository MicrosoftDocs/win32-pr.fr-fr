---
title: Message TDM_UPDATE_ICON (commctrl. h)
description: Actualise l’icône d’une boîte de dialogue de tâche.
ms.assetid: 1094d9ca-90b4-4ba6-a14b-0d4e96243a34
keywords:
- TDM_UPDATE_ICON les contrôles de message Windows
topic_type:
- apiref
api_name:
- TDM_UPDATE_ICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b2da73ebb3bf0355f50bc08a08f0b35de97576b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942844"
---
# <a name="tdm_update_icon-message"></a><span data-ttu-id="14e37-104">\_Message d’icône de mise à jour TDM \_</span><span class="sxs-lookup"><span data-stu-id="14e37-104">TDM\_UPDATE\_ICON message</span></span>

<span data-ttu-id="14e37-105">Actualise l’icône d’une boîte de dialogue de tâche.</span><span class="sxs-lookup"><span data-stu-id="14e37-105">Refreshes the icon of a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="14e37-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="14e37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14e37-107">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="14e37-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14e37-108">Indique l’élément d’icône à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="14e37-108">Indicates which icon element to update.</span></span> <span data-ttu-id="14e37-109">Ce paramètre doit avoir l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="14e37-109">This parameter must be one of the following values:</span></span>



| <span data-ttu-id="14e37-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="14e37-110">Value</span></span>                                                                                                                                                                   | <span data-ttu-id="14e37-111">Signification</span><span class="sxs-lookup"><span data-stu-id="14e37-111">Meaning</span></span>                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="TDIE_ICON_MAIN"></span><span id="tdie_icon_main"></span><dl> <span data-ttu-id="14e37-112"><dt>**TDIE \_ icône \_ main**</dt></span><span class="sxs-lookup"><span data-stu-id="14e37-112"><dt>**TDIE\_ICON\_MAIN**</dt></span></span> </dl>       | <span data-ttu-id="14e37-113">Icône principale.</span><span class="sxs-lookup"><span data-stu-id="14e37-113">Main icon.</span></span><br/>   |
| <span id="TDIE_ICON_FOOTER"></span><span id="tdie_icon_footer"></span><dl> <span data-ttu-id="14e37-114"><dt>**pied de page de l' \_ icône TDIE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14e37-114"><dt>**TDIE\_ICON\_FOOTER**</dt></span></span> </dl> | <span data-ttu-id="14e37-115">Icône de pied de page.</span><span class="sxs-lookup"><span data-stu-id="14e37-115">Footer icon.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="14e37-116">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="14e37-116">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14e37-117">Pointeur vers une chaîne (PCWSTR) ou handle vers une icône (HICON) à afficher.</span><span class="sxs-lookup"><span data-stu-id="14e37-117">A pointer to a string (PCWSTR) or handle to an icon (HICON) to display.</span></span> <span data-ttu-id="14e37-118">Si *lParam* a la valeur **null**, aucune icône n’est affichée, quelle que soit la valeur de *wParam*.</span><span class="sxs-lookup"><span data-stu-id="14e37-118">If *lParam* is **NULL**, no icon is displayed, regardless of the value of *wParam*.</span></span>

<span data-ttu-id="14e37-119">Si la valeur de *wParam* est TDIE \_ Icon \_ main et que l' \_ indicateur de main TDF use \_ HICON \_ est défini sur le membre **dwFlags** de la structure [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) utilisée pour créer la boîte de dialogue de tâche, *lParam* doit contenir un handle vers une icône (HICON) à afficher.</span><span class="sxs-lookup"><span data-stu-id="14e37-119">If the value of *wParam* is TDIE\_ICON\_MAIN and the TDF\_USE\_HICON\_MAIN flag is set on the **dwFlags** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure used to create the task dialog, *lParam* must contain a handle to an icon (HICON) to display.</span></span>

<span data-ttu-id="14e37-120">Si la valeur de *wParam* est le \_ pied de page de l’icône TDIE \_ et que l' \_ indicateur de pied de page TDF use \_ HICON \_ est défini sur le membre **dwFlags** de la structure [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) utilisée pour créer la boîte de dialogue de tâche, *lParam* doit contenir un handle vers une icône (HICON) à afficher.</span><span class="sxs-lookup"><span data-stu-id="14e37-120">If the value of *wParam* is TDIE\_ICON\_FOOTER and the TDF\_USE\_HICON\_FOOTER flag is set on the **dwFlags** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure used to create the task dialog, *lParam* must contain a handle to an icon (HICON) to display.</span></span>

<span data-ttu-id="14e37-121">Si les \_ indicateurs TDF utilisent les \_ \_ \_ indicateurs de pied de page HICON main ou TDF use \_ HICON ne \_ sont **pas** définis sur le membre **DwFlags** , *lParam* doit pointer vers une chaîne Unicode terminée par le caractère null (PCWSTR) qui contient un identificateur de ressource valide passé par la macro [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) .</span><span class="sxs-lookup"><span data-stu-id="14e37-121">If the TDF\_USE\_HICON\_MAIN or TDF\_USE\_HICON\_FOOTER flags are **not** set on the **dwFlags** member, *lParam* must point to a null-terminated, Unicode string (PCWSTR) that contains a valid resource identifier passed through the [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) macro.</span></span> <span data-ttu-id="14e37-122">L’icône s’affiche en fonction de la valeur de *wParam*: si la valeur est TDIE \_ icône \_ main, l’icône s’affiche dans l’en-tête ; si la valeur est TDIE \_ icône pied de \_ page, l’icône s’affiche dans le pied de page.</span><span class="sxs-lookup"><span data-stu-id="14e37-122">The icon is displayed based on the value of *wParam*: if the value is TDIE\_ICON\_MAIN, the icon is displayed in the header; if the value is TDIE\_ICON\_FOOTER, the icon is displayed in the footer.</span></span> <span data-ttu-id="14e37-123">La ressource doit être à partir du module de ressources de l’application (spécifié dans le membre **HINSTANCE** de la structure [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) ), ou si **HINSTANCE** a la **valeur null**, à partir du module de ressources du système (imageres.dll).</span><span class="sxs-lookup"><span data-stu-id="14e37-123">The resource must be either from the application's resource module (specified in the **hInstance** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure), or if **hInstance** is **NULL**, from the system's resource module (imageres.dll).</span></span> <span data-ttu-id="14e37-124">Pour identifier une ressource système, utilisez un identificateur système valide passé par la macro **MAKEINTRESOURCE** ou l’une des valeurs prédéfinies suivantes de commctrl. h :</span><span class="sxs-lookup"><span data-stu-id="14e37-124">To identify a system resource, use a valid system identifier passed through the **MAKEINTRESOURCE** macro or one of the following predefined values from commctrl.h:</span></span>



| <span data-ttu-id="14e37-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="14e37-125">Value</span></span>                                                                                                                                                                            | <span data-ttu-id="14e37-126">Signification</span><span class="sxs-lookup"><span data-stu-id="14e37-126">Meaning</span></span>                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="TD_ERROR_ICON"></span><span id="td_error_icon"></span><dl> <span data-ttu-id="14e37-127"><dt>**\_icône d’erreur TD \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14e37-127"><dt>**TD\_ERROR\_ICON**</dt></span></span> </dl>                   | <span data-ttu-id="14e37-128">Icône de signe stop.</span><span class="sxs-lookup"><span data-stu-id="14e37-128">A stop sign icon.</span></span><br/>                        |
| <span id="TD_WARNING_ICON"></span><span id="td_warning_icon"></span><dl> <span data-ttu-id="14e37-129"><dt>**\_icône d’avertissement TD \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14e37-129"><dt>**TD\_WARNING\_ICON**</dt></span></span> </dl>             | <span data-ttu-id="14e37-130">Icône de point d’exclamation.</span><span class="sxs-lookup"><span data-stu-id="14e37-130">An exclamation point icon.</span></span><br/>               |
| <span id="TD_INFORMATION_ICON"></span><span id="td_information_icon"></span><dl> <span data-ttu-id="14e37-131"><dt>**\_icône d’informations TD \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14e37-131"><dt>**TD\_INFORMATION\_ICON**</dt></span></span> </dl> | <span data-ttu-id="14e37-132">Lettre minuscule « i » dans une icône de cercle.</span><span class="sxs-lookup"><span data-stu-id="14e37-132">A lowercase letter "i" in a circle icon.</span></span><br/> |
| <span id="TD_SHIELD_ICON"></span><span id="td_shield_icon"></span><dl> <span data-ttu-id="14e37-133"><dt>**\_icône de bouclier TD \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14e37-133"><dt>**TD\_SHIELD\_ICON**</dt></span></span> </dl>                | <span data-ttu-id="14e37-134">Icône de bouclier de sécurité.</span><span class="sxs-lookup"><span data-stu-id="14e37-134">A security shield icon.</span></span><br/>                  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14e37-135">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="14e37-135">Return value</span></span>

<span data-ttu-id="14e37-136">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="14e37-136">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="14e37-137">Notes</span><span class="sxs-lookup"><span data-stu-id="14e37-137">Remarks</span></span>

<span data-ttu-id="14e37-138">La disposition de la boîte de dialogue de tâche avec l’icône peut échouer et ne pas être reflétée dans la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="14e37-138">The layout of the task dialog with the icon may fail and this may not be reflected in the return value.</span></span> <span data-ttu-id="14e37-139">Une valeur de retour de S \_ OK reflète uniquement que la boîte de dialogue de tâche a reçu le message et a tenté de le traiter.</span><span class="sxs-lookup"><span data-stu-id="14e37-139">A return value of S\_OK reflects only that the task dialog received the message and attempted to process it.</span></span> <span data-ttu-id="14e37-140">Si la disposition de la boîte de dialogue de tâche échoue, la boîte de dialogue se ferme et un code **HRESULT** est retourné au niveau de la fonction de rappel inscrite.</span><span class="sxs-lookup"><span data-stu-id="14e37-140">If the layout of the task dialog fails, the dialog will close and an **HRESULT** code is returned at the registered callback function.</span></span> <span data-ttu-id="14e37-141">Pour plus d’informations sur la syntaxe de la fonction de rappel, consultez [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).</span><span class="sxs-lookup"><span data-stu-id="14e37-141">For more information on the callback function syntax, see [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).</span></span>

<span data-ttu-id="14e37-142">Si la boîte de dialogue de tâche est créée sans pied de page (autrement dit, les membres de pied de page appropriés de la structure [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) utilisée pour créer la boîte de dialogue de tâche ont la **valeur null**) et que ce message est envoyé, un pied de page n’est pas ajouté dynamiquement à la boîte de dialogue de tâche.</span><span class="sxs-lookup"><span data-stu-id="14e37-142">If the task dialog is created without a footer (that is, the appropriate footer members of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure used to create the task dialog are **NULL**) and this message is sent, a footer is not dynamically added to the task dialog.</span></span> <span data-ttu-id="14e37-143">Il en va de même pour l’envoi de ce message afin de mettre à jour une icône d’en-tête lorsqu’une boîte de dialogue de tâche est créée sans en-tête.</span><span class="sxs-lookup"><span data-stu-id="14e37-143">The same is true for sending this message to update a header icon when a task dialog is created without a header.</span></span> <span data-ttu-id="14e37-144">Pour ajouter un en-tête ou un pied de page au moment de l’exécution, utilisez la fonctionnalité de [**\_ \_ page de navigation TDM**](tdm-navigate-page.md) .</span><span class="sxs-lookup"><span data-stu-id="14e37-144">To add a header or footer at run time, use the [**TDM\_NAVIGATE\_PAGE**](tdm-navigate-page.md) functionality.</span></span>

## <a name="requirements"></a><span data-ttu-id="14e37-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="14e37-145">Requirements</span></span>



| <span data-ttu-id="14e37-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14e37-146">Requirement</span></span> | <span data-ttu-id="14e37-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="14e37-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="14e37-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14e37-148">Minimum supported client</span></span><br/> | <span data-ttu-id="14e37-149">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14e37-149">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="14e37-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14e37-150">Minimum supported server</span></span><br/> | <span data-ttu-id="14e37-151">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14e37-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="14e37-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="14e37-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="14e37-153"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="14e37-153"><dt>Commctrl.h</dt></span></span> </dl> |



 

