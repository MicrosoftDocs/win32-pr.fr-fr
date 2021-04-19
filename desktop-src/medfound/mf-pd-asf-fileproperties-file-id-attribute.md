---
description: Spécifie l’identificateur de fichier d’un fichier ASF (Advanced Systems Format).
ms.assetid: 096c2e1a-7fd7-49ab-aa24-7d7c779d9e79
title: Attribut MF_PD_ASF_FILEPROPERTIES_FILE_ID (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a92d20351c11df4feebd732c670cbacabf3bd67f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544757"
---
# <a name="mf_pd_asf_fileproperties_file_id-attribute"></a><span data-ttu-id="b195a-103">MF \_ PD \_ ASF \_ - \_ attribut de fichier d’ID de fichier \_</span><span class="sxs-lookup"><span data-stu-id="b195a-103">MF\_PD\_ASF\_FILEPROPERTIES\_FILE\_ID attribute</span></span>

<span data-ttu-id="b195a-104">Spécifie l’identificateur de fichier d’un fichier ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="b195a-104">Specifies the file identifier of an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="b195a-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="b195a-105">Data type</span></span>

<span data-ttu-id="b195a-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="b195a-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="b195a-107">Notes</span><span class="sxs-lookup"><span data-stu-id="b195a-107">Remarks</span></span>

<span data-ttu-id="b195a-108">Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.</span><span class="sxs-lookup"><span data-stu-id="b195a-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="b195a-109">La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) génère cet attribut à partir des métadonnées ASF.</span><span class="sxs-lookup"><span data-stu-id="b195a-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="b195a-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b195a-110">Requirements</span></span>



| <span data-ttu-id="b195a-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b195a-111">Requirement</span></span> | <span data-ttu-id="b195a-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="b195a-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b195a-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b195a-113">Minimum supported client</span></span><br/> | <span data-ttu-id="b195a-114">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b195a-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b195a-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b195a-115">Minimum supported server</span></span><br/> | <span data-ttu-id="b195a-116">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b195a-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b195a-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="b195a-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="b195a-118"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="b195a-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b195a-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b195a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b195a-120">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b195a-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b195a-121">**IMFAttributes :: GetGUID**</span><span class="sxs-lookup"><span data-stu-id="b195a-121">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="b195a-122">**IMFAttributes :: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="b195a-122">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="b195a-123">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="b195a-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="b195a-124">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="b195a-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="b195a-125">Objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="b195a-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="b195a-126">Descripteurs de présentation</span><span class="sxs-lookup"><span data-stu-id="b195a-126">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




