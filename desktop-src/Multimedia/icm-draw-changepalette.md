---
title: Message ICM_DRAW_CHANGEPALETTE (VFW. h)
description: Le \_ message CHANGEPALETTE de dessin ICM \_ indique à un pilote de rendu que la palette de films est en modification. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDrawChangePalette.
ms.assetid: 974fc0d8-d0c7-4a82-af84-68b53f753259
keywords:
- Message ICM_DRAW_CHANGEPALETTE Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_CHANGEPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6364abb2c535158b2e64ff311041b00490c5958c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843757"
---
# <a name="icm_draw_changepalette-message"></a><span data-ttu-id="b1585-105">\_Message CHANGEPALETTE de dessin ICM \_</span><span class="sxs-lookup"><span data-stu-id="b1585-105">ICM\_DRAW\_CHANGEPALETTE message</span></span>

<span data-ttu-id="b1585-106">Le **message \_ \_ CHANGEPALETTE de dessin ICM** indique à un pilote de rendu que la palette de films est en modification.</span><span class="sxs-lookup"><span data-stu-id="b1585-106">The **ICM\_DRAW\_CHANGEPALETTE** message notifies a rendering driver that the movie palette is changing.</span></span> <span data-ttu-id="b1585-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDrawChangePalette**](/windows/desktop/api/Vfw/nf-vfw-icdrawchangepalette) .</span><span class="sxs-lookup"><span data-stu-id="b1585-107">You can send this message explicitly or by using the [**ICDrawChangePalette**](/windows/desktop/api/Vfw/nf-vfw-icdrawchangepalette) macro.</span></span>


```C++
ICM_DRAW_CHANGEPALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="b1585-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b1585-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1585-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="b1585-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="b1585-110">Pointeur vers une structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenant le nouveau format et le tableau de couleurs facultatif.</span><span class="sxs-lookup"><span data-stu-id="b1585-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the new format and optional color table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1585-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b1585-111">Return Value</span></span>

<span data-ttu-id="b1585-112">Retourne ICERR \_ OK en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="b1585-112">Returns ICERR\_OK if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1585-113">Notes</span><span class="sxs-lookup"><span data-stu-id="b1585-113">Remarks</span></span>

<span data-ttu-id="b1585-114">Ce message doit être pris en charge par les gestionnaires de rendu installables qui dessinent des fichiers DIB avec une structure interne qui comprend une palette.</span><span class="sxs-lookup"><span data-stu-id="b1585-114">This message should be supported by installable rendering handlers that draw DIBs with an internal structure that includes a palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1585-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1585-115">Requirements</span></span>



| <span data-ttu-id="b1585-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b1585-116">Requirement</span></span> | <span data-ttu-id="b1585-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1585-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b1585-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1585-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b1585-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b1585-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b1585-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1585-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b1585-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b1585-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b1585-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="b1585-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1585-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1585-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1585-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1585-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1585-125">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="b1585-125">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="b1585-126">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="b1585-126">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

