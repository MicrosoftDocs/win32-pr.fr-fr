---
description: Spécifie si le DSP de capture vocale effectue un remplissage de bruit.
ms.assetid: 8bb64686-8f02-4e0d-a664-aeee1744fc8e
title: MFPKEY_WMAAECMA_FEATR_NOISE_FILL, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea0c0af2b47767a7798d9b583ac55ad5112ddf1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527785"
---
# <a name="mfpkey_wmaaecma_featr_noise_fill-property"></a><span data-ttu-id="b59f5-103">\_Propriété de \_ remplissage du \_ bruit \_ de MFPKEY WMAAECMA</span><span class="sxs-lookup"><span data-stu-id="b59f5-103">MFPKEY\_WMAAECMA\_FEATR\_NOISE\_FILL Property</span></span>

<span data-ttu-id="b59f5-104">Spécifie si le DSP de capture vocale effectue un remplissage de bruit.</span><span class="sxs-lookup"><span data-stu-id="b59f5-104">Specifies whether the Voice Capture DSP performs noise filling.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="b59f5-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="b59f5-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="b59f5-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="b59f5-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="b59f5-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="b59f5-107">Data Type</span></span>

<span data-ttu-id="b59f5-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="b59f5-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="b59f5-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="b59f5-109">Default Value</span></span>

<span data-ttu-id="b59f5-110">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="b59f5-110">VARIANT\_TRUE</span></span>

## <a name="applies-to"></a><span data-ttu-id="b59f5-111">S'applique à</span><span class="sxs-lookup"><span data-stu-id="b59f5-111">Applies To</span></span>

-   [<span data-ttu-id="b59f5-112">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="b59f5-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="b59f5-113">Notes</span><span class="sxs-lookup"><span data-stu-id="b59f5-113">Remarks</span></span>

<span data-ttu-id="b59f5-114">Le remplissage du bruit ajoute une petite quantité de bruit aux portions du signal où le découpage de centre a supprimé les échos résiduels.</span><span class="sxs-lookup"><span data-stu-id="b59f5-114">Noise filling adds a small amount of noise to portions of the signal where center clipping has removed the residual echoes.</span></span> <span data-ttu-id="b59f5-115">Cela permet à l’utilisateur d’obtenir une meilleure expérience que de laisser des trous silencieux dans le signal.</span><span class="sxs-lookup"><span data-stu-id="b59f5-115">This results in a better experience for the user than leaving silent gaps in the signal.</span></span>

<span data-ttu-id="b59f5-116">Cette propriété peut avoir les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="b59f5-116">This property can have the following values.</span></span>



| <span data-ttu-id="b59f5-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="b59f5-117">Value</span></span>          | <span data-ttu-id="b59f5-118">Description</span><span class="sxs-lookup"><span data-stu-id="b59f5-118">Description</span></span>            |
|----------------|------------------------|
| <span data-ttu-id="b59f5-119">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="b59f5-119">VARIANT\_TRUE</span></span>  | <span data-ttu-id="b59f5-120">Activez le remplissage de bruit.</span><span class="sxs-lookup"><span data-stu-id="b59f5-120">Enable noise filling.</span></span>  |
| <span data-ttu-id="b59f5-121">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="b59f5-121">VARIANT\_FALSE</span></span> | <span data-ttu-id="b59f5-122">Désactivez le remplissage de bruit.</span><span class="sxs-lookup"><span data-stu-id="b59f5-122">Disable noise filling.</span></span> |



 

<span data-ttu-id="b59f5-123">La valeur par défaut de cette propriété est \_ true (activé).</span><span class="sxs-lookup"><span data-stu-id="b59f5-123">The default value of this property is VARIANT\_TRUE (enabled).</span></span> <span data-ttu-id="b59f5-124">Avant de définir cette propriété, vous devez affecter à la propriété [ \_ mode de \_ fonctionnalité \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) la \_ valeur variant true.</span><span class="sxs-lookup"><span data-stu-id="b59f5-124">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="b59f5-125">Le DSP utilise cette propriété uniquement lorsque le traitement AEC est activé.</span><span class="sxs-lookup"><span data-stu-id="b59f5-125">The DSP uses this property only when AEC processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="b59f5-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b59f5-126">Requirements</span></span>



| <span data-ttu-id="b59f5-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b59f5-127">Requirement</span></span> | <span data-ttu-id="b59f5-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="b59f5-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b59f5-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b59f5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b59f5-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b59f5-130">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b59f5-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b59f5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b59f5-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b59f5-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b59f5-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="b59f5-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b59f5-134"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b59f5-134"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b59f5-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b59f5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b59f5-136">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b59f5-136">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="b59f5-137">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="b59f5-137">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
