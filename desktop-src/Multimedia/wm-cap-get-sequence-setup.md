---
title: Message WM_CAP_GET_SEQUENCE_SETUP (VFW. h)
description: Le \_ \_ \_ \_ message d’installation de la séquence de l’embout du programme WM récupère les paramètres actuels des paramètres de capture de streaming. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capCaptureGetSetup.
ms.assetid: 2220c92a-1994-4f15-9730-1cf01972dda6
keywords:
- Message WM_CAP_GET_SEQUENCE_SETUP Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GET_SEQUENCE_SETUP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5cd1585b165581f9c9646741b92c5dc841472ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941645"
---
# <a name="wm_cap_get_sequence_setup-message"></a><span data-ttu-id="2c404-105">\_ \_ \_ \_ Message d’installation de la séquence de l’embout WM</span><span class="sxs-lookup"><span data-stu-id="2c404-105">WM\_CAP\_GET\_SEQUENCE\_SETUP message</span></span>

<span data-ttu-id="2c404-106">Le **message \_ \_ \_ \_ d’installation** de la séquence de l’embout du programme WM récupère les paramètres actuels des paramètres de capture de streaming.</span><span class="sxs-lookup"><span data-stu-id="2c404-106">The **WM\_CAP\_GET\_SEQUENCE\_SETUP** message retrieves the current settings of the streaming capture parameters.</span></span> <span data-ttu-id="2c404-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) .</span><span class="sxs-lookup"><span data-stu-id="2c404-107">You can send this message explicitly or by using the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro.</span></span>


```C++
WM_CAP_GET_SEQUENCE_SETUP 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPTUREPARMS) (s); 
```



## <a name="parameters"></a><span data-ttu-id="2c404-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2c404-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c404-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="2c404-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="2c404-110">Taille, en octets, de la structure référencée par **s**.</span><span class="sxs-lookup"><span data-stu-id="2c404-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="2c404-111"><span id="s"></span><span id="S"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="2c404-111"><span id="s"></span><span id="S"></span>*s*</span></span>
</dt> <dd>

<span data-ttu-id="2c404-112">Pointeur vers une structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="2c404-112">Pointer to a [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c404-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2c404-113">Return Value</span></span>

<span data-ttu-id="2c404-114">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="2c404-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c404-115">Notes</span><span class="sxs-lookup"><span data-stu-id="2c404-115">Remarks</span></span>

<span data-ttu-id="2c404-116">Pour plus d’informations sur les paramètres utilisés pour contrôler la capture de la diffusion en continu, consultez la structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="2c404-116">For information about the parameters used to control streaming capture, see the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c404-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c404-117">Requirements</span></span>



| <span data-ttu-id="2c404-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c404-118">Requirement</span></span> | <span data-ttu-id="2c404-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c404-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2c404-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c404-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2c404-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c404-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2c404-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c404-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2c404-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c404-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2c404-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="2c404-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c404-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c404-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c404-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c404-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c404-127">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="2c404-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="2c404-128">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="2c404-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





