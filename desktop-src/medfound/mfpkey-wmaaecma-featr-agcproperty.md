---
description: Spécifie si le DSP de capture vocale effectue un contrôle de gain automatique.
ms.assetid: 85ac8de0-ac36-4b34-a93d-0ac792a677b2
title: MFPKEY_WMAAECMA_FEATR_AGC, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f42c7abd854b8fe18b5cfd4fe23ededb28faa6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534401"
---
# <a name="mfpkey_wmaaecma_featr_agc-property"></a><span data-ttu-id="3190e-103">MFPKEY \_ WMAAECMA \_ Fonct, \_ propriété AGC</span><span class="sxs-lookup"><span data-stu-id="3190e-103">MFPKEY\_WMAAECMA\_FEATR\_AGC Property</span></span>

<span data-ttu-id="3190e-104">Spécifie si le DSP de capture vocale effectue un contrôle de gain automatique.</span><span class="sxs-lookup"><span data-stu-id="3190e-104">Specifies whether the Voice Capture DSP performs automatic gain control.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="3190e-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="3190e-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="3190e-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="3190e-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="3190e-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="3190e-107">Data Type</span></span>

<span data-ttu-id="3190e-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="3190e-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="3190e-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="3190e-109">Default Value</span></span>

<span data-ttu-id="3190e-110">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="3190e-110">VARIANT\_FALSE</span></span>

## <a name="applies-to"></a><span data-ttu-id="3190e-111">S'applique à</span><span class="sxs-lookup"><span data-stu-id="3190e-111">Applies To</span></span>

-   [<span data-ttu-id="3190e-112">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="3190e-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="3190e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="3190e-113">Remarks</span></span>

<span data-ttu-id="3190e-114">Le contrôle de gain automatique est un composant DSP (Digital Signal Processing) qui ajuste le gain afin que le niveau de sortie du signal reste dans la même plage approximative.</span><span class="sxs-lookup"><span data-stu-id="3190e-114">Automatic gain control is a digital signal processing (DSP) component that adjusts the gain so that the output level of the signal remains within the same approximate range.</span></span>

<span data-ttu-id="3190e-115">Cette propriété peut avoir les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="3190e-115">This property can have the following values.</span></span>



| <span data-ttu-id="3190e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="3190e-116">Value</span></span>          | <span data-ttu-id="3190e-117">Description</span><span class="sxs-lookup"><span data-stu-id="3190e-117">Description</span></span>                     |
|----------------|---------------------------------|
| <span data-ttu-id="3190e-118">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="3190e-118">VARIANT\_FALSE</span></span> | <span data-ttu-id="3190e-119">Désactivez le contrôle de gain automatique.</span><span class="sxs-lookup"><span data-stu-id="3190e-119">Disable automatic gain control.</span></span> |
| <span data-ttu-id="3190e-120">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="3190e-120">VARIANT\_TRUE</span></span>  | <span data-ttu-id="3190e-121">Activez le contrôle du gain automatique.</span><span class="sxs-lookup"><span data-stu-id="3190e-121">Enable automatic gain control.</span></span>  |



 

<span data-ttu-id="3190e-122">La valeur par défaut de cette propriété est \_ false false (désactivé).</span><span class="sxs-lookup"><span data-stu-id="3190e-122">The default value of this property is VARIANT\_FALSE (disabled).</span></span> <span data-ttu-id="3190e-123">Avant de définir cette propriété, vous devez affecter à la propriété [ \_ mode de \_ fonctionnalité \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) la \_ valeur variant true.</span><span class="sxs-lookup"><span data-stu-id="3190e-123">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="3190e-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3190e-124">Requirements</span></span>



| <span data-ttu-id="3190e-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3190e-125">Requirement</span></span> | <span data-ttu-id="3190e-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="3190e-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3190e-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3190e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3190e-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3190e-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3190e-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3190e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3190e-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3190e-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3190e-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="3190e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3190e-132"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3190e-132"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3190e-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3190e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3190e-134">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3190e-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="3190e-135">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="3190e-135">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
