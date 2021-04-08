---
title: Message WM_CAP_SET_MCI_DEVICE (VFW. h)
description: Le \_ message WM Cap \_ Set \_ MCI \_ Device spécifie le nom du périphérique vidéo MCI à utiliser pour capturer les données. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capSetMCIDeviceName.
ms.assetid: 83fdf567-ceb2-45aa-8529-433a5c64ac0a
keywords:
- Message WM_CAP_SET_MCI_DEVICE Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_MCI_DEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86187f3357bf72866e05b497332454c10bcd2fd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740053"
---
# <a name="wm_cap_set_mci_device-message"></a><span data-ttu-id="aac94-105">Message de l' \_ appareil WM embout \_ Set \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="aac94-105">WM\_CAP\_SET\_MCI\_DEVICE message</span></span>

<span data-ttu-id="aac94-106">Le message **WM \_ Cap \_ Set \_ MCI \_ Device** spécifie le nom du périphérique vidéo MCI à utiliser pour capturer les données.</span><span class="sxs-lookup"><span data-stu-id="aac94-106">The **WM\_CAP\_SET\_MCI\_DEVICE** message specifies the name of the MCI video device to be used to capture data.</span></span> <span data-ttu-id="aac94-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capSetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capsetmcidevicename) .</span><span class="sxs-lookup"><span data-stu-id="aac94-107">You can send this message explicitly or by using the [**capSetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capsetmcidevicename) macro.</span></span>


```C++
WM_CAP_SET_MCI_DEVICE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="aac94-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aac94-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aac94-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="aac94-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="aac94-110">Pointeur vers une chaîne se terminant par un caractère null qui contient le nom de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="aac94-110">Pointer to a null-terminated string containing the name of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aac94-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="aac94-111">Return Value</span></span>

<span data-ttu-id="aac94-112">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="aac94-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="aac94-113">Notes</span><span class="sxs-lookup"><span data-stu-id="aac94-113">Remarks</span></span>

<span data-ttu-id="aac94-114">Ce message stocke le nom du périphérique MCI dans une structure interne.</span><span class="sxs-lookup"><span data-stu-id="aac94-114">This message stores the MCI device name in an internal structure.</span></span> <span data-ttu-id="aac94-115">Il n’ouvre pas ou n’accède pas à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="aac94-115">It does not open or access the device.</span></span> <span data-ttu-id="aac94-116">Le nom de périphérique par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="aac94-116">The default device name is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="aac94-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aac94-117">Requirements</span></span>



| <span data-ttu-id="aac94-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aac94-118">Requirement</span></span> | <span data-ttu-id="aac94-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="aac94-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="aac94-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aac94-120">Minimum supported client</span></span><br/> | <span data-ttu-id="aac94-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aac94-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="aac94-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aac94-122">Minimum supported server</span></span><br/> | <span data-ttu-id="aac94-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aac94-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="aac94-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="aac94-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="aac94-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="aac94-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aac94-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aac94-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aac94-127">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="aac94-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="aac94-128">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="aac94-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





