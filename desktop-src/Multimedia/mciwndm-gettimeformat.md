---
title: Message MCIWNDM_GETTIMEFORMAT (VFW. h)
description: Le \_ message MCIWNDM GETTIMEFORMAT récupère le format d’heure actuel d’un appareil MCI sous deux formes, sous la forme d’une valeur numérique et sous forme de chaîne. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetTimeFormat.
ms.assetid: 01844872-5444-4f3b-92a3-64f80b94d3a0
keywords:
- Message MCIWNDM_GETTIMEFORMAT Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETTIMEFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a09f969c009ff23bc0951ed2efbc0dbf7aa95dda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740237"
---
# <a name="mciwndm_gettimeformat-message"></a><span data-ttu-id="0ac26-105">\_Message MCIWNDM GETTIMEFORMAT</span><span class="sxs-lookup"><span data-stu-id="0ac26-105">MCIWNDM\_GETTIMEFORMAT message</span></span>

<span data-ttu-id="0ac26-106">Le message **MCIWNDM \_ GETTIMEFORMAT** récupère le format d’heure actuel d’un appareil MCI sous deux formes : une valeur numérique et une chaîne.</span><span class="sxs-lookup"><span data-stu-id="0ac26-106">The **MCIWNDM\_GETTIMEFORMAT** message retrieves the current time format of an MCI device in two forms: as a numerical value and as a string.</span></span> <span data-ttu-id="0ac26-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="0ac26-107">You can send this message explicitly or by using the [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) macro.</span></span>


```C++
MCIWNDM_GETTIMEFORMAT 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a><span data-ttu-id="0ac26-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0ac26-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ac26-109"><span id="len"></span><span id="LEN"></span>*Len*</span><span class="sxs-lookup"><span data-stu-id="0ac26-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="0ac26-110">Taille, en octets, de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="0ac26-110">Size, in bytes, of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0ac26-111"><span id="lp"></span><span id="LP"></span>*Aid*</span><span class="sxs-lookup"><span data-stu-id="0ac26-111"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="0ac26-112">Pointeur vers une mémoire tampon destinée à contenir la forme de chaîne terminée par le caractère null du format d’heure.</span><span class="sxs-lookup"><span data-stu-id="0ac26-112">Pointer to a buffer to contain the null-terminated string form of the time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ac26-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0ac26-113">Return Value</span></span>

<span data-ttu-id="0ac26-114">Retourne un entier correspondant à la constante MCI définissant le format d’heure.</span><span class="sxs-lookup"><span data-stu-id="0ac26-114">Returns an integer corresponding to the MCI constant defining the time format.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ac26-115">Notes</span><span class="sxs-lookup"><span data-stu-id="0ac26-115">Remarks</span></span>

<span data-ttu-id="0ac26-116">Si la chaîne de format d’heure est plus longue que la mémoire tampon de retour, MCIWnd tronque la chaîne.</span><span class="sxs-lookup"><span data-stu-id="0ac26-116">If the time format string is longer than the return buffer, MCIWnd truncates the string.</span></span>

<span data-ttu-id="0ac26-117">Un périphérique MCI peut prendre en charge un ou plusieurs des formats d’heure suivants.</span><span class="sxs-lookup"><span data-stu-id="0ac26-117">An MCI device can support one or more of the following time formats.</span></span>



| <span data-ttu-id="0ac26-118">Format de l’heure</span><span class="sxs-lookup"><span data-stu-id="0ac26-118">Time format</span></span>                      | <span data-ttu-id="0ac26-119">MCI, constante</span><span class="sxs-lookup"><span data-stu-id="0ac26-119">MCI constant</span></span>               |
|----------------------------------|----------------------------|
| <span data-ttu-id="0ac26-120">Octets</span><span class="sxs-lookup"><span data-stu-id="0ac26-120">Bytes</span></span>                            | <span data-ttu-id="0ac26-121">\_octets au format MCI \_</span><span class="sxs-lookup"><span data-stu-id="0ac26-121">MCI\_FORMAT\_BYTES</span></span>         |
| <span data-ttu-id="0ac26-122">Frame</span><span class="sxs-lookup"><span data-stu-id="0ac26-122">Frames</span></span>                           | <span data-ttu-id="0ac26-123">\_images au format MCI \_</span><span class="sxs-lookup"><span data-stu-id="0ac26-123">MCI\_FORMAT\_FRAMES</span></span>        |
| <span data-ttu-id="0ac26-124">Heures, minutes, secondes</span><span class="sxs-lookup"><span data-stu-id="0ac26-124">Hours, minutes, seconds</span></span>          | <span data-ttu-id="0ac26-125">\_format MCI \_ HMS</span><span class="sxs-lookup"><span data-stu-id="0ac26-125">MCI\_FORMAT\_HMS</span></span>           |
| <span data-ttu-id="0ac26-126">Millisecondes</span><span class="sxs-lookup"><span data-stu-id="0ac26-126">Milliseconds</span></span>                     | <span data-ttu-id="0ac26-127">FORMAT MCI en \_ \_ millisecondes</span><span class="sxs-lookup"><span data-stu-id="0ac26-127">MCI\_FORMAT\_MILLISECONDS</span></span>  |
| <span data-ttu-id="0ac26-128">Minutes, secondes, frames</span><span class="sxs-lookup"><span data-stu-id="0ac26-128">Minutes, seconds, frames</span></span>         | <span data-ttu-id="0ac26-129">FORMAT MCI ( \_ \_ MSF)</span><span class="sxs-lookup"><span data-stu-id="0ac26-129">MCI\_FORMAT\_MSF</span></span>           |
| <span data-ttu-id="0ac26-130">Exemples</span><span class="sxs-lookup"><span data-stu-id="0ac26-130">Samples</span></span>                          | <span data-ttu-id="0ac26-131">\_exemples de format MCI \_</span><span class="sxs-lookup"><span data-stu-id="0ac26-131">MCI\_FORMAT\_SAMPLES</span></span>       |
| <span data-ttu-id="0ac26-132">SMPTE 24</span><span class="sxs-lookup"><span data-stu-id="0ac26-132">SMPTE 24</span></span>                         | <span data-ttu-id="0ac26-133">\_Format MCI \_ SMPTE \_ 24</span><span class="sxs-lookup"><span data-stu-id="0ac26-133">MCI\_FORMAT\_SMPTE\_24</span></span>     |
| <span data-ttu-id="0ac26-134">SMPTE 25</span><span class="sxs-lookup"><span data-stu-id="0ac26-134">SMPTE 25</span></span>                         | <span data-ttu-id="0ac26-135">\_Format MCI \_ SMPTE \_ 25</span><span class="sxs-lookup"><span data-stu-id="0ac26-135">MCI\_FORMAT\_SMPTE\_25</span></span>     |
| <span data-ttu-id="0ac26-136">Suppression SMPTE 30</span><span class="sxs-lookup"><span data-stu-id="0ac26-136">SMPTE 30 drop</span></span>                    | <span data-ttu-id="0ac26-137">\_Format MCI \_ \_ 30DROP SMPTE</span><span class="sxs-lookup"><span data-stu-id="0ac26-137">MCI\_FORMAT\_SMPTE\_30DROP</span></span> |
| <span data-ttu-id="0ac26-138">SMPTE 30 (non-Drop)</span><span class="sxs-lookup"><span data-stu-id="0ac26-138">SMPTE 30 (non-drop)</span></span>              | <span data-ttu-id="0ac26-139">FORMAT MCI, \_ \_ SMPTE \_ 30</span><span class="sxs-lookup"><span data-stu-id="0ac26-139">MCI\_FORMAT\_SMPTE\_30</span></span>     |
| <span data-ttu-id="0ac26-140">Pistes, minutes, secondes, frames</span><span class="sxs-lookup"><span data-stu-id="0ac26-140">Tracks, minutes, seconds, frames</span></span> | <span data-ttu-id="0ac26-141">\_format MCI \_ TMSF</span><span class="sxs-lookup"><span data-stu-id="0ac26-141">MCI\_FORMAT\_TMSF</span></span>          |



 

## <a name="requirements"></a><span data-ttu-id="0ac26-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0ac26-142">Requirements</span></span>



| <span data-ttu-id="0ac26-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0ac26-143">Requirement</span></span> | <span data-ttu-id="0ac26-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ac26-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0ac26-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ac26-145">Minimum supported client</span></span><br/> | <span data-ttu-id="0ac26-146">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0ac26-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0ac26-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ac26-147">Minimum supported server</span></span><br/> | <span data-ttu-id="0ac26-148">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0ac26-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0ac26-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="0ac26-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ac26-150"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ac26-150"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ac26-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ac26-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ac26-152">**MCIWndGetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="0ac26-152">**MCIWndGetTimeFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)
</dt> </dl>

 

 





