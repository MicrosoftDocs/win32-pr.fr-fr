---
description: Spécifie la précision des coefficients DC, en bits. Cette propriété s’applique aux encodeurs vidéo MPEG.
ms.assetid: 2b4d11c1-767c-4466-8291-7959d841ae65
title: Propriété AVEncMPVIntraDCPrecision (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d4bdd3c08f49586eb2663829271ae4166d917e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846461"
---
# <a name="avencmpvintradcprecision-property"></a><span data-ttu-id="804cc-104">Propriété AVEncMPVIntraDCPrecision</span><span class="sxs-lookup"><span data-stu-id="804cc-104">AVEncMPVIntraDCPrecision property</span></span>

<span data-ttu-id="804cc-105">Spécifie la précision des coefficients DC, en bits.</span><span class="sxs-lookup"><span data-stu-id="804cc-105">Specifies the precision of the DC coefficients, in bits.</span></span> <span data-ttu-id="804cc-106">Cette propriété s’applique aux encodeurs vidéo MPEG.</span><span class="sxs-lookup"><span data-stu-id="804cc-106">This property applies to MPEG video encoders.</span></span>

<span data-ttu-id="804cc-107">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="804cc-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="804cc-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="804cc-108">Data type</span></span>

<span data-ttu-id="804cc-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="804cc-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="804cc-110">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="804cc-110">Property GUID</span></span>

<span data-ttu-id="804cc-111">**CODECAPI \_ AVEncMPVIntraDCPrecision**</span><span class="sxs-lookup"><span data-stu-id="804cc-111">**CODECAPI\_AVEncMPVIntraDCPrecision**</span></span>

## <a name="property-value"></a><span data-ttu-id="804cc-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="804cc-112">Property value</span></span>

<span data-ttu-id="804cc-113">Cette propriété a une plage de valeurs linéaire.</span><span class="sxs-lookup"><span data-stu-id="804cc-113">This property has a linear range of values.</span></span> <span data-ttu-id="804cc-114">Pour accéder à la plage prise en charge, appelez [**ICodecAPI :: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="804cc-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="804cc-115">Notes</span><span class="sxs-lookup"><span data-stu-id="804cc-115">Remarks</span></span>

<span data-ttu-id="804cc-116">La plage habituelle de cette propriété est comprise entre 8 et 11 bits.</span><span class="sxs-lookup"><span data-stu-id="804cc-116">The usual range for this property is 8 to 11 bits.</span></span> <span data-ttu-id="804cc-117">Si la valeur est égale à zéro, l’encodeur sélectionne la précision.</span><span class="sxs-lookup"><span data-stu-id="804cc-117">If the value is zero, the encoder selects the precision.</span></span>

## <a name="requirements"></a><span data-ttu-id="804cc-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="804cc-118">Requirements</span></span>



| <span data-ttu-id="804cc-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="804cc-119">Requirement</span></span> | <span data-ttu-id="804cc-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="804cc-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="804cc-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="804cc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="804cc-122">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="804cc-122">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="804cc-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="804cc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="804cc-124">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="804cc-124">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="804cc-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="804cc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="804cc-126"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="804cc-126"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="804cc-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="804cc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="804cc-128">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="804cc-128">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="804cc-129">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="804cc-129">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




