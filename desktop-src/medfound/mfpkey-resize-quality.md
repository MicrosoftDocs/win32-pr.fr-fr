---
description: Spécifie s’il faut utiliser un algorithme qui produit une vidéo de qualité supérieure, ou un algorithme plus rapide.
ms.assetid: a6760e7e-7c99-4412-bde5-05958fad89a1
title: MFPKEY_RESIZE_QUALITY, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e79ae1cac78b4d836261905afdacaf14fc227fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529152"
---
# <a name="mfpkey_resize_quality-property"></a><span data-ttu-id="725d6-103">\_Propriété de qualité de REdimensionnement MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="725d6-103">MFPKEY\_RESIZE\_QUALITY Property</span></span>

<span data-ttu-id="725d6-104">Spécifie s’il faut utiliser un algorithme qui produit une vidéo de qualité supérieure, ou un algorithme plus rapide.</span><span class="sxs-lookup"><span data-stu-id="725d6-104">Specifies whether to use an algorithm that produces higher-quality video, or a faster algorithm.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="725d6-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="725d6-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="725d6-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="725d6-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="725d6-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="725d6-107">Data Type</span></span>

<span data-ttu-id="725d6-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="725d6-108">VT\_BOOL</span></span>

## <a name="applies-to"></a><span data-ttu-id="725d6-109">S'applique à</span><span class="sxs-lookup"><span data-stu-id="725d6-109">Applies To</span></span>

-   [<span data-ttu-id="725d6-110">Dimensionnement vidéo DSP</span><span class="sxs-lookup"><span data-stu-id="725d6-110">Video Resizer DSP</span></span>](videoresizer.md)

## <a name="remarks"></a><span data-ttu-id="725d6-111">Notes</span><span class="sxs-lookup"><span data-stu-id="725d6-111">Remarks</span></span>

<span data-ttu-id="725d6-112">Utilisez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="725d6-112">Use one of the following values:</span></span>



| <span data-ttu-id="725d6-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="725d6-113">Value</span></span>     | <span data-ttu-id="725d6-114">Description</span><span class="sxs-lookup"><span data-stu-id="725d6-114">Description</span></span>          |
|-----------|----------------------|
| <span data-ttu-id="725d6-115">VT \_ false</span><span class="sxs-lookup"><span data-stu-id="725d6-115">VT\_FALSE</span></span> | <span data-ttu-id="725d6-116">Algorithme plus rapide</span><span class="sxs-lookup"><span data-stu-id="725d6-116">Faster algorithm</span></span>     |
| <span data-ttu-id="725d6-117">VT \_ vrai</span><span class="sxs-lookup"><span data-stu-id="725d6-117">VT\_TRUE</span></span>  | <span data-ttu-id="725d6-118">Vidéo de qualité supérieure</span><span class="sxs-lookup"><span data-stu-id="725d6-118">Higher-quality video</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="725d6-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="725d6-119">Requirements</span></span>



| <span data-ttu-id="725d6-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="725d6-120">Requirement</span></span> | <span data-ttu-id="725d6-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="725d6-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="725d6-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="725d6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="725d6-123">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="725d6-123">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="725d6-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="725d6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="725d6-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="725d6-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="725d6-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="725d6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="725d6-127"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="725d6-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="725d6-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="725d6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="725d6-129">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="725d6-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
