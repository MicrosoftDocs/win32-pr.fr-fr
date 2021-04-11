---
title: Message MCIWNDM_GETDEVICEID (VFW. h)
description: Le \_ message MCIWNDM GETDEVICEID récupère l’identificateur du périphérique MCI actuellement ouvert à utiliser avec la fonction mciSendCommand. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetDeviceID.
ms.assetid: 188f15fa-579a-438e-a812-9a2b684127c0
keywords:
- Message MCIWNDM_GETDEVICEID Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETDEVICEID
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f2271b18dcf8f295594031ab2c7c80dd8dec06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032469"
---
# <a name="mciwndm_getdeviceid-message"></a><span data-ttu-id="27ee1-105">\_Message MCIWNDM GETDEVICEID</span><span class="sxs-lookup"><span data-stu-id="27ee1-105">MCIWNDM\_GETDEVICEID message</span></span>

<span data-ttu-id="27ee1-106">Le message **MCIWNDM \_ GETDEVICEID** récupère l’identificateur du périphérique MCI actuellement ouvert à utiliser avec la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="27ee1-106">The **MCIWNDM\_GETDEVICEID** message retrieves the identifier of the currently open MCI device to use with the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span> <span data-ttu-id="27ee1-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) .</span><span class="sxs-lookup"><span data-stu-id="27ee1-107">You can send this message explicitly or by using the [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) macro.</span></span>


```C++
MCIWNDM_GETDEVICEID 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="27ee1-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="27ee1-108">Return Value</span></span>

<span data-ttu-id="27ee1-109">Retourne l’identificateur de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="27ee1-109">Returns the device identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="27ee1-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="27ee1-110">Requirements</span></span>



| <span data-ttu-id="27ee1-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="27ee1-111">Requirement</span></span> | <span data-ttu-id="27ee1-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="27ee1-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="27ee1-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="27ee1-113">Minimum supported client</span></span><br/> | <span data-ttu-id="27ee1-114">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="27ee1-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="27ee1-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="27ee1-115">Minimum supported server</span></span><br/> | <span data-ttu-id="27ee1-116">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="27ee1-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="27ee1-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="27ee1-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="27ee1-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="27ee1-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27ee1-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27ee1-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="27ee1-120">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="27ee1-120">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="27ee1-121">**MCIWndGetDeviceID**</span><span class="sxs-lookup"><span data-stu-id="27ee1-121">**MCIWndGetDeviceID**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid)
</dt> </dl>

 

