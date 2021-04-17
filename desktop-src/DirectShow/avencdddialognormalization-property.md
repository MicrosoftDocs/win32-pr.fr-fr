---
description: Spécifie le niveau de normalisation de la boîte de dialogue, en décibels (dB), dans un flux audio Dolby Digital. Cette propriété s’applique aux encodeurs audio Dolby Digital.
ms.assetid: c347f8b2-5132-45d6-af66-43d3c409b0d7
title: Propriété AVEncDDDialogNormalization (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 586f241dc8d032767ecb2678c1ee5704dc20e0ef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482496"
---
# <a name="avencdddialognormalization-property"></a><span data-ttu-id="a3b60-104">Propriété AVEncDDDialogNormalization</span><span class="sxs-lookup"><span data-stu-id="a3b60-104">AVEncDDDialogNormalization property</span></span>

<span data-ttu-id="a3b60-105">Spécifie le niveau de normalisation de la boîte de dialogue, en décibels (dB), dans un flux audio Dolby Digital.</span><span class="sxs-lookup"><span data-stu-id="a3b60-105">Specifies the dialog normalization level, in decibels (dB), in a Dolby Digital audio stream.</span></span> <span data-ttu-id="a3b60-106">Cette propriété s’applique aux encodeurs audio Dolby Digital.</span><span class="sxs-lookup"><span data-stu-id="a3b60-106">This property applies to Dolby Digital audio encoders.</span></span>

<span data-ttu-id="a3b60-107">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a3b60-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="a3b60-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="a3b60-108">Data type</span></span>

<span data-ttu-id="a3b60-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="a3b60-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="a3b60-110">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="a3b60-110">Property GUID</span></span>

<span data-ttu-id="a3b60-111">**CODECAPI \_ AVEncDDDialogNormalization**</span><span class="sxs-lookup"><span data-stu-id="a3b60-111">**CODECAPI\_AVEncDDDialogNormalization**</span></span>

## <a name="property-value"></a><span data-ttu-id="a3b60-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a3b60-112">Property value</span></span>

<span data-ttu-id="a3b60-113">Cette propriété a une plage de valeurs linéaire.</span><span class="sxs-lookup"><span data-stu-id="a3b60-113">This property has a linear range of values.</span></span> <span data-ttu-id="a3b60-114">Pour accéder à la plage prise en charge, appelez [**ICodecAPI :: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="a3b60-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="requirements"></a><span data-ttu-id="a3b60-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a3b60-115">Requirements</span></span>



| <span data-ttu-id="a3b60-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a3b60-116">Requirement</span></span> | <span data-ttu-id="a3b60-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3b60-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a3b60-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3b60-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a3b60-119">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="a3b60-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="a3b60-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3b60-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a3b60-121">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="a3b60-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="a3b60-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="a3b60-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3b60-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3b60-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3b60-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3b60-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3b60-125">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="a3b60-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="a3b60-126">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="a3b60-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




