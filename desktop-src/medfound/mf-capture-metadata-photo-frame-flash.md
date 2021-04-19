---
description: Indique si un flash a été déclenché pour le frame capturé.
ms.assetid: CF900CB4-8967-40F3-B60C-867192A641E9
title: Attribut MF_CAPTURE_METADATA_PHOTO_FRAME_FLASH (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ff5e9a47c07c8d7a2cec4e7dbf7b34669301122
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544759"
---
# <a name="mf_capture_metadata_photo_frame_flash-attribute"></a><span data-ttu-id="a5eda-103">\_Attribut Flash de l' \_ \_ \_ image de MÉTADONNÉEs de capture MF \_</span><span class="sxs-lookup"><span data-stu-id="a5eda-103">MF\_CAPTURE\_METADATA\_PHOTO\_FRAME\_FLASH attribute</span></span>

<span data-ttu-id="a5eda-104">Indique si un flash a été déclenché pour le frame capturé.</span><span class="sxs-lookup"><span data-stu-id="a5eda-104">Indicates if a flash was triggered for the captured frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="a5eda-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="a5eda-105">Data type</span></span>

<span data-ttu-id="a5eda-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a5eda-106">**UINT32**</span></span>



| <span data-ttu-id="a5eda-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5eda-107">Value</span></span>                                                                               | <span data-ttu-id="a5eda-108">Signification</span><span class="sxs-lookup"><span data-stu-id="a5eda-108">Meaning</span></span>                                                                                                                                               |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a5eda-109"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a5eda-109"><dt>0</dt></span></span> </dl>        | <span data-ttu-id="a5eda-110">Un flash n’a pas été déclenché sur ce frame.</span><span class="sxs-lookup"><span data-stu-id="a5eda-110">A flash was not triggered on this frame.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="a5eda-111"><dt>Différent de zéro</dt></span><span class="sxs-lookup"><span data-stu-id="a5eda-111"><dt>non-zero</dt></span></span> </dl> | <span data-ttu-id="a5eda-112">Un flash a été déclenché sur ce frame.</span><span class="sxs-lookup"><span data-stu-id="a5eda-112">A flash was triggered on this frame.</span></span><br/>                                                                                                       |
| <dl> <span data-ttu-id="a5eda-113"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a5eda-113"><dt>1</dt></span></span> </dl>        | <span data-ttu-id="a5eda-114">Réservé</span><span class="sxs-lookup"><span data-stu-id="a5eda-114">Reserved</span></span><br/> <span data-ttu-id="a5eda-115">Ne vérifiez pas explicitement la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="a5eda-115">Do not explicitly check for a value of 1.</span></span> <span data-ttu-id="a5eda-116">Les applications doivent uniquement vérifier les ! = 0 pour indiquer si un flash a été déclenché.</span><span class="sxs-lookup"><span data-stu-id="a5eda-116">Applications should only check for !=0 to indicate if a flash was triggered.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a5eda-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5eda-117">Requirements</span></span>



| <span data-ttu-id="a5eda-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5eda-118">Requirement</span></span> | <span data-ttu-id="a5eda-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5eda-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a5eda-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5eda-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a5eda-121">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5eda-121">Windows 8.1 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a5eda-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5eda-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a5eda-123">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5eda-123">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="a5eda-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="a5eda-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5eda-125"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5eda-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5eda-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5eda-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5eda-127">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a5eda-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




