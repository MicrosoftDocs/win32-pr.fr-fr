---
description: Spécifie la langue utilisée par un flux dans un fichier ASF (Advanced Systems Format).
ms.assetid: 834cac0a-0c84-49aa-baf2-32bae26e215b
title: Attribut MF_SD_ASF_EXTSTRMPROP_LANGUAGE_ID_INDEX (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2afcf2388d2c0641aede4ff0eaccac9178207fb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536473"
---
# <a name="mf_sd_asf_extstrmprop_language_id_index-attribute"></a><span data-ttu-id="a218a-103">MF \_ SD \_ ASF \_ EXTSTRMPROP \_ \_ ID d' \_ index de langue</span><span class="sxs-lookup"><span data-stu-id="a218a-103">MF\_SD\_ASF\_EXTSTRMPROP\_LANGUAGE\_ID\_INDEX attribute</span></span>

<span data-ttu-id="a218a-104">Spécifie la langue utilisée par un flux dans un fichier ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="a218a-104">Specifies the language used by a stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="a218a-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="a218a-105">Data type</span></span>

<span data-ttu-id="a218a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a218a-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="a218a-107">Notes</span><span class="sxs-lookup"><span data-stu-id="a218a-107">Remarks</span></span>

<span data-ttu-id="a218a-108">Cet attribut s’applique aux descripteurs de flux pour le contenu ASF.</span><span class="sxs-lookup"><span data-stu-id="a218a-108">This attribute applies to stream descriptors for ASF content.</span></span> <span data-ttu-id="a218a-109">La valeur est un index dans la liste des langues contenues dans l’attribut [**MF \_ PD \_ ASF \_ LANGLIST**](mf-pd-asf-langlist-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="a218a-109">The value is an index into the language list contained in the [**MF\_PD\_ASF\_LANGLIST**](mf-pd-asf-langlist-attribute.md) attribute.</span></span>

<span data-ttu-id="a218a-110">Cet attribut correspond au champ d’index de l’ID de langue du flux dans l’objet de propriétés de flux étendu.</span><span class="sxs-lookup"><span data-stu-id="a218a-110">This attribute corresponds to the Stream Language ID Index field in the Extended Stream Properties object.</span></span> <span data-ttu-id="a218a-111">Pour plus d’informations, reportez-vous à la spécification ASF.</span><span class="sxs-lookup"><span data-stu-id="a218a-111">For more information, refer to the ASF specification.</span></span>

<span data-ttu-id="a218a-112">La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) génère cet attribut à partir des métadonnées ASF.</span><span class="sxs-lookup"><span data-stu-id="a218a-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span> <span data-ttu-id="a218a-113">L’application peut créer le descripteur de flux du flux à partir du descripteur de présentation en appelant [**IMFPresentationDescriptor :: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span><span class="sxs-lookup"><span data-stu-id="a218a-113">The application can create the stream descriptor for the stream from the presentation descriptor by calling [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span></span>

<span data-ttu-id="a218a-114">Vous pouvez également obtenir la balise de langue en interrogeant le descripteur de flux pour l’attribut de [**\_ \_ langage SD MF**](mf-sd-language-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="a218a-114">You can also get the language tag by querying the stream descriptor for the [**MF\_SD\_LANGUAGE**](mf-sd-language-attribute.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="a218a-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a218a-115">Requirements</span></span>



| <span data-ttu-id="a218a-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a218a-116">Requirement</span></span> | <span data-ttu-id="a218a-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a218a-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a218a-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a218a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a218a-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a218a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a218a-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a218a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a218a-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a218a-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a218a-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="a218a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a218a-123"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="a218a-123"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a218a-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a218a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a218a-125">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a218a-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a218a-126">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a218a-126">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="a218a-127">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a218a-127">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="a218a-128">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="a218a-128">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="a218a-129">Attributs du descripteur de flux</span><span class="sxs-lookup"><span data-stu-id="a218a-129">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="a218a-130">Objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="a218a-130">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




