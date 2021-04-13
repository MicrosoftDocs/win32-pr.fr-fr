---
title: Message WM_CAP_GET_USER_DATA (VFW. h)
description: Le \_ message WM Cap \_ obtenir des \_ \_ données utilisateur récupère une \_ valeur de données PTR longue associée à une fenêtre de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capGetUserData.
ms.assetid: f7c121ba-44a1-4916-b602-c53d8332c2af
keywords:
- Message WM_CAP_GET_USER_DATA Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GET_USER_DATA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02951667600acba115f506a610b167b72b69ea99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509146"
---
# <a name="wm_cap_get_user_data-message"></a><span data-ttu-id="46cdf-105">\_Message d' \_ extraction \_ de \_ données utilisateur de l’embout WM</span><span class="sxs-lookup"><span data-stu-id="46cdf-105">WM\_CAP\_GET\_USER\_DATA message</span></span>

<span data-ttu-id="46cdf-106">Le message **WM \_ Cap obtenir des \_ \_ \_ données utilisateur** récupère une valeur de données **\_ ptr longue** associée à une fenêtre de capture.</span><span class="sxs-lookup"><span data-stu-id="46cdf-106">The **WM\_CAP\_GET\_USER\_DATA** message retrieves a **LONG\_PTR** data value associated with a capture window.</span></span> <span data-ttu-id="46cdf-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capGetUserData**](/windows/desktop/api/Vfw/nf-vfw-capgetuserdata) .</span><span class="sxs-lookup"><span data-stu-id="46cdf-107">You can send this message explicitly or by using the [**capGetUserData**](/windows/desktop/api/Vfw/nf-vfw-capgetuserdata) macro.</span></span>


```C++
WM_CAP_GET_USER_DATA 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="46cdf-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="46cdf-108">Return Value</span></span>

<span data-ttu-id="46cdf-109">Retourne une valeur enregistrée précédemment à l’aide du message [**WM \_ embout \_ Set \_ User \_ Data**](wm-cap-set-user-data.md) .</span><span class="sxs-lookup"><span data-stu-id="46cdf-109">Returns a value previously saved by using the [**WM\_CAP\_SET\_USER\_DATA**](wm-cap-set-user-data.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="46cdf-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46cdf-110">Requirements</span></span>



| <span data-ttu-id="46cdf-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46cdf-111">Requirement</span></span> | <span data-ttu-id="46cdf-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="46cdf-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="46cdf-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46cdf-113">Minimum supported client</span></span><br/> | <span data-ttu-id="46cdf-114">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46cdf-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="46cdf-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46cdf-115">Minimum supported server</span></span><br/> | <span data-ttu-id="46cdf-116">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46cdf-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="46cdf-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="46cdf-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="46cdf-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="46cdf-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46cdf-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46cdf-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46cdf-120">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="46cdf-120">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="46cdf-121">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="46cdf-121">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





