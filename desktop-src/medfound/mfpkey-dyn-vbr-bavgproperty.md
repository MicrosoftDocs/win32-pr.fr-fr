---
description: Spécifie la fenêtre de mémoire tampon, en millisecondes, pour un encodeur qui est configuré pour utiliser l’encodage VBR moyen-contrôlable.
ms.assetid: ce330ce0-4bda-4340-b21c-63a8b9168cf4
title: MFPKEY_DYN_VBR_BAVG, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e117c2852f660b015bcdd95224178730d2e2a1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524159"
---
# <a name="mfpkey_dyn_vbr_bavg-property"></a><span data-ttu-id="f3a40-103">MFPKEY \_ dyn \_ VBR \_ BAVG, propriété</span><span class="sxs-lookup"><span data-stu-id="f3a40-103">MFPKEY\_DYN\_VBR\_BAVG Property</span></span>

<span data-ttu-id="f3a40-104">Spécifie la fenêtre de mémoire tampon, en millisecondes, pour un encodeur qui est configuré pour utiliser l’encodage VBR moyen-contrôlable.</span><span class="sxs-lookup"><span data-stu-id="f3a40-104">Specifies the buffer window, in milliseconds, for an encoder that is configured to use average-controllable VBR encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="f3a40-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="f3a40-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="f3a40-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="f3a40-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="f3a40-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="f3a40-107">Data Type</span></span>

<span data-ttu-id="f3a40-108">**VT \_**</span><span class="sxs-lookup"><span data-stu-id="f3a40-108">**VT\_I4**</span></span>

## <a name="remarks"></a><span data-ttu-id="f3a40-109">Notes</span><span class="sxs-lookup"><span data-stu-id="f3a40-109">Remarks</span></span>

<span data-ttu-id="f3a40-110">Si les propriétés [**MFPKEY \_ AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) et [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) sont toutes deux définies sur **Variant \_ true**, l’encodeur utilise l’encodage VBR moyen-contrôlable.</span><span class="sxs-lookup"><span data-stu-id="f3a40-110">If the [**MFPKEY\_AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) and [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) properties are both set to **VARIANT\_TRUE**, the encoder uses average-controllable VBR encoding.</span></span> <span data-ttu-id="f3a40-111">Dans ce cas, l’encodeur configure lui-même en fonction de la valeur de cette propriété et de la propriété [**MFPKEY \_ dyn \_ VBR \_ RAVG**](mfpkey-dyn-vbr-ravgproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="f3a40-111">In that case, the encoder configures itself according to the value of this property and the [**MFPKEY\_DYN\_VBR\_RAVG**](mfpkey-dyn-vbr-ravgproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3a40-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3a40-112">Requirements</span></span>



| <span data-ttu-id="f3a40-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f3a40-113">Requirement</span></span> | <span data-ttu-id="f3a40-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3a40-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3a40-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3a40-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f3a40-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f3a40-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f3a40-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3a40-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f3a40-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f3a40-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f3a40-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="f3a40-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3a40-120"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3a40-120"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3a40-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3a40-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3a40-122">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f3a40-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
