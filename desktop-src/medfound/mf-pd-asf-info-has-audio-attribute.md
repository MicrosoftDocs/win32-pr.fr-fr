---
description: Spécifie si un fichier ASF (Advanced Systems Format) contient des flux audio.
ms.assetid: b7c5cd67-fd2a-49d8-8de5-61783a3b4577
title: Attribut MF_PD_ASF_INFO_HAS_AUDIO (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5e2fbf9698e470af92cbd21fc5f26883dc5fd79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203865"
---
# <a name="mf_pd_asf_info_has_audio-attribute"></a><span data-ttu-id="1112c-103">MF \_ PD \_ ASF \_ info \_ a un \_ attribut audio</span><span class="sxs-lookup"><span data-stu-id="1112c-103">MF\_PD\_ASF\_INFO\_HAS\_AUDIO attribute</span></span>

<span data-ttu-id="1112c-104">Spécifie si un fichier ASF (Advanced Systems Format) contient des flux audio.</span><span class="sxs-lookup"><span data-stu-id="1112c-104">Specifies whether an Advanced Systems Format (ASF) file contains any audio streams.</span></span>

## <a name="data-type"></a><span data-ttu-id="1112c-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="1112c-105">Data type</span></span>

<span data-ttu-id="1112c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1112c-106">**UINT32**</span></span>

<span data-ttu-id="1112c-107">Traiter en tant que valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="1112c-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1112c-108">Notes</span><span class="sxs-lookup"><span data-stu-id="1112c-108">Remarks</span></span>

<span data-ttu-id="1112c-109">Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.</span><span class="sxs-lookup"><span data-stu-id="1112c-109">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="1112c-110">Si la valeur est **true**, le fichier a au moins un flux audio.</span><span class="sxs-lookup"><span data-stu-id="1112c-110">If the value is **TRUE**, the file has at least one audio stream.</span></span> <span data-ttu-id="1112c-111">Dans le cas contraire, le fichier ne contient aucun flux audio.</span><span class="sxs-lookup"><span data-stu-id="1112c-111">Otherwise, the file does not contain any audio streams.</span></span>

<span data-ttu-id="1112c-112">La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) génère cet attribut à partir des métadonnées ASF.</span><span class="sxs-lookup"><span data-stu-id="1112c-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="1112c-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1112c-113">Requirements</span></span>



| <span data-ttu-id="1112c-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1112c-114">Requirement</span></span> | <span data-ttu-id="1112c-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="1112c-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1112c-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1112c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1112c-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1112c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1112c-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1112c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1112c-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1112c-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1112c-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="1112c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1112c-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="1112c-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1112c-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1112c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1112c-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1112c-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1112c-124">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="1112c-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="1112c-125">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="1112c-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="1112c-126">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="1112c-126">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="1112c-127">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="1112c-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="1112c-128">Objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="1112c-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




