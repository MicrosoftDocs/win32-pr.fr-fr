---
title: Message WM_CAP_DRIVER_CONNECT (VFW. h)
description: Le \_ message WM capuchon \_ Driver \_ Connect connecte une fenêtre de capture à un pilote de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capDriverConnect.
ms.assetid: 8804bb3c-d06c-4ddc-b116-3d292205a52d
keywords:
- Message WM_CAP_DRIVER_CONNECT Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_CONNECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d73fdeb89968926429f7225912e3d1b3b348e287
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384471"
---
# <a name="wm_cap_driver_connect-message"></a><span data-ttu-id="65dec-105">\_Message de \_ connexion du pilote WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="65dec-105">WM\_CAP\_DRIVER\_CONNECT message</span></span>

<span data-ttu-id="65dec-106">Le message **WM \_ capuchon \_ Driver \_ Connect** connecte une fenêtre de capture à un pilote de capture.</span><span class="sxs-lookup"><span data-stu-id="65dec-106">The **WM\_CAP\_DRIVER\_CONNECT** message connects a capture window to a capture driver.</span></span> <span data-ttu-id="65dec-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capDriverConnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) .</span><span class="sxs-lookup"><span data-stu-id="65dec-107">You can send this message explicitly or by using the [**capDriverConnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) macro.</span></span>


```C++
WM_CAP_DRIVER_CONNECT 
wParam = (WPARAM) (iIndex); 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="65dec-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65dec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65dec-109"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span><span class="sxs-lookup"><span data-stu-id="65dec-109"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span></span>
</dt> <dd>

<span data-ttu-id="65dec-110">Index du pilote de capture.</span><span class="sxs-lookup"><span data-stu-id="65dec-110">Index of the capture driver.</span></span> <span data-ttu-id="65dec-111">L’index peut être compris entre 0 et 9.</span><span class="sxs-lookup"><span data-stu-id="65dec-111">The index can range from 0 through 9.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65dec-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="65dec-112">Return Value</span></span>

<span data-ttu-id="65dec-113">Retourne la **valeur true** en cas de réussite ou **false** si le pilote de capture spécifié ne peut pas être connecté à la fenêtre de capture.</span><span class="sxs-lookup"><span data-stu-id="65dec-113">Returns **TRUE** if successful or **FALSE** if the specified capture driver cannot be connected to the capture window.</span></span>

## <a name="remarks"></a><span data-ttu-id="65dec-114">Notes</span><span class="sxs-lookup"><span data-stu-id="65dec-114">Remarks</span></span>

<span data-ttu-id="65dec-115">La connexion d’un pilote de capture à une fenêtre de capture déconnecte automatiquement tout pilote de capture précédemment connecté.</span><span class="sxs-lookup"><span data-stu-id="65dec-115">Connecting a capture driver to a capture window automatically disconnects any previously connected capture driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="65dec-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65dec-116">Requirements</span></span>



| <span data-ttu-id="65dec-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65dec-117">Requirement</span></span> | <span data-ttu-id="65dec-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="65dec-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="65dec-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65dec-119">Minimum supported client</span></span><br/> | <span data-ttu-id="65dec-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65dec-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="65dec-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65dec-121">Minimum supported server</span></span><br/> | <span data-ttu-id="65dec-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65dec-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="65dec-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="65dec-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="65dec-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="65dec-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65dec-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65dec-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65dec-126">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="65dec-126">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="65dec-127">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="65dec-127">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





