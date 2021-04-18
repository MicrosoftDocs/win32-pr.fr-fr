---
description: Spécifie le type de détection d’activité vocale effectué par le DSP de capture vocale.
ms.assetid: 59c8e348-8c08-4cf8-9c72-8d0f4fabc473
title: MFPKEY_WMAAECMA_FEATR_VAD, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e41b8ad80d909a0285b266587d02c09c08d794
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533784"
---
# <a name="mfpkey_wmaaecma_featr_vad-property"></a><span data-ttu-id="92874-103">\_Propriété VAD de MFPKEY WMAAECMA \_ Fonct \_</span><span class="sxs-lookup"><span data-stu-id="92874-103">MFPKEY\_WMAAECMA\_FEATR\_VAD Property</span></span>

<span data-ttu-id="92874-104">Spécifie le type de détection d’activité vocale effectué par le DSP de capture vocale.</span><span class="sxs-lookup"><span data-stu-id="92874-104">Specifies the type of voice activity detection that the Voice Capture DSP performs.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="92874-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="92874-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="92874-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="92874-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="92874-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="92874-107">Data Type</span></span>

<span data-ttu-id="92874-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="92874-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="92874-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="92874-109">Default Value</span></span>

<span data-ttu-id="92874-110">0</span><span class="sxs-lookup"><span data-stu-id="92874-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="92874-111">S'applique à</span><span class="sxs-lookup"><span data-stu-id="92874-111">Applies To</span></span>

-   [<span data-ttu-id="92874-112">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="92874-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="92874-113">Notes</span><span class="sxs-lookup"><span data-stu-id="92874-113">Remarks</span></span>

<span data-ttu-id="92874-114">La valeur de cette propriété est un membre de l’énumération du [ \_ \_ mode de l’AEC AEC](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_vad_mode) .</span><span class="sxs-lookup"><span data-stu-id="92874-114">The value of this property is a member of the [AEC\_VAD\_MODE](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_vad_mode) enumeration.</span></span> <span data-ttu-id="92874-115">La sortie de la détection d’activité vocale est un nombre compris entre 0 et 3, calculé pour chaque image audio.</span><span class="sxs-lookup"><span data-stu-id="92874-115">The output from voice activity detection is a number from 0 to 3, calculated for each audio frame.</span></span> <span data-ttu-id="92874-116">Le DSP encode le résultat dans le bit le plus bas des deux premiers échantillons audio de chaque trame audio.</span><span class="sxs-lookup"><span data-stu-id="92874-116">The DSP encodes the result in the lowest bit of the first two audio samples in each audio frame.</span></span> <span data-ttu-id="92874-117">La signification de la valeur dépend du mode spécifié.</span><span class="sxs-lookup"><span data-stu-id="92874-117">The meaning of the value depends on the specified mode.</span></span>

<span data-ttu-id="92874-118">Le code suivant montre comment extraire les résultats des données audio.</span><span class="sxs-lookup"><span data-stu-id="92874-118">The following code shows how to extract the results from the audio data.</span></span> <span data-ttu-id="92874-119">Dans cet exemple, *pOutput* est un pointeur vers le début d’une image audio dans les données de sortie.</span><span class="sxs-lookup"><span data-stu-id="92874-119">In this example, *pOutput* is a pointer to the start of an audio frame in the output data.</span></span>


```
int AecDecodeVAD(short *pOutput)
{
    int iVAD = (*pOutput) & 0x01;
    pOutput++;
    iVAD |= (*pOutput << 1) & 0x02;
    return iVAD;
}
```



<span data-ttu-id="92874-120">La valeur par défaut de cette propriété est 0 (désactivé).</span><span class="sxs-lookup"><span data-stu-id="92874-120">The default value of this property is 0 (disabled).</span></span> <span data-ttu-id="92874-121">Avant de définir cette propriété, vous devez affecter à la propriété [ \_ mode de \_ fonctionnalité \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) la \_ valeur variant true.</span><span class="sxs-lookup"><span data-stu-id="92874-121">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="92874-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92874-122">Requirements</span></span>



| <span data-ttu-id="92874-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="92874-123">Requirement</span></span> | <span data-ttu-id="92874-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="92874-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="92874-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92874-125">Minimum supported client</span></span><br/> | <span data-ttu-id="92874-126">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="92874-126">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="92874-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92874-127">Minimum supported server</span></span><br/> | <span data-ttu-id="92874-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="92874-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="92874-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="92874-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="92874-130"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="92874-130"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92874-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92874-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92874-132">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="92874-132">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
