---
title: Message MCIWNDM_PLAYTO (VFW. h)
description: Le \_ message MCIWNDM point lit le contenu d’un périphérique MCI de la position actuelle à l’emplacement de fin spécifié ou jusqu’à ce qu’une autre commande arrête la lecture.
ms.assetid: ed940ee7-7b96-47da-99d3-6697f8a2e3d5
keywords:
- Message MCIWNDM_PLAYTO Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYTO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf0104204dc0306615ead91be036459cdf3c11d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105430"
---
# <a name="mciwndm_playto-message"></a><span data-ttu-id="b16e8-104">\_Message MCIWNDM point</span><span class="sxs-lookup"><span data-stu-id="b16e8-104">MCIWNDM\_PLAYTO message</span></span>

<span data-ttu-id="b16e8-105">Le message **MCIWNDM \_ point** lit le contenu d’un périphérique MCI de la position actuelle à l’emplacement de fin spécifié ou jusqu’à ce qu’une autre commande arrête la lecture.</span><span class="sxs-lookup"><span data-stu-id="b16e8-105">The **MCIWNDM\_PLAYTO** message plays the content of an MCI device from the current position to the specified ending location or until another command stops playback.</span></span> <span data-ttu-id="b16e8-106">Si l’emplacement de fin spécifié se situe au-delà de la fin du contenu, la lecture s’arrête à la fin du contenu.</span><span class="sxs-lookup"><span data-stu-id="b16e8-106">If the specified ending location is beyond the end of the content, playback stops at the end of the content.</span></span> <span data-ttu-id="b16e8-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) .</span><span class="sxs-lookup"><span data-stu-id="b16e8-107">You can send this message explicitly or by using the [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) macro.</span></span>


```C++
MCIWNDM_PLAYTO 
wParam = 0; 
lParam = (LPARAM) (LONG) lEnd; 
```



## <a name="parameters"></a><span data-ttu-id="b16e8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b16e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b16e8-109"><span id="lEnd"></span><span id="lend"></span><span id="LEND"></span>*Prêter*</span><span class="sxs-lookup"><span data-stu-id="b16e8-109"><span id="lEnd"></span><span id="lend"></span><span id="LEND"></span>*lEnd*</span></span>
</dt> <dd>

<span data-ttu-id="b16e8-110">Emplacement de fin.</span><span class="sxs-lookup"><span data-stu-id="b16e8-110">Ending location.</span></span> <span data-ttu-id="b16e8-111">Les unités de l’emplacement de fin dépendent du format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="b16e8-111">The units for the ending location depend on the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b16e8-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b16e8-112">Return Value</span></span>

<span data-ttu-id="b16e8-113">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="b16e8-113">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b16e8-114">Notes</span><span class="sxs-lookup"><span data-stu-id="b16e8-114">Remarks</span></span>

<span data-ttu-id="b16e8-115">Cette macro est définie à l’aide des macros [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) et [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) , qui à leur tour utilisent la commande [MCI \_ Seek](mci-seek.md) et le message **MCIWNDM \_ point** .</span><span class="sxs-lookup"><span data-stu-id="b16e8-115">This macro is defined using the [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) and [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) macros, which in turn use the [MCI\_SEEK](mci-seek.md) command and the **MCIWNDM\_PLAYTO** message.</span></span>

<span data-ttu-id="b16e8-116">Vous pouvez également spécifier un emplacement de départ et un emplacement de fin pour la lecture à l’aide de la macro [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) .</span><span class="sxs-lookup"><span data-stu-id="b16e8-116">You can also specify both a starting and ending location for playback by using the [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="b16e8-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b16e8-117">Requirements</span></span>



| <span data-ttu-id="b16e8-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b16e8-118">Requirement</span></span> | <span data-ttu-id="b16e8-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="b16e8-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b16e8-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b16e8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b16e8-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b16e8-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b16e8-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b16e8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b16e8-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b16e8-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b16e8-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="b16e8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b16e8-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="b16e8-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b16e8-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b16e8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b16e8-127">\_recherche MCI</span><span class="sxs-lookup"><span data-stu-id="b16e8-127">MCI\_SEEK</span></span>](mci-seek.md)
</dt> <dt>

[<span data-ttu-id="b16e8-128">**MCIWndPlayFromTo**</span><span class="sxs-lookup"><span data-stu-id="b16e8-128">**MCIWndPlayFromTo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
</dt> <dt>

[<span data-ttu-id="b16e8-129">**MCIWndPlayTo**</span><span class="sxs-lookup"><span data-stu-id="b16e8-129">**MCIWndPlayTo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)
</dt> <dt>

[<span data-ttu-id="b16e8-130">**MCIWndSeek**</span><span class="sxs-lookup"><span data-stu-id="b16e8-130">**MCIWndSeek**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndseek)
</dt> </dl>

 

 





