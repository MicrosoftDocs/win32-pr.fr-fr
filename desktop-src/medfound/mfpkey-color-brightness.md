---
description: Ajuste la luminosité.
ms.assetid: 1b3f56eb-3f22-4120-ba6c-331eccd5d303
title: MFPKEY_COLOR_BRIGHTNESS, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 685ab934a91f1843183fcfa88bb94c83e602db27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864774"
---
# <a name="mfpkey_color_brightness-property"></a><span data-ttu-id="df156-103">Propriété de luminosité des \_ couleurs MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="df156-103">MFPKEY\_COLOR\_BRIGHTNESS Property</span></span>

<span data-ttu-id="df156-104">Ajuste la luminosité.</span><span class="sxs-lookup"><span data-stu-id="df156-104">Adjusts the brightness.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="df156-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="df156-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="df156-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="df156-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="df156-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="df156-107">Data Type</span></span>

<span data-ttu-id="df156-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="df156-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="df156-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="df156-109">Default Value</span></span>

<span data-ttu-id="df156-110">0</span><span class="sxs-lookup"><span data-stu-id="df156-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="df156-111">S'applique à</span><span class="sxs-lookup"><span data-stu-id="df156-111">Applies To</span></span>

-   [<span data-ttu-id="df156-112">Transformation de contrôle de couleur DSP</span><span class="sxs-lookup"><span data-stu-id="df156-112">Color Control Transform DSP</span></span>](colorcontroltransform.md)

## <a name="remarks"></a><span data-ttu-id="df156-113">Notes</span><span class="sxs-lookup"><span data-stu-id="df156-113">Remarks</span></span>

<span data-ttu-id="df156-114">L’ajustement de la luminosité s’effectue en ajoutant une valeur au canal de luminance.</span><span class="sxs-lookup"><span data-stu-id="df156-114">Brightness adjustment is performed by adding a value to the luma channel.</span></span>

<span data-ttu-id="df156-115">Cette propriété a une plage comprise entre-127 et 127.</span><span class="sxs-lookup"><span data-stu-id="df156-115">This property has a range of -127 to 127.</span></span> <span data-ttu-id="df156-116">La valeur zéro indique qu’aucune modification n’est apportée à la luminosité.</span><span class="sxs-lookup"><span data-stu-id="df156-116">Zero indicates no change in brightness.</span></span>

## <a name="requirements"></a><span data-ttu-id="df156-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df156-117">Requirements</span></span>



| <span data-ttu-id="df156-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df156-118">Requirement</span></span> | <span data-ttu-id="df156-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="df156-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="df156-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df156-120">Minimum supported client</span></span><br/> | <span data-ttu-id="df156-121">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="df156-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="df156-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df156-122">Minimum supported server</span></span><br/> | <span data-ttu-id="df156-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="df156-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="df156-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="df156-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="df156-125"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="df156-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df156-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df156-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df156-127">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="df156-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
