---
description: Spécifie si un fichier ASF (Advanced Systems Format) contient des flux qui ne sont pas audio ou vidéo.
ms.assetid: ccd61f50-29fb-4a50-80c9-d23d71d768f3
title: Attribut MF_PD_ASF_INFO_HAS_NON_AUDIO_VIDEO (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12d1759427059494a8d0b84c64ac169ce640ab2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952439"
---
# <a name="mf_pd_asf_info_has_non_audio_video-attribute"></a><span data-ttu-id="c2810-103">MF \_ PD \_ ASF \_ info \_ a \_ un \_ \_ attribut Video non audio</span><span class="sxs-lookup"><span data-stu-id="c2810-103">MF\_PD\_ASF\_INFO\_HAS\_NON\_AUDIO\_VIDEO attribute</span></span>

<span data-ttu-id="c2810-104">Spécifie si un fichier ASF (Advanced Systems Format) contient des flux qui ne sont pas audio ou vidéo.</span><span class="sxs-lookup"><span data-stu-id="c2810-104">Specifies whether an Advanced Systems Format (ASF) file contains any streams that are not audio or video.</span></span>

## <a name="data-type"></a><span data-ttu-id="c2810-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="c2810-105">Data type</span></span>

<span data-ttu-id="c2810-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c2810-106">**UINT32**</span></span>

<span data-ttu-id="c2810-107">Traiter en tant que valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="c2810-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2810-108">Notes</span><span class="sxs-lookup"><span data-stu-id="c2810-108">Remarks</span></span>

<span data-ttu-id="c2810-109">Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.</span><span class="sxs-lookup"><span data-stu-id="c2810-109">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="c2810-110">Si la valeur est **true**, le fichier a au moins un flux qui n’est pas audio ou vidéo.</span><span class="sxs-lookup"><span data-stu-id="c2810-110">If the value is **TRUE**, the file has at least one stream that is not audio or video.</span></span> <span data-ttu-id="c2810-111">Les exemples incluent des flux d’images, des commandes de script et des données arbitraires personnalisées.</span><span class="sxs-lookup"><span data-stu-id="c2810-111">Examples include image streams, script commands, and custom arbitrary data.</span></span>

<span data-ttu-id="c2810-112">La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) génère cet attribut à partir des métadonnées ASF.</span><span class="sxs-lookup"><span data-stu-id="c2810-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2810-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2810-113">Requirements</span></span>



| <span data-ttu-id="c2810-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2810-114">Requirement</span></span> | <span data-ttu-id="c2810-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2810-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2810-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2810-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c2810-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2810-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c2810-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2810-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c2810-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2810-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c2810-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="c2810-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2810-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2810-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2810-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2810-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2810-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c2810-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c2810-124">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="c2810-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="c2810-125">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="c2810-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="c2810-126">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="c2810-126">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="c2810-127">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="c2810-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="c2810-128">Objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="c2810-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




