---
description: Spécifie si la capture de la voix DSP effectue le prétraitement du tableau de microphone.
ms.assetid: 0f197165-e6e5-456b-9615-1edc8ada7bb5
title: MFPKEY_WMAAECMA_FEATR_MICARR_PREPROC, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f992d8d26ba547eb1b5d1eac470536a963209f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536131"
---
# <a name="mfpkey_wmaaecma_featr_micarr_preproc-property"></a><span data-ttu-id="e5ff5-103">MFPKEY \_ WMAAECMA \_ fonceur \_ MICARR, \_ propriété de préprocesseur</span><span class="sxs-lookup"><span data-stu-id="e5ff5-103">MFPKEY\_WMAAECMA\_FEATR\_MICARR\_PREPROC Property</span></span>

<span data-ttu-id="e5ff5-104">Spécifie si la capture de la voix DSP effectue le prétraitement du tableau de microphone.</span><span class="sxs-lookup"><span data-stu-id="e5ff5-104">Specifies whether the Voice Capture DSP performs microphone array preprocessing.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="e5ff5-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="e5ff5-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="e5ff5-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="e5ff5-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="e5ff5-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="e5ff5-107">Data Type</span></span>

<span data-ttu-id="e5ff5-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="e5ff5-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="e5ff5-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="e5ff5-109">Default Value</span></span>

<span data-ttu-id="e5ff5-110">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="e5ff5-110">VARIANT\_TRUE</span></span>

## <a name="applies-to"></a><span data-ttu-id="e5ff5-111">S'applique à</span><span class="sxs-lookup"><span data-stu-id="e5ff5-111">Applies To</span></span>

-   [<span data-ttu-id="e5ff5-112">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="e5ff5-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="e5ff5-113">Notes</span><span class="sxs-lookup"><span data-stu-id="e5ff5-113">Remarks</span></span>

<span data-ttu-id="e5ff5-114">Le prétraitement peut supprimer des tons stationnaires qui interfèrent avec le traitement, par exemple une tonalité avec un pas de ton fixe.</span><span class="sxs-lookup"><span data-stu-id="e5ff5-114">Preprocessing can remove stationary tones that interfere with processing, such as a tone with a fixed pitch.</span></span>

<span data-ttu-id="e5ff5-115">Cette propriété peut avoir les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e5ff5-115">This property can have the following values.</span></span>



| <span data-ttu-id="e5ff5-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e5ff5-116">Value</span></span>          | <span data-ttu-id="e5ff5-117">Description</span><span class="sxs-lookup"><span data-stu-id="e5ff5-117">Description</span></span>            |
|----------------|------------------------|
| <span data-ttu-id="e5ff5-118">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="e5ff5-118">VARIANT\_FALSE</span></span> | <span data-ttu-id="e5ff5-119">Désactivez le prétraitement.</span><span class="sxs-lookup"><span data-stu-id="e5ff5-119">Disable preprocessing.</span></span> |
| <span data-ttu-id="e5ff5-120">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="e5ff5-120">VARIANT\_TRUE</span></span>  | <span data-ttu-id="e5ff5-121">Activez le prétraitement.</span><span class="sxs-lookup"><span data-stu-id="e5ff5-121">Enable preprocessing.</span></span>  |



 

<span data-ttu-id="e5ff5-122">La valeur par défaut de cette propriété est \_ true (activé).</span><span class="sxs-lookup"><span data-stu-id="e5ff5-122">The default value of this property is VARIANT\_TRUE (enabled).</span></span> <span data-ttu-id="e5ff5-123">Avant de définir cette propriété, vous devez affecter à la propriété [ \_ mode de \_ fonctionnalité \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) la \_ valeur variant true.</span><span class="sxs-lookup"><span data-stu-id="e5ff5-123">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="e5ff5-124">Le DSP utilise cette propriété uniquement lorsque le traitement du tableau du microphone est activé.</span><span class="sxs-lookup"><span data-stu-id="e5ff5-124">The DSP uses this property only when microphone array processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5ff5-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e5ff5-125">Requirements</span></span>



| <span data-ttu-id="e5ff5-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e5ff5-126">Requirement</span></span> | <span data-ttu-id="e5ff5-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="e5ff5-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5ff5-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5ff5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e5ff5-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e5ff5-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e5ff5-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5ff5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e5ff5-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e5ff5-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e5ff5-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="e5ff5-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5ff5-133"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5ff5-133"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5ff5-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5ff5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5ff5-135">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e5ff5-135">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="e5ff5-136">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="e5ff5-136">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
