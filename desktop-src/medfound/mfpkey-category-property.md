---
description: Contient le GUID de catégorie pour une transformation de Media Foundation (MFT).
ms.assetid: 3c0948fc-42ea-4e43-a312-c98038020214
title: MFPKEY_CATEGORY, propriété (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bbb83ab2c824ff9a4510e520b13c49ae5b3a52a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865577"
---
# <a name="mfpkey_category-property"></a><span data-ttu-id="20a67-103">\_Propriété de catégorie MFPKEY</span><span class="sxs-lookup"><span data-stu-id="20a67-103">MFPKEY\_CATEGORY property</span></span>

<span data-ttu-id="20a67-104">Contient le GUID de catégorie pour une transformation de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="20a67-104">Contains the category GUID for a Media Foundation transform (MFT).</span></span>



<span data-ttu-id="20a67-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="20a67-105">Data type</span></span>

<span data-ttu-id="20a67-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="20a67-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="20a67-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="20a67-107">PROPVARIANT member</span></span>

<span data-ttu-id="20a67-108">**GUID** (**CLSID** \* )</span><span class="sxs-lookup"><span data-stu-id="20a67-108">**GUID** (**CLSID**\*)</span></span>

<span data-ttu-id="20a67-109">\_CLSID VT</span><span class="sxs-lookup"><span data-stu-id="20a67-109">VT\_CLSID</span></span>

<span data-ttu-id="20a67-110">**puuid**</span><span class="sxs-lookup"><span data-stu-id="20a67-110">**puuid**</span></span>



## <a name="remarks"></a><span data-ttu-id="20a67-111">Notes</span><span class="sxs-lookup"><span data-stu-id="20a67-111">Remarks</span></span>

<span data-ttu-id="20a67-112">La valeur de cette propriété est un GUID qui identifie la catégorie MFT.</span><span class="sxs-lookup"><span data-stu-id="20a67-112">The value of this property is a GUID that identifies the MFT category.</span></span> <span data-ttu-id="20a67-113">Pour obtenir la liste des catégories, consultez [**MFT \_ Category**](mft-category.md).</span><span class="sxs-lookup"><span data-stu-id="20a67-113">For a list of categories, see [**MFT\_CATEGORY**](mft-category.md).</span></span>

<span data-ttu-id="20a67-114">Cette propriété est facultative et est à titre d’information uniquement.</span><span class="sxs-lookup"><span data-stu-id="20a67-114">This property is optional and is informational only.</span></span> <span data-ttu-id="20a67-115">Une table MFT peut utiliser cette propriété pour signaler la catégorie sous laquelle elle est inscrite.</span><span class="sxs-lookup"><span data-stu-id="20a67-115">An MFT can use this property to report the category under which it is registered.</span></span> <span data-ttu-id="20a67-116">Pour obtenir cette propriété, interrogez la table MFT pour l’interface **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="20a67-116">To get this property, query the MFT for the **IPropertyStore** interface.</span></span>

<span data-ttu-id="20a67-117">Pour énumérer une catégorie MFT, appelez la fonction [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) .</span><span class="sxs-lookup"><span data-stu-id="20a67-117">To enumerate an MFT category, call the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) function.</span></span> <span data-ttu-id="20a67-118">Il n’existe pas de lien direct entre la fonction **MFTEnum** et cette propriété.</span><span class="sxs-lookup"><span data-stu-id="20a67-118">There is no direct link between the **MFTEnum** function and this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="20a67-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20a67-119">Requirements</span></span>



| <span data-ttu-id="20a67-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20a67-120">Requirement</span></span> | <span data-ttu-id="20a67-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="20a67-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="20a67-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20a67-122">Minimum supported client</span></span><br/> | <span data-ttu-id="20a67-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="20a67-123">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="20a67-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20a67-124">Minimum supported server</span></span><br/> | <span data-ttu-id="20a67-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="20a67-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="20a67-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="20a67-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="20a67-127"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="20a67-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20a67-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20a67-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20a67-129">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="20a67-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="20a67-130">Transformations de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="20a67-130">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> </dl>

 

 




