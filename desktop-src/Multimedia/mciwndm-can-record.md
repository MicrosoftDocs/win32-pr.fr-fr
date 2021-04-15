---
title: Message MCIWNDM_CAN_RECORD (VFW. h)
description: Le MCIWNDM \_ peut \_ enregistrer un message détermine si un appareil MCI prend en charge l’enregistrement. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndCanRecord.
ms.assetid: b5a789fa-6a88-487d-a374-8f4798ee5a62
keywords:
- Message MCIWNDM_CAN_RECORD Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_RECORD
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2acbc9efa3ca973c12112a599d1202ad936107a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466643"
---
# <a name="mciwndm_can_record-message"></a><span data-ttu-id="3c6af-105">MCIWNDM \_ peut \_ enregistrer le message</span><span class="sxs-lookup"><span data-stu-id="3c6af-105">MCIWNDM\_CAN\_RECORD message</span></span>

<span data-ttu-id="3c6af-106">Le **MCIWNDM \_ peut \_ Enregistrer** un message détermine si un appareil MCI prend en charge l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="3c6af-106">The **MCIWNDM\_CAN\_RECORD** message determines if an MCI device supports recording.</span></span> <span data-ttu-id="3c6af-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) .</span><span class="sxs-lookup"><span data-stu-id="3c6af-107">You can send this message explicitly or by using the [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) macro.</span></span>


```C++
MCIWNDM_CAN_RECORD 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="3c6af-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3c6af-108">Return Value</span></span>

<span data-ttu-id="3c6af-109">Retourne la **valeur true** si l’appareil prend en charge l’enregistrement ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="3c6af-109">Returns **TRUE** if the device supports recording or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c6af-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c6af-110">Requirements</span></span>



| <span data-ttu-id="3c6af-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c6af-111">Requirement</span></span> | <span data-ttu-id="3c6af-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c6af-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3c6af-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c6af-113">Minimum supported client</span></span><br/> | <span data-ttu-id="3c6af-114">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3c6af-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3c6af-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c6af-115">Minimum supported server</span></span><br/> | <span data-ttu-id="3c6af-116">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3c6af-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3c6af-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="3c6af-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c6af-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c6af-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c6af-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c6af-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c6af-120">**MCIWndCanRecord**</span><span class="sxs-lookup"><span data-stu-id="3c6af-120">**MCIWndCanRecord**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord)
</dt> </dl>

 

 





