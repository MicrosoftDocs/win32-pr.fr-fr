---
description: Spécifie une liste de vitesses de transmission et les fenêtres de mémoire tampon correspondantes pour un fichier ASF (variable bit rate).
ms.assetid: e45d055f-d404-47e9-b3c8-ac743b290138
title: Attribut MF_PD_ASF_METADATA_LEAKY_BUCKET_PAIRS (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7426d15a806a8c61c9a2ea1fdfb0565372c5f48f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533973"
---
# <a name="mf_pd_asf_metadata_leaky_bucket_pairs-attribute"></a><span data-ttu-id="e1551-103">\_Attribut des \_ \_ paires de \_ \_ compartiments avec fuite de métadonnées ASF PD \_</span><span class="sxs-lookup"><span data-stu-id="e1551-103">MF\_PD\_ASF\_METADATA\_LEAKY\_BUCKET\_PAIRS attribute</span></span>

<span data-ttu-id="e1551-104">Spécifie une liste de vitesses de transmission et les fenêtres de mémoire tampon correspondantes pour un fichier ASF (variable bit rate).</span><span class="sxs-lookup"><span data-stu-id="e1551-104">Specifies a list of bit rates and corresponding buffer windows for a variable bit rate (VBR) Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="e1551-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="e1551-105">Data type</span></span>

<span data-ttu-id="e1551-106">Tableau d’octets</span><span class="sxs-lookup"><span data-stu-id="e1551-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="e1551-107">Notes</span><span class="sxs-lookup"><span data-stu-id="e1551-107">Remarks</span></span>

<span data-ttu-id="e1551-108">Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.</span><span class="sxs-lookup"><span data-stu-id="e1551-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="e1551-109">La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) génère cet attribut qui s’applique au descripteur de présentation pour le contenu ASF.</span><span class="sxs-lookup"><span data-stu-id="e1551-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute that applies to the presentation descriptor for ASF content.</span></span>

<span data-ttu-id="e1551-110">La valeur de l’attribut a le format suivant :</span><span class="sxs-lookup"><span data-stu-id="e1551-110">The value of the attribute has the following format:</span></span>

``` syntax
struct {
    WORD wReserved;
    WM_LEAKY_BUCKET_PAIR bucket[2];
};
```

<span data-ttu-id="e1551-111">La structure de la **\_ \_ \_ paire de compartiments de fuites WM** est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="e1551-111">The **WM\_LEAKY\_BUCKET\_PAIR** structure is defined as follows:</span></span>

``` syntax
typedef struct _WMLeakyBucketPair {
  DWORD  dwBitrate;
  DWORD  msBufferWindow;
} WM_LEAKY_BUCKET_PAIR;
```

<span data-ttu-id="e1551-112">Pour chaque vitesse de transmission, le membre **msBufferWindow** indique la quantité de contenu mis en mémoire tampon avant le début de la lecture, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="e1551-112">For each bit rate, the **msBufferWindow** member indicates how much content is buffered before playback begins, in milliseconds.</span></span> <span data-ttu-id="e1551-113">La taille de la mémoire tampon en octets est égale à **msBufferWinow** x **dwBitrate** /8000.</span><span class="sxs-lookup"><span data-stu-id="e1551-113">The size of the buffer in bytes equals **msBufferWinow** x **dwBitrate** / 8000.</span></span>

> [!Note]  
> <span data-ttu-id="e1551-114">Cet attribut correspond à l’attribut **ASFLeakyBucketPairs** dans le kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e1551-114">This attribute corresponds to the **ASFLeakyBucketPairs** attribute in the Windows Media Format SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e1551-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1551-115">Requirements</span></span>



| <span data-ttu-id="e1551-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1551-116">Requirement</span></span> | <span data-ttu-id="e1551-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1551-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1551-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1551-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e1551-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e1551-119">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e1551-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1551-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e1551-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e1551-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e1551-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="e1551-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1551-123"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1551-123"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1551-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1551-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1551-125">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e1551-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e1551-126">**IMFAttributes :: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="e1551-126">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="e1551-127">**IMFAttributes :: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="e1551-127">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="e1551-128">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="e1551-128">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="e1551-129">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="e1551-129">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="e1551-130">Objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="e1551-130">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="e1551-131">Descripteurs de présentation</span><span class="sxs-lookup"><span data-stu-id="e1551-131">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




