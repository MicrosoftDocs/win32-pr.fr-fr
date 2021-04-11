---
title: Message WM_CAP_GET_AUDIOFORMAT (VFW. h)
description: Le \_ message WM \_ Cap \_ AUDIOFORMAT obtient le format audio ou la taille du format audio. Vous pouvez envoyer ce message explicitement ou à l’aide des macros capGetAudioFormat et capGetAudioFormatSize.
ms.assetid: 25e58863-2b1e-4ed8-9f34-c39617a15bc1
keywords:
- Message WM_CAP_GET_AUDIOFORMAT Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GET_AUDIOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9508972c173c9e189bdc092a63d849adf3be739
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383847"
---
# <a name="wm_cap_get_audioformat-message"></a><span data-ttu-id="39b6f-105">Message WM d' \_ \_ extraction de \_ AUDIOFORMAT</span><span class="sxs-lookup"><span data-stu-id="39b6f-105">WM\_CAP\_GET\_AUDIOFORMAT message</span></span>

<span data-ttu-id="39b6f-106">Le **message \_ WM \_ Cap \_ AUDIOFORMAT** obtient le format audio ou la taille du format audio.</span><span class="sxs-lookup"><span data-stu-id="39b6f-106">The **WM\_CAP\_GET\_AUDIOFORMAT** message obtains the audio format or the size of the audio format.</span></span> <span data-ttu-id="39b6f-107">Vous pouvez envoyer ce message explicitement ou à l’aide des macros [**capGetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) et [**capGetAudioFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) .</span><span class="sxs-lookup"><span data-stu-id="39b6f-107">You can send this message explicitly or by using the [**capGetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) and [**capGetAudioFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) macros.</span></span>


```C++
WM_CAP_GET_AUDIOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPWAVEFORMATEX) (psAudioFormat); 
```



## <a name="parameters"></a><span data-ttu-id="39b6f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="39b6f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39b6f-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="39b6f-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="39b6f-110">Taille, en octets, de la structure référencée par **s**.</span><span class="sxs-lookup"><span data-stu-id="39b6f-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="39b6f-111"><span id="psAudioFormat"></span><span id="psaudioformat"></span><span id="PSAUDIOFORMAT"></span>*psAudioFormat*</span><span class="sxs-lookup"><span data-stu-id="39b6f-111"><span id="psAudioFormat"></span><span id="psaudioformat"></span><span id="PSAUDIOFORMAT"></span>*psAudioFormat*</span></span>
</dt> <dd>

<span data-ttu-id="39b6f-112">Pointeur vers une structure [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) , ou **null**.</span><span class="sxs-lookup"><span data-stu-id="39b6f-112">Pointer to a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure, or **NULL**.</span></span> <span data-ttu-id="39b6f-113">Si la valeur est **null**, la taille, en octets, nécessaire pour contenir la structure est retournée.</span><span class="sxs-lookup"><span data-stu-id="39b6f-113">If the value is **NULL**, the size, in bytes, required to hold the structure is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39b6f-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="39b6f-114">Return Value</span></span>

<span data-ttu-id="39b6f-115">Retourne la taille, en octets, du format audio.</span><span class="sxs-lookup"><span data-stu-id="39b6f-115">Returns the size, in bytes, of the audio format.</span></span>

## <a name="remarks"></a><span data-ttu-id="39b6f-116">Notes</span><span class="sxs-lookup"><span data-stu-id="39b6f-116">Remarks</span></span>

<span data-ttu-id="39b6f-117">Étant donné que les formats audio compressés varient en fonction de la taille requise, les applications doivent d’abord récupérer la taille, puis allouer de la mémoire et enfin demander les données de format audio.</span><span class="sxs-lookup"><span data-stu-id="39b6f-117">Because compressed audio formats vary in size requirements applications must first retrieve the size, then allocate memory, and finally request the audio format data.</span></span>

## <a name="requirements"></a><span data-ttu-id="39b6f-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39b6f-118">Requirements</span></span>



| <span data-ttu-id="39b6f-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39b6f-119">Requirement</span></span> | <span data-ttu-id="39b6f-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="39b6f-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="39b6f-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39b6f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="39b6f-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39b6f-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="39b6f-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39b6f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="39b6f-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39b6f-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="39b6f-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="39b6f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="39b6f-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="39b6f-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39b6f-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39b6f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39b6f-128">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="39b6f-128">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="39b6f-129">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="39b6f-129">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

