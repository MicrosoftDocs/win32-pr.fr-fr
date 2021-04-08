---
title: Message MCIWNDM_GETMODE (VFW. h)
description: Le \_ message MCIWNDM GETMODE récupère le mode d’opération actuel d’un périphérique MCI. Les périphériques MCI disposent de plusieurs modes de fonctionnement, qui sont désignés par des constantes. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetMode.
ms.assetid: cc327281-434e-4047-9e15-c04a10953f47
keywords:
- Message MCIWNDM_GETMODE Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETMODE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5daefea2c550a1d0cf807ae03840c38ae8b2567c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102841"
---
# <a name="mciwndm_getmode-message"></a><span data-ttu-id="00a99-106">\_Message MCIWNDM GETMODE</span><span class="sxs-lookup"><span data-stu-id="00a99-106">MCIWNDM\_GETMODE message</span></span>

<span data-ttu-id="00a99-107">Le message **MCIWNDM \_ GETMODE** récupère le mode d’opération actuel d’un périphérique MCI.</span><span class="sxs-lookup"><span data-stu-id="00a99-107">The **MCIWNDM\_GETMODE** message retrieves the current operating mode of an MCI device.</span></span> <span data-ttu-id="00a99-108">Les périphériques MCI disposent de plusieurs modes de fonctionnement, qui sont désignés par des constantes.</span><span class="sxs-lookup"><span data-stu-id="00a99-108">MCI devices have several operating modes, which are designated by constants.</span></span> <span data-ttu-id="00a99-109">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetMode**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode) .</span><span class="sxs-lookup"><span data-stu-id="00a99-109">You can send this message explicitly or by using the [**MCIWndGetMode**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode) macro.</span></span>


```C++
MCIWNDM_GETMODE 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a><span data-ttu-id="00a99-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="00a99-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00a99-111"><span id="len"></span><span id="LEN"></span>*Len*</span><span class="sxs-lookup"><span data-stu-id="00a99-111"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="00a99-112">Taille, en octets, de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="00a99-112">Size, in bytes, of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="00a99-113"><span id="lp"></span><span id="LP"></span>*Aid*</span><span class="sxs-lookup"><span data-stu-id="00a99-113"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="00a99-114">Pointeur vers la mémoire tampon définie par l’application utilisée pour retourner le mode.</span><span class="sxs-lookup"><span data-stu-id="00a99-114">Pointer to the application-defined buffer used to return the mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00a99-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="00a99-115">Return Value</span></span>

<span data-ttu-id="00a99-116">Retourne un entier correspondant à la constante MCI définissant le mode.</span><span class="sxs-lookup"><span data-stu-id="00a99-116">Returns an integer corresponding to the MCI constant defining the mode.</span></span>

## <a name="remarks"></a><span data-ttu-id="00a99-117">Notes</span><span class="sxs-lookup"><span data-stu-id="00a99-117">Remarks</span></span>

<span data-ttu-id="00a99-118">Si la chaîne se terminant par un caractère null décrivant le mode est plus longue que la mémoire tampon, elle est tronquée.</span><span class="sxs-lookup"><span data-stu-id="00a99-118">If the null-terminated string describing the mode is longer than the buffer, it is truncated.</span></span>

<span data-ttu-id="00a99-119">Tous les appareils ne peuvent pas fonctionner dans chaque mode.</span><span class="sxs-lookup"><span data-stu-id="00a99-119">Not all devices can operate in every mode.</span></span> <span data-ttu-id="00a99-120">Par exemple, l’appareil MCIAVI est un périphérique de lecture ; elle ne prend pas en charge le mode d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="00a99-120">For example, the MCIAVI device is a playback device; it doesn't support the recording mode.</span></span> <span data-ttu-id="00a99-121">Les modes suivants peuvent être récupérés à l’aide de **MCIWNDM \_ GETMODE**.</span><span class="sxs-lookup"><span data-stu-id="00a99-121">The following modes can be retrieved by using **MCIWNDM\_GETMODE**.</span></span>



| <span data-ttu-id="00a99-122">Mode d'opération</span><span class="sxs-lookup"><span data-stu-id="00a99-122">Operating mode</span></span> | <span data-ttu-id="00a99-123">MCI, constante</span><span class="sxs-lookup"><span data-stu-id="00a99-123">MCI constant</span></span>          |
|----------------|-----------------------|
| <span data-ttu-id="00a99-124">non prêt</span><span class="sxs-lookup"><span data-stu-id="00a99-124">not ready</span></span>      | <span data-ttu-id="00a99-125">\_mode MCI \_ non \_ prêt</span><span class="sxs-lookup"><span data-stu-id="00a99-125">MCI\_MODE\_NOT\_READY</span></span> |
| <span data-ttu-id="00a99-126">ouvert</span><span class="sxs-lookup"><span data-stu-id="00a99-126">open</span></span>           | <span data-ttu-id="00a99-127">\_mode MCI \_ ouvert</span><span class="sxs-lookup"><span data-stu-id="00a99-127">MCI\_MODE\_OPEN</span></span>       |
| <span data-ttu-id="00a99-128">en pause</span><span class="sxs-lookup"><span data-stu-id="00a99-128">paused</span></span>         | <span data-ttu-id="00a99-129">\_pause en mode MCI \_</span><span class="sxs-lookup"><span data-stu-id="00a99-129">MCI\_MODE\_PAUSE</span></span>      |
| <span data-ttu-id="00a99-130">lecture en cours</span><span class="sxs-lookup"><span data-stu-id="00a99-130">playing</span></span>        | <span data-ttu-id="00a99-131">\_lecture en mode MCI \_</span><span class="sxs-lookup"><span data-stu-id="00a99-131">MCI\_MODE\_PLAY</span></span>       |
| <span data-ttu-id="00a99-132">enregistrement</span><span class="sxs-lookup"><span data-stu-id="00a99-132">recording</span></span>      | <span data-ttu-id="00a99-133">\_enregistrement en mode MCI \_</span><span class="sxs-lookup"><span data-stu-id="00a99-133">MCI\_MODE\_RECORD</span></span>     |
| <span data-ttu-id="00a99-134">rechercher dans</span><span class="sxs-lookup"><span data-stu-id="00a99-134">seeking</span></span>        | <span data-ttu-id="00a99-135">\_recherche en mode MCI \_</span><span class="sxs-lookup"><span data-stu-id="00a99-135">MCI\_MODE\_SEEK</span></span>       |
| <span data-ttu-id="00a99-136">stopped</span><span class="sxs-lookup"><span data-stu-id="00a99-136">stopped</span></span>        | <span data-ttu-id="00a99-137">\_arrêt en mode MCI \_</span><span class="sxs-lookup"><span data-stu-id="00a99-137">MCI\_MODE\_STOP</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="00a99-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00a99-138">Requirements</span></span>



| <span data-ttu-id="00a99-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="00a99-139">Requirement</span></span> | <span data-ttu-id="00a99-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="00a99-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="00a99-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00a99-141">Minimum supported client</span></span><br/> | <span data-ttu-id="00a99-142">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="00a99-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="00a99-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00a99-143">Minimum supported server</span></span><br/> | <span data-ttu-id="00a99-144">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="00a99-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="00a99-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="00a99-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="00a99-146"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="00a99-146"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00a99-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00a99-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00a99-148">**MCIWndGetMode**</span><span class="sxs-lookup"><span data-stu-id="00a99-148">**MCIWndGetMode**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode)
</dt> </dl>

 

 





