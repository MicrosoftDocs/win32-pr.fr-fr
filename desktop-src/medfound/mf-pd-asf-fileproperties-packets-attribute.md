---
description: Spécifie le nombre de paquets dans la section des données d’un fichier ASF (Advanced Systems Format).
ms.assetid: 29cf2412-0a9a-4cf5-b0c3-668204c1c352
title: Attribut MF_PD_ASF_FILEPROPERTIES_PACKETS (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a35691d2daad712e238c2b5d7d638b0ae30890f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951149"
---
# <a name="mf_pd_asf_fileproperties_packets-attribute"></a><span data-ttu-id="929db-103">\_Attribut de \_ \_ \_ paquets MF PD ASF</span><span class="sxs-lookup"><span data-stu-id="929db-103">MF\_PD\_ASF\_FILEPROPERTIES\_PACKETS attribute</span></span>

<span data-ttu-id="929db-104">Spécifie le nombre de paquets dans la section des données d’un fichier ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="929db-104">Specifies the number of packets in the data section of an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="929db-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="929db-105">Data type</span></span>

<span data-ttu-id="929db-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="929db-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="929db-107">Notes</span><span class="sxs-lookup"><span data-stu-id="929db-107">Remarks</span></span>

<span data-ttu-id="929db-108">Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.</span><span class="sxs-lookup"><span data-stu-id="929db-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="929db-109">La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) génère cet attribut à partir des métadonnées ASF.</span><span class="sxs-lookup"><span data-stu-id="929db-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="929db-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="929db-110">Requirements</span></span>



| <span data-ttu-id="929db-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="929db-111">Requirement</span></span> | <span data-ttu-id="929db-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="929db-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="929db-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="929db-113">Minimum supported client</span></span><br/> | <span data-ttu-id="929db-114">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="929db-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="929db-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="929db-115">Minimum supported server</span></span><br/> | <span data-ttu-id="929db-116">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="929db-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="929db-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="929db-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="929db-118"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="929db-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="929db-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="929db-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="929db-120">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="929db-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="929db-121">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="929db-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="929db-122">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="929db-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="929db-123">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="929db-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="929db-124">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="929db-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="929db-125">Objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="929db-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="929db-126">Descripteurs de présentation</span><span class="sxs-lookup"><span data-stu-id="929db-126">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




