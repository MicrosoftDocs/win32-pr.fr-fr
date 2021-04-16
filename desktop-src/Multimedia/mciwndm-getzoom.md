---
title: Message MCIWNDM_GETZOOM (VFW. h)
description: Le \_ message MCIWNDM GETZOOM récupère la valeur de zoom actuelle utilisée par un périphérique MCI. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetZoom.
ms.assetid: 92db8df2-515a-4616-a0f5-245d466ba379
keywords:
- Message MCIWNDM_GETZOOM Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETZOOM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcb4ae1883787f1b86dcc17f2d4a3e0e0ee29ced
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464982"
---
# <a name="mciwndm_getzoom-message"></a><span data-ttu-id="06f89-105">\_Message MCIWNDM GETZOOM</span><span class="sxs-lookup"><span data-stu-id="06f89-105">MCIWNDM\_GETZOOM message</span></span>

<span data-ttu-id="06f89-106">Le message **MCIWNDM \_ GETZOOM** récupère la valeur de zoom actuelle utilisée par un périphérique MCI.</span><span class="sxs-lookup"><span data-stu-id="06f89-106">The **MCIWNDM\_GETZOOM** message retrieves the current zoom value used by an MCI device.</span></span> <span data-ttu-id="06f89-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) .</span><span class="sxs-lookup"><span data-stu-id="06f89-107">You can send this message explicitly or by using the [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) macro.</span></span>


```C++
MCIWNDM_GETZOOM 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="06f89-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="06f89-108">Return Value</span></span>

<span data-ttu-id="06f89-109">Retourne les valeurs les plus récentes utilisées avec [**MCIWNDM \_ SETZOOM**](mciwndm-setzoom.md).</span><span class="sxs-lookup"><span data-stu-id="06f89-109">Returns the most recent values used with [**MCIWNDM\_SETZOOM**](mciwndm-setzoom.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="06f89-110">Notes</span><span class="sxs-lookup"><span data-stu-id="06f89-110">Remarks</span></span>

<span data-ttu-id="06f89-111">Une valeur de retour de 100 indique que l’image n’est pas zoomée.</span><span class="sxs-lookup"><span data-stu-id="06f89-111">A return value of 100 indicates the image is not zoomed.</span></span> <span data-ttu-id="06f89-112">Une valeur de 200 indique que l’image est agrandie à deux fois sa taille d’origine.</span><span class="sxs-lookup"><span data-stu-id="06f89-112">A value of 200 indicates the image is enlarged to twice its original size.</span></span> <span data-ttu-id="06f89-113">Une valeur de 50 indique que l’image est réduite à la moitié de sa taille d’origine.</span><span class="sxs-lookup"><span data-stu-id="06f89-113">A value of 50 indicates the image is reduced to half its original size.</span></span>

## <a name="requirements"></a><span data-ttu-id="06f89-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06f89-114">Requirements</span></span>



| <span data-ttu-id="06f89-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06f89-115">Requirement</span></span> | <span data-ttu-id="06f89-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="06f89-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="06f89-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06f89-117">Minimum supported client</span></span><br/> | <span data-ttu-id="06f89-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06f89-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="06f89-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06f89-119">Minimum supported server</span></span><br/> | <span data-ttu-id="06f89-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06f89-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="06f89-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="06f89-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="06f89-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="06f89-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06f89-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06f89-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06f89-124">**MCIWndGetZoom**</span><span class="sxs-lookup"><span data-stu-id="06f89-124">**MCIWndGetZoom**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom)
</dt> <dt>

[<span data-ttu-id="06f89-125">**MCIWNDM \_ SETZOOM**</span><span class="sxs-lookup"><span data-stu-id="06f89-125">**MCIWNDM\_SETZOOM**</span></span>](mciwndm-setzoom.md)
</dt> </dl>

 

 





