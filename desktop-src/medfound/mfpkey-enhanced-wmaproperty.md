---
description: Spécifie si l’encodeur principal utilise la &\# 0034 ; Plus \# 0034&fonctionnalité.
ms.assetid: 1ace09da-7dee-469e-a533-63b40ac747ab
title: MFPKEY_ENHANCED_WMA, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df1c7ddc0e7bfb6d62d51e535f10b257eac6f2ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525664"
---
# <a name="mfpkey_enhanced_wma-property"></a><span data-ttu-id="246da-103">MFPKEY \_ , \_ propriété WMA améliorée</span><span class="sxs-lookup"><span data-stu-id="246da-103">MFPKEY\_ENHANCED\_WMA Property</span></span>

<span data-ttu-id="246da-104">Spécifie si l’encodeur principal utilise la fonctionnalité « plus ».</span><span class="sxs-lookup"><span data-stu-id="246da-104">Specifies whether the core encoder uses the "Plus" feature.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="246da-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="246da-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="246da-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="246da-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="246da-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="246da-107">Data Type</span></span>

<span data-ttu-id="246da-108">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="246da-108">**VT\_UI4**</span></span>

## <a name="default-value"></a><span data-ttu-id="246da-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="246da-109">Default Value</span></span>

<span data-ttu-id="246da-110">0</span><span class="sxs-lookup"><span data-stu-id="246da-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="246da-111">Notes</span><span class="sxs-lookup"><span data-stu-id="246da-111">Remarks</span></span>

<span data-ttu-id="246da-112">Cette propriété n’est disponible que pour les Windows Media Audio sans perte.</span><span class="sxs-lookup"><span data-stu-id="246da-112">This property is available only for Windows Media Audio Lossless.</span></span>

<span data-ttu-id="246da-113">Si vous laissez cette propriété à sa valeur par défaut égale à 0 ou si vous la définissez sur 1, l’encodeur principal détermine si la partie « plus » doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="246da-113">If you leave this property at its default value of 0, or if you set it to 1, the core encoder decides whether the "Plus" portion should be used.</span></span> <span data-ttu-id="246da-114">Si vous affectez à cette propriété la valeur 2, l’encodeur principal n’utilise pas la fonctionnalité « plus ».</span><span class="sxs-lookup"><span data-stu-id="246da-114">If you set this property to 2, the core encoder does not use the "Plus" feature.</span></span>

<span data-ttu-id="246da-115">Cette propriété modifie les types de médias énumérés. par conséquent, si vous la définissez, vous devez le faire avant de définir le type de sortie.</span><span class="sxs-lookup"><span data-stu-id="246da-115">This property alters the enumerated media types, so if you set it, you must do so before you set the output type.</span></span>

## <a name="requirements"></a><span data-ttu-id="246da-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="246da-116">Requirements</span></span>



| <span data-ttu-id="246da-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="246da-117">Requirement</span></span> | <span data-ttu-id="246da-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="246da-118">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="246da-119">Client</span><span class="sxs-lookup"><span data-stu-id="246da-119">Client</span></span><br/> | <span data-ttu-id="246da-120">Windows Vista ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="246da-120">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="246da-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="246da-121">Header</span></span><br/> | <dl> <span data-ttu-id="246da-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="246da-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="246da-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="246da-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="246da-124">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="246da-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
