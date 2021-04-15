---
title: Message WM_CAP_FILE_SAVEDIB (VFW. h)
description: Le \_ message WM Cap \_ file \_ SAVEDIB copie le frame en cours dans un fichier DIB. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capFileSaveDIB.
ms.assetid: bf6d343b-9236-4e68-bbda-2ed6e197a5cb
keywords:
- Message WM_CAP_FILE_SAVEDIB Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SAVEDIB
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2155febfdac1b3f24133df47ce206c8e5ec33d3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466870"
---
# <a name="wm_cap_file_savedib-message"></a><span data-ttu-id="bd6ca-105">\_ \_ Message SAVEDIB de fichier de la file d' \_ attente WM</span><span class="sxs-lookup"><span data-stu-id="bd6ca-105">WM\_CAP\_FILE\_SAVEDIB message</span></span>

<span data-ttu-id="bd6ca-106">Le message **WM \_ Cap \_ file \_ SAVEDIB** copie le frame en cours dans un fichier DIB.</span><span class="sxs-lookup"><span data-stu-id="bd6ca-106">The **WM\_CAP\_FILE\_SAVEDIB** message copies the current frame to a DIB file.</span></span> <span data-ttu-id="bd6ca-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capFileSaveDIB**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib) .</span><span class="sxs-lookup"><span data-stu-id="bd6ca-107">You can send this message explicitly or by using the [**capFileSaveDIB**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib) macro.</span></span>


```C++
WM_CAP_FILE_SAVEDIB 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="bd6ca-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bd6ca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd6ca-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="bd6ca-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="bd6ca-110">Pointeur vers la chaîne terminée par le caractère null qui contient le nom du fichier DIB de destination.</span><span class="sxs-lookup"><span data-stu-id="bd6ca-110">Pointer to the null-terminated string that contains the name of the destination DIB file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd6ca-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bd6ca-111">Return Value</span></span>

<span data-ttu-id="bd6ca-112">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="bd6ca-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="bd6ca-113">Si une erreur se produit et qu’une fonction de rappel d’erreur est définie à l’aide du message d' [**\_ erreur WM Cap \_ Set \_ callback \_**](wm-cap-set-callback-error.md) , la fonction de rappel d’erreur est appelée.</span><span class="sxs-lookup"><span data-stu-id="bd6ca-113">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd6ca-114">Notes</span><span class="sxs-lookup"><span data-stu-id="bd6ca-114">Remarks</span></span>

<span data-ttu-id="bd6ca-115">Si le pilote de capture fournit des frames dans un format compressé, cet appel tente de décompresser le frame avant d’écrire le fichier.</span><span class="sxs-lookup"><span data-stu-id="bd6ca-115">If the capture driver supplies frames in a compressed format, this call attempts to decompress the frame before writing the file.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd6ca-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bd6ca-116">Requirements</span></span>



| <span data-ttu-id="bd6ca-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bd6ca-117">Requirement</span></span> | <span data-ttu-id="bd6ca-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="bd6ca-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bd6ca-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd6ca-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bd6ca-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bd6ca-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="bd6ca-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd6ca-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bd6ca-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bd6ca-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="bd6ca-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="bd6ca-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd6ca-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd6ca-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd6ca-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd6ca-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd6ca-126">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="bd6ca-126">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="bd6ca-127">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="bd6ca-127">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





