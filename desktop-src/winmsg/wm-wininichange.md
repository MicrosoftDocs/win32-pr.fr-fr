---
description: Une application envoie le \_ message WM WININICHANGE à toutes les fenêtres de niveau supérieur après avoir apporté une modification au fichier WIN.INI. La fonction SystemParametersInfo envoie ce message après qu’une application a utilisé la fonction pour modifier un paramètre dans WIN.INI.
ms.assetid: 402f8d71-ad52-486d-be26-8b41a3f22045
title: Message WM_WININICHANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b8db6c4794a8c1a572f61028d32eaeaf578d0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951141"
---
# <a name="wm_wininichange-message"></a><span data-ttu-id="dcf68-104">\_Message WM WININICHANGE</span><span class="sxs-lookup"><span data-stu-id="dcf68-104">WM\_WININICHANGE message</span></span>

<span data-ttu-id="dcf68-105">Une application envoie le message **WM \_ WININICHANGE** à toutes les fenêtres de niveau supérieur après avoir apporté une modification au fichier WIN.INI.</span><span class="sxs-lookup"><span data-stu-id="dcf68-105">An application sends the **WM\_WININICHANGE** message to all top-level windows after making a change to the WIN.INI file.</span></span> <span data-ttu-id="dcf68-106">La fonction [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) envoie ce message après qu’une application a utilisé la fonction pour modifier un paramètre dans WIN.INI.</span><span class="sxs-lookup"><span data-stu-id="dcf68-106">The [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function sends this message after an application uses the function to change a setting in WIN.INI.</span></span>

> [!Note]  
> <span data-ttu-id="dcf68-107">Le message **WM \_ WININICHANGE** est fourni uniquement à des fins de compatibilité avec les versions antérieures du système.</span><span class="sxs-lookup"><span data-stu-id="dcf68-107">The **WM\_WININICHANGE** message is provided only for compatibility with earlier versions of the system.</span></span> <span data-ttu-id="dcf68-108">Les applications doivent utiliser le message [**WM \_ SETTINGCHANGE**](wm-settingchange.md) .</span><span class="sxs-lookup"><span data-stu-id="dcf68-108">Applications should use the [**WM\_SETTINGCHANGE**](wm-settingchange.md) message.</span></span>

 

<span data-ttu-id="dcf68-109">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="dcf68-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_WININICHANGE                 0x001A
```



## <a name="parameters"></a><span data-ttu-id="dcf68-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dcf68-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcf68-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dcf68-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dcf68-112">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="dcf68-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dcf68-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dcf68-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dcf68-114">Pointeur vers une chaîne contenant le nom du paramètre système qui a été modifié.</span><span class="sxs-lookup"><span data-stu-id="dcf68-114">A pointer to a string containing the name of the system parameter that was changed.</span></span> <span data-ttu-id="dcf68-115">Par exemple, cette chaîne peut être le nom d’une clé de registre ou le nom d’une section dans le fichier Win.ini.</span><span class="sxs-lookup"><span data-stu-id="dcf68-115">For example, this string can be the name of a registry key or the name of a section in the Win.ini file.</span></span> <span data-ttu-id="dcf68-116">Ce paramètre n’est pas particulièrement utile pour déterminer quel paramètre système a changé.</span><span class="sxs-lookup"><span data-stu-id="dcf68-116">This parameter is not particularly useful in determining which system parameter changed.</span></span> <span data-ttu-id="dcf68-117">Par exemple, lorsque la chaîne est un nom de Registre, elle indique généralement uniquement le nœud terminal dans le registre, et non le chemin d’accès complet.</span><span class="sxs-lookup"><span data-stu-id="dcf68-117">For example, when the string is a registry name, it typically indicates only the leaf node in the registry, not the whole path.</span></span> <span data-ttu-id="dcf68-118">De plus, certaines applications envoient ce message avec *lParam* défini sur **null**.</span><span class="sxs-lookup"><span data-stu-id="dcf68-118">In addition, some applications send this message with *lParam* set to **NULL**.</span></span> <span data-ttu-id="dcf68-119">En général, lorsque vous recevez ce message, vous devez vérifier et recharger les paramètres système qui sont utilisés par votre application.</span><span class="sxs-lookup"><span data-stu-id="dcf68-119">In general, when you receive this message, you should check and reload any system parameter settings that are used by your application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcf68-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dcf68-120">Return value</span></span>

<span data-ttu-id="dcf68-121">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="dcf68-121">Type: **LRESULT**</span></span>

<span data-ttu-id="dcf68-122">Si vous traitez ce message, retournez zéro.</span><span class="sxs-lookup"><span data-stu-id="dcf68-122">If you process this message, return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcf68-123">Notes</span><span class="sxs-lookup"><span data-stu-id="dcf68-123">Remarks</span></span>

<span data-ttu-id="dcf68-124">Pour envoyer le **message \_ WM WININICHANGE** à toutes les fenêtres de niveau supérieur, utilisez la fonction [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) avec le paramètre *HWND* défini **sur \_ Broadcast HWND**.</span><span class="sxs-lookup"><span data-stu-id="dcf68-124">To send the **WM\_WININICHANGE** message to all top-level windows, use the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function with the *hWnd* parameter set to **HWND\_BROADCAST**.</span></span>

<span data-ttu-id="dcf68-125">Les appels aux fonctions qui modifient WIN.INI peuvent être mappés au registre à la place.</span><span class="sxs-lookup"><span data-stu-id="dcf68-125">Calls to functions that change WIN.INI may be mapped to the registry instead.</span></span> <span data-ttu-id="dcf68-126">Ce mappage se produit lorsque WIN.INI et que la section en cours de modification sont spécifiées dans le Registre sous la clé suivante :</span><span class="sxs-lookup"><span data-stu-id="dcf68-126">This mapping occurs when WIN.INI and the section being changed are specified in the registry under the following key:</span></span>

<span data-ttu-id="dcf68-127">**HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ IniFileMapping**</span><span class="sxs-lookup"><span data-stu-id="dcf68-127">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\IniFileMapping**</span></span>

<span data-ttu-id="dcf68-128">La modification de l’emplacement de stockage n’a aucun effet sur le comportement de ce message.</span><span class="sxs-lookup"><span data-stu-id="dcf68-128">The change in the storage location has no effect on the behavior of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcf68-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dcf68-129">Requirements</span></span>



| <span data-ttu-id="dcf68-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dcf68-130">Requirement</span></span> | <span data-ttu-id="dcf68-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="dcf68-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcf68-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dcf68-132">Minimum supported client</span></span><br/> | <span data-ttu-id="dcf68-133">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dcf68-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="dcf68-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dcf68-134">Minimum supported server</span></span><br/> | <span data-ttu-id="dcf68-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dcf68-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="dcf68-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="dcf68-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcf68-137"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dcf68-137"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcf68-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dcf68-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcf68-139">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="dcf68-139">**SystemParametersInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

 
