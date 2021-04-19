---
description: Spécifie si l’encodeur utilise l’encodage VBR moyen-contrôlable.
ms.assetid: 2c150eb1-4ffe-4f77-8ef8-e3bf29b17b10
title: MFPKEY_AVGCONSTRAINED, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0623fb4a73e3721f9079f2a1e5e330ecb466a774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544651"
---
# <a name="mfpkey_avgconstrained-property"></a><span data-ttu-id="9af25-103">MFPKEY \_ propriété AVGCONSTRAINED</span><span class="sxs-lookup"><span data-stu-id="9af25-103">MFPKEY\_AVGCONSTRAINED Property</span></span>

<span data-ttu-id="9af25-104">Spécifie si l’encodeur utilise l’encodage VBR moyen-contrôlable.</span><span class="sxs-lookup"><span data-stu-id="9af25-104">Specifies whether the encoder uses average-controllable VBR encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="9af25-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="9af25-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="9af25-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="9af25-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="9af25-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="9af25-107">Data Type</span></span>

<span data-ttu-id="9af25-108">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="9af25-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="9af25-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="9af25-109">Default Value</span></span>

<span data-ttu-id="9af25-110">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="9af25-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="9af25-111">Notes</span><span class="sxs-lookup"><span data-stu-id="9af25-111">Remarks</span></span>

<span data-ttu-id="9af25-112">Si cette propriété et la [**propriété \_ VBRENABLED MFPKEY**](mfpkey-vbrenabledproperty.md) ont toutes les deux la valeur **Variant \_ true**, l’encodeur utilise l’encodage VBR moyen-contrôlable.</span><span class="sxs-lookup"><span data-stu-id="9af25-112">If this property and the [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) property are both set to **VARIANT\_TRUE**, the encoder uses average-controllable VBR encoding.</span></span> <span data-ttu-id="9af25-113">Dans ce cas, l’encodeur configure lui-même en fonction des valeurs de [**MFPKEY \_ dyn \_ VBR \_ BAVG**](mfpkey-dyn-vbr-bavgproperty.md) et [**MFPKEY \_ dyn \_ VBR \_ RAVG**](mfpkey-dyn-vbr-ravgproperty.md).</span><span class="sxs-lookup"><span data-stu-id="9af25-113">In that case, the encoder configures itself according to the values of [**MFPKEY\_DYN\_VBR\_BAVG**](mfpkey-dyn-vbr-bavgproperty.md) and [**MFPKEY\_DYN\_VBR\_RAVG**](mfpkey-dyn-vbr-ravgproperty.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9af25-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9af25-114">Requirements</span></span>



| <span data-ttu-id="9af25-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9af25-115">Requirement</span></span> | <span data-ttu-id="9af25-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="9af25-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9af25-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9af25-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9af25-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9af25-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9af25-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9af25-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9af25-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9af25-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9af25-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="9af25-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9af25-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9af25-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9af25-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9af25-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9af25-124">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9af25-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
