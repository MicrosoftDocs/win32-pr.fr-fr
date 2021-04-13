---
description: Ajuste la saturation.
ms.assetid: bd71f542-36d9-4dfc-b402-35ee8e574731
title: MFPKEY_COLOR_SATURATION, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 496b1f017ceff6ab4bd01ce01ccfd5da0759befc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528684"
---
# <a name="mfpkey_color_saturation-property"></a><span data-ttu-id="2f508-103">\_ \_ Propriété saturation de la couleur MFPKEY</span><span class="sxs-lookup"><span data-stu-id="2f508-103">MFPKEY\_COLOR\_SATURATION Property</span></span>

<span data-ttu-id="2f508-104">Ajuste la saturation.</span><span class="sxs-lookup"><span data-stu-id="2f508-104">Adjusts the saturation.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="2f508-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="2f508-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="2f508-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="2f508-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="2f508-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="2f508-107">Data Type</span></span>

<span data-ttu-id="2f508-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="2f508-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="2f508-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="2f508-109">Default Value</span></span>

<span data-ttu-id="2f508-110">0</span><span class="sxs-lookup"><span data-stu-id="2f508-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="2f508-111">S'applique à</span><span class="sxs-lookup"><span data-stu-id="2f508-111">Applies To</span></span>

-   [<span data-ttu-id="2f508-112">Transformation de contrôle de couleur DSP</span><span class="sxs-lookup"><span data-stu-id="2f508-112">Color Control Transform DSP</span></span>](colorcontroltransform.md)

## <a name="remarks"></a><span data-ttu-id="2f508-113">Notes</span><span class="sxs-lookup"><span data-stu-id="2f508-113">Remarks</span></span>

<span data-ttu-id="2f508-114">L’ajustement de saturation s’effectue en multipliant les valeurs CB et CR par une constante.</span><span class="sxs-lookup"><span data-stu-id="2f508-114">Saturation adjustment is performed by multiplying the Cb and Cr values by a constant.</span></span>

<span data-ttu-id="2f508-115">Cette propriété a une plage comprise entre-127 et 127.</span><span class="sxs-lookup"><span data-stu-id="2f508-115">This property has a range of -127 to 127.</span></span> <span data-ttu-id="2f508-116">La valeur zéro indique qu’aucune modification n’est apportée à la saturation.</span><span class="sxs-lookup"><span data-stu-id="2f508-116">Zero indicates no change in saturation.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f508-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f508-117">Requirements</span></span>



| <span data-ttu-id="2f508-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f508-118">Requirement</span></span> | <span data-ttu-id="2f508-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f508-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f508-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f508-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2f508-121">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2f508-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2f508-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f508-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2f508-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2f508-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2f508-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="2f508-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f508-125"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f508-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f508-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f508-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f508-127">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2f508-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
