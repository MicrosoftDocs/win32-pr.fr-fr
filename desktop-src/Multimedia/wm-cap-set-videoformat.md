---
title: Message WM_CAP_SET_VIDEOFORMAT (VFW. h)
description: Le \_ message WM Cap \_ Set \_ VIDEOFORMAT définit le format des données de la vidéo capturée. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capSetVideoFormat.
ms.assetid: 4f9cf90d-7ccb-4fc7-aad5-3d7e082526be
keywords:
- Message WM_CAP_SET_VIDEOFORMAT Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ba6154ec1532bd83f482eb81a0e286795aa3341
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942793"
---
# <a name="wm_cap_set_videoformat-message"></a><span data-ttu-id="2c8d2-105">\_Message VIDEOFORMAT de l’ensemble de connexions WM \_ \_</span><span class="sxs-lookup"><span data-stu-id="2c8d2-105">WM\_CAP\_SET\_VIDEOFORMAT message</span></span>

<span data-ttu-id="2c8d2-106">Le message **WM \_ Cap \_ Set \_ VIDEOFORMAT** définit le format des données de la vidéo capturée.</span><span class="sxs-lookup"><span data-stu-id="2c8d2-106">The **WM\_CAP\_SET\_VIDEOFORMAT** message sets the format of captured video data.</span></span> <span data-ttu-id="2c8d2-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capSetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) .</span><span class="sxs-lookup"><span data-stu-id="2c8d2-107">You can send this message explicitly or by using the [**capSetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) macro.</span></span>


```C++
WM_CAP_SET_VIDEOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (psVideoFormat); 
```



## <a name="parameters"></a><span data-ttu-id="2c8d2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2c8d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c8d2-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="2c8d2-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="2c8d2-110">Taille, en octets, de la structure référencée par **s**.</span><span class="sxs-lookup"><span data-stu-id="2c8d2-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="2c8d2-111"><span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*psVideoFormat*</span><span class="sxs-lookup"><span data-stu-id="2c8d2-111"><span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*psVideoFormat*</span></span>
</dt> <dd>

<span data-ttu-id="2c8d2-112">Pointeur vers une structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) .</span><span class="sxs-lookup"><span data-stu-id="2c8d2-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c8d2-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2c8d2-113">Return Value</span></span>

<span data-ttu-id="2c8d2-114">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="2c8d2-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c8d2-115">Notes</span><span class="sxs-lookup"><span data-stu-id="2c8d2-115">Remarks</span></span>

<span data-ttu-id="2c8d2-116">Étant donné que les formats vidéo sont spécifiques à l’appareil, les applications doivent vérifier la valeur de retour de cette fonction pour déterminer si le format est accepté par le pilote.</span><span class="sxs-lookup"><span data-stu-id="2c8d2-116">Because video formats are device-specific, applications should check the return value from this function to determine if the format is accepted by the driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c8d2-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c8d2-117">Requirements</span></span>



| <span data-ttu-id="2c8d2-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c8d2-118">Requirement</span></span> | <span data-ttu-id="2c8d2-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c8d2-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2c8d2-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c8d2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2c8d2-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c8d2-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2c8d2-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c8d2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2c8d2-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c8d2-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2c8d2-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="2c8d2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c8d2-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c8d2-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c8d2-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c8d2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c8d2-127">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="2c8d2-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="2c8d2-128">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="2c8d2-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

