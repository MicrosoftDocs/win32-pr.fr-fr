---
title: Message MCIWNDM_PLAYFROM (VFW. h)
description: Le \_ message MCIWNDM PLAYFROM lit le contenu d’un périphérique MCI à partir de l’emplacement spécifié jusqu’à la fin du contenu ou jusqu’à ce qu’une autre commande arrête la lecture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndPlayFrom.
ms.assetid: 1c47f8eb-2a1b-4671-a9f8-fd6d59a5c7c6
keywords:
- Message MCIWNDM_PLAYFROM Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYFROM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0fa1b3f4b3359e1609b3ba12009fe5879c304a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941780"
---
# <a name="mciwndm_playfrom-message"></a><span data-ttu-id="37851-105">\_Message MCIWNDM PLAYFROM</span><span class="sxs-lookup"><span data-stu-id="37851-105">MCIWNDM\_PLAYFROM message</span></span>

<span data-ttu-id="37851-106">Le message **MCIWNDM \_ PLAYFROM** lit le contenu d’un périphérique MCI à partir de l’emplacement spécifié jusqu’à la fin du contenu ou jusqu’à ce qu’une autre commande arrête la lecture.</span><span class="sxs-lookup"><span data-stu-id="37851-106">The **MCIWNDM\_PLAYFROM** message plays the content of an MCI device from the specified location to the end of the content or until another command stops playback.</span></span> <span data-ttu-id="37851-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) .</span><span class="sxs-lookup"><span data-stu-id="37851-107">You can send this message explicitly or by using the [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) macro.</span></span>


```C++
MCIWNDM_PLAYFROM 
wParam = 0; 
lParam = (LPARAM) (LONG) lPos; 
```



## <a name="parameters"></a><span data-ttu-id="37851-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="37851-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37851-109"><span id="lPos"></span><span id="lpos"></span><span id="LPOS"></span>*lPos*</span><span class="sxs-lookup"><span data-stu-id="37851-109"><span id="lPos"></span><span id="lpos"></span><span id="LPOS"></span>*lPos*</span></span>
</dt> <dd>

<span data-ttu-id="37851-110">Emplacement de départ.</span><span class="sxs-lookup"><span data-stu-id="37851-110">Starting location.</span></span> <span data-ttu-id="37851-111">Les unités de l’emplacement de départ dépendent du format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="37851-111">The units for the starting location depend on the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37851-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="37851-112">Return Value</span></span>

<span data-ttu-id="37851-113">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="37851-113">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="37851-114">Notes</span><span class="sxs-lookup"><span data-stu-id="37851-114">Remarks</span></span>

<span data-ttu-id="37851-115">Vous pouvez également spécifier un emplacement de départ et un emplacement de fin pour la lecture à l’aide de la macro [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) .</span><span class="sxs-lookup"><span data-stu-id="37851-115">You can also specify both a starting and ending location for playback by using the [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="37851-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37851-116">Requirements</span></span>



| <span data-ttu-id="37851-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37851-117">Requirement</span></span> | <span data-ttu-id="37851-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="37851-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="37851-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37851-119">Minimum supported client</span></span><br/> | <span data-ttu-id="37851-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37851-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="37851-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37851-121">Minimum supported server</span></span><br/> | <span data-ttu-id="37851-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37851-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="37851-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="37851-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="37851-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="37851-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37851-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37851-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37851-126">**MCIWndPlayFrom**</span><span class="sxs-lookup"><span data-stu-id="37851-126">**MCIWndPlayFrom**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom)
</dt> <dt>

[<span data-ttu-id="37851-127">**MCIWndPlayFromTo**</span><span class="sxs-lookup"><span data-stu-id="37851-127">**MCIWndPlayFromTo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
</dt> </dl>

 

 





