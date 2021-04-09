---
title: Message ICM_GETQUALITY (VFW. h)
description: Le \_ message GETQUALITY ICM interroge un pilote de compression vidéo pour retourner son paramètre de qualité actuel.
ms.assetid: 8da99a26-7b2a-4118-89e1-7485915cbdc9
keywords:
- Message ICM_GETQUALITY Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_GETQUALITY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c4fa2a26e1fe5fa111585ce0a59422a2fe9b072
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942897"
---
# <a name="icm_getquality-message"></a><span data-ttu-id="8e463-104">\_Message GETQUALITY ICM</span><span class="sxs-lookup"><span data-stu-id="8e463-104">ICM\_GETQUALITY message</span></span>

<span data-ttu-id="8e463-105">Le **message \_ GETQUALITY ICM** interroge un pilote de compression vidéo pour retourner son paramètre de qualité actuel.</span><span class="sxs-lookup"><span data-stu-id="8e463-105">The **ICM\_GETQUALITY** message queries a video compression driver to return its current quality setting.</span></span>


```C++
ICM_GETQUALITY 
wParam = (DWORD) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="8e463-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8e463-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e463-107"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span><span class="sxs-lookup"><span data-stu-id="8e463-107"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span></span>
</dt> <dd>

<span data-ttu-id="8e463-108">Adresse qui doit contenir la valeur de qualité actuelle.</span><span class="sxs-lookup"><span data-stu-id="8e463-108">Address to contain the current quality value.</span></span> <span data-ttu-id="8e463-109">Les valeurs de qualité sont comprises entre 0 et 10 000.</span><span class="sxs-lookup"><span data-stu-id="8e463-109">Quality values range from 0 to 10,000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e463-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8e463-110">Return Value</span></span>

<span data-ttu-id="8e463-111">Retourne ICERR \_ OK si le pilote prend en charge ce message ou ICERR \_ non pris en charge dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="8e463-111">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e463-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8e463-112">Requirements</span></span>



| <span data-ttu-id="8e463-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8e463-113">Requirement</span></span> | <span data-ttu-id="8e463-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="8e463-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8e463-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e463-115">Minimum supported client</span></span><br/> | <span data-ttu-id="8e463-116">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8e463-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8e463-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e463-117">Minimum supported server</span></span><br/> | <span data-ttu-id="8e463-118">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8e463-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8e463-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="8e463-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e463-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e463-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e463-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e463-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e463-122">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="8e463-122">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="8e463-123">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="8e463-123">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





