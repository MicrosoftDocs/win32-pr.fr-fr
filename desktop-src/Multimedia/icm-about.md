---
title: Message ICM_ABOUT (VFW. h)
description: Le \_ message ICM about notifie à un pilote de compression vidéo qu’il doit afficher sa boîte de dialogue à propos de ou interroge un pilote de compression vidéo pour déterminer s’il possède une boîte de dialogue à propos de. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICAbout.
ms.assetid: 6eca69a3-0463-48e6-befb-5003b7515e7d
keywords:
- Message ICM_ABOUT Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_ABOUT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1e03e88993ba1e345a3ea32a9de7adb2d63abe9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032331"
---
# <a name="icm_about-message"></a><span data-ttu-id="3d8f0-105">ICM \_ à propos du message</span><span class="sxs-lookup"><span data-stu-id="3d8f0-105">ICM\_ABOUT message</span></span>

<span data-ttu-id="3d8f0-106">Le message **ICM \_ about** notifie à un pilote de compression vidéo qu’il doit afficher sa boîte de dialogue à propos de ou interroge un pilote de compression vidéo pour déterminer s’il possède une boîte de dialogue à propos de.</span><span class="sxs-lookup"><span data-stu-id="3d8f0-106">The **ICM\_ABOUT** message notifies a video compression driver to display its About dialog box or queries a video compression driver to determine if it has an About dialog box.</span></span> <span data-ttu-id="3d8f0-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) .</span><span class="sxs-lookup"><span data-stu-id="3d8f0-107">You can send this message explicitly or by using the [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) macro.</span></span>


```C++
ICM_ABOUT 
wParam = (DWORD_PTR) (UINT_PTR) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="3d8f0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3d8f0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d8f0-109"><span id="hwnd"></span><span id="HWND"></span>*HWND*</span><span class="sxs-lookup"><span data-stu-id="3d8f0-109"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="3d8f0-110">Handle de la fenêtre parente de la boîte de dialogue affichée.</span><span class="sxs-lookup"><span data-stu-id="3d8f0-110">Handle to the parent window of the displayed dialog box.</span></span> <span data-ttu-id="3d8f0-111">Vous pouvez également déterminer si un pilote a une boîte de dialogue à propos de en spécifiant-1 dans ce paramètre, comme dans la macro [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) .</span><span class="sxs-lookup"><span data-stu-id="3d8f0-111">You can also determine if a driver has an About dialog box by specifying -1 in this parameter, as in the [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) macro.</span></span> <span data-ttu-id="3d8f0-112">Le pilote retourne ICERR \_ OK s’il possède une boîte de dialogue à propos de ou ICERR \_ non prise en charge dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="3d8f0-112">The driver returns ICERR\_OK if it has an About dialog box or ICERR\_UNSUPPORTED otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d8f0-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3d8f0-113">Return Value</span></span>

<span data-ttu-id="3d8f0-114">Retourne ICERR \_ OK si le pilote prend en charge ce message ou ICERR \_ non pris en charge dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="3d8f0-114">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d8f0-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3d8f0-115">Requirements</span></span>



| <span data-ttu-id="3d8f0-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3d8f0-116">Requirement</span></span> | <span data-ttu-id="3d8f0-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d8f0-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3d8f0-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d8f0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3d8f0-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3d8f0-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3d8f0-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d8f0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3d8f0-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3d8f0-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3d8f0-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="3d8f0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d8f0-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d8f0-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d8f0-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d8f0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d8f0-125">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="3d8f0-125">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="3d8f0-126">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="3d8f0-126">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





