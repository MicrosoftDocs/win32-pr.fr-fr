---
description: Ces indicateurs définissent les paramètres de processeur vidéo (ProcAmp).
ms.assetid: 60d97b9e-d77c-4e53-94ea-ebd59c2601df
title: Paramètres de ProcAmp (Dxva2api. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0181d7491d948a4ec4219ada4241397b8a721b0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517579"
---
# <a name="procamp-settings"></a><span data-ttu-id="18eb3-103">Paramètres de ProcAmp</span><span class="sxs-lookup"><span data-stu-id="18eb3-103">ProcAmp Settings</span></span>

<span data-ttu-id="18eb3-104">Ces indicateurs définissent les paramètres de processeur vidéo (ProcAmp).</span><span class="sxs-lookup"><span data-stu-id="18eb3-104">These flags define video processor (ProcAmp) settings.</span></span>



| <span data-ttu-id="18eb3-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="18eb3-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                         | <span data-ttu-id="18eb3-106">Description</span><span class="sxs-lookup"><span data-stu-id="18eb3-106">Description</span></span>           |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------|
| <span id="DXVA2_ProcAmp_None"></span><span id="dxva2_procamp_none"></span><span id="DXVA2_PROCAMP_NONE"></span><dl> <span data-ttu-id="18eb3-107"><dt>**DXVA2 \_ ProcAmp \_ aucun**</dt> <dt>0x0000</dt></span><span class="sxs-lookup"><span data-stu-id="18eb3-107"><dt>**DXVA2\_ProcAmp\_None**</dt> <dt>0x0000</dt></span></span> </dl>                         | <span data-ttu-id="18eb3-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="18eb3-108">None</span></span><br/>       |
| <span id="DXVA2_ProcAmp_Brightness"></span><span id="dxva2_procamp_brightness"></span><span id="DXVA2_PROCAMP_BRIGHTNESS"></span><dl> <span data-ttu-id="18eb3-109"><dt>**DXVA2 \_ \_Luminosité ProcAmp**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="18eb3-109"><dt>**DXVA2\_ProcAmp\_Brightness**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="18eb3-110">Luminosité</span><span class="sxs-lookup"><span data-stu-id="18eb3-110">Brightness</span></span><br/> |
| <span id="DXVA2_ProcAmp_Contrast"></span><span id="dxva2_procamp_contrast"></span><span id="DXVA2_PROCAMP_CONTRAST"></span><dl> <span data-ttu-id="18eb3-111"><dt>**DXVA2 \_ \_Contraste ProcAmp**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="18eb3-111"><dt>**DXVA2\_ProcAmp\_Contrast**</dt> <dt>0x0002</dt></span></span> </dl>         | <span data-ttu-id="18eb3-112">Comparez</span><span class="sxs-lookup"><span data-stu-id="18eb3-112">Contrast</span></span><br/>   |
| <span id="DXVA2_ProcAmp_Hue"></span><span id="dxva2_procamp_hue"></span><span id="DXVA2_PROCAMP_HUE"></span><dl> <span data-ttu-id="18eb3-113"><dt>**DXVA2 \_ ProcAmp \_ teinte**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="18eb3-113"><dt>**DXVA2\_ProcAmp\_Hue**</dt> <dt>0x0004</dt></span></span> </dl>                             | <span data-ttu-id="18eb3-114">Teinte</span><span class="sxs-lookup"><span data-stu-id="18eb3-114">Hue</span></span><br/>        |
| <span id="DXVA2_ProcAmp_Saturation"></span><span id="dxva2_procamp_saturation"></span><span id="DXVA2_PROCAMP_SATURATION"></span><dl> <span data-ttu-id="18eb3-115"><dt>**DXVA2 \_ \_Saturation de ProcAmp**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="18eb3-115"><dt>**DXVA2\_ProcAmp\_Saturation**</dt> <dt>0x0008</dt></span></span> </dl> | <span data-ttu-id="18eb3-116">Saturation</span><span class="sxs-lookup"><span data-stu-id="18eb3-116">Saturation</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="18eb3-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18eb3-117">Requirements</span></span>



| <span data-ttu-id="18eb3-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18eb3-118">Requirement</span></span> | <span data-ttu-id="18eb3-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="18eb3-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="18eb3-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18eb3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="18eb3-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18eb3-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="18eb3-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18eb3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="18eb3-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18eb3-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="18eb3-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="18eb3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="18eb3-125"><dt>Dxva2api. h</dt></span><span class="sxs-lookup"><span data-stu-id="18eb3-125"><dt>Dxva2api.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18eb3-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18eb3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18eb3-127">Constantes Media Foundation</span><span class="sxs-lookup"><span data-stu-id="18eb3-127">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> </dl>

 

 




