---
description: Ajuste le contraste.
ms.assetid: 32ae514a-eeba-4205-b6e6-70fc01b93a95
title: MFPKEY_COLOR_CONTRAST, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5de0733e743c3ce12bfe9a04159a2e881bf2143
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533840"
---
# <a name="mfpkey_color_contrast-property"></a><span data-ttu-id="d5f31-103">MFPKEY \_ , \_ propriété de contraste de couleur</span><span class="sxs-lookup"><span data-stu-id="d5f31-103">MFPKEY\_COLOR\_CONTRAST Property</span></span>

<span data-ttu-id="d5f31-104">Ajuste le contraste.</span><span class="sxs-lookup"><span data-stu-id="d5f31-104">Adjusts the contrast.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="d5f31-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="d5f31-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="d5f31-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="d5f31-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="d5f31-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="d5f31-107">Data Type</span></span>

<span data-ttu-id="d5f31-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="d5f31-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="d5f31-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="d5f31-109">Default Value</span></span>

<span data-ttu-id="d5f31-110">0</span><span class="sxs-lookup"><span data-stu-id="d5f31-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="d5f31-111">S'applique à</span><span class="sxs-lookup"><span data-stu-id="d5f31-111">Applies To</span></span>

-   [<span data-ttu-id="d5f31-112">Transformation de contrôle de couleur DSP</span><span class="sxs-lookup"><span data-stu-id="d5f31-112">Color Control Transform DSP</span></span>](colorcontroltransform.md)

## <a name="remarks"></a><span data-ttu-id="d5f31-113">Notes</span><span class="sxs-lookup"><span data-stu-id="d5f31-113">Remarks</span></span>

<span data-ttu-id="d5f31-114">L’ajustement du contraste est effectué en multipliant les valeurs YCbCr par un facteur d’échelle.</span><span class="sxs-lookup"><span data-stu-id="d5f31-114">Contrast adjustment is performed by multiplying the YCbCr values by a scaling factor.</span></span>

<span data-ttu-id="d5f31-115">Cette propriété a une plage comprise entre-127 et 127.</span><span class="sxs-lookup"><span data-stu-id="d5f31-115">This property has a range of -127 to 127.</span></span> <span data-ttu-id="d5f31-116">La valeur zéro indique qu’aucune modification n’est apportée.</span><span class="sxs-lookup"><span data-stu-id="d5f31-116">Zero indicates no change in contrast.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5f31-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5f31-117">Requirements</span></span>



| <span data-ttu-id="d5f31-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5f31-118">Requirement</span></span> | <span data-ttu-id="d5f31-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5f31-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5f31-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5f31-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d5f31-121">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d5f31-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d5f31-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5f31-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d5f31-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d5f31-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d5f31-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="d5f31-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5f31-125"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5f31-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5f31-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5f31-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5f31-127">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d5f31-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
