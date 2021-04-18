---
description: Spécifie la durée, en millisecondes, de la mise en mémoire tampon des données avant la diffusion d’un fichier ASF (Advanced Systems Format).
ms.assetid: 6aebe1cf-bd45-4b02-a3c8-6599bb683d7c
title: Attribut MF_PD_ASF_FILEPROPERTIES_PREROLL (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 502ba715cc2802f9710d579e0c7afd6477b83454
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203867"
---
# <a name="mf_pd_asf_fileproperties_preroll-attribute"></a><span data-ttu-id="f9044-103">\_Attribut de \_ \_ \_ préroll ASF pour MF PD ASF</span><span class="sxs-lookup"><span data-stu-id="f9044-103">MF\_PD\_ASF\_FILEPROPERTIES\_PREROLL attribute</span></span>

<span data-ttu-id="f9044-104">Spécifie la durée, en millisecondes, de la mise en mémoire tampon des données avant la diffusion d’un fichier ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="f9044-104">Specifies the amount of time, in milliseconds, to buffer data before playing an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="f9044-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="f9044-105">Data type</span></span>

<span data-ttu-id="f9044-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="f9044-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="f9044-107">Notes</span><span class="sxs-lookup"><span data-stu-id="f9044-107">Remarks</span></span>

<span data-ttu-id="f9044-108">Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.</span><span class="sxs-lookup"><span data-stu-id="f9044-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="f9044-109">La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) génère cet attribut à partir des métadonnées ASF.</span><span class="sxs-lookup"><span data-stu-id="f9044-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9044-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9044-110">Requirements</span></span>



| <span data-ttu-id="f9044-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9044-111">Requirement</span></span> | <span data-ttu-id="f9044-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9044-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9044-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9044-113">Minimum supported client</span></span><br/> | <span data-ttu-id="f9044-114">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9044-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f9044-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9044-115">Minimum supported server</span></span><br/> | <span data-ttu-id="f9044-116">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9044-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f9044-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="f9044-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9044-118"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9044-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9044-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9044-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9044-120">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f9044-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f9044-121">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="f9044-121">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="f9044-122">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="f9044-122">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="f9044-123">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="f9044-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="f9044-124">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="f9044-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="f9044-125">Objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="f9044-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="f9044-126">Descripteurs de présentation</span><span class="sxs-lookup"><span data-stu-id="f9044-126">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




