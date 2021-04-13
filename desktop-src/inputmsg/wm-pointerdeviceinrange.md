---
title: Message WM_POINTERDEVICEINRANGE
description: Envoyé à une fenêtre lorsqu’un dispositif de pointage est détecté dans la plage d’un numériseur d’entrée. Ce message contient des informations relatives à l’appareil et à sa proximité.
ms.assetid: 04244758-E662-4FB2-850E-20B4B3D1294A
keywords:
- WM_POINTERDEVICEINRANGE les messages d’entrée du message et les notifications
topic_type:
- apiref
api_name:
- WM_POINTERDEVICEINRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 76ab6ac4f96d1df4e4e29afbcefe86d34b8b602d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509234"
---
# <a name="wm_pointerdeviceinrange-message"></a><span data-ttu-id="a536f-105">Message WM_POINTERDEVICEINRANGE</span><span class="sxs-lookup"><span data-stu-id="a536f-105">WM_POINTERDEVICEINRANGE message</span></span>

<span data-ttu-id="a536f-106">Envoyé à une fenêtre lorsqu’un dispositif de pointage est détecté dans la plage d’un numériseur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="a536f-106">Sent to a window when a pointer device is detected within range of an input digitizer.</span></span> <span data-ttu-id="a536f-107">Ce message contient des informations relatives à l’appareil et à sa proximité.</span><span class="sxs-lookup"><span data-stu-id="a536f-107">This message contains information regarding the device and its proximity.</span></span>

> <span data-ttu-id="a536f-108">\[! Précieuse\]</span><span class="sxs-lookup"><span data-stu-id="a536f-108">\[!Important\]</span></span>  
> <span data-ttu-id="a536f-109">Les applications de bureau doivent prendre en charge DPI.</span><span class="sxs-lookup"><span data-stu-id="a536f-109">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="a536f-110">Si votre application n’a pas de prise en charge DPI, les coordonnées d’écran contenues dans les messages de pointeur et les structures associées peuvent apparaître inexactes en raison de la virtualisation DPI.</span><span class="sxs-lookup"><span data-stu-id="a536f-110">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="a536f-111">La virtualisation PPP offre une prise en charge de la mise à l’échelle automatique aux applications qui ne prennent pas en charge la fonction PPP et est active par défaut (les utilisateurs peuvent la désactiver).</span><span class="sxs-lookup"><span data-stu-id="a536f-111">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="a536f-112">Pour plus d’informations, consultez [écriture d’applications Win32 à haute résolution](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a536f-112">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_POINTERDEVICEINRANGE       0X239
```



## <a name="parameters"></a><span data-ttu-id="a536f-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a536f-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a536f-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a536f-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a536f-115">Informations supplémentaires spécifiques au message.</span><span class="sxs-lookup"><span data-stu-id="a536f-115">Additional message-specific information.</span></span>

</dd> <dt>

<span data-ttu-id="a536f-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a536f-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a536f-117">Informations supplémentaires spécifiques au message.</span><span class="sxs-lookup"><span data-stu-id="a536f-117">Additional message-specific information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a536f-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a536f-118">Return value</span></span>

<span data-ttu-id="a536f-119">Si l’application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="a536f-119">If the application processes this message, it should return zero.</span></span>

<span data-ttu-id="a536f-120">Si l’application ne traite pas ce message, elle doit appeler [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="a536f-120">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="requirements"></a><span data-ttu-id="a536f-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a536f-121">Requirements</span></span>



| <span data-ttu-id="a536f-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a536f-122">Requirement</span></span> | <span data-ttu-id="a536f-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="a536f-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a536f-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a536f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a536f-125">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a536f-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="a536f-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a536f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a536f-127">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a536f-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a536f-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="a536f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a536f-129"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a536f-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a536f-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a536f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a536f-131">Messages</span><span class="sxs-lookup"><span data-stu-id="a536f-131">Messages</span></span>](messages.md)
</dt> </dl>

 

