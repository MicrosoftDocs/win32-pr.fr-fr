---
description: Spécifie la durée d’écho que l’algorithme d’annulation de l’écho acoustique (AEC) peut gérer, en millisecondes.
ms.assetid: d451b90f-7ef7-4f66-be83-aca93e3ad894
title: MFPKEY_WMAAECMA_FEATR_ECHO_LENGTH, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d66f7dcc4764447495e0f3ae55d2d038c2a8d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518589"
---
# <a name="mfpkey_wmaaecma_featr_echo_length-property"></a><span data-ttu-id="47c5d-103">MFPKEY \_ WMAAECMA \_ Fonct \_ echo \_ Length, propriété</span><span class="sxs-lookup"><span data-stu-id="47c5d-103">MFPKEY\_WMAAECMA\_FEATR\_ECHO\_LENGTH Property</span></span>

<span data-ttu-id="47c5d-104">Spécifie la durée d’écho que l’algorithme d’annulation de l’écho acoustique (AEC) peut gérer, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="47c5d-104">Specifies the duration of echo that the acoustic echo cancellation (AEC) algorithm can handle, in milliseconds.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="47c5d-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="47c5d-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="47c5d-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="47c5d-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="47c5d-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="47c5d-107">Data Type</span></span>

<span data-ttu-id="47c5d-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="47c5d-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="47c5d-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="47c5d-109">Default Value</span></span>

<span data-ttu-id="47c5d-110">256</span><span class="sxs-lookup"><span data-stu-id="47c5d-110">256</span></span>

## <a name="applies-to"></a><span data-ttu-id="47c5d-111">S'applique à</span><span class="sxs-lookup"><span data-stu-id="47c5d-111">Applies To</span></span>

-   [<span data-ttu-id="47c5d-112">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="47c5d-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="47c5d-113">Notes</span><span class="sxs-lookup"><span data-stu-id="47c5d-113">Remarks</span></span>

<span data-ttu-id="47c5d-114">L’algorithme AEC utilise un filtre adaptatif dont la longueur est déterminée par la durée de l’écho.</span><span class="sxs-lookup"><span data-stu-id="47c5d-114">The AEC algorithm uses an adaptive filter whose length is determined by the duration of the echo.</span></span> <span data-ttu-id="47c5d-115">Il est recommandé que les applications utilisent l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="47c5d-115">It is recommended that applications use one of the following values:</span></span>

-   <span data-ttu-id="47c5d-116">128</span><span class="sxs-lookup"><span data-stu-id="47c5d-116">128</span></span>
-   <span data-ttu-id="47c5d-117">256</span><span class="sxs-lookup"><span data-stu-id="47c5d-117">256</span></span>
-   <span data-ttu-id="47c5d-118">512</span><span class="sxs-lookup"><span data-stu-id="47c5d-118">512</span></span>
-   <span data-ttu-id="47c5d-119">1 024</span><span class="sxs-lookup"><span data-stu-id="47c5d-119">1024</span></span>

<span data-ttu-id="47c5d-120">La valeur par défaut est 256 millisecondes, ce qui est suffisant pour la plupart des environnements Office et personnels.</span><span class="sxs-lookup"><span data-stu-id="47c5d-120">The default value is 256 milliseconds, which is sufficient for most office and home environments.</span></span> <span data-ttu-id="47c5d-121">Avant de définir cette propriété, vous devez affecter à la propriété [ \_ mode de \_ fonctionnalité \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) la \_ valeur variant true.</span><span class="sxs-lookup"><span data-stu-id="47c5d-121">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="47c5d-122">Le DSP utilise cette propriété uniquement lorsque le traitement AEC est activé.</span><span class="sxs-lookup"><span data-stu-id="47c5d-122">The DSP uses this property only when AEC processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="47c5d-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="47c5d-123">Requirements</span></span>



| <span data-ttu-id="47c5d-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="47c5d-124">Requirement</span></span> | <span data-ttu-id="47c5d-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="47c5d-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="47c5d-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47c5d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="47c5d-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="47c5d-127">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="47c5d-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47c5d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="47c5d-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="47c5d-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="47c5d-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="47c5d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="47c5d-131"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="47c5d-131"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47c5d-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47c5d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47c5d-133">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="47c5d-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="47c5d-134">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="47c5d-134">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
