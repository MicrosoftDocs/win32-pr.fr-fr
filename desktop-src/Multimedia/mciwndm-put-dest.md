---
title: Message MCIWNDM_PUT_DEST (VFW. h)
description: Le \_ message MCIWNDM put \_ dest redéfinit les coordonnées du rectangle de destination utilisé pour le zoom ou l’étirement des images d’un fichier AVI lors de la lecture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndPutDest.
ms.assetid: 0b13d473-ef93-41a2-bbb2-09fbf264493e
keywords:
- Message MCIWNDM_PUT_DEST Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_PUT_DEST
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba150f450f71c3593976f98c9935233918becd70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742949"
---
# <a name="mciwndm_put_dest-message"></a><span data-ttu-id="b0fae-105">MCIWNDM \_ put \_ dest message</span><span class="sxs-lookup"><span data-stu-id="b0fae-105">MCIWNDM\_PUT\_DEST message</span></span>

<span data-ttu-id="b0fae-106">Le message **MCIWNDM \_ put \_ dest** redéfinit les coordonnées du rectangle de destination utilisé pour le zoom ou l’étirement des images d’un fichier AVI lors de la lecture.</span><span class="sxs-lookup"><span data-stu-id="b0fae-106">The **MCIWNDM\_PUT\_DEST** message redefines the coordinates of the destination rectangle used for zooming or stretching the images of an AVI file during playback.</span></span> <span data-ttu-id="b0fae-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) .</span><span class="sxs-lookup"><span data-stu-id="b0fae-107">You can send this message explicitly or by using the [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) macro.</span></span>


```C++
MCIWNDM_PUT_DEST 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a><span data-ttu-id="b0fae-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b0fae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0fae-109"><span id="prc"></span><span id="PRC"></span>*République*</span><span class="sxs-lookup"><span data-stu-id="b0fae-109"><span id="prc"></span><span id="PRC"></span>*prc*</span></span>
</dt> <dd>

<span data-ttu-id="b0fae-110">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) contenant les coordonnées du rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="b0fae-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure containing the coordinates of the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0fae-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b0fae-111">Return Value</span></span>

<span data-ttu-id="b0fae-112">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="b0fae-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0fae-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b0fae-113">Requirements</span></span>



| <span data-ttu-id="b0fae-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b0fae-114">Requirement</span></span> | <span data-ttu-id="b0fae-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="b0fae-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b0fae-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0fae-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b0fae-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b0fae-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b0fae-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0fae-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b0fae-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b0fae-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b0fae-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="b0fae-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0fae-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0fae-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0fae-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0fae-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0fae-123">**MCIWndPutDest**</span><span class="sxs-lookup"><span data-stu-id="b0fae-123">**MCIWndPutDest**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest)
</dt> </dl>

 

