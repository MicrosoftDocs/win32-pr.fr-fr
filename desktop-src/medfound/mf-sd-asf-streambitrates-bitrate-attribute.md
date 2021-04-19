---
description: Spécifie la vitesse de transmission moyenne, en bits par seconde, d’un flux dans un fichier ASF (Advanced Systems Format). Cet attribut correspond à l’objet de propriétés de débit binaire défini dans la spécification ASF.
ms.assetid: 7ec6004f-c71b-413f-b2fd-dc03a5bf8c57
title: Attribut MF_SD_ASF_STREAMBITRATES_BITRATE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5132ba69f88ce3c0f62160e88d11a6b794b2f5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522028"
---
# <a name="mf_sd_asf_streambitrates_bitrate-attribute"></a><span data-ttu-id="33881-104">\_Attribut de \_ \_ \_ débit binaire STREAMBITRATES MF SD ASF</span><span class="sxs-lookup"><span data-stu-id="33881-104">MF\_SD\_ASF\_STREAMBITRATES\_BITRATE attribute</span></span>

<span data-ttu-id="33881-105">Spécifie la vitesse de transmission moyenne, en bits par seconde, d’un flux dans un fichier ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="33881-105">Specifies the average bit rate, in bits per second, of a stream in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="33881-106">Cet attribut correspond à l’objet de propriétés de débit binaire défini dans la spécification ASF.</span><span class="sxs-lookup"><span data-stu-id="33881-106">This attribute corresponds to the Stream Bitrate Properties Object defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="33881-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="33881-107">Data type</span></span>

<span data-ttu-id="33881-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="33881-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="33881-109">Notes</span><span class="sxs-lookup"><span data-stu-id="33881-109">Remarks</span></span>

<span data-ttu-id="33881-110">La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) génère cet attribut et le définit sur le descripteur de flux.</span><span class="sxs-lookup"><span data-stu-id="33881-110">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute and sets it on the stream descriptor.</span></span> <span data-ttu-id="33881-111">L’application peut créer le descripteur de flux du flux à partir du descripteur de présentation en appelant [**IMFPresentationDescriptor :: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span><span class="sxs-lookup"><span data-stu-id="33881-111">The application can create the stream descriptor for the stream from the presentation descriptor by calling [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span></span>

<span data-ttu-id="33881-112">La valeur de l’attribut est égale au champ vitesse de transmission moyenne de l’objet de propriétés vitesse de transmission de flux.</span><span class="sxs-lookup"><span data-stu-id="33881-112">The attribute value equals the Average Bit Rate field in the Stream Bit Rate Properties object.</span></span>

## <a name="requirements"></a><span data-ttu-id="33881-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33881-113">Requirements</span></span>



| <span data-ttu-id="33881-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33881-114">Requirement</span></span> | <span data-ttu-id="33881-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="33881-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="33881-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33881-116">Minimum supported client</span></span><br/> | <span data-ttu-id="33881-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33881-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="33881-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33881-118">Minimum supported server</span></span><br/> | <span data-ttu-id="33881-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33881-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="33881-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="33881-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="33881-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="33881-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33881-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33881-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33881-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="33881-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="33881-124">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="33881-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="33881-125">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="33881-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="33881-126">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="33881-126">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="33881-127">Attributs du descripteur de flux</span><span class="sxs-lookup"><span data-stu-id="33881-127">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="33881-128">Objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="33881-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




