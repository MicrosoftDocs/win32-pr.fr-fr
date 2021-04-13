---
title: Message ICM_DRAW_QUERY (VFW. h)
description: Le \_ message de requête ICM Draw \_ interroge un pilote de rendu pour déterminer s’il peut restituer des données dans un format spécifique. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDrawQuery.
ms.assetid: b829a04b-c1be-47c6-96e9-a6dc6f802811
keywords:
- Message ICM_DRAW_QUERY Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27266484cffa503583df32b60c6e8a0c04f344f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465667"
---
# <a name="icm_draw_query-message"></a><span data-ttu-id="2b56c-105">Message de requête ICM de \_ dessin \_</span><span class="sxs-lookup"><span data-stu-id="2b56c-105">ICM\_DRAW\_QUERY message</span></span>

<span data-ttu-id="2b56c-106">Le message de **\_ \_ requête ICM Draw** interroge un pilote de rendu pour déterminer s’il peut restituer des données dans un format spécifique.</span><span class="sxs-lookup"><span data-stu-id="2b56c-106">The **ICM\_DRAW\_QUERY** message queries a rendering driver to determine if it can render data in a specific format.</span></span> <span data-ttu-id="2b56c-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDrawQuery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) .</span><span class="sxs-lookup"><span data-stu-id="2b56c-107">You can send this message explicitly or by using the [**ICDrawQuery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) macro.</span></span>


```C++
ICM_DRAW_QUERY 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="2b56c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2b56c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b56c-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="2b56c-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="2b56c-110">Pointeur vers une structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenant le format d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2b56c-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b56c-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2b56c-111">Return Value</span></span>

<span data-ttu-id="2b56c-112">Retourne ICERR \_ OK si le pilote peut restituer des données au format spécifié ou ICERR BADFORMAT dans le \_ cas contraire.</span><span class="sxs-lookup"><span data-stu-id="2b56c-112">Returns ICERR\_OK if the driver can render data in the specified format or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b56c-113">Notes</span><span class="sxs-lookup"><span data-stu-id="2b56c-113">Remarks</span></span>

<span data-ttu-id="2b56c-114">Ce message diffère du message [**ICM \_ Draw \_ Begin**](icm-draw-begin.md) dans le sens où il interroge le pilote de manière générale.</span><span class="sxs-lookup"><span data-stu-id="2b56c-114">This message differs from the [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) message in that it queries the driver in a general sense.</span></span> <span data-ttu-id="2b56c-115">**ICM \_ DESSINER \_ commencer** détermine si le pilote peut dessiner les données à l’aide du format spécifié dans des conditions spécifiques, telles que l’étirement de l’image.</span><span class="sxs-lookup"><span data-stu-id="2b56c-115">**ICM\_DRAW\_BEGIN** determines if the driver can draw the data using the specified format under specific conditions, such as stretching the image.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b56c-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2b56c-116">Requirements</span></span>



| <span data-ttu-id="2b56c-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2b56c-117">Requirement</span></span> | <span data-ttu-id="2b56c-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b56c-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2b56c-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b56c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2b56c-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2b56c-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2b56c-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b56c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2b56c-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2b56c-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2b56c-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="2b56c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b56c-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b56c-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b56c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b56c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b56c-126">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="2b56c-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="2b56c-127">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="2b56c-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

