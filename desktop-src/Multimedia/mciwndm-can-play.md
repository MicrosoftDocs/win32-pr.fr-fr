---
title: Message MCIWNDM_CAN_PLAY (VFW. h)
description: Le MCIWNDM \_ peut \_ lire le message détermine si un périphérique MCI peut lire un fichier de données ou un contenu d’un autre type. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndCanPlay.
ms.assetid: dbb742b0-b8ab-4b80-96da-c4823a4747c9
keywords:
- Message MCIWNDM_CAN_PLAY Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 043a0fc15260f7448df8d009a6b468616244269d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106527579"
---
# <a name="mciwndm_can_play-message"></a><span data-ttu-id="df9a4-105">MCIWNDM \_ peut \_ lire le message</span><span class="sxs-lookup"><span data-stu-id="df9a4-105">MCIWNDM\_CAN\_PLAY message</span></span>

<span data-ttu-id="df9a4-106">Le **MCIWNDM \_ peut \_ lire** le message détermine si un périphérique MCI peut lire un fichier de données ou un contenu d’un autre type.</span><span class="sxs-lookup"><span data-stu-id="df9a4-106">The **MCIWNDM\_CAN\_PLAY** message determines if an MCI device can play a data file or content of some other kind.</span></span> <span data-ttu-id="df9a4-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndCanPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay) .</span><span class="sxs-lookup"><span data-stu-id="df9a4-107">You can send this message explicitly or by using the [**MCIWndCanPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay) macro.</span></span>


```C++
MCIWNDM_CAN_PLAY 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="df9a4-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="df9a4-108">Return Value</span></span>

<span data-ttu-id="df9a4-109">Retourne la **valeur true** si l’appareil prend en charge la diffusion des données ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="df9a4-109">Returns **TRUE** if the device supports playing the data or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="df9a4-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df9a4-110">Requirements</span></span>



| <span data-ttu-id="df9a4-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df9a4-111">Requirement</span></span> | <span data-ttu-id="df9a4-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="df9a4-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="df9a4-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df9a4-113">Minimum supported client</span></span><br/> | <span data-ttu-id="df9a4-114">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="df9a4-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="df9a4-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df9a4-115">Minimum supported server</span></span><br/> | <span data-ttu-id="df9a4-116">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="df9a4-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="df9a4-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="df9a4-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="df9a4-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="df9a4-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df9a4-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df9a4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df9a4-120">**MCIWndCanPlay**</span><span class="sxs-lookup"><span data-stu-id="df9a4-120">**MCIWndCanPlay**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)
</dt> </dl>

 

 





