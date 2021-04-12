---
title: Message ICM_GETDEFAULTQUALITY (VFW. h)
description: Le \_ message GETDEFAULTQUALITY ICM interroge un pilote de compression vidéo pour fournir son paramètre de qualité par défaut. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICGetDefaultQuality.
ms.assetid: bba7f451-52c2-4684-a7c9-e4b05cb946c5
keywords:
- Message ICM_GETDEFAULTQUALITY Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_GETDEFAULTQUALITY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4350539851ca720e3538d297f955a56fedfc4a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464630"
---
# <a name="icm_getdefaultquality-message"></a><span data-ttu-id="2d411-105">\_Message GETDEFAULTQUALITY ICM</span><span class="sxs-lookup"><span data-stu-id="2d411-105">ICM\_GETDEFAULTQUALITY message</span></span>

<span data-ttu-id="2d411-106">Le **message \_ GETDEFAULTQUALITY ICM** interroge un pilote de compression vidéo pour fournir son paramètre de qualité par défaut.</span><span class="sxs-lookup"><span data-stu-id="2d411-106">The **ICM\_GETDEFAULTQUALITY** message queries a video compression driver to provide its default quality setting.</span></span> <span data-ttu-id="2d411-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) .</span><span class="sxs-lookup"><span data-stu-id="2d411-107">You can send this message explicitly or by using the [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) macro.</span></span>


```C++
ICM_GETDEFAULTQUALITY 
wParam = (DWORD_PTR) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="2d411-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d411-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d411-109"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span><span class="sxs-lookup"><span data-stu-id="2d411-109"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span></span>
</dt> <dd>

<span data-ttu-id="2d411-110">Adresse qui doit contenir la valeur de qualité par défaut.</span><span class="sxs-lookup"><span data-stu-id="2d411-110">Address to contain the default quality value.</span></span> <span data-ttu-id="2d411-111">Les valeurs de qualité sont comprises entre 0 et 10 000.</span><span class="sxs-lookup"><span data-stu-id="2d411-111">Quality values range from 0 to 10,000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d411-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2d411-112">Return Value</span></span>

<span data-ttu-id="2d411-113">Retourne ICERR \_ OK si le pilote prend en charge ce message ou ICERR \_ non pris en charge dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="2d411-113">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d411-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d411-114">Requirements</span></span>



| <span data-ttu-id="2d411-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d411-115">Requirement</span></span> | <span data-ttu-id="2d411-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d411-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2d411-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d411-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2d411-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2d411-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2d411-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d411-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2d411-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2d411-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2d411-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="2d411-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d411-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d411-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d411-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d411-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d411-124">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="2d411-124">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="2d411-125">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="2d411-125">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





