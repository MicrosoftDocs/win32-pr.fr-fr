---
description: Spécifie la vitesse de transmission instantanée maximale, en bits par seconde, pour un fichier ASF (Advanced Systems Format).
ms.assetid: 07e94448-13a9-4ea5-9ac7-a1e35668e0a0
title: Attribut MF_PD_ASF_FILEPROPERTIES_MAX_BITRATE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14b2c4d8b3061a0865bf3b2f3c2a4c1597c2c76f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864974"
---
# <a name="mf_pd_asf_fileproperties_max_bitrate-attribute"></a><span data-ttu-id="b0c18-103">\_Attribut de \_ Vitesse \_ de \_ \_ transmission maximale MF PD ASF FichierPropriétés</span><span class="sxs-lookup"><span data-stu-id="b0c18-103">MF\_PD\_ASF\_FILEPROPERTIES\_MAX\_BITRATE attribute</span></span>

<span data-ttu-id="b0c18-104">Spécifie la vitesse de transmission instantanée maximale, en bits par seconde, pour un fichier ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="b0c18-104">Specifies the maximum instantaneous bit rate, in bits per second, for an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="b0c18-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="b0c18-105">Data type</span></span>

<span data-ttu-id="b0c18-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b0c18-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="b0c18-107">Notes</span><span class="sxs-lookup"><span data-stu-id="b0c18-107">Remarks</span></span>

<span data-ttu-id="b0c18-108">Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.</span><span class="sxs-lookup"><span data-stu-id="b0c18-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="b0c18-109">La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) génère cet attribut à partir des métadonnées ASF.</span><span class="sxs-lookup"><span data-stu-id="b0c18-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0c18-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b0c18-110">Requirements</span></span>



| <span data-ttu-id="b0c18-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b0c18-111">Requirement</span></span> | <span data-ttu-id="b0c18-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="b0c18-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0c18-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0c18-113">Minimum supported client</span></span><br/> | <span data-ttu-id="b0c18-114">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b0c18-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b0c18-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0c18-115">Minimum supported server</span></span><br/> | <span data-ttu-id="b0c18-116">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b0c18-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b0c18-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="b0c18-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0c18-118"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0c18-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0c18-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0c18-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0c18-120">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b0c18-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b0c18-121">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="b0c18-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="b0c18-122">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="b0c18-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="b0c18-123">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="b0c18-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="b0c18-124">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="b0c18-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="b0c18-125">Objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="b0c18-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="b0c18-126">Descripteurs de présentation</span><span class="sxs-lookup"><span data-stu-id="b0c18-126">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




