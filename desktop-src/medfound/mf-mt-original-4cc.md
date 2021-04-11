---
description: Contient le FOURCC du codec d’origine pour un flux vidéo.
ms.assetid: 2e6ef198-5754-4ded-9fe3-61edd0742a17
title: Attribut MF_MT_ORIGINAL_4CC (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b374ba3ef74cb98925edcc5d809e1fd5e0b7fbcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952660"
---
# <a name="mf_mt_original_4cc-attribute"></a><span data-ttu-id="15f3b-103">\_ \_ Attribut 4cc d’origine MF MT \_</span><span class="sxs-lookup"><span data-stu-id="15f3b-103">MF\_MT\_ORIGINAL\_4CC attribute</span></span>

<span data-ttu-id="15f3b-104">Contient le FOURCC du codec d’origine pour un flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="15f3b-104">Contains the original codec FOURCC for a video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="15f3b-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="15f3b-105">Data type</span></span>

<span data-ttu-id="15f3b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="15f3b-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="15f3b-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="15f3b-107">Get/set</span></span>

<span data-ttu-id="15f3b-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="15f3b-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="15f3b-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="15f3b-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="15f3b-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="15f3b-110">Applies to</span></span>

[<span data-ttu-id="15f3b-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="15f3b-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="15f3b-112">Notes</span><span class="sxs-lookup"><span data-stu-id="15f3b-112">Remarks</span></span>

<span data-ttu-id="15f3b-113">En fonction du fichier source, la source du média AVI peut définir cet attribut sur les types de médias qu’elle propose.</span><span class="sxs-lookup"><span data-stu-id="15f3b-113">Depending on the source file, the AVI media source might set this attribute on the media types that it offers.</span></span>

<span data-ttu-id="15f3b-114">Un fichier AVI contient un en-tête de flux pour chaque flux du fichier.</span><span class="sxs-lookup"><span data-stu-id="15f3b-114">An AVI file contains a stream header for each stream in the file.</span></span> <span data-ttu-id="15f3b-115">La source de média AVI traduit l’en-tête de flux en un type de média.</span><span class="sxs-lookup"><span data-stu-id="15f3b-115">The AVI media source translates the stream header into a media type.</span></span> <span data-ttu-id="15f3b-116">Pour les flux vidéo compressés, l’en-tête de flux contient un FOURCC qui identifie le codec vidéo.</span><span class="sxs-lookup"><span data-stu-id="15f3b-116">For compressed video streams, the stream header contains a FOURCC that identifies the video codec.</span></span> <span data-ttu-id="15f3b-117">Dans la plupart des cas, la source de média AVI convertit ce FOURCC directement en un GUID de sous-type, comme décrit dans la rubrique GUID de sous- [type de vidéo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="15f3b-117">In most cases, the AVI media source converts this FOURCC directly to a subtype GUID, as described in the topic [Video Subtype GUIDs](video-subtype-guids.md).</span></span> <span data-ttu-id="15f3b-118">Toutefois, dans certains cas, il mappe le FOURCC d’origine à un autre FOURCC équivalent.</span><span class="sxs-lookup"><span data-stu-id="15f3b-118">In some cases, however, it maps the original FOURCC to another FOURCC that is equivalent.</span></span> <span data-ttu-id="15f3b-119">Si c’est le cas, la source du média stocke le FOURCC d’origine dans le type de média, à l’aide de l' \_ \_ attribut 4cc d’origine MF MT \_ .</span><span class="sxs-lookup"><span data-stu-id="15f3b-119">If so, the media source stores the original FOURCC in the media type, using the MF\_MT\_ORIGINAL\_4CC attribute.</span></span>

<span data-ttu-id="15f3b-120">Les mappages FOURCC sont stockés dans le Registre sous la clé suivante :</span><span class="sxs-lookup"><span data-stu-id="15f3b-120">The FOURCC mappings are stored in the Registry under the following key:</span></span>

<span data-ttu-id="15f3b-121">**HKEY \_ CLASSES \_ racine** \\ **MediaFoundation** \\ **MapVideo4cc**</span><span class="sxs-lookup"><span data-stu-id="15f3b-121">**HKEY\_CLASSES\_ROOT**\\**MediaFoundation**\\**MapVideo4cc**</span></span>

<span data-ttu-id="15f3b-122">Chaque entrée est une valeur **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="15f3b-122">Each entry is a **DWORD** value.</span></span> <span data-ttu-id="15f3b-123">Le nom de l’entrée est la représentation hexadécimale du FOURCC, sans préfixe « 0x », et le premier caractère apparaissant en premier dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="15f3b-123">The name of the entry is the hexadecimal representation of the FOURCC, without an "0x" prefix, and with the first character appearing first in the string.</span></span> <span data-ttu-id="15f3b-124">Par exemple, le code FOURCC « ABCD » apparaît sous la forme « 61626364 ».</span><span class="sxs-lookup"><span data-stu-id="15f3b-124">For example, the FOURCC code 'abcd' would appear as "61626364".</span></span> <span data-ttu-id="15f3b-125">La valeur de l’entrée est le code FOURCC équivalent.</span><span class="sxs-lookup"><span data-stu-id="15f3b-125">The value of the entry is the equivalent FOURCC code.</span></span>

<span data-ttu-id="15f3b-126">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="15f3b-126">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="15f3b-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="15f3b-127">Requirements</span></span>



| <span data-ttu-id="15f3b-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="15f3b-128">Requirement</span></span> | <span data-ttu-id="15f3b-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="15f3b-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="15f3b-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15f3b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="15f3b-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15f3b-131">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="15f3b-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15f3b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="15f3b-133">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15f3b-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="15f3b-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="15f3b-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="15f3b-135"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="15f3b-135"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15f3b-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15f3b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15f3b-137">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="15f3b-137">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="15f3b-138">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="15f3b-138">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




