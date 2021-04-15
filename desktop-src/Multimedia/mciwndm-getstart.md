---
title: Message MCIWNDM_GETSTART (VFW. h)
description: Le \_ message MCIWNDM GETSTART récupère l’emplacement du début du contenu d’un périphérique ou d’un fichier MCI. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetStart.
ms.assetid: 2350616c-2aac-4ff6-b074-bb785a97cdfb
keywords:
- Message MCIWNDM_GETSTART Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETSTART
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63cbe88df006f1f98854e42259074d82bbd87dc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464514"
---
# <a name="mciwndm_getstart-message"></a><span data-ttu-id="e6e34-105">\_Message MCIWNDM GETSTART</span><span class="sxs-lookup"><span data-stu-id="e6e34-105">MCIWNDM\_GETSTART message</span></span>

<span data-ttu-id="e6e34-106">Le message **MCIWNDM \_ GETSTART** récupère l’emplacement du début du contenu d’un périphérique ou d’un fichier MCI.</span><span class="sxs-lookup"><span data-stu-id="e6e34-106">The **MCIWNDM\_GETSTART** message retrieves the location of the beginning of the content of an MCI device or file.</span></span> <span data-ttu-id="e6e34-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) .</span><span class="sxs-lookup"><span data-stu-id="e6e34-107">You can send this message explicitly or by using the [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) macro.</span></span>


```C++
MCIWNDM_GETSTART 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="e6e34-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e6e34-108">Return Value</span></span>

<span data-ttu-id="e6e34-109">Retourne l’emplacement au format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="e6e34-109">Returns the location in the current time format.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6e34-110">Notes</span><span class="sxs-lookup"><span data-stu-id="e6e34-110">Remarks</span></span>

<span data-ttu-id="e6e34-111">En règle générale, la valeur de retour est zéro ; Toutefois, certains appareils utilisent un emplacement de départ différent de zéro.</span><span class="sxs-lookup"><span data-stu-id="e6e34-111">Typically, the return value is zero; but some devices use a nonzero starting location.</span></span> <span data-ttu-id="e6e34-112">La recherche de cet emplacement définit l’appareil au début du support.</span><span class="sxs-lookup"><span data-stu-id="e6e34-112">Seeking to this location sets the device to the start of the media.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6e34-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6e34-113">Requirements</span></span>



| <span data-ttu-id="e6e34-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6e34-114">Requirement</span></span> | <span data-ttu-id="e6e34-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6e34-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e6e34-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6e34-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e6e34-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6e34-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e6e34-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6e34-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e6e34-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6e34-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e6e34-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="e6e34-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6e34-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6e34-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6e34-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6e34-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6e34-123">**MCIWndGetStart**</span><span class="sxs-lookup"><span data-stu-id="e6e34-123">**MCIWndGetStart**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart)
</dt> </dl>

 

 





