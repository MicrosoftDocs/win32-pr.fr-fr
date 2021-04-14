---
title: Message WM_CAP_DRIVER_GET_CAPS (VFW. h)
description: Le \_ message WM Cap \_ Driver to Cap \_ \_ retourne les fonctionnalités matérielles du pilote de capture actuellement connecté à une fenêtre de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capDriverGetCaps.
ms.assetid: 898a800c-1109-47cd-bcc9-cb61d86a4a2e
keywords:
- Message WM_CAP_DRIVER_GET_CAPS Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_CAPS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 027e530be82c76afebc343ceebe4905daef9b126
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509362"
---
# <a name="wm_cap_driver_get_caps-message"></a><span data-ttu-id="05743-105">Message d’accès aux \_ \_ \_ majuscules du pilote WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="05743-105">WM\_CAP\_DRIVER\_GET\_CAPS message</span></span>

<span data-ttu-id="05743-106">Le message **WM \_ Cap Driver to Cap \_ \_ \_** retourne les fonctionnalités matérielles du pilote de capture actuellement connecté à une fenêtre de capture.</span><span class="sxs-lookup"><span data-stu-id="05743-106">The **WM\_CAP\_DRIVER\_GET\_CAPS** message returns the hardware capabilities of the capture driver currently connected to a capture window.</span></span> <span data-ttu-id="05743-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) .</span><span class="sxs-lookup"><span data-stu-id="05743-107">You can send this message explicitly or by using the [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) macro.</span></span>


```C++
WM_CAP_DRIVER_GET_CAPS 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPDRIVERCAPS) (psCaps); 
```



## <a name="parameters"></a><span data-ttu-id="05743-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05743-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05743-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="05743-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="05743-110">Taille, en octets, de la structure référencée par **s**.</span><span class="sxs-lookup"><span data-stu-id="05743-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="05743-111"><span id="psCaps"></span><span id="pscaps"></span><span id="PSCAPS"></span>*psCaps*</span><span class="sxs-lookup"><span data-stu-id="05743-111"><span id="psCaps"></span><span id="pscaps"></span><span id="PSCAPS"></span>*psCaps*</span></span>
</dt> <dd>

<span data-ttu-id="05743-112">Pointeur vers la structure [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) pour contenir les fonctionnalités matérielles.</span><span class="sxs-lookup"><span data-stu-id="05743-112">Pointer to the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure to contain the hardware capabilities.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05743-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="05743-113">Return Value</span></span>

<span data-ttu-id="05743-114">Retourne la **valeur true** en cas de réussite ou **false** si la fenêtre de capture n’est pas connectée à un pilote de capture.</span><span class="sxs-lookup"><span data-stu-id="05743-114">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="remarks"></a><span data-ttu-id="05743-115">Notes</span><span class="sxs-lookup"><span data-stu-id="05743-115">Remarks</span></span>

<span data-ttu-id="05743-116">Les fonctionnalités retournées dans [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) sont constantes pour un pilote de capture donné.</span><span class="sxs-lookup"><span data-stu-id="05743-116">The capabilities returned in [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) are constant for a given capture driver.</span></span> <span data-ttu-id="05743-117">Les applications doivent récupérer ces informations une seule fois lorsque le pilote de capture est connecté pour la première fois à une fenêtre de capture.</span><span class="sxs-lookup"><span data-stu-id="05743-117">Applications need to retrieve this information once when the capture driver is first connected to a capture window.</span></span>

## <a name="requirements"></a><span data-ttu-id="05743-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05743-118">Requirements</span></span>



| <span data-ttu-id="05743-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05743-119">Requirement</span></span> | <span data-ttu-id="05743-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="05743-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="05743-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05743-121">Minimum supported client</span></span><br/> | <span data-ttu-id="05743-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05743-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="05743-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05743-123">Minimum supported server</span></span><br/> | <span data-ttu-id="05743-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05743-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="05743-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="05743-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="05743-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="05743-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05743-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05743-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05743-128">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="05743-128">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="05743-129">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="05743-129">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





