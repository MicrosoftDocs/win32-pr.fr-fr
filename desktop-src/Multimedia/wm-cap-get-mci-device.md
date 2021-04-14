---
title: Message WM_CAP_GET_MCI_DEVICE (VFW. h)
description: Le \_ message WM \_ Cap \_ obtenir \_ un appareil MCI récupère le nom d’un périphérique MCI précédemment défini avec le \_ message WM Cap \_ Set \_ MCI \_ Device. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capGetMCIDeviceName.
ms.assetid: c5d7d955-ab6a-4959-b79e-9ff35a282ba2
keywords:
- Message WM_CAP_GET_MCI_DEVICE Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GET_MCI_DEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0960ff9aa1366802611f444383212c4bcc45bcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464211"
---
# <a name="wm_cap_get_mci_device-message"></a><span data-ttu-id="20be8-105">Message de l’appareil WM d’accès à \_ \_ \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="20be8-105">WM\_CAP\_GET\_MCI\_DEVICE message</span></span>

<span data-ttu-id="20be8-106">Le message **WM \_ Cap obtenir un \_ \_ \_ appareil MCI** récupère le nom d’un périphérique MCI précédemment défini avec le message [**WM \_ Cap \_ Set \_ MCI \_ Device**](wm-cap-set-mci-device.md) .</span><span class="sxs-lookup"><span data-stu-id="20be8-106">The **WM\_CAP\_GET\_MCI\_DEVICE** message retrieves the name of an MCI device previously set with the [**WM\_CAP\_SET\_MCI\_DEVICE**](wm-cap-set-mci-device.md) message.</span></span> <span data-ttu-id="20be8-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capGetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capgetmcidevicename) .</span><span class="sxs-lookup"><span data-stu-id="20be8-107">You can send this message explicitly or by using the [**capGetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capgetmcidevicename) macro.</span></span>


```C++
WM_CAP_GET_MCI_DEVICE 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="20be8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20be8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20be8-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="20be8-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="20be8-110">Longueur, en octets, de la mémoire tampon référencée par **szName**.</span><span class="sxs-lookup"><span data-stu-id="20be8-110">Length, in bytes, of the buffer referenced by **szName**.</span></span>

</dd> <dt>

<span data-ttu-id="20be8-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="20be8-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="20be8-112">Pointeur vers une chaîne se terminant par un caractère null qui contient le nom du périphérique MCI.</span><span class="sxs-lookup"><span data-stu-id="20be8-112">Pointer to a null-terminated string that contains the MCI device name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20be8-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="20be8-113">Return Value</span></span>

<span data-ttu-id="20be8-114">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="20be8-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="20be8-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20be8-115">Requirements</span></span>



| <span data-ttu-id="20be8-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20be8-116">Requirement</span></span> | <span data-ttu-id="20be8-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="20be8-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="20be8-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20be8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="20be8-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="20be8-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="20be8-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20be8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="20be8-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="20be8-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="20be8-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="20be8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="20be8-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="20be8-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20be8-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20be8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20be8-125">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="20be8-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="20be8-126">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="20be8-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





