---
title: Message WM_CAP_GET_VIDEOFORMAT (VFW. h)
description: Le \_ message WM \_ Cap \_ VIDEOFORMAT récupère une copie du format vidéo utilisé ou la taille requise pour le format vidéo. Vous pouvez envoyer ce message explicitement ou à l’aide des macros capGetVideoFormat et capGetVideoFormatSize.
ms.assetid: ac72dfdb-fe1a-4007-bdce-41e5e67d076a
keywords:
- Message WM_CAP_GET_VIDEOFORMAT Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GET_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 072d71366efee550b037d4a20388817954937854
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942095"
---
# <a name="wm_cap_get_videoformat-message"></a><span data-ttu-id="57aa0-105">Message WM d' \_ \_ extraction de \_ VIDEOFORMAT</span><span class="sxs-lookup"><span data-stu-id="57aa0-105">WM\_CAP\_GET\_VIDEOFORMAT message</span></span>

<span data-ttu-id="57aa0-106">Le **message \_ WM \_ Cap \_ VIDEOFORMAT** récupère une copie du format vidéo utilisé ou la taille requise pour le format vidéo.</span><span class="sxs-lookup"><span data-stu-id="57aa0-106">The **WM\_CAP\_GET\_VIDEOFORMAT** message retrieves a copy of the video format in use or the size required for the video format.</span></span> <span data-ttu-id="57aa0-107">Vous pouvez envoyer ce message explicitement ou à l’aide des macros [**capGetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) et [**capGetVideoFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) .</span><span class="sxs-lookup"><span data-stu-id="57aa0-107">You can send this message explicitly or by using the [**capGetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) and [**capGetVideoFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) macros.</span></span>


```C++
WM_CAP_GET_VIDEOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (psVideoFormat); 
```



## <a name="parameters"></a><span data-ttu-id="57aa0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57aa0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57aa0-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="57aa0-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="57aa0-110">Taille, en octets, de la structure référencée par **s**.</span><span class="sxs-lookup"><span data-stu-id="57aa0-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="57aa0-111"><span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*psVideoFormat*</span><span class="sxs-lookup"><span data-stu-id="57aa0-111"><span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*psVideoFormat*</span></span>
</dt> <dd>

<span data-ttu-id="57aa0-112">Pointeur vers une structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) .</span><span class="sxs-lookup"><span data-stu-id="57aa0-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure.</span></span> <span data-ttu-id="57aa0-113">Vous pouvez également spécifier la **valeur null** pour récupérer le nombre d’octets nécessaires.</span><span class="sxs-lookup"><span data-stu-id="57aa0-113">You can also specify **NULL** to retrieve the number of bytes needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57aa0-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="57aa0-114">Return Value</span></span>

<span data-ttu-id="57aa0-115">Retourne la taille, en octets, du format vidéo ou zéro si la fenêtre de capture n’est pas connectée à un pilote de capture.</span><span class="sxs-lookup"><span data-stu-id="57aa0-115">Returns the size, in bytes, of the video format or zero if the capture window is not connected to a capture driver.</span></span> <span data-ttu-id="57aa0-116">Pour les formats vidéo qui nécessitent une palette, la palette active est également retournée.</span><span class="sxs-lookup"><span data-stu-id="57aa0-116">For video formats that require a palette, the current palette is also returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="57aa0-117">Notes</span><span class="sxs-lookup"><span data-stu-id="57aa0-117">Remarks</span></span>

<span data-ttu-id="57aa0-118">Étant donné que les formats vidéo compressés varient en fonction de la taille requise, les applications doivent d’abord récupérer la taille, puis allouer de la mémoire et enfin demander les données au format vidéo.</span><span class="sxs-lookup"><span data-stu-id="57aa0-118">Because compressed video formats vary in size requirements applications must first retrieve the size, then allocate memory, and finally request the video format data.</span></span>

## <a name="requirements"></a><span data-ttu-id="57aa0-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57aa0-119">Requirements</span></span>



| <span data-ttu-id="57aa0-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="57aa0-120">Requirement</span></span> | <span data-ttu-id="57aa0-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="57aa0-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="57aa0-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57aa0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="57aa0-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57aa0-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="57aa0-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57aa0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="57aa0-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57aa0-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="57aa0-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="57aa0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="57aa0-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="57aa0-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57aa0-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57aa0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57aa0-129">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="57aa0-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="57aa0-130">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="57aa0-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

