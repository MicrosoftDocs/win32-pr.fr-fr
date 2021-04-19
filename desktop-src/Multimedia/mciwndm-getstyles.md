---
title: Message MCIWNDM_GETSTYLES (VFW. h)
description: Le \_ message MCIWNDM GETSTYLES récupère les indicateurs qui spécifient les styles de fenêtre MCIWnd actuels utilisés par une fenêtre. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetStyles.
ms.assetid: cd34ba05-47cb-488e-a6c6-4ec1c0d25de8
keywords:
- Message MCIWNDM_GETSTYLES Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETSTYLES
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 983e37291977edf2473c2b603cd5b40792fb7989
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518116"
---
# <a name="mciwndm_getstyles-message"></a><span data-ttu-id="2e074-105">\_Message MCIWNDM GETSTYLES</span><span class="sxs-lookup"><span data-stu-id="2e074-105">MCIWNDM\_GETSTYLES message</span></span>

<span data-ttu-id="2e074-106">Le message **MCIWNDM \_ GETSTYLES** récupère les indicateurs qui spécifient les styles de fenêtre MCIWnd actuels utilisés par une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="2e074-106">The **MCIWNDM\_GETSTYLES** message retrieves the flags specifying the current MCIWnd window styles used by a window.</span></span> <span data-ttu-id="2e074-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) .</span><span class="sxs-lookup"><span data-stu-id="2e074-107">You can send this message explicitly or by using the [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) macro.</span></span>


```C++
MCIWNDM_GETSTYLES 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="2e074-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2e074-108">Return Value</span></span>

<span data-ttu-id="2e074-109">Retourne une valeur représentant les styles actuels de la fenêtre MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="2e074-109">Returns a value representing the current styles of the MCIWnd window.</span></span> <span data-ttu-id="2e074-110">La valeur de retour est l’opérateur or au niveau du bit des styles de fenêtre MCIWnd (indicateurs MCIWNDF).</span><span class="sxs-lookup"><span data-stu-id="2e074-110">The return value is the bitwise OR operator of the MCIWnd window styles (MCIWNDF flags).</span></span>

## <a name="requirements"></a><span data-ttu-id="2e074-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2e074-111">Requirements</span></span>



| <span data-ttu-id="2e074-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e074-112">Requirement</span></span> | <span data-ttu-id="2e074-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e074-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2e074-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e074-114">Minimum supported client</span></span><br/> | <span data-ttu-id="2e074-115">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2e074-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2e074-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e074-116">Minimum supported server</span></span><br/> | <span data-ttu-id="2e074-117">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2e074-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2e074-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="2e074-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e074-119"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e074-119"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e074-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e074-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e074-121">**MCIWndGetStyles**</span><span class="sxs-lookup"><span data-stu-id="2e074-121">**MCIWndGetStyles**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles)
</dt> </dl>

 

 





