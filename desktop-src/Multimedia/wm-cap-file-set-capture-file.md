---
title: Message WM_CAP_FILE_SET_CAPTURE_FILE (VFW. h)
description: Le message du fichier \_ \_ \_ de capture du jeu de fichiers WM Cap \_ \_ désigne le fichier utilisé pour la capture vidéo. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capFileSetCaptureFile.
ms.assetid: d96e498b-6322-4d48-a5d7-156e95f23740
keywords:
- Message WM_CAP_FILE_SET_CAPTURE_FILE Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SET_CAPTURE_FILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12b3f59edfc9bf01f6bd2af3b9028f8e3315e2de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941646"
---
# <a name="wm_cap_file_set_capture_file-message"></a><span data-ttu-id="603b1-105">\_Message du \_ \_ fichier de capture du jeu de fichiers de \_ l’embout WM \_</span><span class="sxs-lookup"><span data-stu-id="603b1-105">WM\_CAP\_FILE\_SET\_CAPTURE\_FILE message</span></span>

<span data-ttu-id="603b1-106">Le message du fichier de **\_ capture du jeu de \_ fichiers \_ \_ \_ WM Cap** désigne le fichier utilisé pour la capture vidéo.</span><span class="sxs-lookup"><span data-stu-id="603b1-106">The **WM\_CAP\_FILE\_SET\_CAPTURE\_FILE** message names the file used for video capture.</span></span> <span data-ttu-id="603b1-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) .</span><span class="sxs-lookup"><span data-stu-id="603b1-107">You can send this message explicitly or by using the [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) macro.</span></span>


```C++
WM_CAP_FILE_SET_CAPTURE_FILE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="603b1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="603b1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="603b1-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="603b1-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="603b1-110">Pointeur vers la chaîne terminée par le caractère null qui contient le nom du fichier de capture à utiliser.</span><span class="sxs-lookup"><span data-stu-id="603b1-110">Pointer to the null-terminated string that contains the name of the capture file to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="603b1-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="603b1-111">Return Value</span></span>

<span data-ttu-id="603b1-112">Retourne la **valeur true** en cas de réussite ou **false** si le nom de fichier n’est pas valide, ou si la diffusion en continu ou la capture de frame unique est en cours.</span><span class="sxs-lookup"><span data-stu-id="603b1-112">Returns **TRUE** if successful or **FALSE** if the filename is invalid, or if streaming or single-frame capture is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="603b1-113">Notes</span><span class="sxs-lookup"><span data-stu-id="603b1-113">Remarks</span></span>

<span data-ttu-id="603b1-114">Ce message stocke le nom de fichier dans une structure interne.</span><span class="sxs-lookup"><span data-stu-id="603b1-114">This message stores the filename in an internal structure.</span></span> <span data-ttu-id="603b1-115">Il ne crée pas, n’alloue pas ou n’ouvre pas le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="603b1-115">It does not create, allocate, or open the specified file.</span></span> <span data-ttu-id="603b1-116">Le nom de fichier de capture par défaut est C : \\CAPTURE.AVI.</span><span class="sxs-lookup"><span data-stu-id="603b1-116">The default capture filename is C:\\CAPTURE.AVI.</span></span>

## <a name="requirements"></a><span data-ttu-id="603b1-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="603b1-117">Requirements</span></span>



| <span data-ttu-id="603b1-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="603b1-118">Requirement</span></span> | <span data-ttu-id="603b1-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="603b1-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="603b1-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="603b1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="603b1-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="603b1-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="603b1-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="603b1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="603b1-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="603b1-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="603b1-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="603b1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="603b1-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="603b1-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="603b1-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="603b1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="603b1-127">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="603b1-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="603b1-128">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="603b1-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





