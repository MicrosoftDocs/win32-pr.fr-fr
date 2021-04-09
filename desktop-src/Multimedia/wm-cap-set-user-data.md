---
title: Message WM_CAP_SET_USER_DATA (VFW. h)
description: Le \_ message WM Cap \_ Set \_ User \_ Data associe une \_ valeur de données PTR longue à une fenêtre de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capSetUserData.
ms.assetid: 067502e3-f009-4cf2-b612-4a0b64624416
keywords:
- Message WM_CAP_SET_USER_DATA Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_USER_DATA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 542b8e49f740bfc265824947237841dede1f6065
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106108"
---
# <a name="wm_cap_set_user_data-message"></a><span data-ttu-id="62aac-105">\_Message WM Cap \_ Set \_ User \_ Data</span><span class="sxs-lookup"><span data-stu-id="62aac-105">WM\_CAP\_SET\_USER\_DATA message</span></span>

<span data-ttu-id="62aac-106">Le message **WM \_ Cap \_ Set \_ User \_ Data** associe une valeur de données **\_ ptr longue** à une fenêtre de capture.</span><span class="sxs-lookup"><span data-stu-id="62aac-106">The **WM\_CAP\_SET\_USER\_DATA** message associates a **LONG\_PTR** data value with a capture window.</span></span> <span data-ttu-id="62aac-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capSetUserData**](/windows/desktop/api/Vfw/nf-vfw-capsetuserdata) .</span><span class="sxs-lookup"><span data-stu-id="62aac-107">You can send this message explicitly or by using the [**capSetUserData**](/windows/desktop/api/Vfw/nf-vfw-capsetuserdata) macro.</span></span>


```C++
WM_CAP_SET_USER_DATA 
wParam = (WPARAM) 0; 
lParam = (LPARAM)lUser; 
```



## <a name="parameters"></a><span data-ttu-id="62aac-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="62aac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62aac-109"><span id="lUser"></span><span id="luser"></span><span id="LUSER"></span>*lUser*</span><span class="sxs-lookup"><span data-stu-id="62aac-109"><span id="lUser"></span><span id="luser"></span><span id="LUSER"></span>*lUser*</span></span>
</dt> <dd>

<span data-ttu-id="62aac-110">Valeur de données à associer à une fenêtre de capture.</span><span class="sxs-lookup"><span data-stu-id="62aac-110">Data value to associate with a capture window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62aac-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="62aac-111">Return Value</span></span>

<span data-ttu-id="62aac-112">Retourne la **valeur true** en cas de réussite ou **false** si la capture en continu est en cours.</span><span class="sxs-lookup"><span data-stu-id="62aac-112">Returns **TRUE** if successful or **FALSE** if streaming capture is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="62aac-113">Notes</span><span class="sxs-lookup"><span data-stu-id="62aac-113">Remarks</span></span>

<span data-ttu-id="62aac-114">En général, ce message est utilisé pour pointer vers un bloc de données associé à une fenêtre de capture.</span><span class="sxs-lookup"><span data-stu-id="62aac-114">Typically this message is used to point to a block of data associated with a capture window.</span></span>

## <a name="requirements"></a><span data-ttu-id="62aac-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="62aac-115">Requirements</span></span>



| <span data-ttu-id="62aac-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="62aac-116">Requirement</span></span> | <span data-ttu-id="62aac-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="62aac-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="62aac-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62aac-118">Minimum supported client</span></span><br/> | <span data-ttu-id="62aac-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="62aac-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="62aac-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62aac-120">Minimum supported server</span></span><br/> | <span data-ttu-id="62aac-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="62aac-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="62aac-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="62aac-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="62aac-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="62aac-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62aac-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62aac-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62aac-125">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="62aac-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="62aac-126">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="62aac-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





