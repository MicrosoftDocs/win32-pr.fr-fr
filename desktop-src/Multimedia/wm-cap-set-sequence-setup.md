---
title: Message WM_CAP_SET_SEQUENCE_SETUP (VFW. h)
description: Le \_ \_ message d’installation de la séquence WM Cap Set \_ \_ définit les paramètres de configuration utilisés avec la capture de streaming. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capCaptureSetSetup.
ms.assetid: ba9adb26-6627-469b-a836-f4f277ddb7c4
keywords:
- Message WM_CAP_SET_SEQUENCE_SETUP Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_SEQUENCE_SETUP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54a2129021f31694d9e601ecd97503e2a5f5c925
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509358"
---
# <a name="wm_cap_set_sequence_setup-message"></a><span data-ttu-id="d853e-105">\_ \_ \_ \_ Message d’installation de la séquence de définition de l’embout WM</span><span class="sxs-lookup"><span data-stu-id="d853e-105">WM\_CAP\_SET\_SEQUENCE\_SETUP message</span></span>

<span data-ttu-id="d853e-106">Le **message \_ \_ \_ \_ d’installation de la séquence WM Cap Set** définit les paramètres de configuration utilisés avec la capture de streaming.</span><span class="sxs-lookup"><span data-stu-id="d853e-106">The **WM\_CAP\_SET\_SEQUENCE\_SETUP** message sets the configuration parameters used with streaming capture.</span></span> <span data-ttu-id="d853e-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) .</span><span class="sxs-lookup"><span data-stu-id="d853e-107">You can send this message explicitly or by using the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro.</span></span>


```C++
WM_CAP_SET_SEQUENCE_SETUP 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPTUREPARMS) (psCapParms); 
```



## <a name="parameters"></a><span data-ttu-id="d853e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d853e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d853e-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="d853e-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="d853e-110">Taille, en octets, de la structure référencée par **s**.</span><span class="sxs-lookup"><span data-stu-id="d853e-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="d853e-111"><span id="psCapParms"></span><span id="pscapparms"></span><span id="PSCAPPARMS"></span>*psCapParms*</span><span class="sxs-lookup"><span data-stu-id="d853e-111"><span id="psCapParms"></span><span id="pscapparms"></span><span id="PSCAPPARMS"></span>*psCapParms*</span></span>
</dt> <dd>

<span data-ttu-id="d853e-112">Pointeur vers une structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="d853e-112">Pointer to a [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d853e-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d853e-113">Return Value</span></span>

<span data-ttu-id="d853e-114">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d853e-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d853e-115">Notes</span><span class="sxs-lookup"><span data-stu-id="d853e-115">Remarks</span></span>

<span data-ttu-id="d853e-116">Pour plus d’informations sur les paramètres utilisés pour contrôler la capture de la diffusion en continu, consultez la structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="d853e-116">For information about the parameters used to control streaming capture, see the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="d853e-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d853e-117">Requirements</span></span>



| <span data-ttu-id="d853e-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d853e-118">Requirement</span></span> | <span data-ttu-id="d853e-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d853e-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d853e-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d853e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d853e-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d853e-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d853e-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d853e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d853e-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d853e-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d853e-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="d853e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d853e-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d853e-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d853e-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d853e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d853e-127">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="d853e-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="d853e-128">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="d853e-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





