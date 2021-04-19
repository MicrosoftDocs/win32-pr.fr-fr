---
description: Spécifie la plage nominale des informations de couleur dans un type de média vidéo.
ms.assetid: 7b2b809e-aae4-401c-816a-626fb88f5f87
title: Attribut MF_MT_VIDEO_NOMINAL_RANGE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4539b06281655e079d9ff6ca4000e0ed75462b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527704"
---
# <a name="mf_mt_video_nominal_range-attribute"></a><span data-ttu-id="b9539-103">\_Attribut de \_ \_ plage nominale \_ de la vidéo MF MT</span><span class="sxs-lookup"><span data-stu-id="b9539-103">MF\_MT\_VIDEO\_NOMINAL\_RANGE attribute</span></span>

<span data-ttu-id="b9539-104">Spécifie la plage nominale des informations de couleur dans un type de média vidéo.</span><span class="sxs-lookup"><span data-stu-id="b9539-104">Specifies the nominal range of the color information in a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="b9539-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="b9539-105">Data type</span></span>

<span data-ttu-id="b9539-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b9539-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="b9539-107">Notes</span><span class="sxs-lookup"><span data-stu-id="b9539-107">Remarks</span></span>

<span data-ttu-id="b9539-108">La valeur de cet attribut est un membre de l’énumération [**MFNominalRange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange) .</span><span class="sxs-lookup"><span data-stu-id="b9539-108">The value of this attribute is a member of the [**MFNominalRange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange) enumeration.</span></span>

<span data-ttu-id="b9539-109">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b9539-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

<span data-ttu-id="b9539-110">**Encodeurs H. 264/AVC :**</span><span class="sxs-lookup"><span data-stu-id="b9539-110">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="b9539-111">Sur le type de média de sortie, la \_ vidéo MF Mt de \_ \_ \_ plage nominale peut être définie avec **MFNominalRange \_ 0 \_ 255** et **MFNominalRange \_ 16 \_ 235**.</span><span class="sxs-lookup"><span data-stu-id="b9539-111">On the output media type, MF\_MT\_VIDEO\_NOMINAL\_RANGE can be set with **MFNominalRange\_0\_255** and **MFNominalRange\_16\_235**.</span></span>

<span data-ttu-id="b9539-112">L’encodeur H. 264/AVC traitera **MFNominalRange \_** comme **MFNominalRange \_ 16 \_ 235**.</span><span class="sxs-lookup"><span data-stu-id="b9539-112">H.264/AVC encoder shall treat **MFNominalRange\_Unknown** as **MFNominalRange\_16\_235**.</span></span>

<span data-ttu-id="b9539-113">L’encodeur H. 264/AVC rejettera un type de support de sortie lorsque la \_ vidéo MF MT \_ \_ nominale \_ est définie sur **MFNominalRange \_ 48 \_ 208**, **MFNominalRange \_ 64 \_ 127**, ou toute autre valeur non définie sur [**MFNominalRange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange).</span><span class="sxs-lookup"><span data-stu-id="b9539-113">H.264/AVC encoder shall reject a output media type when MF\_MT\_VIDEO\_NOMINAL\_RANGE is set to **MFNominalRange\_48\_208**, **MFNominalRange\_64\_127**, or any other values not defined on [**MFNominalRange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange).</span></span>

## <a name="requirements"></a><span data-ttu-id="b9539-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b9539-114">Requirements</span></span>



| <span data-ttu-id="b9539-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b9539-115">Requirement</span></span> | <span data-ttu-id="b9539-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="b9539-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b9539-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b9539-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b9539-118">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="b9539-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="b9539-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b9539-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b9539-120">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="b9539-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="b9539-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="b9539-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9539-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9539-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9539-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9539-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9539-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b9539-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b9539-125">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="b9539-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="b9539-126">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="b9539-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="b9539-127">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="b9539-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="b9539-128">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="b9539-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="b9539-129">Informations sur les couleurs étendues</span><span class="sxs-lookup"><span data-stu-id="b9539-129">Extended Color Information</span></span>](extended-color-information.md)
</dt> </dl>

 

 




