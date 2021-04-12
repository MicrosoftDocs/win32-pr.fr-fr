---
description: Spécifie la langue d’un flux.
ms.assetid: b64a9554-a560-4212-8964-b68ebbadc046
title: Attribut MF_SD_LANGUAGE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad13ec4d7d17e715bd2583e499c686de26c7b9da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209788"
---
# <a name="mf_sd_language-attribute"></a><span data-ttu-id="e24d3-103">\_Attribut de \_ langage SD MF</span><span class="sxs-lookup"><span data-stu-id="e24d3-103">MF\_SD\_LANGUAGE attribute</span></span>

<span data-ttu-id="e24d3-104">Spécifie la langue d’un flux.</span><span class="sxs-lookup"><span data-stu-id="e24d3-104">Specifies the language for a stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="e24d3-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="e24d3-105">Data type</span></span>

<span data-ttu-id="e24d3-106">Chaîne de caractères larges</span><span class="sxs-lookup"><span data-stu-id="e24d3-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="e24d3-107">Notes</span><span class="sxs-lookup"><span data-stu-id="e24d3-107">Remarks</span></span>

<span data-ttu-id="e24d3-108">La valeur de cet attribut est une balise de langue conforme à la norme RFC 1766.</span><span class="sxs-lookup"><span data-stu-id="e24d3-108">The value of this attribute is an RFC 1766-compliant language tag.</span></span> <span data-ttu-id="e24d3-109">Cet attribut s’applique aux descripteurs de flux.</span><span class="sxs-lookup"><span data-stu-id="e24d3-109">This attribute applies to stream descriptors.</span></span>

<span data-ttu-id="e24d3-110">Une source de média (ou tout objet qui crée un descripteur de flux) peut définir cet attribut si le flux a un langage spécifié.</span><span class="sxs-lookup"><span data-stu-id="e24d3-110">A media source (or any object that creates a stream descriptor) can set this attribute if the stream has a specified language.</span></span> <span data-ttu-id="e24d3-111">Les applications peuvent interroger cet attribut pour obtenir la langue.</span><span class="sxs-lookup"><span data-stu-id="e24d3-111">Applications can query this attribute to get the language.</span></span> <span data-ttu-id="e24d3-112">Si l’attribut n’est pas défini, le flux n’a pas de langue spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e24d3-112">If the attribute is not set, the stream does not have a specified language.</span></span>

<span data-ttu-id="e24d3-113">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="e24d3-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e24d3-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e24d3-114">Requirements</span></span>



| <span data-ttu-id="e24d3-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e24d3-115">Requirement</span></span> | <span data-ttu-id="e24d3-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e24d3-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e24d3-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e24d3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e24d3-118">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="e24d3-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="e24d3-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e24d3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e24d3-120">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="e24d3-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="e24d3-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="e24d3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e24d3-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e24d3-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e24d3-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e24d3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e24d3-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e24d3-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e24d3-125">**IMFAttributes :: GetString**</span><span class="sxs-lookup"><span data-stu-id="e24d3-125">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="e24d3-126">**IMFAttributes :: SetString**</span><span class="sxs-lookup"><span data-stu-id="e24d3-126">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="e24d3-127">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="e24d3-127">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="e24d3-128">Attributs du descripteur de flux</span><span class="sxs-lookup"><span data-stu-id="e24d3-128">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> </dl>

 

 




