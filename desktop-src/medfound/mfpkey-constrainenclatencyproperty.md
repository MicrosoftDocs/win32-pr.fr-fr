---
description: Spécifie si l’encodeur est limité par une latence maximale.
ms.assetid: 8148ae1e-239e-40fa-a88d-810a1d93d8e9
title: MFPKEY_CONSTRAINENCLATENCY, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f880006bf2aba04196547a79e74f94a7210edd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543492"
---
# <a name="mfpkey_constrainenclatency-property"></a><span data-ttu-id="30f6e-103">MFPKEY \_ propriété CONSTRAINENCLATENCY</span><span class="sxs-lookup"><span data-stu-id="30f6e-103">MFPKEY\_CONSTRAINENCLATENCY Property</span></span>

<span data-ttu-id="30f6e-104">Spécifie si l’encodeur est limité par une latence maximale.</span><span class="sxs-lookup"><span data-stu-id="30f6e-104">Specifies whether the encoder is constrained by a maximum latency requirement.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="30f6e-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="30f6e-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="30f6e-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="30f6e-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="30f6e-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="30f6e-107">Data Type</span></span>

<span data-ttu-id="30f6e-108">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="30f6e-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="30f6e-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="30f6e-109">Default Value</span></span>

<span data-ttu-id="30f6e-110">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="30f6e-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="30f6e-111">Notes</span><span class="sxs-lookup"><span data-stu-id="30f6e-111">Remarks</span></span>

<span data-ttu-id="30f6e-112">Si vous laissez cette propriété à sa valeur par défaut **Variant \_ false**, l’encodeur énumère un ensemble de modes par défaut qui ont environ 2000 millisecondes de latence de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="30f6e-112">If you leave this property at its default value of **VARIANT\_FALSE**, the encoder enumerates a default set of modes that have about 2000 milliseconds of encoder latency.</span></span> <span data-ttu-id="30f6e-113">Si vous affectez à cette propriété la **\_ valeur variant true**, vous devez également spécifier une latence maximale de l’encodeur en définissant la propriété [**MFPKEY \_ MAXENCLATENCYMS**](mfpkey-maxenclatencymsproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="30f6e-113">If you set this property to **VARIANT\_TRUE**, you must also specify a maximum encoder latency by setting the [**MFPKEY\_MAXENCLATENCYMS**](mfpkey-maxenclatencymsproperty.md) property.</span></span> <span data-ttu-id="30f6e-114">Dans ce cas, l’encodeur crée des modes qui répondent aux exigences de latence et énumère uniquement ces modes.</span><span class="sxs-lookup"><span data-stu-id="30f6e-114">In that case, the encoder creates modes that satisfy the latency requirement and enumerates only those modes.</span></span> <span data-ttu-id="30f6e-115">L’encodeur garantit un échantillon de sortie dès que l’encodeur a reçu une entrée pour une période de temps égale à **MFPKEY \_ MAXENCLATENCYMS**.</span><span class="sxs-lookup"><span data-stu-id="30f6e-115">The encoder guarantees an output sample as soon as the encoder has received input for a time period equal to **MFPKEY\_MAXENCLATENCYMS**.</span></span>

## <a name="requirements"></a><span data-ttu-id="30f6e-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30f6e-116">Requirements</span></span>



| <span data-ttu-id="30f6e-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30f6e-117">Requirement</span></span> | <span data-ttu-id="30f6e-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="30f6e-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30f6e-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30f6e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="30f6e-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30f6e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="30f6e-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30f6e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="30f6e-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30f6e-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="30f6e-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="30f6e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="30f6e-124"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="30f6e-124"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30f6e-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30f6e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30f6e-126">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="30f6e-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
