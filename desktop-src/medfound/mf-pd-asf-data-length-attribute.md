---
description: Spécifie la taille, en octets, de la section de données d’un fichier ASF (Advanced Systems Format).
ms.assetid: 93a0bf27-23db-4e8a-b471-a42122e8f9aa
title: Attribut MF_PD_ASF_DATA_LENGTH (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8e62bccc594a12010cc477c241deac565d7ea62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514864"
---
# <a name="mf_pd_asf_data_length-attribute"></a><span data-ttu-id="ae20d-103">\_Attribut de \_ \_ longueur de données ASF \_ pour MF PD</span><span class="sxs-lookup"><span data-stu-id="ae20d-103">MF\_PD\_ASF\_DATA\_LENGTH attribute</span></span>

<span data-ttu-id="ae20d-104">Spécifie la taille, en octets, de la section de données d’un fichier ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="ae20d-104">Specifies the size, in bytes, of the data section of an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="ae20d-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="ae20d-105">Data type</span></span>

<span data-ttu-id="ae20d-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="ae20d-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="ae20d-107">Notes</span><span class="sxs-lookup"><span data-stu-id="ae20d-107">Remarks</span></span>

<span data-ttu-id="ae20d-108">Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.</span><span class="sxs-lookup"><span data-stu-id="ae20d-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="ae20d-109">La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) génère cet attribut à partir des métadonnées ASF.</span><span class="sxs-lookup"><span data-stu-id="ae20d-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae20d-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae20d-110">Requirements</span></span>



| <span data-ttu-id="ae20d-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae20d-111">Requirement</span></span> | <span data-ttu-id="ae20d-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae20d-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae20d-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae20d-113">Minimum supported client</span></span><br/> | <span data-ttu-id="ae20d-114">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae20d-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ae20d-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae20d-115">Minimum supported server</span></span><br/> | <span data-ttu-id="ae20d-116">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae20d-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ae20d-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="ae20d-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae20d-118"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae20d-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae20d-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae20d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae20d-120">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ae20d-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ae20d-121">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="ae20d-121">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="ae20d-122">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="ae20d-122">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="ae20d-123">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="ae20d-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="ae20d-124">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="ae20d-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="ae20d-125">Objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="ae20d-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




