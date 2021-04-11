---
description: Spécifie la catégorie pour une transformation de Media Foundation (MFT).
ms.assetid: cebd64ea-b20f-4ccc-805f-0deab3096bc3
title: Attribut MF_TRANSFORM_CATEGORY_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3c64fd5e19bba10646957e7c247294b6d82a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201715"
---
# <a name="mf_transform_category_attribute-attribute"></a><span data-ttu-id="81d1c-103">\_Attribut d' \_ attribut de catégorie de transformation MF \_</span><span class="sxs-lookup"><span data-stu-id="81d1c-103">MF\_TRANSFORM\_CATEGORY\_Attribute attribute</span></span>

<span data-ttu-id="81d1c-104">Spécifie la catégorie pour une transformation de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="81d1c-104">Specifies the category for a Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="81d1c-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="81d1c-105">Data type</span></span>

<span data-ttu-id="81d1c-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="81d1c-106">**GUID**</span></span>

<span data-ttu-id="81d1c-107">Pour obtenir la liste des valeurs possibles, consultez la rubrique [**\_ catégorie MFT**](mft-category.md).</span><span class="sxs-lookup"><span data-stu-id="81d1c-107">For a list of possible values, see [**MFT\_CATEGORY**](mft-category.md).</span></span>

## <a name="getset"></a><span data-ttu-id="81d1c-108">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="81d1c-108">Get/set</span></span>

<span data-ttu-id="81d1c-109">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span><span class="sxs-lookup"><span data-stu-id="81d1c-109">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span></span>

<span data-ttu-id="81d1c-110">Pour définir cet attribut, appelez [**IMFAttributes :: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span><span class="sxs-lookup"><span data-stu-id="81d1c-110">To set this attribute, call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span>

## <a name="remarks"></a><span data-ttu-id="81d1c-111">Notes</span><span class="sxs-lookup"><span data-stu-id="81d1c-111">Remarks</span></span>

<span data-ttu-id="81d1c-112">Cet attribut est défini sur les pointeurs [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) retournés par la fonction [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="81d1c-112">This attribute is set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="81d1c-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81d1c-113">Requirements</span></span>



| <span data-ttu-id="81d1c-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81d1c-114">Requirement</span></span> | <span data-ttu-id="81d1c-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="81d1c-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="81d1c-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81d1c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="81d1c-117">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="81d1c-117">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="81d1c-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81d1c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="81d1c-119">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="81d1c-119">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="81d1c-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="81d1c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="81d1c-121"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="81d1c-121"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81d1c-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81d1c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81d1c-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="81d1c-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="81d1c-124">Attributs de transformation</span><span class="sxs-lookup"><span data-stu-id="81d1c-124">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




