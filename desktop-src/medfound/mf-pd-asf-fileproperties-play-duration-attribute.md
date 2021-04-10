---
description: Spécifie le temps nécessaire pour lire un fichier ASF (Advanced Systems Format), en unités de 100 nanosecondes.
ms.assetid: 3d36808b-aa13-4205-ad92-97e951ee827e
title: Attribut MF_PD_ASF_FILEPROPERTIES_PLAY_DURATION (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac62dfbd86dfcbd001555343309568033787186b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952441"
---
# <a name="mf_pd_asf_fileproperties_play_duration-attribute"></a><span data-ttu-id="ad31a-103">\_Attribut de \_ \_ durée de \_ lecture \_ MF PD ASF</span><span class="sxs-lookup"><span data-stu-id="ad31a-103">MF\_PD\_ASF\_FILEPROPERTIES\_PLAY\_DURATION attribute</span></span>

<span data-ttu-id="ad31a-104">Spécifie le temps nécessaire pour lire un fichier ASF (Advanced Systems Format), en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="ad31a-104">Specifies the time needed to play an Advanced Systems Format (ASF) file, in 100-nanosecond units.</span></span>

<span data-ttu-id="ad31a-105">Cette valeur comprend le temps de préroll.</span><span class="sxs-lookup"><span data-stu-id="ad31a-105">This value includes the preroll time.</span></span> <span data-ttu-id="ad31a-106">Pour récupérer la durée de lecture réelle, récupérez la valeur de l’attribut de [**\_ \_ durée MF PD**](mf-pd-duration-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="ad31a-106">To retrieve the actual playback duration, get the value of the [**MF\_PD\_DURATION**](mf-pd-duration-attribute.md) attribute.</span></span> <span data-ttu-id="ad31a-107">Toutefois, si la valeur du préroll est supérieure à la durée de lecture, la valeur de la **\_ \_ durée MF** est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="ad31a-107">However, if the preroll value is greater than the play duration, the value of **MF\_PD\_DURATION** is zero.</span></span>

## <a name="data-type"></a><span data-ttu-id="ad31a-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="ad31a-108">Data type</span></span>

<span data-ttu-id="ad31a-109">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="ad31a-109">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="ad31a-110">Notes</span><span class="sxs-lookup"><span data-stu-id="ad31a-110">Remarks</span></span>

<span data-ttu-id="ad31a-111">Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.</span><span class="sxs-lookup"><span data-stu-id="ad31a-111">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="ad31a-112">La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) génère cet attribut à partir des métadonnées ASF.</span><span class="sxs-lookup"><span data-stu-id="ad31a-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="examples"></a><span data-ttu-id="ad31a-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="ad31a-113">Examples</span></span>


```C++
HRESULT GetPlayDuration(
    IMFASFContentInfo *pContentInfo,  // An initialized ContentInfo object. 
    UINT64 *pcbPlayDuration           // Receives the play duration.
    )
{
    IMFPresentationDescriptor* pPD = NULL;

    HRESULT hr = pContentInfo->GeneratePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_FILEPROPERTIES_PLAY_DURATION, pcbPlayDuration);
        pPD->Release();
    }
    return hr;
}

```



## <a name="requirements"></a><span data-ttu-id="ad31a-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad31a-114">Requirements</span></span>



| <span data-ttu-id="ad31a-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad31a-115">Requirement</span></span> | <span data-ttu-id="ad31a-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad31a-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad31a-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad31a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ad31a-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ad31a-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ad31a-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad31a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ad31a-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ad31a-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ad31a-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="ad31a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad31a-122"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad31a-122"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad31a-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad31a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad31a-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ad31a-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ad31a-125">**IMFAttributes :: GetGUID**</span><span class="sxs-lookup"><span data-stu-id="ad31a-125">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="ad31a-126">**IMFAttributes :: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="ad31a-126">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="ad31a-127">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="ad31a-127">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="ad31a-128">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="ad31a-128">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="ad31a-129">Objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="ad31a-129">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="ad31a-130">Descripteurs de présentation</span><span class="sxs-lookup"><span data-stu-id="ad31a-130">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




