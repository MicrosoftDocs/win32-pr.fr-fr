---
description: Spécifie la complexité de l’algorithme d’encodage.
ms.assetid: 5dd34818-f282-4859-b423-97e9c4944aec
title: MFPKEY_ENCCOMPLEXITY, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51f50e7966a05affe8ae75869b670cf75f088b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864165"
---
# <a name="mfpkey_enccomplexity-property"></a><span data-ttu-id="4de0e-103">MFPKEY \_ propriété ENCCOMPLEXITY</span><span class="sxs-lookup"><span data-stu-id="4de0e-103">MFPKEY\_ENCCOMPLEXITY Property</span></span>

<span data-ttu-id="4de0e-104">Spécifie la complexité de l’algorithme d’encodage.</span><span class="sxs-lookup"><span data-stu-id="4de0e-104">Specifies the complexity of the encoding algorithm.</span></span> <span data-ttu-id="4de0e-105">La valeur est un entier compris entre 0 et 100, où 0 spécifie l’algorithme le moins complexe et 100 spécifie l’algorithme le plus complexe.</span><span class="sxs-lookup"><span data-stu-id="4de0e-105">The value is an integer between 0 and 100, where 0 specifies the least complex algorithm, and 100 specifies the most complex algorithm.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="4de0e-106">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="4de0e-106">Constant for IPropertyBag</span></span>

<span data-ttu-id="4de0e-107">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="4de0e-107">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="4de0e-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="4de0e-108">Data Type</span></span>

<span data-ttu-id="4de0e-109">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="4de0e-109">**VT\_UI4**</span></span>

## <a name="default-value"></a><span data-ttu-id="4de0e-110">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="4de0e-110">Default Value</span></span>

<span data-ttu-id="4de0e-111">100 pour Windows Media Audio 10 et Windows Media Audio 10 professionnel</span><span class="sxs-lookup"><span data-stu-id="4de0e-111">100 for Windows Media Audio 10 and Windows Media Audio 10 Professional</span></span>

<span data-ttu-id="4de0e-112">100 pour la version Windows Vista de Windows Media Audio 10 sans perte</span><span class="sxs-lookup"><span data-stu-id="4de0e-112">100 for the Windows Vista release of Windows Media Audio 10 Lossless</span></span>

<span data-ttu-id="4de0e-113">0 pour la version Windows 7 Windows Media Audio 10 sans perte</span><span class="sxs-lookup"><span data-stu-id="4de0e-113">0 for the Windows 7 release Windows Media Audio 10 Lossless</span></span>

## <a name="remarks"></a><span data-ttu-id="4de0e-114">Notes</span><span class="sxs-lookup"><span data-stu-id="4de0e-114">Remarks</span></span>

<span data-ttu-id="4de0e-115">Si la propriété [**MFPKEY \_ CONSTRAINECOMPLEXITY**](mfpkey-constrainenccomplexityproperty.md) a la valeur **Variant \_ true**, l’encodeur ajuste la complexité de son algorithme en fonction de la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="4de0e-115">If the [**MFPKEY\_CONSTRAINECOMPLEXITY**](mfpkey-constrainenccomplexityproperty.md) property has a value of **VARIANT\_TRUE**, the encoder adjusts the complexity of its algorithm according to the value of this property.</span></span>

<span data-ttu-id="4de0e-116">Pour l’encodeur Windows Media Audio 10 et l’encodeur Windows Media Audio 10 Professional, si la valeur de cette propriété est 100, l’encodeur place une demande élevée sur le processeur et produit une sortie de qualité supérieure.</span><span class="sxs-lookup"><span data-stu-id="4de0e-116">For the Windows Media Audio 10 encoder and the Windows Media Audio 10 Professional encoder, if the value of this property is 100, the encoder places a high demand on the CPU and produces the highest quality output.</span></span> <span data-ttu-id="4de0e-117">À mesure que la valeur de cette propriété diminue, la demande sur le processeur diminue, mais la qualité de la sortie diminue également.</span><span class="sxs-lookup"><span data-stu-id="4de0e-117">As the value of this property decreases, the demand on the CPU decreases, but the quality of the output also decreases.</span></span>

<span data-ttu-id="4de0e-118">Pour l’encodeur Windows Media Audio 10 sans perte, si la valeur de cette propriété est 0, l’encodeur place une faible demande sur le processeur.</span><span class="sxs-lookup"><span data-stu-id="4de0e-118">For the Windows Media Audio 10 Lossless encoder, if the value of this property is 0, the encoder places a low demand on the CPU.</span></span> <span data-ttu-id="4de0e-119">À mesure que la valeur de cette propriété augmente, la demande sur le processeur augmente, et la taille de la sortie de l’encodeur diminue légèrement.</span><span class="sxs-lookup"><span data-stu-id="4de0e-119">As the value of this property increases, the demand on the CPU increases, and the size of the encoder output decreases slightly.</span></span> <span data-ttu-id="4de0e-120">La sortie est sans perte, quelle que soit la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="4de0e-120">The output is lossless regardless of the value of this property.</span></span>

<span data-ttu-id="4de0e-121">Si vous laissez cette propriété à sa valeur par défaut **Variant \_ false**, l’encodeur utilise son algorithme par défaut.</span><span class="sxs-lookup"><span data-stu-id="4de0e-121">If you leave this property at its default value of **VARIANT\_FALSE**, the encoder uses its default algorithm.</span></span> <span data-ttu-id="4de0e-122">L’algorithme par défaut dépend de l’encodeur que vous utilisez et de la version de Windows en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="4de0e-122">The default algorithm depends on which encoder you are using and which version of Windows is running.</span></span> <span data-ttu-id="4de0e-123">Le tableau suivant décrit le comportement par défaut pour les différentes combinaisons.</span><span class="sxs-lookup"><span data-stu-id="4de0e-123">The following table describes the default behavior for the different combinations.</span></span>



| <span data-ttu-id="4de0e-124">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="4de0e-124">Operating system</span></span> | <span data-ttu-id="4de0e-125">Comportement par défaut</span><span class="sxs-lookup"><span data-stu-id="4de0e-125">Default behavior</span></span>                                                                                                                                                                                                |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4de0e-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4de0e-126">Windows Vista</span></span>    | <span data-ttu-id="4de0e-127">Les encodeurs Windows Media Audio 10, Windows Media Audio 10 Professional et Windows Media Audio 10 Lossless utilisent tous l’algorithme le plus complexe par défaut.</span><span class="sxs-lookup"><span data-stu-id="4de0e-127">The Windows Media Audio 10, Windows Media Audio 10 Professional, and Windows Media Audio 10 Lossless encoders all use the most complex algorithm by default.</span></span>                                                    |
| <span data-ttu-id="4de0e-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4de0e-128">Windows 7</span></span>        | <span data-ttu-id="4de0e-129">Les encodeurs Windows Media Audio 10 et Windows Media Audio 10 Professional utilisent l’algorithme le plus complexe par défaut.</span><span class="sxs-lookup"><span data-stu-id="4de0e-129">The Windows Media Audio 10 and Windows Media Audio 10 Professional encoders use the most complex algorithm by default.</span></span> <span data-ttu-id="4de0e-130">L’encodeur Windows Media Audio 10 Lossless utilise l’algorithme le moins complexe par défaut.</span><span class="sxs-lookup"><span data-stu-id="4de0e-130">The Windows Media Audio 10 Lossless encoder uses the least complex algorithm by default.</span></span> |



 

<span data-ttu-id="4de0e-131">Si la propriété [**MFPKEY \_ CONSTRAINECOMPLEXITY**](mfpkey-constrainenccomplexityproperty.md) a la valeur **Variant \_ false**, l’encodeur ignore cette propriété.</span><span class="sxs-lookup"><span data-stu-id="4de0e-131">If the [**MFPKEY\_CONSTRAINECOMPLEXITY**](mfpkey-constrainenccomplexityproperty.md) property has a value of **VARIANT\_FALSE**, the encoder ignores this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="4de0e-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4de0e-132">Requirements</span></span>



| <span data-ttu-id="4de0e-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4de0e-133">Requirement</span></span> | <span data-ttu-id="4de0e-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="4de0e-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4de0e-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4de0e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4de0e-136">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4de0e-136">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4de0e-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4de0e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4de0e-138">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4de0e-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4de0e-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="4de0e-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="4de0e-140"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4de0e-140"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4de0e-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4de0e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4de0e-142">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4de0e-142">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
