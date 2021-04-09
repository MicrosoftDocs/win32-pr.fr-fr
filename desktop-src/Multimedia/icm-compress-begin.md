---
title: Message ICM_COMPRESS_BEGIN (VFW. h)
description: Le message de début de la \_ compression ICM \_ indique à un pilote de compression vidéo de préparer la compression des données. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICCompressBegin.
ms.assetid: dd1d3a66-c625-4f55-b65a-8545c1c16301
keywords:
- Message ICM_COMPRESS_BEGIN Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_COMPRESS_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e358aa3ab589af0be1e4e490c141ed41baeb5874
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033240"
---
# <a name="icm_compress_begin-message"></a><span data-ttu-id="e58b3-105">Message de début de la \_ compression ICM \_</span><span class="sxs-lookup"><span data-stu-id="e58b3-105">ICM\_COMPRESS\_BEGIN message</span></span>

<span data-ttu-id="e58b3-106">Le message de **\_ \_ début de la compression ICM** indique à un pilote de compression vidéo de préparer la compression des données.</span><span class="sxs-lookup"><span data-stu-id="e58b3-106">The **ICM\_COMPRESS\_BEGIN** message notifies a video compression driver to prepare to compress data.</span></span> <span data-ttu-id="e58b3-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICCompressBegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) .</span><span class="sxs-lookup"><span data-stu-id="e58b3-107">You can send this message explicitly or by using the [**ICCompressBegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) macro.</span></span>


```C++
ICM_COMPRESS_BEGIN 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="e58b3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e58b3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e58b3-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="e58b3-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="e58b3-110">Pointeur vers une structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenant le format d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e58b3-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="e58b3-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="e58b3-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="e58b3-112">Pointeur vers une structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenant le format de sortie.</span><span class="sxs-lookup"><span data-stu-id="e58b3-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the output format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e58b3-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e58b3-113">Return Value</span></span>

<span data-ttu-id="e58b3-114">Retourne ICERR \_ OK si le pilote prend en charge le BADFORMAT de compression ou de ICERR spécifié \_ si le format d’entrée ou de sortie n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e58b3-114">Returns ICERR\_OK if the driver supports the specified compression or ICERR\_BADFORMAT if the input or output format is not supported.</span></span>

## <a name="remarks"></a><span data-ttu-id="e58b3-115">Notes</span><span class="sxs-lookup"><span data-stu-id="e58b3-115">Remarks</span></span>

<span data-ttu-id="e58b3-116">Le pilote doit allouer et initialiser les tables ou la mémoire dont il a besoin pour compresser les formats de données lorsqu’il reçoit le message de [**\_ compression ICM**](icm-compress.md) .</span><span class="sxs-lookup"><span data-stu-id="e58b3-116">The driver should allocate and initialize any tables or memory that it needs for compressing the data formats when it receives the [**ICM\_COMPRESS**](icm-compress.md) message.</span></span>

<span data-ttu-id="e58b3-117">VCM enregistre les paramètres du message de début de la **\_ \_ compression ICM** le plus récent.</span><span class="sxs-lookup"><span data-stu-id="e58b3-117">VCM saves the settings of the most recent **ICM\_COMPRESS\_BEGIN** message.</span></span> <span data-ttu-id="e58b3-118">Les messages de [**\_ \_ fin**](icm-compress-end.md) de compression **ICM \_ \_ Begin** et ICM ne sont pas imbriqués.</span><span class="sxs-lookup"><span data-stu-id="e58b3-118">The **ICM\_COMPRESS\_BEGIN** and [**ICM\_COMPRESS\_END**](icm-compress-end.md) messages do not nest.</span></span> <span data-ttu-id="e58b3-119">Si votre pilote reçoit la compression ICM avant que la compression soit arrêtée avec la **\_ \_ terminaison** de compression ICM, il doit redémarrer la compression avec les nouveaux paramètres. **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="e58b3-119">If your driver receives **ICM\_COMPRESS\_BEGIN** before compression is stopped with **ICM\_COMPRESS\_END**, it should restart compression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="e58b3-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e58b3-120">Requirements</span></span>



| <span data-ttu-id="e58b3-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e58b3-121">Requirement</span></span> | <span data-ttu-id="e58b3-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="e58b3-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e58b3-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e58b3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e58b3-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e58b3-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e58b3-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e58b3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e58b3-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e58b3-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e58b3-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="e58b3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e58b3-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e58b3-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e58b3-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e58b3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e58b3-130">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="e58b3-130">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="e58b3-131">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="e58b3-131">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

