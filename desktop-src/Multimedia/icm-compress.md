---
title: Message ICM_COMPRESS (VFW. h)
description: Le message de compression ICM \_ indique à un pilote de compression vidéo de compresser une trame de données dans une mémoire tampon définie par l’application.
ms.assetid: d95b943f-458d-4a5e-bab1-e3648d323395
keywords:
- Message ICM_COMPRESS Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_COMPRESS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8021a4c18ab47c9b5b848dd1cb097358f2714bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512187"
---
# <a name="icm_compress-message"></a><span data-ttu-id="4a679-104">\_Message de compression ICM</span><span class="sxs-lookup"><span data-stu-id="4a679-104">ICM\_COMPRESS message</span></span>

<span data-ttu-id="4a679-105">Le **message \_ de compression ICM** indique à un pilote de compression vidéo de compresser une trame de données dans une mémoire tampon définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="4a679-105">The **ICM\_COMPRESS** message notifies a video compression driver to compress a frame of data into an application-defined buffer.</span></span>


```C++
ICM_COMPRESS 
wParam = (DWORD) (LPVOID) &icc; 
lParam = sizeof(ICCOMPRESS); 
```



## <a name="parameters"></a><span data-ttu-id="4a679-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4a679-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a679-107"><span id="icc"></span><span id="ICC"></span>*rencontres*</span><span class="sxs-lookup"><span data-stu-id="4a679-107"><span id="icc"></span><span id="ICC"></span>*icc*</span></span>
</dt> <dd>

<span data-ttu-id="4a679-108">Pointeur vers une structure [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress) .</span><span class="sxs-lookup"><span data-stu-id="4a679-108">Pointer to an [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress) structure.</span></span> <span data-ttu-id="4a679-109">Les membres suivants de cette structure spécifient les paramètres de compression suivants : **lpbiInput**, **lpInput**, **lpbiOutput**, **lpOutput**, **lpbiPrev**, **lpPrev**, **lpckid**, **lpdwFlags**, **dwFrameSize** et **dwQuality**.</span><span class="sxs-lookup"><span data-stu-id="4a679-109">The following members of this structure specify the compression parameters: **lpbiInput**, **lpInput**, **lpbiOutput**, **lpOutput**, **lpbiPrev**, **lpPrev**, **lpckid**, **lpdwFlags**, **dwFrameSize**, and **dwQuality**.</span></span> <span data-ttu-id="4a679-110">Le pilote doit également utiliser le membre **biSizeImage** de la structure [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) associée à **lpbiOutput** de **ICCOMPRESS** pour retourner la taille du frame compressé.</span><span class="sxs-lookup"><span data-stu-id="4a679-110">The driver should also use the **biSizeImage** member of the [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) structure associated with **lpbiOutput** of **ICCOMPRESS** to return the size of the compressed frame.</span></span>

</dd> <dt>

<span data-ttu-id="4a679-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="4a679-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="4a679-112">Taille, en octets, de [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress).</span><span class="sxs-lookup"><span data-stu-id="4a679-112">Size, in bytes, of [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a679-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4a679-113">Return Value</span></span>

<span data-ttu-id="4a679-114">Retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="4a679-114">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a679-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4a679-115">Requirements</span></span>



| <span data-ttu-id="4a679-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4a679-116">Requirement</span></span> | <span data-ttu-id="4a679-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a679-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4a679-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a679-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4a679-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a679-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4a679-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a679-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4a679-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a679-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4a679-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="4a679-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a679-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a679-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a679-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a679-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a679-125">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="4a679-125">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="4a679-126">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="4a679-126">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

