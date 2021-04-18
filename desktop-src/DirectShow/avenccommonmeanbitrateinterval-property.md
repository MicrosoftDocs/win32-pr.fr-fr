---
description: Spécifie l’intervalle de temps pendant lequel la vitesse de transmission moyenne s’applique. Cette propriété est utilisée conjointement avec la propriété AVEncCommonMeanBitRate.
ms.assetid: 3cf26f46-e8ac-448a-a031-800915cad1ef
title: Propriété AVEncCommonMeanBitRateInterval (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ffee31b0ac54d195051f1cc973d2fdcb058f202
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482521"
---
# <a name="avenccommonmeanbitrateinterval-property"></a><span data-ttu-id="c29f2-104">Propriété AVEncCommonMeanBitRateInterval</span><span class="sxs-lookup"><span data-stu-id="c29f2-104">AVEncCommonMeanBitRateInterval property</span></span>

<span data-ttu-id="c29f2-105">Spécifie l’intervalle de temps pendant lequel la vitesse de transmission moyenne s’applique.</span><span class="sxs-lookup"><span data-stu-id="c29f2-105">Specifies the time interval over which the average bit rate applies.</span></span> <span data-ttu-id="c29f2-106">Cette propriété est utilisée conjointement avec la propriété [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md) .</span><span class="sxs-lookup"><span data-stu-id="c29f2-106">This property is used in conjunction with the [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md) property.</span></span>

<span data-ttu-id="c29f2-107">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="c29f2-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="c29f2-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="c29f2-108">Data type</span></span>

<span data-ttu-id="c29f2-109">**UINT64** (**VT \_ UI8**)</span><span class="sxs-lookup"><span data-stu-id="c29f2-109">**UINT64** (**VT\_UI8**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="c29f2-110">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="c29f2-110">Property GUID</span></span>

<span data-ttu-id="c29f2-111">**CODECAPI \_ AVEncCommonMeanBitRateInterval**</span><span class="sxs-lookup"><span data-stu-id="c29f2-111">**CODECAPI\_AVEncCommonMeanBitRateInterval**</span></span>

## <a name="property-value"></a><span data-ttu-id="c29f2-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c29f2-112">Property value</span></span>

<span data-ttu-id="c29f2-113">Cette propriété a une plage de valeurs linéaire.</span><span class="sxs-lookup"><span data-stu-id="c29f2-113">This property has a linear range of values.</span></span> <span data-ttu-id="c29f2-114">Pour accéder à la plage prise en charge, appelez [**ICodecAPI :: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="c29f2-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="c29f2-115">Notes</span><span class="sxs-lookup"><span data-stu-id="c29f2-115">Remarks</span></span>

<span data-ttu-id="c29f2-116">Pour l’encodage VBR (variable bit rate) à deux passes, la valeur zéro indique que l’intervalle de temps correspond à la durée totale du contenu.</span><span class="sxs-lookup"><span data-stu-id="c29f2-116">For two-pass variable bit rate (VBR) encoding, the value zero indicates that the time interval is the entire duration of the content.</span></span> <span data-ttu-id="c29f2-117">Pour l’encodage CBR (Single-passe constant bit rate), la valeur zéro indique que l’encodeur sélectionne l’intervalle (en général 0,5 secondes).</span><span class="sxs-lookup"><span data-stu-id="c29f2-117">For single-pass constant bit rate (CBR) encoding, the value zero indicates that the encoder selects the interval (typically 0.5 seconds).</span></span>

## <a name="requirements"></a><span data-ttu-id="c29f2-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c29f2-118">Requirements</span></span>



| <span data-ttu-id="c29f2-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c29f2-119">Requirement</span></span> | <span data-ttu-id="c29f2-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c29f2-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c29f2-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c29f2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c29f2-122">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="c29f2-122">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="c29f2-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c29f2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c29f2-124">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="c29f2-124">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="c29f2-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="c29f2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c29f2-126"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c29f2-126"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c29f2-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c29f2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c29f2-128">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="c29f2-128">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="c29f2-129">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="c29f2-129">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




