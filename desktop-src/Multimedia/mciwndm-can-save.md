---
title: Message MCIWNDM_CAN_SAVE (VFW. h)
description: Le MCIWNDM \_ peut \_ enregistrer un message détermine si un périphérique MCI peut enregistrer des données. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndCanSave.
ms.assetid: b4e27190-b095-494b-9ed3-10653bea187b
keywords:
- Message MCIWNDM_CAN_SAVE Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_SAVE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11b60b8a5d93ac80befc8beeb6665399efe44f1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464618"
---
# <a name="mciwndm_can_save-message"></a><span data-ttu-id="d3bd7-105">MCIWNDM \_ peut \_ enregistrer le message</span><span class="sxs-lookup"><span data-stu-id="d3bd7-105">MCIWNDM\_CAN\_SAVE message</span></span>

<span data-ttu-id="d3bd7-106">Le **MCIWNDM \_ peut \_ Enregistrer** un message détermine si un périphérique MCI peut enregistrer des données.</span><span class="sxs-lookup"><span data-stu-id="d3bd7-106">The **MCIWNDM\_CAN\_SAVE** message determines if an MCI device can save data.</span></span> <span data-ttu-id="d3bd7-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave) .</span><span class="sxs-lookup"><span data-stu-id="d3bd7-107">You can send this message explicitly or by using the [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave) macro.</span></span>


```C++
MCIWNDM_CAN_SAVE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="d3bd7-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d3bd7-108">Return Value</span></span>

<span data-ttu-id="d3bd7-109">Retourne la **valeur true** si l’appareil prend en charge l’enregistrement ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d3bd7-109">Returns **TRUE** if the device supports saving or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3bd7-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d3bd7-110">Requirements</span></span>



| <span data-ttu-id="d3bd7-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d3bd7-111">Requirement</span></span> | <span data-ttu-id="d3bd7-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3bd7-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d3bd7-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3bd7-113">Minimum supported client</span></span><br/> | <span data-ttu-id="d3bd7-114">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d3bd7-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d3bd7-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3bd7-115">Minimum supported server</span></span><br/> | <span data-ttu-id="d3bd7-116">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d3bd7-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d3bd7-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="d3bd7-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3bd7-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3bd7-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3bd7-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3bd7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3bd7-120">**MCIWndCanSave**</span><span class="sxs-lookup"><span data-stu-id="d3bd7-120">**MCIWndCanSave**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)
</dt> </dl>

 

 





