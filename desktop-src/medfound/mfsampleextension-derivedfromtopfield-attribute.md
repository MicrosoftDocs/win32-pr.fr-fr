---
description: Spécifie si une image vidéo désentrelacée a été dérivée du champ supérieur ou du champ inférieur.
ms.assetid: 3710ab94-afb3-44d3-a680-b4a716810ec1
title: Attribut MFSampleExtension_DerivedFromTopField (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f90a67edf0b08337748bc118b0aa4ff024ec0ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544787"
---
# <a name="mfsampleextension_derivedfromtopfield-attribute"></a><span data-ttu-id="f049f-103">\_Attribut MFSampleExtension DerivedFromTopField</span><span class="sxs-lookup"><span data-stu-id="f049f-103">MFSampleExtension\_DerivedFromTopField attribute</span></span>

<span data-ttu-id="f049f-104">Spécifie si une image vidéo désentrelacée a été dérivée du champ supérieur ou du champ inférieur.</span><span class="sxs-lookup"><span data-stu-id="f049f-104">Specifies whether a deinterlaced video frame was derived from the upper field or the lower field.</span></span> <span data-ttu-id="f049f-105">Cet attribut s’applique aux exemples de supports.</span><span class="sxs-lookup"><span data-stu-id="f049f-105">This attribute applies to media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="f049f-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="f049f-106">Data type</span></span>

<span data-ttu-id="f049f-107">**Bool** stocké comme **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f049f-107">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="f049f-108">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="f049f-108">Get/set</span></span>

<span data-ttu-id="f049f-109">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="f049f-109">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="f049f-110">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="f049f-110">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="f049f-111">S’applique à</span><span class="sxs-lookup"><span data-stu-id="f049f-111">Applies to</span></span>

[<span data-ttu-id="f049f-112">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="f049f-112">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="f049f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="f049f-113">Remarks</span></span>

<span data-ttu-id="f049f-114">Cet attribut n’est valide que pour les exemples désentrelacés.</span><span class="sxs-lookup"><span data-stu-id="f049f-114">This attribute is valid for deinterlaced samples only.</span></span> <span data-ttu-id="f049f-115">Définissez cet attribut si le frame a été désentrelacé en interpolant l’un des champs.</span><span class="sxs-lookup"><span data-stu-id="f049f-115">Set this attribute if the frame was deinterlaced by interpolating one of the fields.</span></span>

<span data-ttu-id="f049f-116">Si la valeur est **true**, le champ inférieur a été interpolé à partir du champ supérieur.</span><span class="sxs-lookup"><span data-stu-id="f049f-116">If the value is **TRUE**, the lower field was interpolated from the upper field.</span></span> <span data-ttu-id="f049f-117">Si la valeur est **false**, le champ supérieur a été interpolé à partir du champ inférieur.</span><span class="sxs-lookup"><span data-stu-id="f049f-117">If the value is **FALSE**, the upper field was interpolated from the lower field.</span></span>

<span data-ttu-id="f049f-118">Si l’attribut n’est pas défini, le frame n’a pas été désentrelacé.</span><span class="sxs-lookup"><span data-stu-id="f049f-118">If the attribute is not set, the frame has not been deinterlaced.</span></span> <span data-ttu-id="f049f-119">Le cadre est soit une vraie image progressive, soit une image entrelacée.</span><span class="sxs-lookup"><span data-stu-id="f049f-119">The frame is either a true progressive frame, or it is an interlaced frame.</span></span>

<span data-ttu-id="f049f-120">Cet attribut est informatif.</span><span class="sxs-lookup"><span data-stu-id="f049f-120">This attribute is informational.</span></span> <span data-ttu-id="f049f-121">Un désentrelaceur logiciel peut définir cet attribut.</span><span class="sxs-lookup"><span data-stu-id="f049f-121">A software deinterlacer could set this attribute.</span></span> <span data-ttu-id="f049f-122">Si cet attribut est défini, il fournit une indication que vous pouvez récupérer le champ d’origine en supprimant les lignes de numérisation interpolées.</span><span class="sxs-lookup"><span data-stu-id="f049f-122">If this attribute is set, it provides a hint that you can recover the original field by dropping the interpolated scan lines.</span></span> <span data-ttu-id="f049f-123">Par exemple, si l’attribut a la **valeur true**, vous pouvez récupérer le champ supérieur d’origine en supprimant le champ inférieur interpolé.</span><span class="sxs-lookup"><span data-stu-id="f049f-123">For example, if the attribute is **TRUE**, you can recover the original upper field by dropping the interpolated lower field.</span></span>

<span data-ttu-id="f049f-124">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="f049f-124">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f049f-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f049f-125">Requirements</span></span>



| <span data-ttu-id="f049f-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f049f-126">Requirement</span></span> | <span data-ttu-id="f049f-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="f049f-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f049f-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f049f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f049f-129">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="f049f-129">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="f049f-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f049f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f049f-131">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="f049f-131">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="f049f-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="f049f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="f049f-133"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f049f-133"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f049f-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f049f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f049f-135">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f049f-135">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f049f-136">Exemples d’attributs</span><span class="sxs-lookup"><span data-stu-id="f049f-136">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="f049f-137">Exemples de supports</span><span class="sxs-lookup"><span data-stu-id="f049f-137">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="f049f-138">Entrelacement de vidéos</span><span class="sxs-lookup"><span data-stu-id="f049f-138">Video Interlacing</span></span>](video-interlacing.md)
</dt> </dl>

 

 




