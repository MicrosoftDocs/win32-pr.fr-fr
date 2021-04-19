---
description: Spécifie la vitesse de transmission maximale, en bits par seconde, d’un flux de données dans un fichier ASF (Advanced Systems Format).
ms.assetid: d20d374a-a259-4e89-8eeb-942bbe53e959
title: Attribut MF_SD_ASF_EXTSTRMPROP_MAX_DATA_BITRATE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85626be11afe2e9413852e8aec3533f987538473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521362"
---
# <a name="mf_sd_asf_extstrmprop_max_data_bitrate-attribute"></a><span data-ttu-id="5fc97-103">\_Attribut de \_ \_ \_ débit maximal de \_ données max. ASF EXTSTRMPROP ASF \_</span><span class="sxs-lookup"><span data-stu-id="5fc97-103">MF\_SD\_ASF\_EXTSTRMPROP\_MAX\_DATA\_BITRATE attribute</span></span>

<span data-ttu-id="5fc97-104">Spécifie la vitesse de transmission maximale, en bits par seconde, d’un flux de données dans un fichier ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="5fc97-104">Specifies the maximum data bit rate, in bits per second, of a stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="5fc97-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="5fc97-105">Data type</span></span>

<span data-ttu-id="5fc97-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5fc97-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="5fc97-107">Notes</span><span class="sxs-lookup"><span data-stu-id="5fc97-107">Remarks</span></span>

<span data-ttu-id="5fc97-108">Cet attribut s’applique aux descripteurs de flux pour le contenu ASF.</span><span class="sxs-lookup"><span data-stu-id="5fc97-108">This attribute applies to stream descriptors for ASF content.</span></span> <span data-ttu-id="5fc97-109">Elle correspond au champ autre vitesse de transmission de données dans l’objet de propriétés de flux étendu.</span><span class="sxs-lookup"><span data-stu-id="5fc97-109">It corresponds to the Alternate Data Bit Rate field in the Extended Stream Properties object.</span></span> <span data-ttu-id="5fc97-110">Pour plus d’informations, reportez-vous à la spécification ASF.</span><span class="sxs-lookup"><span data-stu-id="5fc97-110">For more information, refer to the ASF specification.</span></span>

<span data-ttu-id="5fc97-111">La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) génère cet attribut à partir des métadonnées ASF.</span><span class="sxs-lookup"><span data-stu-id="5fc97-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span> <span data-ttu-id="5fc97-112">L’application peut créer le descripteur de flux du flux à partir du descripteur de présentation en appelant [**IMFPresentationDescriptor :: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span><span class="sxs-lookup"><span data-stu-id="5fc97-112">The application can create the stream descriptor for the stream from the presentation descriptor by calling [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span></span>

## <a name="requirements"></a><span data-ttu-id="5fc97-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5fc97-113">Requirements</span></span>



| <span data-ttu-id="5fc97-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5fc97-114">Requirement</span></span> | <span data-ttu-id="5fc97-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="5fc97-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fc97-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5fc97-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5fc97-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5fc97-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5fc97-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5fc97-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5fc97-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5fc97-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5fc97-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="5fc97-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fc97-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fc97-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fc97-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5fc97-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fc97-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5fc97-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5fc97-124">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="5fc97-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="5fc97-125">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="5fc97-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="5fc97-126">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="5fc97-126">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="5fc97-127">Attributs du descripteur de flux</span><span class="sxs-lookup"><span data-stu-id="5fc97-127">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="5fc97-128">Objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="5fc97-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




