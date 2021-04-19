---
description: Spécifie la taille moyenne de la mémoire tampon nécessaire pour un fichier ASF (variable bit rate).
ms.assetid: 508d8670-5f5f-422b-9fa1-150115e2dbb8
title: Attribut MF_PD_ASF_METADATA_V8_BUFFERAVERAGE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3f1efcb464ee62a1f3838c1a684e3c87dc58227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519771"
---
# <a name="mf_pd_asf_metadata_v8_bufferaverage-attribute"></a><span data-ttu-id="16fd5-103">\_ \_ Attribut BUFFERAVERAGE MF PD ASF \_ Metadata \_ V8 \_</span><span class="sxs-lookup"><span data-stu-id="16fd5-103">MF\_PD\_ASF\_METADATA\_V8\_BUFFERAVERAGE attribute</span></span>

<span data-ttu-id="16fd5-104">Spécifie la taille moyenne de la mémoire tampon nécessaire pour un fichier ASF (variable bit rate).</span><span class="sxs-lookup"><span data-stu-id="16fd5-104">Specifies the average buffer size needed for a variable bit rate (VBR) Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="16fd5-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="16fd5-105">Data type</span></span>

<span data-ttu-id="16fd5-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="16fd5-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="16fd5-107">Notes</span><span class="sxs-lookup"><span data-stu-id="16fd5-107">Remarks</span></span>

<span data-ttu-id="16fd5-108">Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.</span><span class="sxs-lookup"><span data-stu-id="16fd5-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="16fd5-109">La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) génère cet attribut qui s’applique au descripteur de présentation pour le contenu ASF.</span><span class="sxs-lookup"><span data-stu-id="16fd5-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute that applies to the presentation descriptor for ASF content.</span></span>

> [!Note]  
> <span data-ttu-id="16fd5-110">Cet attribut s’applique uniquement aux fichiers créés par la version 8 du kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="16fd5-110">This attribute applies only to files created by version 8 of the Windows Media Format SDK.</span></span> <span data-ttu-id="16fd5-111">Il correspond à l’attribut **BufferAverage** dans le kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="16fd5-111">It corresponds to the **BufferAverage** attribute in the Windows Media Format SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="16fd5-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16fd5-112">Requirements</span></span>



| <span data-ttu-id="16fd5-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16fd5-113">Requirement</span></span> | <span data-ttu-id="16fd5-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="16fd5-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="16fd5-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="16fd5-115">Minimum supported client</span></span><br/> | <span data-ttu-id="16fd5-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="16fd5-116">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="16fd5-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="16fd5-117">Minimum supported server</span></span><br/> | <span data-ttu-id="16fd5-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="16fd5-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="16fd5-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="16fd5-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="16fd5-120"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="16fd5-120"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16fd5-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16fd5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16fd5-122">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="16fd5-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="16fd5-123">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="16fd5-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="16fd5-124">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="16fd5-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="16fd5-125">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="16fd5-125">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="16fd5-126">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="16fd5-126">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="16fd5-127">Objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="16fd5-127">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="16fd5-128">Descripteurs de présentation</span><span class="sxs-lookup"><span data-stu-id="16fd5-128">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




