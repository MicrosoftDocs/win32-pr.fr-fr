---
title: Message MCIWNDM_SETVOLUME (VFW. h)
description: Le \_ message MCIWNDM SETVOLUME définit le niveau de volume d’un périphérique MCI. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndSetVolume.
ms.assetid: 04151588-b761-447a-9a57-808c034c3059
keywords:
- Message MCIWNDM_SETVOLUME Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETVOLUME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2215f8df3ea6f7b36b224318ebac68175ff9c265
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740229"
---
# <a name="mciwndm_setvolume-message"></a><span data-ttu-id="e12c3-105">\_Message MCIWNDM SETVOLUME</span><span class="sxs-lookup"><span data-stu-id="e12c3-105">MCIWNDM\_SETVOLUME message</span></span>

<span data-ttu-id="e12c3-106">Le message **MCIWNDM \_ SETVOLUME** définit le niveau de volume d’un périphérique MCI.</span><span class="sxs-lookup"><span data-stu-id="e12c3-106">The **MCIWNDM\_SETVOLUME** message sets the volume level of an MCI device.</span></span> <span data-ttu-id="e12c3-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) .</span><span class="sxs-lookup"><span data-stu-id="e12c3-107">You can send this message explicitly or by using the [**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) macro.</span></span>


```C++
MCIWNDM_SETVOLUME 
wParam = 0; 
lParam = (LPARAM) (UINT) iVol; 
```



## <a name="parameters"></a><span data-ttu-id="e12c3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e12c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e12c3-109"><span id="iVol"></span><span id="ivol"></span><span id="IVOL"></span>*iVol*</span><span class="sxs-lookup"><span data-stu-id="e12c3-109"><span id="iVol"></span><span id="ivol"></span><span id="IVOL"></span>*iVol*</span></span>
</dt> <dd>

<span data-ttu-id="e12c3-110">Nouveau niveau de volume.</span><span class="sxs-lookup"><span data-stu-id="e12c3-110">New volume level.</span></span> <span data-ttu-id="e12c3-111">Spécifiez 1000 pour le niveau de volume normal.</span><span class="sxs-lookup"><span data-stu-id="e12c3-111">Specify 1000 for normal volume level.</span></span> <span data-ttu-id="e12c3-112">Spécifiez une valeur plus élevée pour un volume plus fort ou une valeur inférieure pour un volume plus silencieux.</span><span class="sxs-lookup"><span data-stu-id="e12c3-112">Specify a higher value for a louder volume or a lower value for a quieter volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e12c3-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e12c3-113">Return Value</span></span>

<span data-ttu-id="e12c3-114">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="e12c3-114">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="e12c3-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e12c3-115">Requirements</span></span>



| <span data-ttu-id="e12c3-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e12c3-116">Requirement</span></span> | <span data-ttu-id="e12c3-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="e12c3-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e12c3-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e12c3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e12c3-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e12c3-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e12c3-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e12c3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e12c3-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e12c3-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e12c3-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="e12c3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e12c3-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e12c3-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e12c3-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e12c3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e12c3-125">**MCIWndSetVolume**</span><span class="sxs-lookup"><span data-stu-id="e12c3-125">**MCIWndSetVolume**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume)
</dt> </dl>

 

 





