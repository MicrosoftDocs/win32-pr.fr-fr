---
title: Message MCIWNDM_SETTIMEFORMAT (VFW. h)
description: Le \_ message MCIWNDM SETTIMEFORMAT définit le format d’heure d’un appareil MCI. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndSetTimeFormat.
ms.assetid: 7de82094-6d35-44fd-88e7-ebd18a558cfd
keywords:
- Message MCIWNDM_SETTIMEFORMAT Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETTIMEFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcec1f0db5accad93211bf1eb6f1c9297e2b9f33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508333"
---
# <a name="mciwndm_settimeformat-message"></a><span data-ttu-id="8f663-105">\_Message MCIWNDM SETTIMEFORMAT</span><span class="sxs-lookup"><span data-stu-id="8f663-105">MCIWNDM\_SETTIMEFORMAT message</span></span>

<span data-ttu-id="8f663-106">Le message **MCIWNDM \_ SETTIMEFORMAT** définit le format d’heure d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="8f663-106">The **MCIWNDM\_SETTIMEFORMAT** message sets the time format of an MCI device.</span></span> <span data-ttu-id="8f663-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="8f663-107">You can send this message explicitly or by using the [**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) macro.</span></span>


```C++
MCIWNDM_SETTIMEFORMAT 
wParam = 0; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a><span data-ttu-id="8f663-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8f663-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f663-109"><span id="lp"></span><span id="LP"></span>*Aid*</span><span class="sxs-lookup"><span data-stu-id="8f663-109"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="8f663-110">Pointeur vers une mémoire tampon contenant la chaîne terminée par le caractère null qui indique le format d’heure.</span><span class="sxs-lookup"><span data-stu-id="8f663-110">Pointer to a buffer containing the null-terminated string indicating the time format.</span></span> <span data-ttu-id="8f663-111">Spécifiez « frames » pour définir le format d’heure sur frames, ou « MS » pour définir le format d’heure sur millisecondes.</span><span class="sxs-lookup"><span data-stu-id="8f663-111">Specify "frames" to set the time format to frames, or "ms" to set the time format to milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f663-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8f663-112">Return Value</span></span>

<span data-ttu-id="8f663-113">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="8f663-113">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f663-114">Notes</span><span class="sxs-lookup"><span data-stu-id="8f663-114">Remarks</span></span>

<span data-ttu-id="8f663-115">Une application peut spécifier des formats d’heure autres que des images ou des millisecondes tant que les formats sont pris en charge par l’appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="8f663-115">An application can specify time formats other than frames or milliseconds as long as the formats are supported by the MCI device.</span></span> <span data-ttu-id="8f663-116">Les formats incontinus, tels que Tracks et SMPTE, peuvent entraîner un comportement erratique du TrackBar.</span><span class="sxs-lookup"><span data-stu-id="8f663-116">Noncontinuous formats, such as tracks and SMPTE, can cause the trackbar to behave erratically.</span></span> <span data-ttu-id="8f663-117">Pour ces formats d’heure, vous souhaiterez peut-être désactiver la barre d’outils à l’aide de la macro [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) et en spécifiant le \_ style de fenêtre NOPLAYBAR MCIWNDF.</span><span class="sxs-lookup"><span data-stu-id="8f663-117">For these time formats, you might want to turn off the toolbar by using the [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) macro and specifying the MCIWNDF\_NOPLAYBAR window style.</span></span>

<span data-ttu-id="8f663-118">Si vous souhaitez définir le format d’heure sur des images ou des millisecondes, vous pouvez également utiliser la macro [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) ou [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) .</span><span class="sxs-lookup"><span data-stu-id="8f663-118">If you want to set the time format to frames or milliseconds, you can also use the [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) or [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) macro.</span></span> <span data-ttu-id="8f663-119">Pour obtenir la liste des formats d’heure, consultez la macro [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="8f663-119">For a list of time formats, see the [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f663-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f663-120">Requirements</span></span>



| <span data-ttu-id="8f663-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f663-121">Requirement</span></span> | <span data-ttu-id="8f663-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f663-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8f663-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f663-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8f663-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8f663-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8f663-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f663-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8f663-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8f663-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8f663-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="8f663-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f663-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f663-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f663-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f663-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f663-130">**MCIWndChangeStyles**</span><span class="sxs-lookup"><span data-stu-id="8f663-130">**MCIWndChangeStyles**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)
</dt> <dt>

[<span data-ttu-id="8f663-131">**MCIWndGetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="8f663-131">**MCIWndGetTimeFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)
</dt> <dt>

[<span data-ttu-id="8f663-132">**MCIWndSetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="8f663-132">**MCIWndSetTimeFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat)
</dt> <dt>

[<span data-ttu-id="8f663-133">**MCIWndUseFrames**</span><span class="sxs-lookup"><span data-stu-id="8f663-133">**MCIWndUseFrames**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes)
</dt> <dt>

[<span data-ttu-id="8f663-134">**MCIWndUseTime**</span><span class="sxs-lookup"><span data-stu-id="8f663-134">**MCIWndUseTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime)
</dt> </dl>

 

 





