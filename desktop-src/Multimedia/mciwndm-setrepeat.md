---
title: Message MCIWNDM_SETREPEAT (VFW. h)
description: Le \_ message MCIWNDM SETREPEAT définit l’indicateur de répétition associé à la lecture continue.
ms.assetid: 9a8da201-9ce8-4b6c-8b76-cd9e1356c75d
keywords:
- Message MCIWNDM_SETREPEAT Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETREPEAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aeae2ac3cb57f8ddbb2343ee3f42d30fa8def370
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843913"
---
# <a name="mciwndm_setrepeat-message"></a><span data-ttu-id="13f59-104">\_Message MCIWNDM SETREPEAT</span><span class="sxs-lookup"><span data-stu-id="13f59-104">MCIWNDM\_SETREPEAT message</span></span>

<span data-ttu-id="13f59-105">Le message **MCIWNDM \_ SETREPEAT** définit l’indicateur de répétition associé à la lecture continue.</span><span class="sxs-lookup"><span data-stu-id="13f59-105">The **MCIWNDM\_SETREPEAT** message sets the repeat flag associated with continuous playback.</span></span> <span data-ttu-id="13f59-106">Le message **MCIWNDM \_ SETREPEAT** fonctionne conjointement avec la commande [MCI \_ Play](mci-play.md) pour fournir une boucle de lecture continue.</span><span class="sxs-lookup"><span data-stu-id="13f59-106">The **MCIWNDM\_SETREPEAT** message works in conjunction with the [MCI\_PLAY](mci-play.md) command to provide a continuous playback loop.</span></span> <span data-ttu-id="13f59-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) .</span><span class="sxs-lookup"><span data-stu-id="13f59-107">You can send this message explicitly or by using the [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) macro.</span></span>


```C++
MCIWNDM_SETREPEAT 
wParam = 0; 
lParam = (LPARAM) (BOOL) f; 
```



## <a name="parameters"></a><span data-ttu-id="13f59-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="13f59-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13f59-109"><span id="f"></span><span id="F"></span>*FA*</span><span class="sxs-lookup"><span data-stu-id="13f59-109"><span id="f"></span><span id="F"></span>*f*</span></span>
</dt> <dd>

<span data-ttu-id="13f59-110">Nouvel état de l’indicateur de répétition.</span><span class="sxs-lookup"><span data-stu-id="13f59-110">New state of the repeat flag.</span></span> <span data-ttu-id="13f59-111">Spécifiez **true** pour activer la lecture continue.</span><span class="sxs-lookup"><span data-stu-id="13f59-111">Specify **TRUE** to turn on continuous playback.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13f59-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="13f59-112">Return Value</span></span>

<span data-ttu-id="13f59-113">Retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="13f59-113">Returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="13f59-114">Notes</span><span class="sxs-lookup"><span data-stu-id="13f59-114">Remarks</span></span>

<span data-ttu-id="13f59-115">À l’heure actuelle, MCIAVI est le seul périphérique qui prend en charge la lecture continue.</span><span class="sxs-lookup"><span data-stu-id="13f59-115">Currently, MCIAVI is the only device that supports continuous playback.</span></span>

## <a name="requirements"></a><span data-ttu-id="13f59-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="13f59-116">Requirements</span></span>



| <span data-ttu-id="13f59-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="13f59-117">Requirement</span></span> | <span data-ttu-id="13f59-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="13f59-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="13f59-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13f59-119">Minimum supported client</span></span><br/> | <span data-ttu-id="13f59-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="13f59-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="13f59-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13f59-121">Minimum supported server</span></span><br/> | <span data-ttu-id="13f59-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="13f59-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="13f59-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="13f59-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="13f59-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="13f59-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13f59-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13f59-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13f59-126">\_lecture MCI</span><span class="sxs-lookup"><span data-stu-id="13f59-126">MCI\_PLAY</span></span>](mci-play.md)
</dt> <dt>

[<span data-ttu-id="13f59-127">**MCIWndSetRepeat**</span><span class="sxs-lookup"><span data-stu-id="13f59-127">**MCIWndSetRepeat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat)
</dt> </dl>

 

 





