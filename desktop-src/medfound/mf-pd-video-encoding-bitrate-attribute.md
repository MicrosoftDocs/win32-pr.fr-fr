---
description: Spécifie la vitesse de transmission de l’encodage vidéo pour la présentation, en bits par seconde. Cet attribut s’applique aux descripteurs de présentation.
ms.assetid: 0fe8cf64-2256-4e48-9853-2c734f97f3c7
title: Attribut MF_PD_VIDEO_ENCODING_BITRATE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 477d0954b4db8fa11c1540153c096e42f6d255b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544322"
---
# <a name="mf_pd_video_encoding_bitrate-attribute"></a><span data-ttu-id="a627b-104">\_Attribut de \_ \_ \_ débit binaire d’encodage vidéo MF PD</span><span class="sxs-lookup"><span data-stu-id="a627b-104">MF\_PD\_VIDEO\_ENCODING\_BITRATE attribute</span></span>

<span data-ttu-id="a627b-105">Spécifie la vitesse de transmission de l’encodage vidéo pour la présentation, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="a627b-105">Specifies the video encoding bit rate for the presentation, in bits per second.</span></span> <span data-ttu-id="a627b-106">Cet attribut s’applique aux descripteurs de présentation.</span><span class="sxs-lookup"><span data-stu-id="a627b-106">This attribute applies to presentation descriptors.</span></span>

## <a name="data-type"></a><span data-ttu-id="a627b-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="a627b-107">Data type</span></span>

<span data-ttu-id="a627b-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a627b-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="a627b-109">Notes</span><span class="sxs-lookup"><span data-stu-id="a627b-109">Remarks</span></span>

<span data-ttu-id="a627b-110">Cet attribut est facultatif.</span><span class="sxs-lookup"><span data-stu-id="a627b-110">This attribute is optional.</span></span> <span data-ttu-id="a627b-111">Certains formats ont des schémas d’encodage plus complexes qui ne peuvent pas être résumés à l’aide de cet attribut.</span><span class="sxs-lookup"><span data-stu-id="a627b-111">Some formats have more complex encoding schemes that cannot be summarized by using this attribute.</span></span> <span data-ttu-id="a627b-112">Pour les fichiers ASF (Advanced Systems Format), les attributs suivants décrivent collectivement la vitesse de transmission du codage :</span><span class="sxs-lookup"><span data-stu-id="a627b-112">For Advanced Systems Format (ASF) files, the following attributes collectively describe the encoding bit rate:</span></span>

-   [<span data-ttu-id="a627b-113">**\_vitesse de \_ \_ \_ \_ transmission maximale MF PD ASF FichierPropriétés**</span><span class="sxs-lookup"><span data-stu-id="a627b-113">**MF\_PD\_ASF\_FILEPROPERTIES\_MAX\_BITRATE**</span></span>](mf-pd-asf-fileproperties-max-bitrate-attribute.md)
-   [<span data-ttu-id="a627b-114">**\_vitesse de \_ \_ \_ transmission moyenne des \_ données EXTSTRMPROP \_ MF SD ASF**</span><span class="sxs-lookup"><span data-stu-id="a627b-114">**MF\_SD\_ASF\_EXTSTRMPROP\_AVG\_DATA\_BITRATE**</span></span>](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)
-   [<span data-ttu-id="a627b-115">**\_vitesse de \_ \_ transmission de \_ \_ données Max \_ . ASF EXTSTRMPROP ASF**</span><span class="sxs-lookup"><span data-stu-id="a627b-115">**MF\_SD\_ASF\_EXTSTRMPROP\_MAX\_DATA\_BITRATE**</span></span>](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)
-   [<span data-ttu-id="a627b-116">**\_vitesse de \_ \_ transmission de STREAMBITRATES MF SD ASF \_**</span><span class="sxs-lookup"><span data-stu-id="a627b-116">**MF\_SD\_ASF\_STREAMBITRATES\_BITRATE**</span></span>](mf-sd-asf-streambitrates-bitrate-attribute.md)

<span data-ttu-id="a627b-117">Les formats tiers peuvent utiliser d’autres attributs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="a627b-117">Third-party formats might use other custom attributes.</span></span>

<span data-ttu-id="a627b-118">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="a627b-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a627b-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a627b-119">Requirements</span></span>



| <span data-ttu-id="a627b-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a627b-120">Requirement</span></span> | <span data-ttu-id="a627b-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="a627b-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a627b-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a627b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a627b-123">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="a627b-123">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="a627b-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a627b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a627b-125">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="a627b-125">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="a627b-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="a627b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a627b-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a627b-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a627b-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a627b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a627b-129">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a627b-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a627b-130">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a627b-130">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="a627b-131">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a627b-131">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="a627b-132">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="a627b-132">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="a627b-133">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="a627b-133">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




