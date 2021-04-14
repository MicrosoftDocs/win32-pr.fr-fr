---
title: Message ICM_SETQUALITY (VFW. h)
description: Le \_ message SETQUALITY ICM fournit un pilote de compression vidéo avec un niveau de qualité à utiliser pendant la compression.
ms.assetid: 487ff1de-7178-440a-b38d-0b82a30d7297
keywords:
- Message ICM_SETQUALITY Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_SETQUALITY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a1523996ad336e64d4b34143cc26cd8d0937d5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385299"
---
# <a name="icm_setquality-message"></a><span data-ttu-id="2b5cd-104">\_Message SETQUALITY ICM</span><span class="sxs-lookup"><span data-stu-id="2b5cd-104">ICM\_SETQUALITY message</span></span>

<span data-ttu-id="2b5cd-105">Le **message \_ SETQUALITY ICM** fournit un pilote de compression vidéo avec un niveau de qualité à utiliser pendant la compression.</span><span class="sxs-lookup"><span data-stu-id="2b5cd-105">The **ICM\_SETQUALITY** message provides a video compression driver with a quality level to use during compression.</span></span>


```C++
ICM_SETQUALITY 
wParam = (DWORD) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="2b5cd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2b5cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b5cd-107"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span><span class="sxs-lookup"><span data-stu-id="2b5cd-107"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span></span>
</dt> <dd>

<span data-ttu-id="2b5cd-108">Nouvelle valeur de qualité.</span><span class="sxs-lookup"><span data-stu-id="2b5cd-108">New quality value.</span></span> <span data-ttu-id="2b5cd-109">Les valeurs de qualité sont comprises entre 0 et 10 000.</span><span class="sxs-lookup"><span data-stu-id="2b5cd-109">Quality values range from 0 to 10,000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b5cd-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2b5cd-110">Return Value</span></span>

<span data-ttu-id="2b5cd-111">Retourne ICERR \_ OK si le pilote prend en charge ce message ou ICERR \_ non pris en charge dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="2b5cd-111">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b5cd-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2b5cd-112">Requirements</span></span>



| <span data-ttu-id="2b5cd-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2b5cd-113">Requirement</span></span> | <span data-ttu-id="2b5cd-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b5cd-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2b5cd-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b5cd-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2b5cd-116">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2b5cd-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2b5cd-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b5cd-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2b5cd-118">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2b5cd-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2b5cd-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="2b5cd-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b5cd-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b5cd-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b5cd-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b5cd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b5cd-122">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="2b5cd-122">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="2b5cd-123">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="2b5cd-123">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





