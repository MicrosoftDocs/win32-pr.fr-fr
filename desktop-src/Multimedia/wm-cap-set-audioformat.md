---
title: Message WM_CAP_SET_AUDIOFORMAT (VFW. h)
description: Le \_ message WM Cap \_ Set \_ AUDIOFORMAT définit le format audio à utiliser lors de la diffusion en continu ou de l’étape de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capSetAudioFormat.
ms.assetid: 8bffa401-3d36-43bb-9f69-988ebc69b860
keywords:
- Message WM_CAP_SET_AUDIOFORMAT Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_AUDIOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c519ed936d2e71d9eee88435a94acc8c567a9a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104152"
---
# <a name="wm_cap_set_audioformat-message"></a><span data-ttu-id="91809-105">\_Message AUDIOFORMAT de l’ensemble de connexions WM \_ \_</span><span class="sxs-lookup"><span data-stu-id="91809-105">WM\_CAP\_SET\_AUDIOFORMAT message</span></span>

<span data-ttu-id="91809-106">Le message **WM \_ Cap \_ Set \_ AUDIOFORMAT** définit le format audio à utiliser lors de la diffusion en continu ou de l’étape de capture.</span><span class="sxs-lookup"><span data-stu-id="91809-106">The **WM\_CAP\_SET\_AUDIOFORMAT** message sets the audio format to use when performing streaming or step capture.</span></span> <span data-ttu-id="91809-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capSetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) .</span><span class="sxs-lookup"><span data-stu-id="91809-107">You can send this message explicitly or by using the [**capSetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) macro.</span></span>


```C++
WM_CAP_SET_AUDIOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPWAVEFORMATEX) (psAudioFormat); 
```



## <a name="parameters"></a><span data-ttu-id="91809-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91809-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91809-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="91809-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="91809-110">Taille, en octets, de la structure référencée par **s**.</span><span class="sxs-lookup"><span data-stu-id="91809-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="91809-111"><span id="psAudioFormat"></span><span id="psaudioformat"></span><span id="PSAUDIOFORMAT"></span>*psAudioFormat*</span><span class="sxs-lookup"><span data-stu-id="91809-111"><span id="psAudioFormat"></span><span id="psaudioformat"></span><span id="PSAUDIOFORMAT"></span>*psAudioFormat*</span></span>
</dt> <dd>

<span data-ttu-id="91809-112">Pointeur vers une structure [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) ou [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) qui définit le format audio.</span><span class="sxs-lookup"><span data-stu-id="91809-112">Pointer to a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) or [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) structure that defines the audio format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91809-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="91809-113">Return Value</span></span>

<span data-ttu-id="91809-114">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="91809-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="91809-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91809-115">Requirements</span></span>



| <span data-ttu-id="91809-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91809-116">Requirement</span></span> | <span data-ttu-id="91809-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="91809-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="91809-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91809-118">Minimum supported client</span></span><br/> | <span data-ttu-id="91809-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91809-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="91809-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91809-120">Minimum supported server</span></span><br/> | <span data-ttu-id="91809-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91809-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="91809-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="91809-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="91809-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="91809-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91809-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91809-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91809-125">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="91809-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="91809-126">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="91809-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

