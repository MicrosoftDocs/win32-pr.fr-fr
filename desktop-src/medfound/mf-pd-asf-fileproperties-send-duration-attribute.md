---
description: Spécifie la durée, en unités de 100 nanosecondes, nécessaire pour envoyer un fichier ASF (Advanced Systems Format). L’heure d’envoi d’un paquet est l’heure à laquelle le paquet doit être remis sur le réseau. Il ne s’agit pas de l’heure de présentation du paquet.
ms.assetid: 2bd427e2-106d-4997-86aa-fae221e429eb
title: Attribut MF_PD_ASF_FILEPROPERTIES_SEND_DURATION (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: deed3f78208a0f0c7e555e8113f05ac0800cdb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524330"
---
# <a name="mf_pd_asf_fileproperties_send_duration-attribute"></a><span data-ttu-id="59717-105">\_Attribut de \_ \_ durée d' \_ envoi \_ MF PD ASF</span><span class="sxs-lookup"><span data-stu-id="59717-105">MF\_PD\_ASF\_FILEPROPERTIES\_SEND\_DURATION attribute</span></span>

<span data-ttu-id="59717-106">Spécifie la durée, en unités de 100 nanosecondes, nécessaire pour envoyer un fichier ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="59717-106">Specifies the time, in 100-nanosecond units, needed to send an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="59717-107">L’heure d' *envoi* d’un paquet est l’heure à laquelle le paquet doit être remis sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="59717-107">A packet's *send time* is the time when the packet should be delivered over the network.</span></span> <span data-ttu-id="59717-108">Il ne s’agit pas de l’heure de présentation du paquet.</span><span class="sxs-lookup"><span data-stu-id="59717-108">It is not the presentation time of the packet.</span></span>

## <a name="data-type"></a><span data-ttu-id="59717-109">Type de données</span><span class="sxs-lookup"><span data-stu-id="59717-109">Data type</span></span>

<span data-ttu-id="59717-110">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="59717-110">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="59717-111">Notes</span><span class="sxs-lookup"><span data-stu-id="59717-111">Remarks</span></span>

<span data-ttu-id="59717-112">Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.</span><span class="sxs-lookup"><span data-stu-id="59717-112">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="59717-113">La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) génère cet attribut à partir des métadonnées ASF.</span><span class="sxs-lookup"><span data-stu-id="59717-113">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="59717-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59717-114">Requirements</span></span>



| <span data-ttu-id="59717-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59717-115">Requirement</span></span> | <span data-ttu-id="59717-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="59717-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="59717-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59717-117">Minimum supported client</span></span><br/> | <span data-ttu-id="59717-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59717-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="59717-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59717-119">Minimum supported server</span></span><br/> | <span data-ttu-id="59717-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59717-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="59717-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="59717-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="59717-122"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="59717-122"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59717-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59717-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59717-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="59717-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="59717-125">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="59717-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="59717-126">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="59717-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="59717-127">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="59717-127">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="59717-128">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="59717-128">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="59717-129">Objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="59717-129">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="59717-130">Descripteurs de présentation</span><span class="sxs-lookup"><span data-stu-id="59717-130">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




