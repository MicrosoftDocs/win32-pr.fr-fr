---
description: Contient un GUID de format DirectShow pour un type de média.
ms.assetid: dc532791-39e1-4acb-9e62-21d8f25be870
title: Attribut MF_MT_AM_FORMAT_TYPE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18a8faf88128075e5c5b51c1b5ace39329d4e1fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318805"
---
# <a name="mf_mt_am_format_type-attribute"></a><span data-ttu-id="215a7-103">\_Attribut de \_ \_ type de format AM MT MF \_</span><span class="sxs-lookup"><span data-stu-id="215a7-103">MF\_MT\_AM\_FORMAT\_TYPE attribute</span></span>

<span data-ttu-id="215a7-104">Contient un GUID de format DirectShow pour un type de média.</span><span class="sxs-lookup"><span data-stu-id="215a7-104">Contains a DirectShow format GUID for a media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="215a7-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="215a7-105">Data type</span></span>

<span data-ttu-id="215a7-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="215a7-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="215a7-107">Notes</span><span class="sxs-lookup"><span data-stu-id="215a7-107">Remarks</span></span>

<span data-ttu-id="215a7-108">Cet attribut peut être défini lorsqu’un type de média DirectShow est converti en Media Foundation type de média.</span><span class="sxs-lookup"><span data-stu-id="215a7-108">This attribute might be set when a DirectShow media type is converted into a Media Foundation media type.</span></span> <span data-ttu-id="215a7-109">L’attribut indique le type de format DirectShow d’origine.</span><span class="sxs-lookup"><span data-stu-id="215a7-109">The attribute indicates the original DirectShow format type.</span></span> <span data-ttu-id="215a7-110">La valeur correspond au membre formatType de la structure [**de \_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="215a7-110">The value corresponds to the formattype member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

<span data-ttu-id="215a7-111">Pour un format audio, l’attribut de [**\_ \_ \_ données utilisateur MF MT**](mf-mt-user-data-attribute.md) peut contenir le bloc de format d’origine, si le type de format DirectShow n’a pas été reconnu.</span><span class="sxs-lookup"><span data-stu-id="215a7-111">For an audio format, the [**MF\_MT\_USER\_DATA**](mf-mt-user-data-attribute.md) attribute might contain the original format block, if the DirectShow format type was not recognized.</span></span>

<span data-ttu-id="215a7-112">Ne définissez pas cet attribut sur un type de média, sauf si vous convertissez une structure de format DirectShow.</span><span class="sxs-lookup"><span data-stu-id="215a7-112">Do not set this attribute on a media type unless you are converting a DirectShow format structure.</span></span>

<span data-ttu-id="215a7-113">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="215a7-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="215a7-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="215a7-114">Requirements</span></span>



| <span data-ttu-id="215a7-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="215a7-115">Requirement</span></span> | <span data-ttu-id="215a7-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="215a7-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="215a7-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="215a7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="215a7-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="215a7-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="215a7-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="215a7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="215a7-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="215a7-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="215a7-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="215a7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="215a7-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="215a7-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="215a7-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="215a7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="215a7-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="215a7-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="215a7-125">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="215a7-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="215a7-126">Conversions de type de média</span><span class="sxs-lookup"><span data-stu-id="215a7-126">Media Type Conversions</span></span>](media-type-conversions.md)
</dt> <dt>

[<span data-ttu-id="215a7-127">Types de médias</span><span class="sxs-lookup"><span data-stu-id="215a7-127">Media Types</span></span>](media-types.md)
</dt> <dt>

[<span data-ttu-id="215a7-128">**IMFAttributes :: GetGUID**</span><span class="sxs-lookup"><span data-stu-id="215a7-128">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="215a7-129">**IMFAttributes :: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="215a7-129">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="215a7-130">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="215a7-130">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="215a7-131">**MFCreateMediaTypeFromRepresentation**</span><span class="sxs-lookup"><span data-stu-id="215a7-131">**MFCreateMediaTypeFromRepresentation**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatypefromrepresentation)
</dt> </dl>

 

 
