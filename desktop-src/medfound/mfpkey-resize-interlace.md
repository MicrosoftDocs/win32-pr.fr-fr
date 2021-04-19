---
description: Spécifie si le flux d’entrée est entrelacé.
ms.assetid: 01ee0766-06ed-4255-9057-2fe033a772cd
title: MFPKEY_RESIZE_INTERLACE, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a27504bd6da92bc48fee04afc999568a514fdef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106525001"
---
# <a name="mfpkey_resize_interlace-property"></a><span data-ttu-id="c6c39-103">\_Propriété entrelacé de REdimensionnement MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="c6c39-103">MFPKEY\_RESIZE\_INTERLACE Property</span></span>

<span data-ttu-id="c6c39-104">Spécifie si le flux d’entrée est entrelacé.</span><span class="sxs-lookup"><span data-stu-id="c6c39-104">Specifies whether the input stream is interlaced.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="c6c39-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="c6c39-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="c6c39-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="c6c39-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="c6c39-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="c6c39-107">Data Type</span></span>

<span data-ttu-id="c6c39-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="c6c39-108">VT\_BOOL</span></span>

## <a name="applies-to"></a><span data-ttu-id="c6c39-109">S'applique à</span><span class="sxs-lookup"><span data-stu-id="c6c39-109">Applies To</span></span>

-   [<span data-ttu-id="c6c39-110">Dimensionnement vidéo DSP</span><span class="sxs-lookup"><span data-stu-id="c6c39-110">Video Resizer DSP</span></span>](videoresizer.md)

## <a name="remarks"></a><span data-ttu-id="c6c39-111">Notes</span><span class="sxs-lookup"><span data-stu-id="c6c39-111">Remarks</span></span>

<span data-ttu-id="c6c39-112">Utilisez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="c6c39-112">Use one of the following values:</span></span>



| <span data-ttu-id="c6c39-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="c6c39-113">Value</span></span>     | <span data-ttu-id="c6c39-114">Description</span><span class="sxs-lookup"><span data-stu-id="c6c39-114">Description</span></span> |
|-----------|-------------|
| <span data-ttu-id="c6c39-115">VT \_ false</span><span class="sxs-lookup"><span data-stu-id="c6c39-115">VT\_FALSE</span></span> | <span data-ttu-id="c6c39-116">Progressif</span><span class="sxs-lookup"><span data-stu-id="c6c39-116">Progressive</span></span> |
| <span data-ttu-id="c6c39-117">VT \_ vrai</span><span class="sxs-lookup"><span data-stu-id="c6c39-117">VT\_TRUE</span></span>  | <span data-ttu-id="c6c39-118">Interlaced</span><span class="sxs-lookup"><span data-stu-id="c6c39-118">Interlaced</span></span>  |



 

<span data-ttu-id="c6c39-119">Si cette propriété n’est pas définie, le DSP utilise le type de média d’entrée pour déterminer si la vidéo est entrelacée.</span><span class="sxs-lookup"><span data-stu-id="c6c39-119">If this property is not set, the DSP uses the input media type to determine whether the video is interlaced.</span></span> <span data-ttu-id="c6c39-120">Vous pouvez définir cette propriété pour remplacer le paramètre de type de média.</span><span class="sxs-lookup"><span data-stu-id="c6c39-120">You can set this property to override the media type setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6c39-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c6c39-121">Requirements</span></span>



| <span data-ttu-id="c6c39-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c6c39-122">Requirement</span></span> | <span data-ttu-id="c6c39-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="c6c39-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6c39-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6c39-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c6c39-125">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c6c39-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c6c39-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6c39-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c6c39-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c6c39-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c6c39-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="c6c39-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6c39-129"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6c39-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6c39-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6c39-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6c39-131">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c6c39-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
