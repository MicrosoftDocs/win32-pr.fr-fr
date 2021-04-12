---
title: Message MCIWNDM_GET_SOURCE (VFW. h)
description: Le \_ \_ message source MCIWNDM obtient les coordonnées du rectangle source utilisé pour le rognage des images d’un fichier AVI lors de la lecture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetSource.
ms.assetid: d5f25926-5a3d-412e-8248-fbf307583757
keywords:
- Message MCIWNDM_GET_SOURCE Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GET_SOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85147182d06386efed73229fcdd6c75372244fd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385024"
---
# <a name="mciwndm_get_source-message"></a><span data-ttu-id="6898d-105">MCIWNDM \_ recevoir le \_ message source</span><span class="sxs-lookup"><span data-stu-id="6898d-105">MCIWNDM\_GET\_SOURCE message</span></span>

<span data-ttu-id="6898d-106">Le **message \_ \_ source MCIWNDM obtient** les coordonnées du rectangle source utilisé pour le rognage des images d’un fichier AVI lors de la lecture.</span><span class="sxs-lookup"><span data-stu-id="6898d-106">The **MCIWNDM\_GET\_SOURCE** message retrieves the coordinates of the source rectangle used for cropping the images of an AVI file during playback.</span></span> <span data-ttu-id="6898d-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) .</span><span class="sxs-lookup"><span data-stu-id="6898d-107">You can send this message explicitly or by using the [**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) macro.</span></span>


```C++
MCIWNDM_GET_SOURCE 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a><span data-ttu-id="6898d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6898d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6898d-109"><span id="prc"></span><span id="PRC"></span>*République*</span><span class="sxs-lookup"><span data-stu-id="6898d-109"><span id="prc"></span><span id="PRC"></span>*prc*</span></span>
</dt> <dd>

<span data-ttu-id="6898d-110">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) pour contenir les coordonnées du rectangle source.</span><span class="sxs-lookup"><span data-stu-id="6898d-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to contain the coordinates of the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6898d-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6898d-111">Return Value</span></span>

<span data-ttu-id="6898d-112">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="6898d-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6898d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6898d-113">Requirements</span></span>



| <span data-ttu-id="6898d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6898d-114">Requirement</span></span> | <span data-ttu-id="6898d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="6898d-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6898d-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6898d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6898d-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6898d-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6898d-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6898d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6898d-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6898d-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6898d-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="6898d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6898d-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="6898d-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6898d-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6898d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6898d-123">**MCIWndGetSource**</span><span class="sxs-lookup"><span data-stu-id="6898d-123">**MCIWndGetSource**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource)
</dt> </dl>

 

