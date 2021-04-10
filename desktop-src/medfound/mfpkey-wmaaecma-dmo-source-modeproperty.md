---
description: Spécifie si le DSP de capture vocale utilise le mode source ou le mode filtre.
ms.assetid: d1d3beba-678c-48fd-ad12-45e0418e1236
title: MFPKEY_WMAAECMA_DMO_SOURCE_MODE, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5749ff1f142603cc45df475caae7bc71182bde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201888"
---
# <a name="mfpkey_wmaaecma_dmo_source_mode-property"></a><span data-ttu-id="01475-103">\_Propriété du \_ \_ mode source \_ MFPKEY WMAAECMA DMO</span><span class="sxs-lookup"><span data-stu-id="01475-103">MFPKEY\_WMAAECMA\_DMO\_SOURCE\_MODE Property</span></span>

<span data-ttu-id="01475-104">Spécifie si le DSP de capture vocale utilise le mode source ou le mode filtre.</span><span class="sxs-lookup"><span data-stu-id="01475-104">Specifies whether the Voice Capture DSP uses source mode or filter mode.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="01475-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="01475-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="01475-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="01475-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="01475-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="01475-107">Data Type</span></span>

<span data-ttu-id="01475-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="01475-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="01475-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="01475-109">Default Value</span></span>

<span data-ttu-id="01475-110">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="01475-110">VARIANT\_TRUE</span></span>

## <a name="applies-to"></a><span data-ttu-id="01475-111">S'applique à</span><span class="sxs-lookup"><span data-stu-id="01475-111">Applies To</span></span>

-   [<span data-ttu-id="01475-112">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="01475-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="01475-113">Notes</span><span class="sxs-lookup"><span data-stu-id="01475-113">Remarks</span></span>

<span data-ttu-id="01475-114">En mode Source, l’application n’a pas besoin d’envoyer des données d’entrée au DSP, car le DSP extrait automatiquement les données des périphériques audio.</span><span class="sxs-lookup"><span data-stu-id="01475-114">In source mode, the application does not need to send input data to the DSP, because the DSP automatically pulls data from the audio devices.</span></span> <span data-ttu-id="01475-115">En mode filtre, l’application doit envoyer les données d’entrée au DSP.</span><span class="sxs-lookup"><span data-stu-id="01475-115">In filter mode, the application must send the input data to the DSP.</span></span>

<span data-ttu-id="01475-116">Cette propriété peut avoir les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="01475-116">This property can have the following values.</span></span>



| <span data-ttu-id="01475-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="01475-117">Value</span></span>          | <span data-ttu-id="01475-118">Description</span><span class="sxs-lookup"><span data-stu-id="01475-118">Description</span></span>  |
|----------------|--------------|
| <span data-ttu-id="01475-119">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="01475-119">VARIANT\_FALSE</span></span> | <span data-ttu-id="01475-120">Mode filtre.</span><span class="sxs-lookup"><span data-stu-id="01475-120">Filter mode.</span></span> |
| <span data-ttu-id="01475-121">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="01475-121">VARIANT\_TRUE</span></span>  | <span data-ttu-id="01475-122">Mode Source.</span><span class="sxs-lookup"><span data-stu-id="01475-122">Source mode.</span></span> |



 

> [!Note]  
> <span data-ttu-id="01475-123">Lorsque DMO est en mode Source, vous devez uniquement appeler [**IMediaObject :: SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) pour définir le format de flux de sortie et n’appelez pas [**IMediaObject :: SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) pour définir des formats de flux d’entrée.</span><span class="sxs-lookup"><span data-stu-id="01475-123">When the DMO is in source mode, you should only call [**IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) to set output stream format, and do not call [**IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) to set input stream formats.</span></span> <span data-ttu-id="01475-124">Sinon, l’initialisation DMO échoue.</span><span class="sxs-lookup"><span data-stu-id="01475-124">Otherwise DMO initialization will fail.</span></span>

 

<span data-ttu-id="01475-125">Si la valeur de cette propriété est \_ true, le fournisseur de base de données n’a aucune entrée.</span><span class="sxs-lookup"><span data-stu-id="01475-125">If the value of this property is VARIANT\_TRUE, the DSP has zero inputs.</span></span> <span data-ttu-id="01475-126">Si la valeur est \_ false, le DSP a une ou deux entrées, en fonction de la valeur de la propriété [MFPKEY \_ WMAAECMA \_ System \_ mode](mfpkey-wmaaecma-system-modeproperty.md) , comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="01475-126">If the value is VARIANT\_FALSE, the DSP has one or two inputs, depending on the value of the [MFPKEY\_WMAAECMA\_SYSTEM\_MODE](mfpkey-wmaaecma-system-modeproperty.md) property, as shown in the following table.</span></span>



| <span data-ttu-id="01475-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="01475-127">Value</span></span>                     | <span data-ttu-id="01475-128">Nombre d'entrées</span><span class="sxs-lookup"><span data-stu-id="01475-128">Number of inputs</span></span> |
|---------------------------|------------------|
| <span data-ttu-id="01475-129">\_tableau OPTIBEAM \_ et \_ AEC</span><span class="sxs-lookup"><span data-stu-id="01475-129">OPTIBEAM\_ARRAY\_AND\_AEC</span></span> | <span data-ttu-id="01475-130">2</span><span class="sxs-lookup"><span data-stu-id="01475-130">2</span></span>                |
| <span data-ttu-id="01475-131">\_tableau OPTIBEAM \_ uniquement</span><span class="sxs-lookup"><span data-stu-id="01475-131">OPTIBEAM\_ARRAY\_ONLY</span></span>     | <span data-ttu-id="01475-132">1</span><span class="sxs-lookup"><span data-stu-id="01475-132">1</span></span>                |
| <span data-ttu-id="01475-133">\_AEC à canal unique \_</span><span class="sxs-lookup"><span data-stu-id="01475-133">SINGLE\_CHANNEL\_AEC</span></span>      | <span data-ttu-id="01475-134">2</span><span class="sxs-lookup"><span data-stu-id="01475-134">2</span></span>                |
| <span data-ttu-id="01475-135">\_NSAGC à canal unique \_</span><span class="sxs-lookup"><span data-stu-id="01475-135">SINGLE\_CHANNEL\_NSAGC</span></span>    | <span data-ttu-id="01475-136">1</span><span class="sxs-lookup"><span data-stu-id="01475-136">1</span></span>                |



 

> [!Note]  
> <span data-ttu-id="01475-137">Seuls les modes avec une seule entrée fonctionnent avec le filtre de wrapper DMO à partir de l’API DirectShow 9,0.</span><span class="sxs-lookup"><span data-stu-id="01475-137">Only modes with a single input will work with the wrapper filter DMO from the DirectShow 9.0 API.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="01475-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01475-138">Requirements</span></span>



| <span data-ttu-id="01475-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01475-139">Requirement</span></span> | <span data-ttu-id="01475-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="01475-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01475-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01475-141">Minimum supported client</span></span><br/> | <span data-ttu-id="01475-142">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="01475-142">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="01475-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01475-143">Minimum supported server</span></span><br/> | <span data-ttu-id="01475-144">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="01475-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="01475-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="01475-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="01475-146"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="01475-146"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01475-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01475-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01475-148">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="01475-148">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="01475-149">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="01475-149">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
