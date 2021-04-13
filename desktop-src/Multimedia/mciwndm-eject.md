---
title: Message MCIWNDM_EJECT (VFW. h)
description: Le \_ message MCIWNDM EJECT envoie une commande à un périphérique MCI pour éjecter son support. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndEject.
ms.assetid: a492f504-8b58-480e-9766-bc2878466c44
keywords:
- Message MCIWNDM_EJECT Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_EJECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e41686ce41b82dc48ee6c22ac556606c79c5b24a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384123"
---
# <a name="mciwndm_eject-message"></a><span data-ttu-id="d4a64-105">MCIWNDM \_ éjecter le message</span><span class="sxs-lookup"><span data-stu-id="d4a64-105">MCIWNDM\_EJECT message</span></span>

<span data-ttu-id="d4a64-106">Le message **MCIWNDM \_ EJECT** envoie une commande à un périphérique MCI pour éjecter son support.</span><span class="sxs-lookup"><span data-stu-id="d4a64-106">The **MCIWNDM\_EJECT** message sends a command to an MCI device to eject its media.</span></span> <span data-ttu-id="d4a64-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject) .</span><span class="sxs-lookup"><span data-stu-id="d4a64-107">You can send this message explicitly or by using the [**MCIWndEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject) macro.</span></span>


```C++
MCIWNDM_EJECT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="d4a64-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d4a64-108">Return Value</span></span>

<span data-ttu-id="d4a64-109">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="d4a64-109">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4a64-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4a64-110">Requirements</span></span>



| <span data-ttu-id="d4a64-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4a64-111">Requirement</span></span> | <span data-ttu-id="d4a64-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4a64-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d4a64-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4a64-113">Minimum supported client</span></span><br/> | <span data-ttu-id="d4a64-114">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d4a64-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d4a64-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4a64-115">Minimum supported server</span></span><br/> | <span data-ttu-id="d4a64-116">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d4a64-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d4a64-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="d4a64-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4a64-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4a64-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4a64-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4a64-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4a64-120">**MCIWndEject**</span><span class="sxs-lookup"><span data-stu-id="d4a64-120">**MCIWndEject**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndeject)
</dt> </dl>

 

 





