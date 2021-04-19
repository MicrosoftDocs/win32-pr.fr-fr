---
title: Message WM_POINTERDEVICECHANGE
description: Envoyé à une fenêtre en cas de modification des paramètres d’une analyse à laquelle un digitaliseur est attaché. Ce message contient des informations relatives à la mise à l’échelle du mode d’affichage.
ms.assetid: 9ED01D4C-58B4-4A21-B510-784281F9A909
keywords:
- WM_POINTERDEVICECHANGE les messages d’entrée du message et les notifications
topic_type:
- apiref
api_name:
- WM_POINTERDEVICECHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 38f570059f374f64e393e960a8458e605983d6c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106532051"
---
# <a name="wm_pointerdevicechange-message"></a><span data-ttu-id="acfda-105">Message WM_POINTERDEVICECHANGE</span><span class="sxs-lookup"><span data-stu-id="acfda-105">WM_POINTERDEVICECHANGE message</span></span>

<span data-ttu-id="acfda-106">Envoyé à une fenêtre en cas de modification des paramètres d’une analyse à laquelle un digitaliseur est attaché.</span><span class="sxs-lookup"><span data-stu-id="acfda-106">Sent to a window when there is a change in the settings of a monitor that has a digitizer attached to it.</span></span> <span data-ttu-id="acfda-107">Ce message contient des informations relatives à la mise à l’échelle du mode d’affichage.</span><span class="sxs-lookup"><span data-stu-id="acfda-107">This message contains information regarding the scaling of the display mode.</span></span>

> <span data-ttu-id="acfda-108">\[! Précieuse\]</span><span class="sxs-lookup"><span data-stu-id="acfda-108">\[!Important\]</span></span>  
> <span data-ttu-id="acfda-109">Les applications de bureau doivent prendre en charge DPI.</span><span class="sxs-lookup"><span data-stu-id="acfda-109">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="acfda-110">Si votre application n’a pas de prise en charge DPI, les coordonnées d’écran contenues dans les messages de pointeur et les structures associées peuvent apparaître inexactes en raison de la virtualisation DPI.</span><span class="sxs-lookup"><span data-stu-id="acfda-110">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="acfda-111">La virtualisation PPP offre une prise en charge de la mise à l’échelle automatique aux applications qui ne prennent pas en charge la fonction PPP et est active par défaut (les utilisateurs peuvent la désactiver).</span><span class="sxs-lookup"><span data-stu-id="acfda-111">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="acfda-112">Pour plus d’informations, consultez [écriture d’applications Win32 à haute résolution](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="acfda-112">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_POINTERDEVICECHANGE       0X238
```



## <a name="parameters"></a><span data-ttu-id="acfda-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="acfda-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acfda-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="acfda-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="acfda-115">Contient une valeur des [**constantes de modification**](pointer-device-change-constants.md)de l’appareil du pointeur.</span><span class="sxs-lookup"><span data-stu-id="acfda-115">Contains a value from [**Pointer Device Change Constants**](pointer-device-change-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="acfda-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="acfda-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="acfda-117">Informations supplémentaires spécifiques au message.</span><span class="sxs-lookup"><span data-stu-id="acfda-117">Additional message-specific information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acfda-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="acfda-118">Return value</span></span>

<span data-ttu-id="acfda-119">Si l’application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="acfda-119">If the application processes this message, it should return zero.</span></span>

<span data-ttu-id="acfda-120">Si l’application ne traite pas ce message, elle doit appeler [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="acfda-120">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="requirements"></a><span data-ttu-id="acfda-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="acfda-121">Requirements</span></span>



| <span data-ttu-id="acfda-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="acfda-122">Requirement</span></span> | <span data-ttu-id="acfda-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="acfda-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acfda-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="acfda-124">Minimum supported client</span></span><br/> | <span data-ttu-id="acfda-125">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="acfda-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="acfda-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="acfda-126">Minimum supported server</span></span><br/> | <span data-ttu-id="acfda-127">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="acfda-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="acfda-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="acfda-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="acfda-129"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="acfda-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acfda-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="acfda-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acfda-131">Messages</span><span class="sxs-lookup"><span data-stu-id="acfda-131">Messages</span></span>](messages.md)
</dt> </dl>

 

