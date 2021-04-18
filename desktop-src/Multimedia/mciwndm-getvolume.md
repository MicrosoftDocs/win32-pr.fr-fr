---
title: Message MCIWNDM_GETVOLUME (VFW. h)
description: Le \_ message MCIWNDM GETVOLUME récupère le paramètre de volume actuel d’un périphérique MCI. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetVolume.
ms.assetid: 3f1de023-4da8-4899-accc-409701d6e921
keywords:
- Message MCIWNDM_GETVOLUME Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETVOLUME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4aa11fb13a56dda7cb83e3d6c98b4b66083e91b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385195"
---
# <a name="mciwndm_getvolume-message"></a><span data-ttu-id="cc998-105">\_Message MCIWNDM GETVOLUME</span><span class="sxs-lookup"><span data-stu-id="cc998-105">MCIWNDM\_GETVOLUME message</span></span>

<span data-ttu-id="cc998-106">Le message **MCIWNDM \_ GETVOLUME** récupère le paramètre de volume actuel d’un périphérique MCI.</span><span class="sxs-lookup"><span data-stu-id="cc998-106">The **MCIWNDM\_GETVOLUME** message retrieves the current volume setting of an MCI device.</span></span> <span data-ttu-id="cc998-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) .</span><span class="sxs-lookup"><span data-stu-id="cc998-107">You can send this message explicitly or by using the [**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) macro.</span></span>


```C++
MCIWNDM_GETVOLUME 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="cc998-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cc998-108">Return Value</span></span>

<span data-ttu-id="cc998-109">Retourne le paramètre de volume actuel.</span><span class="sxs-lookup"><span data-stu-id="cc998-109">Returns the current volume setting.</span></span> <span data-ttu-id="cc998-110">La valeur par défaut est 1000.</span><span class="sxs-lookup"><span data-stu-id="cc998-110">The default value is 1000.</span></span> <span data-ttu-id="cc998-111">Des valeurs plus élevées indiquent des volumes plus forts, les valeurs inférieures indiquent des volumes plus silencieux.</span><span class="sxs-lookup"><span data-stu-id="cc998-111">Higher values indicate louder volumes, lower values indicate quieter volumes.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc998-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc998-112">Requirements</span></span>



| <span data-ttu-id="cc998-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc998-113">Requirement</span></span> | <span data-ttu-id="cc998-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc998-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cc998-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc998-115">Minimum supported client</span></span><br/> | <span data-ttu-id="cc998-116">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cc998-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="cc998-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc998-117">Minimum supported server</span></span><br/> | <span data-ttu-id="cc998-118">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cc998-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cc998-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="cc998-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc998-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc998-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc998-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc998-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc998-122">**MCIWndGetVolume**</span><span class="sxs-lookup"><span data-stu-id="cc998-122">**MCIWndGetVolume**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume)
</dt> </dl>

 

 





