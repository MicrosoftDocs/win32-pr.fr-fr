---
title: Message MCIWNDM_GET_DEST (VFW. h)
description: Le \_ message MCIWNDM obtenir \_ dest récupère les coordonnées du rectangle de destination utilisé pour le zoom ou l’étirement des images d’un fichier AVI lors de la lecture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetDest.
ms.assetid: d4d8a3eb-aad4-4435-a23b-7a9c55fc194d
keywords:
- Message MCIWNDM_GET_DEST Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GET_DEST
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab5f16b434caef56e6c6aa97bfd767770dc05ee1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032327"
---
# <a name="mciwndm_get_dest-message"></a><span data-ttu-id="680f0-105">MCIWNDM \_ obtient le \_ message de dest.</span><span class="sxs-lookup"><span data-stu-id="680f0-105">MCIWNDM\_GET\_DEST message</span></span>

<span data-ttu-id="680f0-106">Le message **MCIWNDM \_ obtenir \_ dest** récupère les coordonnées du rectangle de destination utilisé pour le zoom ou l’étirement des images d’un fichier AVI lors de la lecture.</span><span class="sxs-lookup"><span data-stu-id="680f0-106">The **MCIWNDM\_GET\_DEST** message retrieves the coordinates of the destination rectangle used for zooming or stretching the images of an AVI file during playback.</span></span> <span data-ttu-id="680f0-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest) .</span><span class="sxs-lookup"><span data-stu-id="680f0-107">You can send this message explicitly or by using the [**MCIWndGetDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest) macro.</span></span>


```C++
MCIWNDM_GET_DEST 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a><span data-ttu-id="680f0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="680f0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="680f0-109"><span id="prc"></span><span id="PRC"></span>*République*</span><span class="sxs-lookup"><span data-stu-id="680f0-109"><span id="prc"></span><span id="PRC"></span>*prc*</span></span>
</dt> <dd>

<span data-ttu-id="680f0-110">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) pour retourner les coordonnées du rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="680f0-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to return the coordinates of the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="680f0-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="680f0-111">Return Value</span></span>

<span data-ttu-id="680f0-112">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="680f0-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="680f0-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="680f0-113">Requirements</span></span>



| <span data-ttu-id="680f0-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="680f0-114">Requirement</span></span> | <span data-ttu-id="680f0-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="680f0-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="680f0-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="680f0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="680f0-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="680f0-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="680f0-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="680f0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="680f0-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="680f0-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="680f0-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="680f0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="680f0-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="680f0-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="680f0-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="680f0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="680f0-123">**MCIWndGetDest**</span><span class="sxs-lookup"><span data-stu-id="680f0-123">**MCIWndGetDest**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest)
</dt> </dl>

 

