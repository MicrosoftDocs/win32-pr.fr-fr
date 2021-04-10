---
description: Spécifie la date et l’heure de création d’un fichier ASF (Advanced Systems Format).
ms.assetid: 97f80584-9d74-4ba5-80f4-ddb6f2bc4625
title: Attribut MF_PD_ASF_FILEPROPERTIES_CREATION_TIME (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0f48f251f5ff9c7332de0e355c58782ed98fad0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951150"
---
# <a name="mf_pd_asf_fileproperties_creation_time-attribute"></a><span data-ttu-id="686d8-103">\_Attribut de \_ \_ Date de \_ création \_ MF PD ASF</span><span class="sxs-lookup"><span data-stu-id="686d8-103">MF\_PD\_ASF\_FILEPROPERTIES\_CREATION\_TIME attribute</span></span>

<span data-ttu-id="686d8-104">Spécifie la date et l’heure de création d’un fichier ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="686d8-104">Specifies the date and time when an Advanced Systems Format (ASF) file was created.</span></span>

## <a name="data-type"></a><span data-ttu-id="686d8-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="686d8-105">Data type</span></span>

<span data-ttu-id="686d8-106">Tableau d’octets</span><span class="sxs-lookup"><span data-stu-id="686d8-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="686d8-107">Notes</span><span class="sxs-lookup"><span data-stu-id="686d8-107">Remarks</span></span>

<span data-ttu-id="686d8-108">Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.</span><span class="sxs-lookup"><span data-stu-id="686d8-108">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="686d8-109">La valeur de l’attribut est une structure **fileTime** , qui est documentée dans la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="686d8-109">The value of the attribute is a **FILETIME** structure, which is documented in the Windows SDK.</span></span>

<span data-ttu-id="686d8-110">La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) génère cet attribut à partir des métadonnées ASF.</span><span class="sxs-lookup"><span data-stu-id="686d8-110">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="686d8-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="686d8-111">Requirements</span></span>



| <span data-ttu-id="686d8-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="686d8-112">Requirement</span></span> | <span data-ttu-id="686d8-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="686d8-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="686d8-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="686d8-114">Minimum supported client</span></span><br/> | <span data-ttu-id="686d8-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="686d8-115">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="686d8-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="686d8-116">Minimum supported server</span></span><br/> | <span data-ttu-id="686d8-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="686d8-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="686d8-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="686d8-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="686d8-119"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="686d8-119"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="686d8-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="686d8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="686d8-121">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="686d8-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="686d8-122">**IMFAttributes :: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="686d8-122">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="686d8-123">**IMFAttributes :: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="686d8-123">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="686d8-124">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="686d8-124">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="686d8-125">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="686d8-125">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="686d8-126">Objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="686d8-126">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="686d8-127">Descripteurs de présentation</span><span class="sxs-lookup"><span data-stu-id="686d8-127">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




