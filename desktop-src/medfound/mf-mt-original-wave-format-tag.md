---
description: Contient la balise WAVE format d’origine pour un flux audio.
ms.assetid: 2b30a1c2-4a42-4b09-acb6-b76267cc7ed0
title: Attribut MF_MT_ORIGINAL_WAVE_FORMAT_TAG (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba89171f9ae2bf3ab99df05bd3ae64b7d52be6d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535625"
---
# <a name="mf_mt_original_wave_format_tag-attribute"></a><span data-ttu-id="fdbee-103">\_Attribut de \_ \_ \_ balise de format Wave d’origine MF MT \_</span><span class="sxs-lookup"><span data-stu-id="fdbee-103">MF\_MT\_ORIGINAL\_WAVE\_FORMAT\_TAG attribute</span></span>

<span data-ttu-id="fdbee-104">Contient la balise WAVE format d’origine pour un flux audio.</span><span class="sxs-lookup"><span data-stu-id="fdbee-104">Contains the original WAVE format tag for an audio stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="fdbee-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="fdbee-105">Data type</span></span>

<span data-ttu-id="fdbee-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="fdbee-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="fdbee-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="fdbee-107">Get/set</span></span>

<span data-ttu-id="fdbee-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="fdbee-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="fdbee-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="fdbee-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="fdbee-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="fdbee-110">Applies to</span></span>

[<span data-ttu-id="fdbee-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="fdbee-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="fdbee-112">Notes</span><span class="sxs-lookup"><span data-stu-id="fdbee-112">Remarks</span></span>

<span data-ttu-id="fdbee-113">En fonction du fichier source, la source du média AVI peut définir cet attribut sur les types de médias qu’elle propose.</span><span class="sxs-lookup"><span data-stu-id="fdbee-113">Depending on the source file, the AVI media source might set this attribute on the media types that it offers.</span></span>

<span data-ttu-id="fdbee-114">Un fichier AVI contient un en-tête de flux pour chaque flux du fichier.</span><span class="sxs-lookup"><span data-stu-id="fdbee-114">An AVI file contains a stream header for each stream in the file.</span></span> <span data-ttu-id="fdbee-115">La source de média AVI traduit l’en-tête de flux en un type de média.</span><span class="sxs-lookup"><span data-stu-id="fdbee-115">The AVI media source translates the stream header into a media type.</span></span> <span data-ttu-id="fdbee-116">Pour les flux audio, l’en-tête de flux contient une balise de format qui identifie le format audio.</span><span class="sxs-lookup"><span data-stu-id="fdbee-116">For audio streams, the stream header contains a format tag that identifies the audio format.</span></span> <span data-ttu-id="fdbee-117">(La balise format est contenue dans le membre **wFormatTag** de la structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .) Dans la plupart des cas, la source de média AVI convertit directement la balise de format en un GUID de sous-type, comme décrit dans la rubrique GUID de sous- [**type audio**](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="fdbee-117">(The format tag is contained in the **wFormatTag** member of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.) In most cases, the AVI media source converts the format tag directly to a subtype GUID, as described in the topic [**Audio Subtype GUIDs**](audio-subtype-guids.md).</span></span> <span data-ttu-id="fdbee-118">Toutefois, dans certains cas, il mappe la balise de format d’origine à une autre balise de format équivalente.</span><span class="sxs-lookup"><span data-stu-id="fdbee-118">In some cases, however, it maps the original format tag to another format tag that is equivalent.</span></span> <span data-ttu-id="fdbee-119">Si c’est le cas, la source du média stocke la balise de format d’origine dans le type de média, à l’aide de l' \_ \_ attribut de \_ \_ balise de format Wave MF d’origine \_ .</span><span class="sxs-lookup"><span data-stu-id="fdbee-119">If so, the media source stores the original format tag in the media type, using the MF\_MT\_ORIGINAL\_WAVE\_FORMAT\_TAG attribute.</span></span>

<span data-ttu-id="fdbee-120">Les mappages de format sont stockés dans le Registre sous la clé suivante :</span><span class="sxs-lookup"><span data-stu-id="fdbee-120">The format mappings are stored in the Registry under the following key:</span></span>

<span data-ttu-id="fdbee-121">**HKEY \_ CLASSES \_ racine** \\ **MediaFoundation** \\ **MapAudioFormatTag**</span><span class="sxs-lookup"><span data-stu-id="fdbee-121">**HKEY\_CLASSES\_ROOT**\\**MediaFoundation**\\**MapAudioFormatTag**</span></span>

<span data-ttu-id="fdbee-122">Chaque entrée est une valeur **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="fdbee-122">Each entry is a **DWORD** value.</span></span> <span data-ttu-id="fdbee-123">Le nom de l’entrée est la représentation décimale de la balise de format.</span><span class="sxs-lookup"><span data-stu-id="fdbee-123">The name of the entry is the decimal representation of the format tag.</span></span> <span data-ttu-id="fdbee-124">La valeur de l’entrée correspond à la balise de format équivalente.</span><span class="sxs-lookup"><span data-stu-id="fdbee-124">The value of the entry is the equivalent format tag.</span></span>

<span data-ttu-id="fdbee-125">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="fdbee-125">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdbee-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fdbee-126">Requirements</span></span>



| <span data-ttu-id="fdbee-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fdbee-127">Requirement</span></span> | <span data-ttu-id="fdbee-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="fdbee-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fdbee-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fdbee-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fdbee-130">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fdbee-130">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fdbee-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fdbee-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fdbee-132">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fdbee-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="fdbee-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="fdbee-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdbee-134"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdbee-134"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdbee-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fdbee-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdbee-136">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fdbee-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fdbee-137">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="fdbee-137">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
