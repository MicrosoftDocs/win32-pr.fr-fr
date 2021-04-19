---
description: Spécifie le nombre de fois que le DSP de capture vocale effectue la suppression de l’écho acoustique (AES) sur le signal résiduel.
ms.assetid: 409b40f8-38eb-49f7-be30-348ab5cdd33a
title: MFPKEY_WMAAECMA_FEATR_AES, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5da7505a259a51ca8456f3caffa153790649320
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521458"
---
# <a name="mfpkey_wmaaecma_featr_aes-property"></a><span data-ttu-id="78c4e-103">\_Propriété AES de MFPKEY WMAAECMA \_ Fonct \_</span><span class="sxs-lookup"><span data-stu-id="78c4e-103">MFPKEY\_WMAAECMA\_FEATR\_AES Property</span></span>

<span data-ttu-id="78c4e-104">Spécifie le nombre de fois que le DSP de capture vocale effectue la suppression de l’écho acoustique (AES) sur le signal résiduel.</span><span class="sxs-lookup"><span data-stu-id="78c4e-104">Specifies how many times the Voice Capture DSP performs acoustic echo suppression (AES) on the residual signal.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="78c4e-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="78c4e-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="78c4e-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="78c4e-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="78c4e-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="78c4e-107">Data Type</span></span>

<span data-ttu-id="78c4e-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="78c4e-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="78c4e-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="78c4e-109">Default Value</span></span>

<span data-ttu-id="78c4e-110">0</span><span class="sxs-lookup"><span data-stu-id="78c4e-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="78c4e-111">S'applique à</span><span class="sxs-lookup"><span data-stu-id="78c4e-111">Applies To</span></span>

-   [<span data-ttu-id="78c4e-112">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="78c4e-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="78c4e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="78c4e-113">Remarks</span></span>

<span data-ttu-id="78c4e-114">Le DSP de capture vocale peut exécuter AES sur le signal résiduel après l’annulation de l’écho.</span><span class="sxs-lookup"><span data-stu-id="78c4e-114">The Voice Capture DSP can perform AES on the residual signal after echo cancellation.</span></span> <span data-ttu-id="78c4e-115">Cette propriété peut avoir la valeur 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="78c4e-115">This property can have the value 0, 1, or 2.</span></span> <span data-ttu-id="78c4e-116">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="78c4e-116">The default value is 0.</span></span> <span data-ttu-id="78c4e-117">Avant de définir cette propriété, vous devez affecter à la propriété [ \_ mode de \_ fonctionnalité \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) la \_ valeur variant true.</span><span class="sxs-lookup"><span data-stu-id="78c4e-117">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="78c4e-118">Le DSP utilise cette propriété uniquement lorsque le traitement AEC est activé.</span><span class="sxs-lookup"><span data-stu-id="78c4e-118">The DSP uses this property only when AEC processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="78c4e-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="78c4e-119">Requirements</span></span>



| <span data-ttu-id="78c4e-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="78c4e-120">Requirement</span></span> | <span data-ttu-id="78c4e-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="78c4e-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="78c4e-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78c4e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="78c4e-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="78c4e-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="78c4e-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78c4e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="78c4e-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="78c4e-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="78c4e-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="78c4e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="78c4e-127"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="78c4e-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78c4e-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78c4e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78c4e-129">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="78c4e-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="78c4e-130">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="78c4e-130">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
