---
title: Message WM_CAP_FILE_GET_CAPTURE_FILE (VFW. h)
description: Le \_ message WM Cap \_ file \_ obtenir \_ \_ un fichier de capture renvoie le nom du fichier de capture actuel. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capFileGetCaptureFile.
ms.assetid: 86ce2904-834d-449f-9ef8-5a158c55bbaa
keywords:
- Message WM_CAP_FILE_GET_CAPTURE_FILE Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_FILE_GET_CAPTURE_FILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7008e0b217f29ad9602afbdc41cc97f9cb7ecaa3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843186"
---
# <a name="wm_cap_file_get_capture_file-message"></a><span data-ttu-id="0f872-105">Message de capture de fichier de la \_ \_ file d' \_ \_ \_ attente WM</span><span class="sxs-lookup"><span data-stu-id="0f872-105">WM\_CAP\_FILE\_GET\_CAPTURE\_FILE message</span></span>

<span data-ttu-id="0f872-106">Le message **WM \_ Cap \_ file obtenir un \_ \_ \_ fichier de capture** renvoie le nom du fichier de capture actuel.</span><span class="sxs-lookup"><span data-stu-id="0f872-106">The **WM\_CAP\_FILE\_GET\_CAPTURE\_FILE** message returns the name of the current capture file.</span></span> <span data-ttu-id="0f872-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capFileGetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) .</span><span class="sxs-lookup"><span data-stu-id="0f872-107">You can send this message explicitly or by using the [**capFileGetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) macro.</span></span>


```C++
WM_CAP_FILE_GET_CAPTURE_FILE 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="0f872-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f872-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f872-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="0f872-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="0f872-110">Taille, en octets, de la mémoire tampon définie par l’application référencée par **szName**.</span><span class="sxs-lookup"><span data-stu-id="0f872-110">Size, in bytes, of the application-defined buffer referenced by **szName**.</span></span>

</dd> <dt>

<span data-ttu-id="0f872-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="0f872-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="0f872-112">Pointeur vers une mémoire tampon définie par l’application utilisée pour retourner le nom du fichier de capture sous la forme d’une chaîne terminée par le caractère null.</span><span class="sxs-lookup"><span data-stu-id="0f872-112">Pointer to an application-defined buffer used to return the name of the capture file as a null-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f872-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0f872-113">Return Value</span></span>

<span data-ttu-id="0f872-114">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="0f872-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f872-115">Notes</span><span class="sxs-lookup"><span data-stu-id="0f872-115">Remarks</span></span>

<span data-ttu-id="0f872-116">Le nom de fichier de capture par défaut est C : \\CAPTURE.AVI.</span><span class="sxs-lookup"><span data-stu-id="0f872-116">The default capture filename is C:\\CAPTURE.AVI.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f872-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f872-117">Requirements</span></span>



| <span data-ttu-id="0f872-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f872-118">Requirement</span></span> | <span data-ttu-id="0f872-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f872-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0f872-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f872-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0f872-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f872-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0f872-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f872-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0f872-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f872-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0f872-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="0f872-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f872-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f872-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f872-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f872-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f872-127">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="0f872-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="0f872-128">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="0f872-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





