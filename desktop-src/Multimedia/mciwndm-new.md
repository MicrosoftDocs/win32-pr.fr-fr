---
title: Message MCIWNDM_NEW (VFW. h)
description: Le \_ nouveau message MCIWNDM crée un nouveau fichier pour l’appareil MCI actuel. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndNew.
ms.assetid: 18b2340d-8303-415a-867f-bd346034db2a
keywords:
- Message MCIWNDM_NEW Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_NEW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 293323cd0404da45e648024b35b7f96ef60fea61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741164"
---
# <a name="mciwndm_new-message"></a><span data-ttu-id="adde3-105">MCIWNDM \_ un nouveau message</span><span class="sxs-lookup"><span data-stu-id="adde3-105">MCIWNDM\_NEW message</span></span>

<span data-ttu-id="adde3-106">Le **\_ nouveau message MCIWNDM** crée un nouveau fichier pour l’appareil MCI actuel.</span><span class="sxs-lookup"><span data-stu-id="adde3-106">The **MCIWNDM\_NEW** message creates a new file for the current MCI device.</span></span> <span data-ttu-id="adde3-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) .</span><span class="sxs-lookup"><span data-stu-id="adde3-107">You can send this message explicitly or by using the [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) macro.</span></span>


```C++
MCIWNDM_NEW 
wParam = 0; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a><span data-ttu-id="adde3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="adde3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adde3-109"><span id="lp"></span><span id="LP"></span>*Aid*</span><span class="sxs-lookup"><span data-stu-id="adde3-109"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="adde3-110">Pointeur vers une mémoire tampon contenant le nom du périphérique MCI qui utilisera le fichier.</span><span class="sxs-lookup"><span data-stu-id="adde3-110">Pointer to a buffer containing the name of the MCI device that will use the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adde3-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="adde3-111">Return Value</span></span>

<span data-ttu-id="adde3-112">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="adde3-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="adde3-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="adde3-113">Requirements</span></span>



| <span data-ttu-id="adde3-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="adde3-114">Requirement</span></span> | <span data-ttu-id="adde3-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="adde3-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="adde3-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="adde3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="adde3-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="adde3-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="adde3-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="adde3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="adde3-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="adde3-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="adde3-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="adde3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="adde3-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="adde3-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adde3-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="adde3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adde3-123">**MCIWndNew**</span><span class="sxs-lookup"><span data-stu-id="adde3-123">**MCIWndNew**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndnew)
</dt> </dl>

 

 





