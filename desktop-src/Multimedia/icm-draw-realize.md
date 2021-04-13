---
title: Message ICM_DRAW_REALIZE (VFW. h)
description: Le \_ message d’établissement de dessin ICM \_ informe un pilote de rendu de réaliser sa palette de dessin pendant le dessin. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDrawRealize.
ms.assetid: 501540cd-41e2-4f80-abf8-2ec2179970a9
keywords:
- Message ICM_DRAW_REALIZE Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_REALIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd054c16caae55cba25c30098337e54b0ec4b681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384487"
---
# <a name="icm_draw_realize-message"></a><span data-ttu-id="ab73c-105">\_Message d’établissement de dessin ICM \_</span><span class="sxs-lookup"><span data-stu-id="ab73c-105">ICM\_DRAW\_REALIZE message</span></span>

<span data-ttu-id="ab73c-106">Le message d' **établissement de dessin ICM informe \_ \_** un pilote de rendu de réaliser sa palette de dessin pendant le dessin.</span><span class="sxs-lookup"><span data-stu-id="ab73c-106">The **ICM\_DRAW\_REALIZE** message notifies a rendering driver to realize its drawing palette while drawing.</span></span> <span data-ttu-id="ab73c-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDrawRealize**](/windows/desktop/api/Vfw/nf-vfw-icdrawrealize) .</span><span class="sxs-lookup"><span data-stu-id="ab73c-107">You can send this message explicitly or by using the [**ICDrawRealize**](/windows/desktop/api/Vfw/nf-vfw-icdrawrealize) macro.</span></span>


```C++
ICM_DRAW_REALIZE 
wParam = (DWORD_PTR) (UINT_PTR) (HDC) hdc; 
lParam = (DWORD_PTR) (BOOL) fBackground; 
```



## <a name="parameters"></a><span data-ttu-id="ab73c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ab73c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab73c-109"><span id="hdc"></span><span id="HDC"></span>*HDC*</span><span class="sxs-lookup"><span data-stu-id="ab73c-109"><span id="hdc"></span><span id="HDC"></span>*hdc*</span></span>
</dt> <dd>

<span data-ttu-id="ab73c-110">Handle vers le contrôleur de périphérique utilisé pour réaliser la palette.</span><span class="sxs-lookup"><span data-stu-id="ab73c-110">Handle to the DC used to realize the palette.</span></span>

</dd> <dt>

<span data-ttu-id="ab73c-111"><span id="fBackground"></span><span id="fbackground"></span><span id="FBACKGROUND"></span>*fBackground*</span><span class="sxs-lookup"><span data-stu-id="ab73c-111"><span id="fBackground"></span><span id="fbackground"></span><span id="FBACKGROUND"></span>*fBackground*</span></span>
</dt> <dd>

<span data-ttu-id="ab73c-112">Indicateur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="ab73c-112">Background flag.</span></span> <span data-ttu-id="ab73c-113">Spécifiez **true** pour réaliser la palette en tant que tâche en arrière-plan ou **false** pour réaliser la palette au premier plan.</span><span class="sxs-lookup"><span data-stu-id="ab73c-113">Specify **TRUE** to realize the palette as a background task or **FALSE** to realize the palette in the foreground.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab73c-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ab73c-114">Return Value</span></span>

<span data-ttu-id="ab73c-115">Retourne ICERR \_ OK si la palette de dessin est réalisée ou ICERR \_ non prise en charge si la palette associée aux données décompressées est obtenue.</span><span class="sxs-lookup"><span data-stu-id="ab73c-115">Returns ICERR\_OK if the drawing palette is realized or ICERR\_UNSUPPORTED if the palette associated with the decompressed data is realized.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab73c-116">Notes</span><span class="sxs-lookup"><span data-stu-id="ab73c-116">Remarks</span></span>

<span data-ttu-id="ab73c-117">Les pilotes doivent répondre à ce message uniquement si la palette de dessin est différente de la palette décompressée.</span><span class="sxs-lookup"><span data-stu-id="ab73c-117">Drivers need to respond to this message only if the drawing palette is different from the decompressed palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab73c-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab73c-118">Requirements</span></span>



| <span data-ttu-id="ab73c-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ab73c-119">Requirement</span></span> | <span data-ttu-id="ab73c-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab73c-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ab73c-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab73c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ab73c-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ab73c-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ab73c-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab73c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ab73c-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ab73c-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ab73c-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="ab73c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab73c-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab73c-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab73c-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab73c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab73c-128">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="ab73c-128">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="ab73c-129">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="ab73c-129">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





