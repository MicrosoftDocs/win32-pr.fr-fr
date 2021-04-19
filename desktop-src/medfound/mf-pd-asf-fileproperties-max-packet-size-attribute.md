---
description: Spécifie la taille de paquet maximale, en octets, d’un fichier ASF (Advanced Systems Format).
ms.assetid: 8dcae150-2363-47ba-b0d3-0bc182574d81
title: Attribut MF_PD_ASF_FILEPROPERTIES_MAX_PACKET_SIZE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d9c95b7511525570a9e04a33db8128f374f9472
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530110"
---
# <a name="mf_pd_asf_fileproperties_max_packet_size-attribute"></a><span data-ttu-id="5455b-103">\_Attribut de \_ \_ \_ taille maximale des \_ paquets \_ MF PD ASF</span><span class="sxs-lookup"><span data-stu-id="5455b-103">MF\_PD\_ASF\_FILEPROPERTIES\_MAX\_PACKET\_SIZE attribute</span></span>

<span data-ttu-id="5455b-104">Spécifie la taille de paquet maximale, en octets, d’un fichier ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="5455b-104">Specifies the maximum packet size, in bytes, of an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="5455b-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="5455b-105">Data type</span></span>

<span data-ttu-id="5455b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5455b-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="5455b-107">Notes</span><span class="sxs-lookup"><span data-stu-id="5455b-107">Remarks</span></span>

<span data-ttu-id="5455b-108">Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.</span><span class="sxs-lookup"><span data-stu-id="5455b-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="5455b-109">La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) génère cet attribut à partir des métadonnées ASF.</span><span class="sxs-lookup"><span data-stu-id="5455b-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="5455b-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5455b-110">Requirements</span></span>



| <span data-ttu-id="5455b-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5455b-111">Requirement</span></span> | <span data-ttu-id="5455b-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="5455b-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5455b-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5455b-113">Minimum supported client</span></span><br/> | <span data-ttu-id="5455b-114">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5455b-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5455b-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5455b-115">Minimum supported server</span></span><br/> | <span data-ttu-id="5455b-116">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5455b-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5455b-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="5455b-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="5455b-118"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="5455b-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5455b-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5455b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5455b-120">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5455b-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5455b-121">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="5455b-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="5455b-122">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="5455b-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="5455b-123">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="5455b-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="5455b-124">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="5455b-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="5455b-125">Objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="5455b-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="5455b-126">Descripteurs de présentation</span><span class="sxs-lookup"><span data-stu-id="5455b-126">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




