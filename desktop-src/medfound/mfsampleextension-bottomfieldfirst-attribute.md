---
description: Spécifie la dominante de champ pour une image vidéo entrelacée.
ms.assetid: 680c42e4-2808-46ed-98a8-c77b14a55def
title: Attribut MFSampleExtension_BottomFieldFirst (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e608160c92fa53e8cde6adee1831d6c3e8789bc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318922"
---
# <a name="mfsampleextension_bottomfieldfirst-attribute"></a><span data-ttu-id="75e9c-103">\_Attribut MFSampleExtension BottomFieldFirst</span><span class="sxs-lookup"><span data-stu-id="75e9c-103">MFSampleExtension\_BottomFieldFirst attribute</span></span>

<span data-ttu-id="75e9c-104">Spécifie la dominante de champ pour une image vidéo entrelacée.</span><span class="sxs-lookup"><span data-stu-id="75e9c-104">Specifies the field dominance for an interlaced video frame.</span></span> <span data-ttu-id="75e9c-105">Cet attribut s’applique aux exemples de supports.</span><span class="sxs-lookup"><span data-stu-id="75e9c-105">This attribute applies to media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="75e9c-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="75e9c-106">Data type</span></span>

<span data-ttu-id="75e9c-107">**Bool** stocké comme **UInt32**</span><span class="sxs-lookup"><span data-stu-id="75e9c-107">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="75e9c-108">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="75e9c-108">Get/set</span></span>

<span data-ttu-id="75e9c-109">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="75e9c-109">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="75e9c-110">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="75e9c-110">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="75e9c-111">S’applique à</span><span class="sxs-lookup"><span data-stu-id="75e9c-111">Applies to</span></span>

[<span data-ttu-id="75e9c-112">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="75e9c-112">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="75e9c-113">Notes</span><span class="sxs-lookup"><span data-stu-id="75e9c-113">Remarks</span></span>

<span data-ttu-id="75e9c-114">Si la trame vidéo est entrelacée et que l’échantillon contient deux champs entrelacés, cet attribut indique quel champ est affiché en premier.</span><span class="sxs-lookup"><span data-stu-id="75e9c-114">If the video frame is interlaced and the sample contains two interleaved fields, this attribute indicates which field is displayed first.</span></span> <span data-ttu-id="75e9c-115">Si la **valeur est true**, le champ inférieur est tout d’abord dans le temps.</span><span class="sxs-lookup"><span data-stu-id="75e9c-115">If **TRUE**, the bottom field is first in time.</span></span> <span data-ttu-id="75e9c-116">Si la **valeur est false**, le champ supérieur est tout d’abord.</span><span class="sxs-lookup"><span data-stu-id="75e9c-116">If **FALSE**, the top field is first.</span></span>

<span data-ttu-id="75e9c-117">Si le frame est entrelacé et que l’exemple contient un champ unique, cet attribut indique le champ contenu dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="75e9c-117">If the frame is interlaced and the sample contains a single field, this attribute indicates which field the sample contains.</span></span> <span data-ttu-id="75e9c-118">Si la **valeur est true**, l’exemple contient le champ du bas.</span><span class="sxs-lookup"><span data-stu-id="75e9c-118">If **TRUE**, the sample contains the bottom field.</span></span> <span data-ttu-id="75e9c-119">Si la **valeur est false**, l’exemple contient le champ supérieur.</span><span class="sxs-lookup"><span data-stu-id="75e9c-119">If **FALSE**, the sample contains the top field.</span></span>

<span data-ttu-id="75e9c-120">Si le frame est progressif, cet attribut décrit comment les champs doivent être triés lorsque la sortie est entrelacée.</span><span class="sxs-lookup"><span data-stu-id="75e9c-120">If the frame is progressive, this attribute describes how the fields should be ordered when the output is interlaced.</span></span> <span data-ttu-id="75e9c-121">Si la **valeur est true**, le champ du bas doit être généré en premier.</span><span class="sxs-lookup"><span data-stu-id="75e9c-121">If **TRUE**, the bottom field should be output first.</span></span> <span data-ttu-id="75e9c-122">Si la **valeur est false**, le champ supérieur doit être généré en premier.</span><span class="sxs-lookup"><span data-stu-id="75e9c-122">If **FALSE**, the top field should be output first.</span></span>

<span data-ttu-id="75e9c-123">Si cet attribut n’est pas défini, le type de média décrit la zone de texte dominante.</span><span class="sxs-lookup"><span data-stu-id="75e9c-123">If this attribute not set, the media type describes the field dominance.</span></span>

<span data-ttu-id="75e9c-124">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="75e9c-124">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="75e9c-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75e9c-125">Requirements</span></span>



| <span data-ttu-id="75e9c-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="75e9c-126">Requirement</span></span> | <span data-ttu-id="75e9c-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="75e9c-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="75e9c-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75e9c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="75e9c-129">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="75e9c-129">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="75e9c-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75e9c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="75e9c-131">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="75e9c-131">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="75e9c-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="75e9c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="75e9c-133"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="75e9c-133"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75e9c-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75e9c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75e9c-135">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="75e9c-135">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="75e9c-136">Exemples d’attributs</span><span class="sxs-lookup"><span data-stu-id="75e9c-136">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="75e9c-137">Exemples de supports</span><span class="sxs-lookup"><span data-stu-id="75e9c-137">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="75e9c-138">Entrelacement de vidéos</span><span class="sxs-lookup"><span data-stu-id="75e9c-138">Video Interlacing</span></span>](video-interlacing.md)
</dt> </dl>

 

 




