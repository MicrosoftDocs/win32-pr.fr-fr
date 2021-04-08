---
description: Spécifie si le flux d’entrée est entrelacé.
ms.assetid: d0d93151-5b0d-44a7-8497-f11b3e23a031
title: MFPKEY_COLORCONV_MODE, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd8c01a6dce595eb270b734947492deea014259
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755493"
---
# <a name="mfpkey_colorconv_mode-property"></a><span data-ttu-id="06c8c-103">MFPKEY \_ \_ propriété mode COLORCONV</span><span class="sxs-lookup"><span data-stu-id="06c8c-103">MFPKEY\_COLORCONV\_MODE Property</span></span>

<span data-ttu-id="06c8c-104">Spécifie si le flux d’entrée est entrelacé.</span><span class="sxs-lookup"><span data-stu-id="06c8c-104">Specifies whether the input stream is interlaced.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="06c8c-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="06c8c-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="06c8c-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="06c8c-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="06c8c-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="06c8c-107">Data Type</span></span>

<span data-ttu-id="06c8c-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="06c8c-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="06c8c-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="06c8c-109">Default Value</span></span>

<span data-ttu-id="06c8c-110">Calculé par le DSP à partir de la vidéo source.</span><span class="sxs-lookup"><span data-stu-id="06c8c-110">Computed by the DSP from the source video.</span></span>

## <a name="applies-to"></a><span data-ttu-id="06c8c-111">S'applique à</span><span class="sxs-lookup"><span data-stu-id="06c8c-111">Applies To</span></span>

-   [<span data-ttu-id="06c8c-112">Convertisseur de couleurs DSP</span><span class="sxs-lookup"><span data-stu-id="06c8c-112">Color Converter DSP</span></span>](colorconverter.md)

## <a name="remarks"></a><span data-ttu-id="06c8c-113">Notes</span><span class="sxs-lookup"><span data-stu-id="06c8c-113">Remarks</span></span>

<span data-ttu-id="06c8c-114">Utilisez l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="06c8c-114">Use one of the following values.</span></span>



| <span data-ttu-id="06c8c-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="06c8c-115">Value</span></span> | <span data-ttu-id="06c8c-116">Description</span><span class="sxs-lookup"><span data-stu-id="06c8c-116">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="06c8c-117">0</span><span class="sxs-lookup"><span data-stu-id="06c8c-117">0</span></span>     | <span data-ttu-id="06c8c-118">Progressif</span><span class="sxs-lookup"><span data-stu-id="06c8c-118">Progressive</span></span> |
| <span data-ttu-id="06c8c-119">2</span><span class="sxs-lookup"><span data-stu-id="06c8c-119">2</span></span>     | <span data-ttu-id="06c8c-120">Interlaced</span><span class="sxs-lookup"><span data-stu-id="06c8c-120">Interlaced</span></span>  |



 

<span data-ttu-id="06c8c-121">Si cette propriété n’est pas définie, le DSP utilise le type de média d’entrée pour déterminer si la vidéo est entrelacée.</span><span class="sxs-lookup"><span data-stu-id="06c8c-121">If this property is not set, the DSP uses the input media type to determine whether the video is interlaced.</span></span> <span data-ttu-id="06c8c-122">Vous pouvez définir cette propriété pour remplacer le paramètre de type de média.</span><span class="sxs-lookup"><span data-stu-id="06c8c-122">You can set this property to override the media type setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="06c8c-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06c8c-123">Requirements</span></span>



| <span data-ttu-id="06c8c-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06c8c-124">Requirement</span></span> | <span data-ttu-id="06c8c-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="06c8c-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="06c8c-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06c8c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="06c8c-127">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06c8c-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="06c8c-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06c8c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="06c8c-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06c8c-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="06c8c-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="06c8c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="06c8c-131"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="06c8c-131"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06c8c-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06c8c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06c8c-133">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="06c8c-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
