---
title: Message WM_POINTERDEVICEOUTOFRANGE
description: Envoyé à une fenêtre lorsqu’un appareil de pointeur a fait l’ensemble de la plage d’un numériseur d’entrée. Ce message contient des informations relatives à l’appareil et à sa proximité.
ms.assetid: 6BC667C1-6D9A-4E69-BAC6-761A1859F09E
keywords:
- WM_POINTERDEVICEOUTOFRANGE les messages d’entrée du message et les notifications
topic_type:
- apiref
api_name:
- WM_POINTERDEVICEOUTOFRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: c222d9a35cae89838d7b6e1d99dcecd11f85b54d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103389"
---
# <a name="wm_pointerdeviceoutofrange-message"></a><span data-ttu-id="03d34-105">Message WM_POINTERDEVICEOUTOFRANGE</span><span class="sxs-lookup"><span data-stu-id="03d34-105">WM_POINTERDEVICEOUTOFRANGE message</span></span>

<span data-ttu-id="03d34-106">Envoyé à une fenêtre lorsqu’un appareil de pointeur a fait l’ensemble de la plage d’un numériseur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="03d34-106">Sent to a window when a pointer device has departed the range of an input digitizer.</span></span> <span data-ttu-id="03d34-107">Ce message contient des informations relatives à l’appareil et à sa proximité.</span><span class="sxs-lookup"><span data-stu-id="03d34-107">This message contains information regarding the device and its proximity.</span></span>

> <span data-ttu-id="03d34-108">\[! Précieuse\]</span><span class="sxs-lookup"><span data-stu-id="03d34-108">\[!Important\]</span></span>  
> <span data-ttu-id="03d34-109">Les applications de bureau doivent prendre en charge DPI.</span><span class="sxs-lookup"><span data-stu-id="03d34-109">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="03d34-110">Si votre application n’a pas de prise en charge DPI, les coordonnées d’écran contenues dans les messages de pointeur et les structures associées peuvent apparaître inexactes en raison de la virtualisation DPI.</span><span class="sxs-lookup"><span data-stu-id="03d34-110">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="03d34-111">La virtualisation PPP offre une prise en charge de la mise à l’échelle automatique aux applications qui ne prennent pas en charge la fonction PPP et est active par défaut (les utilisateurs peuvent la désactiver).</span><span class="sxs-lookup"><span data-stu-id="03d34-111">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="03d34-112">Pour plus d’informations, consultez [écriture d’applications Win32 à haute résolution](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="03d34-112">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_POINTERDEVICEOUTOFRANGE       0X23A
```



## <a name="parameters"></a><span data-ttu-id="03d34-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="03d34-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03d34-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="03d34-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03d34-115">Informations supplémentaires spécifiques au message.</span><span class="sxs-lookup"><span data-stu-id="03d34-115">Additional message-specific information.</span></span>

</dd> <dt>

<span data-ttu-id="03d34-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="03d34-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03d34-117">Informations supplémentaires spécifiques au message.</span><span class="sxs-lookup"><span data-stu-id="03d34-117">Additional message-specific information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03d34-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="03d34-118">Return value</span></span>

<span data-ttu-id="03d34-119">Si l’application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="03d34-119">If the application processes this message, it should return zero.</span></span>

<span data-ttu-id="03d34-120">Si l’application ne traite pas ce message, elle doit appeler [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="03d34-120">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="requirements"></a><span data-ttu-id="03d34-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="03d34-121">Requirements</span></span>



| <span data-ttu-id="03d34-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="03d34-122">Requirement</span></span> | <span data-ttu-id="03d34-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="03d34-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03d34-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03d34-124">Minimum supported client</span></span><br/> | <span data-ttu-id="03d34-125">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="03d34-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="03d34-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03d34-126">Minimum supported server</span></span><br/> | <span data-ttu-id="03d34-127">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="03d34-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="03d34-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="03d34-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="03d34-129"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="03d34-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03d34-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03d34-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03d34-131">Messages</span><span class="sxs-lookup"><span data-stu-id="03d34-131">Messages</span></span>](messages.md)
</dt> </dl>

 

