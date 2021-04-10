---
description: Ajuste la teinte.
ms.assetid: 8dc3c888-5ab8-40a1-8768-bec58b62eaf0
title: MFPKEY_COLOR_HUE, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b3ddf0109090bfb56102560dc06a853c970e7ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115135"
---
# <a name="mfpkey_color_hue-property"></a><span data-ttu-id="69882-103">\_ \_ Propriété teinte de couleur MFPKEY</span><span class="sxs-lookup"><span data-stu-id="69882-103">MFPKEY\_COLOR\_HUE Property</span></span>

<span data-ttu-id="69882-104">Ajuste la teinte.</span><span class="sxs-lookup"><span data-stu-id="69882-104">Adjusts the hue.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="69882-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="69882-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="69882-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="69882-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="69882-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="69882-107">Data Type</span></span>

<span data-ttu-id="69882-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="69882-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="69882-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="69882-109">Default Value</span></span>

<span data-ttu-id="69882-110">0</span><span class="sxs-lookup"><span data-stu-id="69882-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="69882-111">S'applique à</span><span class="sxs-lookup"><span data-stu-id="69882-111">Applies To</span></span>

-   [<span data-ttu-id="69882-112">Transformation de contrôle de couleur DSP</span><span class="sxs-lookup"><span data-stu-id="69882-112">Color Control Transform DSP</span></span>](colorcontroltransform.md)

## <a name="remarks"></a><span data-ttu-id="69882-113">Notes</span><span class="sxs-lookup"><span data-stu-id="69882-113">Remarks</span></span>

<span data-ttu-id="69882-114">L’ajustement de la teinte est effectué en combinant les valeurs CB et CR.</span><span class="sxs-lookup"><span data-stu-id="69882-114">Hue adjustment is performed by mixing the Cb and Cr values.</span></span> <span data-ttu-id="69882-115">(Si CB et CR sont tracés dans un espace à deux dimensions, l’ajustement de la teinte est effectué en faisant tourner l’origine.)</span><span class="sxs-lookup"><span data-stu-id="69882-115">(If Cb and Cr are plotted in a 2-dimensional space, hue adjustment is performed by rotating around the origin.)</span></span>

<span data-ttu-id="69882-116">Cette propriété a une plage comprise entre-127 et 127.</span><span class="sxs-lookup"><span data-stu-id="69882-116">This property has a range of -127 to 127.</span></span> <span data-ttu-id="69882-117">La valeur zéro indique qu’il n’y a aucune modification de la teinte.</span><span class="sxs-lookup"><span data-stu-id="69882-117">Zero indicates no change in hue.</span></span>

## <a name="requirements"></a><span data-ttu-id="69882-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69882-118">Requirements</span></span>



| <span data-ttu-id="69882-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69882-119">Requirement</span></span> | <span data-ttu-id="69882-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="69882-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="69882-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69882-121">Minimum supported client</span></span><br/> | <span data-ttu-id="69882-122">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69882-122">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="69882-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69882-123">Minimum supported server</span></span><br/> | <span data-ttu-id="69882-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69882-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="69882-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="69882-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="69882-126"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="69882-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69882-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69882-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69882-128">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="69882-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
