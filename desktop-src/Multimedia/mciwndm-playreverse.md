---
title: Message MCIWNDM_PLAYREVERSE (VFW. h)
description: Le \_ message MCIWNDM PLAYREVERSE lit le contenu actuel dans le sens inverse, en commençant à la position actuelle et en se terminant au début du contenu ou jusqu’à ce qu’une autre commande arrête la lecture.
ms.assetid: 93a22454-eca6-453f-abbe-6cf20198dbad
keywords:
- Message MCIWNDM_PLAYREVERSE Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYREVERSE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84b0a2e230e3c57e8314e455be5dfbc5cea2c013
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102840"
---
# <a name="mciwndm_playreverse-message"></a><span data-ttu-id="191fb-104">\_Message MCIWNDM PLAYREVERSE</span><span class="sxs-lookup"><span data-stu-id="191fb-104">MCIWNDM\_PLAYREVERSE message</span></span>

<span data-ttu-id="191fb-105">Le message **MCIWNDM \_ PLAYREVERSE** lit le contenu actuel dans le sens inverse, en commençant à la position actuelle et en se terminant au début du contenu ou jusqu’à ce qu’une autre commande arrête la lecture.</span><span class="sxs-lookup"><span data-stu-id="191fb-105">The **MCIWNDM\_PLAYREVERSE** message plays the current content in the reverse direction, beginning at the current position and ending at the beginning of the content or until another command stops playback.</span></span> <span data-ttu-id="191fb-106">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) .</span><span class="sxs-lookup"><span data-stu-id="191fb-106">You can send this message explicitly or by using the [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) macro.</span></span>


```C++
MCIWNDM_PLAYREVERSE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="191fb-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="191fb-107">Return Value</span></span>

<span data-ttu-id="191fb-108">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="191fb-108">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="191fb-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="191fb-109">Requirements</span></span>



| <span data-ttu-id="191fb-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="191fb-110">Requirement</span></span> | <span data-ttu-id="191fb-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="191fb-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="191fb-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="191fb-112">Minimum supported client</span></span><br/> | <span data-ttu-id="191fb-113">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="191fb-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="191fb-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="191fb-114">Minimum supported server</span></span><br/> | <span data-ttu-id="191fb-115">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="191fb-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="191fb-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="191fb-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="191fb-117"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="191fb-117"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="191fb-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="191fb-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="191fb-119">**MCIWndPlayReverse**</span><span class="sxs-lookup"><span data-stu-id="191fb-119">**MCIWndPlayReverse**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse)
</dt> </dl>

 

 





