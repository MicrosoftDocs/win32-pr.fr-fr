---
description: Spécifie si un fichier ASF (Advanced Systems Format) contient au moins un flux vidéo.
ms.assetid: 98411c75-519f-4ace-999f-1ea22457ed4a
title: Attribut MF_PD_ASF_INFO_HAS_VIDEO (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c1a11f672ec4063d14131946ef4e1a820cc3ee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521063"
---
# <a name="mf_pd_asf_info_has_video-attribute"></a><span data-ttu-id="5d4cf-103">MF \_ PD \_ les \_ informations ASF \_ ont un \_ attribut Video</span><span class="sxs-lookup"><span data-stu-id="5d4cf-103">MF\_PD\_ASF\_INFO\_HAS\_VIDEO attribute</span></span>

<span data-ttu-id="5d4cf-104">Spécifie si un fichier ASF (Advanced Systems Format) contient au moins un flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="5d4cf-104">Specifies whether an Advanced Systems Format (ASF) file contains at least one video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="5d4cf-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="5d4cf-105">Data type</span></span>

<span data-ttu-id="5d4cf-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5d4cf-106">**UINT32**</span></span>

<span data-ttu-id="5d4cf-107">Traiter en tant que valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="5d4cf-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d4cf-108">Notes</span><span class="sxs-lookup"><span data-stu-id="5d4cf-108">Remarks</span></span>

<span data-ttu-id="5d4cf-109">Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.</span><span class="sxs-lookup"><span data-stu-id="5d4cf-109">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="5d4cf-110">Si la valeur est **true**, le fichier a au moins un flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="5d4cf-110">If the value is **TRUE**, the file has at least one video stream.</span></span> <span data-ttu-id="5d4cf-111">Dans le cas contraire, le fichier ne contient pas de flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="5d4cf-111">Otherwise, the file does not contain any video streams.</span></span>

<span data-ttu-id="5d4cf-112">La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) génère cet attribut à partir des métadonnées ASF.</span><span class="sxs-lookup"><span data-stu-id="5d4cf-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d4cf-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d4cf-113">Requirements</span></span>



| <span data-ttu-id="5d4cf-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d4cf-114">Requirement</span></span> | <span data-ttu-id="5d4cf-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d4cf-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d4cf-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d4cf-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5d4cf-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5d4cf-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5d4cf-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d4cf-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5d4cf-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5d4cf-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5d4cf-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="5d4cf-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d4cf-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d4cf-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d4cf-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d4cf-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d4cf-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5d4cf-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5d4cf-124">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="5d4cf-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="5d4cf-125">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="5d4cf-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="5d4cf-126">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="5d4cf-126">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="5d4cf-127">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="5d4cf-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="5d4cf-128">Objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="5d4cf-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




