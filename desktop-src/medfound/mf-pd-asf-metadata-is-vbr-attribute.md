---
description: Spécifie si un fichier ASF (Advanced Systems Format) utilise l’encodage VBR (variable binaire rate).
ms.assetid: 69888d66-8e96-4a20-b8c5-a01267ff3c05
title: Attribut MF_PD_ASF_METADATA_IS_VBR (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5863d5366fd94e230040f81d3f67f4c75fd3fe3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530881"
---
# <a name="mf_pd_asf_metadata_is_vbr-attribute"></a><span data-ttu-id="0d451-103">Les \_ \_ métadonnées MF PD ASF \_ sont des \_ \_ attributs VBR</span><span class="sxs-lookup"><span data-stu-id="0d451-103">MF\_PD\_ASF\_METADATA\_IS\_VBR attribute</span></span>

<span data-ttu-id="0d451-104">Spécifie si un fichier ASF (Advanced Systems Format) utilise l’encodage VBR (variable binaire rate).</span><span class="sxs-lookup"><span data-stu-id="0d451-104">Specifies whether an Advanced Systems Format (ASF) file uses variable bit rate (VBR) encoding.</span></span>

## <a name="data-type"></a><span data-ttu-id="0d451-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="0d451-105">Data type</span></span>

<span data-ttu-id="0d451-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0d451-106">**UINT32**</span></span>

<span data-ttu-id="0d451-107">Traiter en tant que valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="0d451-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d451-108">Notes</span><span class="sxs-lookup"><span data-stu-id="0d451-108">Remarks</span></span>

<span data-ttu-id="0d451-109">Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.</span><span class="sxs-lookup"><span data-stu-id="0d451-109">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="0d451-110">Si la valeur est **true**, le fichier a été encodé à l’aide de VBR.</span><span class="sxs-lookup"><span data-stu-id="0d451-110">If the value is **TRUE**, the file was encoded using VBR.</span></span> <span data-ttu-id="0d451-111">Si la valeur est **false** ou si l’attribut n’est pas présent, le fichier n’utilise pas le codage VBR.</span><span class="sxs-lookup"><span data-stu-id="0d451-111">If the value is **FALSE** or the attribute is not present, the file does not use VBR encoding.</span></span>

<span data-ttu-id="0d451-112">La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) génère cet attribut et le définit sur le descripteur de présentation.</span><span class="sxs-lookup"><span data-stu-id="0d451-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute and sets it on the presentation descriptor.</span></span>

> [!Note]  
> <span data-ttu-id="0d451-113">Cet attribut correspond à l’attribut **IsVBR** dans le kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0d451-113">This attribute corresponds to the **IsVBR** attribute in the Windows Media Format SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0d451-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d451-114">Requirements</span></span>



| <span data-ttu-id="0d451-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d451-115">Requirement</span></span> | <span data-ttu-id="0d451-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d451-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d451-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d451-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0d451-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d451-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0d451-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d451-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0d451-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d451-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0d451-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="0d451-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d451-122"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d451-122"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d451-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d451-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d451-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0d451-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0d451-125">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="0d451-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="0d451-126">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="0d451-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="0d451-127">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="0d451-127">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="0d451-128">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="0d451-128">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="0d451-129">Objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="0d451-129">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="0d451-130">Descripteurs de présentation</span><span class="sxs-lookup"><span data-stu-id="0d451-130">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




