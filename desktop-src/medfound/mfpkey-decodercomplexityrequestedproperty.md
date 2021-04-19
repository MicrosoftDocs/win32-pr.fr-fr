---
description: Spécifie le modèle de conformité de périphérique que vous souhaitez utiliser pour l’encodage vidéo.
ms.assetid: cd2c068a-dbbc-42c5-bc92-bbb73f0259d1
title: MFPKEY_DECODERCOMPLEXITYREQUESTED, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e017361d7e8267d33ecb2cfdbce2a6e79758fac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517788"
---
# <a name="mfpkey_decodercomplexityrequested-property"></a><span data-ttu-id="c7a6c-103">MFPKEY \_ propriété DECODERCOMPLEXITYREQUESTED</span><span class="sxs-lookup"><span data-stu-id="c7a6c-103">MFPKEY\_DECODERCOMPLEXITYREQUESTED Property</span></span>

<span data-ttu-id="c7a6c-104">Spécifie le modèle de conformité de périphérique que vous souhaitez utiliser pour l’encodage vidéo.</span><span class="sxs-lookup"><span data-stu-id="c7a6c-104">Specifies the device conformance template that you want to use for video encoding.</span></span>

## <a name="data-type"></a><span data-ttu-id="c7a6c-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="c7a6c-105">Data Type</span></span>

<span data-ttu-id="c7a6c-106">VT \_</span><span class="sxs-lookup"><span data-stu-id="c7a6c-106">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="c7a6c-107">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="c7a6c-107">Default Value</span></span>

<span data-ttu-id="c7a6c-108">1</span><span class="sxs-lookup"><span data-stu-id="c7a6c-108">1</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="c7a6c-109">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="c7a6c-109">Constant for IPropertyBag</span></span>

<span data-ttu-id="c7a6c-110">\_wszWMVCDecoderComplexityRequested g</span><span class="sxs-lookup"><span data-stu-id="c7a6c-110">g\_wszWMVCDecoderComplexityRequested</span></span>

## <a name="data-type-for-ipropertybag"></a><span data-ttu-id="c7a6c-111">Type de données pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="c7a6c-111">Data Type for IPropertyBag</span></span>

<span data-ttu-id="c7a6c-112">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="c7a6c-112">VT\_BSTR</span></span>

## <a name="default-value-for-ipropertybag"></a><span data-ttu-id="c7a6c-113">Valeur par défaut pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="c7a6c-113">Default Value for IPropertyBag</span></span>

<span data-ttu-id="c7a6c-114">CANAL</span><span class="sxs-lookup"><span data-stu-id="c7a6c-114">"MP"</span></span>

## <a name="remarks"></a><span data-ttu-id="c7a6c-115">Notes</span><span class="sxs-lookup"><span data-stu-id="c7a6c-115">Remarks</span></span>

<span data-ttu-id="c7a6c-116">Le codec tentera d’encoder le contenu à l’aide du modèle de conformité de périphérique spécifié par cette valeur.</span><span class="sxs-lookup"><span data-stu-id="c7a6c-116">The codec will attempt to encode the content using the device conformance template specified by this value.</span></span> <span data-ttu-id="c7a6c-117">Le modèle réel auquel le contenu encodé est conforme peut être récupéré à partir de la propriété [MFPKEY \_ DECODERCOMPLEXITYPROFILE](mfpkey-decodercomplexityprofileproperty.md) après l’encodage.</span><span class="sxs-lookup"><span data-stu-id="c7a6c-117">The actual template to which the encoded content conforms can be retrieved from the [MFPKEY\_DECODERCOMPLEXITYPROFILE](mfpkey-decodercomplexityprofileproperty.md) property after encoding.</span></span>

<span data-ttu-id="c7a6c-118">Cette propriété doit avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c7a6c-118">This property must be one of the following values.</span></span>



| <span data-ttu-id="c7a6c-119">Valeur pour IPropertyStore</span><span class="sxs-lookup"><span data-stu-id="c7a6c-119">Value for IPropertyStore</span></span> | <span data-ttu-id="c7a6c-120">Valeur pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="c7a6c-120">Value for IPropertyBag</span></span> | <span data-ttu-id="c7a6c-121">Description</span><span class="sxs-lookup"><span data-stu-id="c7a6c-121">Description</span></span>         |
|--------------------------|------------------------|---------------------|
| <span data-ttu-id="c7a6c-122">0</span><span class="sxs-lookup"><span data-stu-id="c7a6c-122">0</span></span>                        | <span data-ttu-id="c7a6c-123">SR</span><span class="sxs-lookup"><span data-stu-id="c7a6c-123">"SP"</span></span>                   | <span data-ttu-id="c7a6c-124">Profil simple</span><span class="sxs-lookup"><span data-stu-id="c7a6c-124">simple profile</span></span>      |
| <span data-ttu-id="c7a6c-125">1</span><span class="sxs-lookup"><span data-stu-id="c7a6c-125">1</span></span>                        | <span data-ttu-id="c7a6c-126">CANAL</span><span class="sxs-lookup"><span data-stu-id="c7a6c-126">"MP"</span></span>                   | <span data-ttu-id="c7a6c-127">Profil principal</span><span class="sxs-lookup"><span data-stu-id="c7a6c-127">main profile</span></span>        |
| <span data-ttu-id="c7a6c-128">2</span><span class="sxs-lookup"><span data-stu-id="c7a6c-128">2</span></span>                        | <span data-ttu-id="c7a6c-129">CP</span><span class="sxs-lookup"><span data-stu-id="c7a6c-129">"CP"</span></span>                   | <span data-ttu-id="c7a6c-130">n’est plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7a6c-130">no longer supported</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="c7a6c-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7a6c-131">Requirements</span></span>



| <span data-ttu-id="c7a6c-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7a6c-132">Requirement</span></span> | <span data-ttu-id="c7a6c-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7a6c-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7a6c-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7a6c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c7a6c-135">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c7a6c-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c7a6c-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7a6c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c7a6c-137">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c7a6c-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c7a6c-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="c7a6c-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7a6c-139"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7a6c-139"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7a6c-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7a6c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7a6c-141">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c7a6c-141">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




