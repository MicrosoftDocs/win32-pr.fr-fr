---
description: Spécifie le modèle de conformité de périphérique pour un flux dans un fichier ASF (Advanced Systems Format).
ms.assetid: e0bfb393-c8de-47cf-b80a-b0d88722e815
title: Attribut MF_SD_ASF_METADATA_DEVICE_CONFORMANCE_TEMPLATE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e0ae20ae02617fab6f9669a50c7b8383b90a9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519931"
---
# <a name="mf_sd_asf_metadata_device_conformance_template-attribute"></a><span data-ttu-id="00329-103">Attribut de modèle de conformité de l' \_ \_ \_ appareil de métadonnées SD SD ASF \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="00329-103">MF\_SD\_ASF\_METADATA\_DEVICE\_CONFORMANCE\_TEMPLATE attribute</span></span>

<span data-ttu-id="00329-104">Spécifie le modèle de conformité de périphérique pour un flux dans un fichier ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="00329-104">Specifies the device conformance template for a stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="00329-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="00329-105">Data type</span></span>

<span data-ttu-id="00329-106">Chaîne de caractères larges</span><span class="sxs-lookup"><span data-stu-id="00329-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="00329-107">Notes</span><span class="sxs-lookup"><span data-stu-id="00329-107">Remarks</span></span>

<span data-ttu-id="00329-108">Cet attribut s’applique aux descripteurs de flux pour le contenu ASF.</span><span class="sxs-lookup"><span data-stu-id="00329-108">This attribute applies to stream descriptors for ASF content.</span></span> <span data-ttu-id="00329-109">Pour plus d’informations sur les modèles de conformité des appareils, consultez la rubrique « paramètres du modèle de conformité des appareils » dans le kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="00329-109">For more information about device conformance templates, see the topic "Device Conformance Template Parameters" in the Windows Media Format SDK.</span></span>

<span data-ttu-id="00329-110">La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) génère cet attribut à partir des métadonnées ASF.</span><span class="sxs-lookup"><span data-stu-id="00329-110">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="00329-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00329-111">Requirements</span></span>



| <span data-ttu-id="00329-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="00329-112">Requirement</span></span> | <span data-ttu-id="00329-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="00329-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="00329-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00329-114">Minimum supported client</span></span><br/> | <span data-ttu-id="00329-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="00329-115">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="00329-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00329-116">Minimum supported server</span></span><br/> | <span data-ttu-id="00329-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="00329-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="00329-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="00329-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="00329-119"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="00329-119"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00329-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00329-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00329-121">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="00329-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="00329-122">**IMFAttributes :: GetString**</span><span class="sxs-lookup"><span data-stu-id="00329-122">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="00329-123">**IMFAttributes :: SetString**</span><span class="sxs-lookup"><span data-stu-id="00329-123">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="00329-124">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="00329-124">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="00329-125">Attributs du descripteur de flux</span><span class="sxs-lookup"><span data-stu-id="00329-125">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="00329-126">Objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="00329-126">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




