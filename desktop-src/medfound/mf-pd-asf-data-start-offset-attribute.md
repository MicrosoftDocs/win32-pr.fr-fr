---
description: Spécifie l’offset, en octets, entre le début d’un fichier ASF (Advanced Systems Format) et le début du premier paquet de données.
ms.assetid: 5145d952-19d9-4bf8-9046-0b5d28f5e641
title: Attribut MF_PD_ASF_DATA_START_OFFSET (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 125ae1263467afe7e0aa9017e8049b13796538fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867541"
---
# <a name="mf_pd_asf_data_start_offset-attribute"></a><span data-ttu-id="562be-103">\_Attribut de \_ décalage de \_ données ASF PD ASF \_ \_</span><span class="sxs-lookup"><span data-stu-id="562be-103">MF\_PD\_ASF\_DATA\_START\_OFFSET attribute</span></span>

<span data-ttu-id="562be-104">Spécifie l’offset, en octets, entre le début d’un fichier ASF (Advanced Systems Format) et le début du premier paquet de données.</span><span class="sxs-lookup"><span data-stu-id="562be-104">Specifies the offset, in bytes, from the start of an Advanced Systems Format (ASF) file to the start of the first data packet.</span></span>

## <a name="data-type"></a><span data-ttu-id="562be-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="562be-105">Data type</span></span>

<span data-ttu-id="562be-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="562be-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="562be-107">Notes</span><span class="sxs-lookup"><span data-stu-id="562be-107">Remarks</span></span>

<span data-ttu-id="562be-108">Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.</span><span class="sxs-lookup"><span data-stu-id="562be-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="562be-109">La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) génère cet attribut à partir des métadonnées ASF.</span><span class="sxs-lookup"><span data-stu-id="562be-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="562be-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="562be-110">Requirements</span></span>



| <span data-ttu-id="562be-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="562be-111">Requirement</span></span> | <span data-ttu-id="562be-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="562be-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="562be-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="562be-113">Minimum supported client</span></span><br/> | <span data-ttu-id="562be-114">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="562be-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="562be-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="562be-115">Minimum supported server</span></span><br/> | <span data-ttu-id="562be-116">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="562be-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="562be-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="562be-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="562be-118"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="562be-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="562be-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="562be-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="562be-120">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="562be-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="562be-121">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="562be-121">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="562be-122">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="562be-122">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="562be-123">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="562be-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="562be-124">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="562be-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="562be-125">Objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="562be-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




