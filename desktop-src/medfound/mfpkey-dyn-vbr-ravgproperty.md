---
description: Spécifie la vitesse de transmission moyenne, en bits par seconde, pour un encodeur qui est configuré pour utiliser l’encodage VBR moyen-contrôlable.
ms.assetid: d689a34c-97f7-4b1c-82b6-863ce3b8403f
title: MFPKEY_DYN_VBR_RAVG, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8103d36db5a9e946449231943e076c26258eec19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951668"
---
# <a name="mfpkey_dyn_vbr_ravg-property"></a><span data-ttu-id="465e7-103">MFPKEY \_ dyn \_ VBR \_ RAVG, propriété</span><span class="sxs-lookup"><span data-stu-id="465e7-103">MFPKEY\_DYN\_VBR\_RAVG Property</span></span>

<span data-ttu-id="465e7-104">Spécifie la vitesse de transmission moyenne, en bits par seconde, pour un encodeur qui est configuré pour utiliser l’encodage VBR moyen-contrôlable.</span><span class="sxs-lookup"><span data-stu-id="465e7-104">Specifies the average bit rate, in bits per second, for an encoder that is configured to use average-controllable VBR encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="465e7-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="465e7-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="465e7-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="465e7-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="465e7-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="465e7-107">Data Type</span></span>

<span data-ttu-id="465e7-108">**VT \_**</span><span class="sxs-lookup"><span data-stu-id="465e7-108">**VT\_I4**</span></span>

## <a name="remarks"></a><span data-ttu-id="465e7-109">Notes</span><span class="sxs-lookup"><span data-stu-id="465e7-109">Remarks</span></span>

<span data-ttu-id="465e7-110">Si les propriétés [**MFPKEY \_ AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) et [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) sont toutes deux définies sur **Variant \_ true**, l’encodeur utilise l’encodage VBR moyen-contrôlable.</span><span class="sxs-lookup"><span data-stu-id="465e7-110">If the [**MFPKEY\_AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) and [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) properties are both set to **VARIANT\_TRUE**, the encoder uses average-controllable VBR encoding.</span></span> <span data-ttu-id="465e7-111">Dans ce cas, l’encodeur configure lui-même en fonction de la valeur de cette propriété et de la propriété [**MFPKEY \_ dyn \_ VBR \_ BAVG**](mfpkey-dyn-vbr-bavgproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="465e7-111">In that case, the encoder configures itself according to the value of this property and the [**MFPKEY\_DYN\_VBR\_BAVG**](mfpkey-dyn-vbr-bavgproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="465e7-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="465e7-112">Requirements</span></span>



| <span data-ttu-id="465e7-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="465e7-113">Requirement</span></span> | <span data-ttu-id="465e7-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="465e7-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="465e7-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="465e7-115">Minimum supported client</span></span><br/> | <span data-ttu-id="465e7-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="465e7-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="465e7-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="465e7-117">Minimum supported server</span></span><br/> | <span data-ttu-id="465e7-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="465e7-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="465e7-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="465e7-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="465e7-120"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="465e7-120"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="465e7-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="465e7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="465e7-122">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="465e7-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
