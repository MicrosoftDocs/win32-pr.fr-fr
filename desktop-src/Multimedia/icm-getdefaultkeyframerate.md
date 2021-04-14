---
title: Message ICM_GETDEFAULTKEYFRAMERATE (VFW. h)
description: Le \_ message GETDEFAULTKEYFRAMERATE ICM interroge un pilote de compression vidéo pour son espace d’image clé par défaut (ou préféré). Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICGetDefaulteyFrameRate.
ms.assetid: 2ebe37cc-3ec2-4b52-bd8f-71c44b704647
keywords:
- Message ICM_GETDEFAULTKEYFRAMERATE Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_GETDEFAULTKEYFRAMERATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64f2796ca1c2de10222330217a0e1deb7883baa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384771"
---
# <a name="icm_getdefaultkeyframerate-message"></a><span data-ttu-id="18c69-105">\_Message GETDEFAULTKEYFRAMERATE ICM</span><span class="sxs-lookup"><span data-stu-id="18c69-105">ICM\_GETDEFAULTKEYFRAMERATE message</span></span>

<span data-ttu-id="18c69-106">Le **message \_ GETDEFAULTKEYFRAMERATE ICM** interroge un pilote de compression vidéo pour son espace d’image clé par défaut (ou préféré).</span><span class="sxs-lookup"><span data-stu-id="18c69-106">The **ICM\_GETDEFAULTKEYFRAMERATE** message queries a video compression driver for its default (or preferred) key-frame spacing.</span></span> <span data-ttu-id="18c69-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICGetDefaulteyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) .</span><span class="sxs-lookup"><span data-stu-id="18c69-107">You can send this message explicitly or by using the [**ICGetDefaulteyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) macro.</span></span>


```C++
ICM_GETDEFAULTKEYFRAMERATE 
wParam = (DWORD_PTR) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="18c69-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="18c69-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18c69-109"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span><span class="sxs-lookup"><span data-stu-id="18c69-109"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span></span>
</dt> <dd>

<span data-ttu-id="18c69-110">Adresse qui doit contenir l’espacement de l’image clé préféré.</span><span class="sxs-lookup"><span data-stu-id="18c69-110">Address to contain the preferred key-frame spacing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18c69-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="18c69-111">Return Value</span></span>

<span data-ttu-id="18c69-112">Retourne ICERR \_ OK si le pilote prend en charge ce message ou ICERR \_ non pris en charge dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="18c69-112">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="18c69-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18c69-113">Requirements</span></span>



| <span data-ttu-id="18c69-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18c69-114">Requirement</span></span> | <span data-ttu-id="18c69-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="18c69-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="18c69-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18c69-116">Minimum supported client</span></span><br/> | <span data-ttu-id="18c69-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18c69-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="18c69-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18c69-118">Minimum supported server</span></span><br/> | <span data-ttu-id="18c69-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18c69-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="18c69-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="18c69-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="18c69-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="18c69-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18c69-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18c69-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18c69-123">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="18c69-123">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="18c69-124">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="18c69-124">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





