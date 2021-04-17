---
title: Message ICM_COMPRESS_FRAMES_INFO (VFW. h)
description: Le \_ message d' \_ informations sur les trames de compression ICM \_ avertit un pilote de compression de la définition des paramètres de la compression en attente.
ms.assetid: d2f6f3b7-dff6-4fef-a642-cb77b00119af
keywords:
- Message ICM_COMPRESS_FRAMES_INFO Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_COMPRESS_FRAMES_INFO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbb6df0eab7706ebfc03a5e3069d4323be26ecdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466474"
---
# <a name="icm_compress_frames_info-message"></a><span data-ttu-id="e0c04-104">\_Message d' \_ \_ informations sur les trames de compression ICM</span><span class="sxs-lookup"><span data-stu-id="e0c04-104">ICM\_COMPRESS\_FRAMES\_INFO message</span></span>

<span data-ttu-id="e0c04-105">Le message d' **\_ \_ \_ informations sur les trames** de compression ICM avertit un pilote de compression de la définition des paramètres de la compression en attente.</span><span class="sxs-lookup"><span data-stu-id="e0c04-105">The **ICM\_COMPRESS\_FRAMES\_INFO** message notifies a compression driver to set the parameters for the pending compression.</span></span>


```C++
ICM_COMPRESS_FRAMES_INFO 
wParam = (DWORD) (LPVOID) &icf; 
lParam = sizeof(ICCOMPRESSFRAMES); 
```



## <a name="parameters"></a><span data-ttu-id="e0c04-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e0c04-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0c04-107"><span id="icf"></span><span id="ICF"></span>*ICF*</span><span class="sxs-lookup"><span data-stu-id="e0c04-107"><span id="icf"></span><span id="ICF"></span>*icf*</span></span>
</dt> <dd>

<span data-ttu-id="e0c04-108">Pointeur vers une structure [**ICCOMPRESSFRAMES**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes) .</span><span class="sxs-lookup"><span data-stu-id="e0c04-108">Pointer to an [**ICCOMPRESSFRAMES**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes) structure.</span></span> <span data-ttu-id="e0c04-109">Les membres **GetData** et **PutData** de cette structure ne sont pas utilisés avec ce message.</span><span class="sxs-lookup"><span data-stu-id="e0c04-109">The **GetData** and **PutData** members of this structure are not used with this message.</span></span>

</dd> <dt>

<span data-ttu-id="e0c04-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="e0c04-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="e0c04-111">Taille, en octets, de [**ICCOMPRESSFRAMES**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes).</span><span class="sxs-lookup"><span data-stu-id="e0c04-111">Size, in bytes, of [**ICCOMPRESSFRAMES**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0c04-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e0c04-112">Return Value</span></span>

<span data-ttu-id="e0c04-113">Retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="e0c04-113">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0c04-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e0c04-114">Remarks</span></span>

<span data-ttu-id="e0c04-115">Un compresseur peut utiliser ce message pour déterminer la quantité d’espace à allouer pour chaque image pendant la compression.</span><span class="sxs-lookup"><span data-stu-id="e0c04-115">A compressor can use this message to determine how much space to allocate for each frame while compressing.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0c04-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e0c04-116">Requirements</span></span>



| <span data-ttu-id="e0c04-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e0c04-117">Requirement</span></span> | <span data-ttu-id="e0c04-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0c04-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e0c04-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0c04-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e0c04-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e0c04-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e0c04-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0c04-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e0c04-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e0c04-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e0c04-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="e0c04-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0c04-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0c04-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0c04-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0c04-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0c04-126">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="e0c04-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="e0c04-127">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="e0c04-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





