---
description: Message qui est envoyé à toutes les fenêtres de niveau supérieur lorsque la fonction SystemParametersInfo modifie un paramètre à l’échelle du système ou lorsque les paramètres de stratégie ont été modifiés.
ms.assetid: 77174e06-a25b-440a-9e9c-4fd5979c433c
title: Message WM_SETTINGCHANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1c3d1360b5e4cc5de2dbd23b09b8f2ad034948f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210459"
---
# <a name="wm_settingchange-message"></a><span data-ttu-id="e7f63-103">\_Message WM SETTINGCHANGE</span><span class="sxs-lookup"><span data-stu-id="e7f63-103">WM\_SETTINGCHANGE message</span></span>

<span data-ttu-id="e7f63-104">Message qui est envoyé à toutes les fenêtres de niveau supérieur lorsque la fonction [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) modifie un paramètre à l’échelle du système ou lorsque les paramètres de stratégie ont été modifiés.</span><span class="sxs-lookup"><span data-stu-id="e7f63-104">A message that is sent to all top-level windows when the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function changes a system-wide setting or when policy settings have changed.</span></span>

<span data-ttu-id="e7f63-105">Les applications doivent envoyer **WM \_ SETTINGCHANGE** à toutes les fenêtres de niveau supérieur lorsqu’elles apportent des modifications aux paramètres système.</span><span class="sxs-lookup"><span data-stu-id="e7f63-105">Applications should send **WM\_SETTINGCHANGE** to all top-level windows when they make changes to system parameters.</span></span> <span data-ttu-id="e7f63-106">(Ce message ne peut pas être envoyé directement à une fenêtre.) Pour envoyer le **message \_ WM SETTINGCHANGE** à toutes les fenêtres de niveau supérieur, utilisez la fonction [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) avec le paramètre *HWND* défini **sur \_ Broadcast HWND**.</span><span class="sxs-lookup"><span data-stu-id="e7f63-106">(This message cannot be sent directly to a window.) To send the **WM\_SETTINGCHANGE** message to all top-level windows, use the [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) function with the *hwnd* parameter set to **HWND\_BROADCAST**.</span></span>

<span data-ttu-id="e7f63-107">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e7f63-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_WININICHANGE                 0x001A
#define WM_SETTINGCHANGE                WM_WININICHANGE
```



## <a name="parameters"></a><span data-ttu-id="e7f63-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7f63-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7f63-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e7f63-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7f63-110">Lorsque le système envoie ce message à la suite d’un appel [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) , le paramètre *wParam* est la valeur du paramètre *UiAction* passé à la fonction **SystemParametersInfo** .</span><span class="sxs-lookup"><span data-stu-id="e7f63-110">When the system sends this message as a result of a [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) call, the *wParam* parameter is the value of the *uiAction* parameter passed to the **SystemParametersInfo** function.</span></span> <span data-ttu-id="e7f63-111">Pour obtenir la liste des valeurs, consultez **SystemParametersInfo**.</span><span class="sxs-lookup"><span data-stu-id="e7f63-111">For a list of values, see **SystemParametersInfo**.</span></span>

<span data-ttu-id="e7f63-112">Lorsque le système envoie ce message suite à une modification des paramètres de stratégie, ce paramètre indique le type de stratégie qui a été appliqué.</span><span class="sxs-lookup"><span data-stu-id="e7f63-112">When the system sends this message as a result of a change in policy settings, this parameter indicates the type of policy that was applied.</span></span> <span data-ttu-id="e7f63-113">Cette valeur est 1 si la stratégie de l’ordinateur a été appliquée ou zéro si la stratégie de l’utilisateur a été appliquée.</span><span class="sxs-lookup"><span data-stu-id="e7f63-113">This value is 1 if computer policy was applied or zero if user policy was applied.</span></span>

<span data-ttu-id="e7f63-114">Lorsque le système envoie ce message suite à une modification des paramètres régionaux, ce paramètre est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="e7f63-114">When the system sends this message as a result of a change in locale settings, this parameter is zero.</span></span>

<span data-ttu-id="e7f63-115">Quand une application envoie ce message, ce paramètre doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="e7f63-115">When an application sends this message, this parameter must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e7f63-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e7f63-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7f63-117">Quand le système envoie ce message à la suite d’un appel [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) , *lParam* est un pointeur vers une chaîne qui indique la zone contenant le paramètre système qui a été modifié.</span><span class="sxs-lookup"><span data-stu-id="e7f63-117">When the system sends this message as a result of a [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) call, *lParam* is a pointer to a string that indicates the area containing the system parameter that was changed.</span></span> <span data-ttu-id="e7f63-118">Ce paramètre n’indique généralement pas le paramètre système spécifique modifié.</span><span class="sxs-lookup"><span data-stu-id="e7f63-118">This parameter does not usually indicate which specific system parameter changed.</span></span> <span data-ttu-id="e7f63-119">(Notez que certaines applications envoient ce message avec *lParam* défini sur **null**.) En général, lorsque vous recevez ce message, vous devez vérifier et recharger les paramètres système qui sont utilisés par votre application.</span><span class="sxs-lookup"><span data-stu-id="e7f63-119">(Note that some applications send this message with *lParam* set to **NULL**.) In general, when you receive this message, you should check and reload any system parameter settings that are used by your application.</span></span>

<span data-ttu-id="e7f63-120">Cette chaîne peut être le nom d’une clé de registre ou le nom d’une section dans le fichier Win.ini.</span><span class="sxs-lookup"><span data-stu-id="e7f63-120">This string can be the name of a registry key or the name of a section in the Win.ini file.</span></span> <span data-ttu-id="e7f63-121">Lorsque la chaîne est un nom de Registre, elle indique généralement uniquement le nœud terminal dans le registre, et non le chemin d’accès complet.</span><span class="sxs-lookup"><span data-stu-id="e7f63-121">When the string is a registry name, it typically indicates only the leaf node in the registry, not the full path.</span></span>

<span data-ttu-id="e7f63-122">Lorsque le système envoie ce message suite à une modification des paramètres de stratégie, ce paramètre pointe vers la chaîne « stratégie ».</span><span class="sxs-lookup"><span data-stu-id="e7f63-122">When the system sends this message as a result of a change in policy settings, this parameter points to the string "Policy".</span></span>

<span data-ttu-id="e7f63-123">Lorsque le système envoie ce message suite à une modification des paramètres régionaux, ce paramètre pointe vers la chaîne « Intl ».</span><span class="sxs-lookup"><span data-stu-id="e7f63-123">When the system sends this message as a result of a change in locale settings, this parameter points to the string "intl".</span></span>

<span data-ttu-id="e7f63-124">Pour appliquer une modification dans les variables d’environnement du système ou de l’utilisateur, diffusez ce message avec *lParam* défini sur la chaîne « environnement ».</span><span class="sxs-lookup"><span data-stu-id="e7f63-124">To effect a change in the environment variables for the system or the user, broadcast this message with *lParam* set to the string "Environment".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7f63-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e7f63-125">Return value</span></span>

<span data-ttu-id="e7f63-126">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="e7f63-126">Type: **LRESULT**</span></span>

<span data-ttu-id="e7f63-127">Si vous traitez ce message, retournez zéro.</span><span class="sxs-lookup"><span data-stu-id="e7f63-127">If you process this message, return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7f63-128">Notes</span><span class="sxs-lookup"><span data-stu-id="e7f63-128">Remarks</span></span>

<span data-ttu-id="e7f63-129">Le paramètre *lParam* indique quelle mesure système a changé, par exemple « ConvertibleSlateMode » si l’indicateur ConvertibleSlateMode a été activé ou « SystemDockMode » si l’indicateur ancré a été activé.</span><span class="sxs-lookup"><span data-stu-id="e7f63-129">The *lParam* parameter indicates which system metric has changed, for example, "ConvertibleSlateMode" if the CONVERTIBLESLATEMODE indicator was toggled or "SystemDockMode" if the DOCKED indicator was toggled.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7f63-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7f63-130">Requirements</span></span>



| <span data-ttu-id="e7f63-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7f63-131">Requirement</span></span> | <span data-ttu-id="e7f63-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7f63-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7f63-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7f63-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e7f63-134">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7f63-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e7f63-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7f63-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e7f63-136">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7f63-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e7f63-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="e7f63-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7f63-138"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e7f63-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7f63-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7f63-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7f63-140">Événements de stratégie</span><span class="sxs-lookup"><span data-stu-id="e7f63-140">Policy Events</span></span>](/previous-versions/windows/desktop/Policy/policy-events)
</dt> <dt>

[<span data-ttu-id="e7f63-141">**SendMessageTimeout**</span><span class="sxs-lookup"><span data-stu-id="e7f63-141">**SendMessageTimeout**</span></span>](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta)
</dt> <dt>

[<span data-ttu-id="e7f63-142">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="e7f63-142">**SystemParametersInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

 
