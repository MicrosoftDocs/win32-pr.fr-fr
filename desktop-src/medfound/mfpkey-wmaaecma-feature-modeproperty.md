---
description: Permet à l’application de remplacer les paramètres par défaut sur les différentes propriétés du DSP de capture vocale.
ms.assetid: 1c11e817-36bd-4a5d-9c2b-6a91e86f623f
title: MFPKEY_WMAAECMA_FEATURE_MODE, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9a47ef86a2acf83131800e9cb55b86de2cd3d98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753957"
---
# <a name="mfpkey_wmaaecma_feature_mode-property"></a><span data-ttu-id="997f2-103">MFPKEY \_ \_ propriété mode de fonctionnalité WMAAECMA \_</span><span class="sxs-lookup"><span data-stu-id="997f2-103">MFPKEY\_WMAAECMA\_FEATURE\_MODE Property</span></span>

<span data-ttu-id="997f2-104">Permet à l’application de remplacer les paramètres par défaut sur les différentes propriétés du DSP de capture vocale.</span><span class="sxs-lookup"><span data-stu-id="997f2-104">Enables the application to override the default settings on various properties of the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="997f2-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="997f2-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="997f2-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="997f2-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="997f2-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="997f2-107">Data Type</span></span>

<span data-ttu-id="997f2-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="997f2-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="997f2-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="997f2-109">Default Value</span></span>

<span data-ttu-id="997f2-110">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="997f2-110">VARIANT\_FALSE</span></span>

## <a name="applies-to"></a><span data-ttu-id="997f2-111">S'applique à</span><span class="sxs-lookup"><span data-stu-id="997f2-111">Applies To</span></span>

-   [<span data-ttu-id="997f2-112">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="997f2-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="997f2-113">Notes</span><span class="sxs-lookup"><span data-stu-id="997f2-113">Remarks</span></span>

<span data-ttu-id="997f2-114">Si cette propriété a la \_ valeur true, l’application peut définir les propriétés suivantes sur le DSP :</span><span class="sxs-lookup"><span data-stu-id="997f2-114">If this property is VARIANT\_TRUE, the application can set the following properties on the DSP:</span></span>

-   [<span data-ttu-id="997f2-115">MFPKEY \_ WMAAECMA \_ fonceur \_ AES</span><span class="sxs-lookup"><span data-stu-id="997f2-115">MFPKEY\_WMAAECMA\_FEATR\_AES</span></span>](mfpkey-wmaaecma-featr-aesproperty.md)
-   [<span data-ttu-id="997f2-116">MFPKEY \_ WMAAECMA \_ Fonct, \_ AGC</span><span class="sxs-lookup"><span data-stu-id="997f2-116">MFPKEY\_WMAAECMA\_FEATR\_AGC</span></span>](mfpkey-wmaaecma-featr-agcproperty.md)
-   [<span data-ttu-id="997f2-117">\_clip du \_ \_ Centre \_ d’MFPKEY WMAAECMA</span><span class="sxs-lookup"><span data-stu-id="997f2-117">MFPKEY\_WMAAECMA\_FEATR\_CENTER\_CLIP</span></span>](mfpkey-wmaaecma-featr-center-clipproperty.md)
-   [<span data-ttu-id="997f2-118">longueur de l' \_ \_ écho du Feature WMAAECMA MFPKEY \_ \_</span><span class="sxs-lookup"><span data-stu-id="997f2-118">MFPKEY\_WMAAECMA\_FEATR\_ECHO\_LENGTH</span></span>](mfpkey-wmaaecma-featr-echo-lengthproperty.md)
-   [<span data-ttu-id="997f2-119">\_taille du \_ \_ frame \_ de MFPKEY WMAAECMA</span><span class="sxs-lookup"><span data-stu-id="997f2-119">MFPKEY\_WMAAECMA\_FEATR\_FRAME\_SIZE</span></span>](mfpkey-wmaaecma-featr-frame-sizeproperty.md)
-   [<span data-ttu-id="997f2-120">\_ \_ \_ mode MICARR MFPKEY WMAAECMA \_</span><span class="sxs-lookup"><span data-stu-id="997f2-120">MFPKEY\_WMAAECMA\_FEATR\_MICARR\_MODE</span></span>](mfpkey-wmaaecma-featr-micarr-modeproperty.md)
-   [<span data-ttu-id="997f2-121">MFPKEY \_ WMAAECMA \_ Feature \_ MICARR \_ préproc</span><span class="sxs-lookup"><span data-stu-id="997f2-121">MFPKEY\_WMAAECMA\_FEATR\_MICARR\_PREPROC</span></span>](mfpkey-wmaaecma-featr-micarr-preprocproperty.md)
-   [<span data-ttu-id="997f2-122">\_remplissage du \_ \_ bruit \_ du MFPKEY WMAAECMA</span><span class="sxs-lookup"><span data-stu-id="997f2-122">MFPKEY\_WMAAECMA\_FEATR\_NOISE\_FILL</span></span>](mfpkey-wmaaecma-featr-noise-fillproperty.md)
-   [<span data-ttu-id="997f2-123">MFPKEY \_ WMAAECMA \_ Feature \_</span><span class="sxs-lookup"><span data-stu-id="997f2-123">MFPKEY\_WMAAECMA\_FEATR\_NS</span></span>](mfpkey-wmaaecma-featr-nsproperty.md)
-   [<span data-ttu-id="997f2-124">\_VAD MFPKEY WMAAECMA \_ Fonct \_</span><span class="sxs-lookup"><span data-stu-id="997f2-124">MFPKEY\_WMAAECMA\_FEATR\_VAD</span></span>](mfpkey-wmaaecma-featr-vadproperty.md)

<span data-ttu-id="997f2-125">Si cette propriété a \_ la valeur false, le DSP ignore ces propriétés et utilise ses paramètres par défaut.</span><span class="sxs-lookup"><span data-stu-id="997f2-125">If this property is VARIANT\_FALSE, the DSP ignores these properties and uses its default settings.</span></span> <span data-ttu-id="997f2-126">La valeur par défaut de cette propriété est \_ false false.</span><span class="sxs-lookup"><span data-stu-id="997f2-126">The default value of this property is VARIANT\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="997f2-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="997f2-127">Requirements</span></span>



| <span data-ttu-id="997f2-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="997f2-128">Requirement</span></span> | <span data-ttu-id="997f2-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="997f2-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="997f2-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="997f2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="997f2-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="997f2-131">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="997f2-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="997f2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="997f2-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="997f2-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="997f2-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="997f2-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="997f2-135"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="997f2-135"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="997f2-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="997f2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="997f2-137">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="997f2-137">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="997f2-138">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="997f2-138">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
