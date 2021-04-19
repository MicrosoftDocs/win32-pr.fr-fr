---
description: Spécifie comment un décodeur audio doit transformer l’audio multicanal en sortie stéréo. Ce processus est également appelé « repliable ».
ms.assetid: 6dfe2b97-1ebc-4954-b478-85b3bbba89e3
title: Attribut MF_MT_AUDIO_FOLDDOWN_MATRIX (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10bb8aa00835ab31f6c05eaa9a1d0e5d9d126b41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524550"
---
# <a name="mf_mt_audio_folddown_matrix-attribute"></a><span data-ttu-id="84acb-104">\_Attribut de \_ \_ matrice FOLDDOWN audio MF MT \_</span><span class="sxs-lookup"><span data-stu-id="84acb-104">MF\_MT\_AUDIO\_FOLDDOWN\_MATRIX attribute</span></span>

<span data-ttu-id="84acb-105">Spécifie comment un décodeur audio doit transformer l’audio multicanal en sortie stéréo.</span><span class="sxs-lookup"><span data-stu-id="84acb-105">Specifies how an audio decoder should transform multichannel audio to stereo output.</span></span> <span data-ttu-id="84acb-106">Ce processus est également appelé « *repliable »*.</span><span class="sxs-lookup"><span data-stu-id="84acb-106">This process is also called *fold-down*.</span></span>

## <a name="data-type"></a><span data-ttu-id="84acb-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="84acb-107">Data type</span></span>

<span data-ttu-id="84acb-108">Tableau d’octets</span><span class="sxs-lookup"><span data-stu-id="84acb-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="84acb-109">Notes</span><span class="sxs-lookup"><span data-stu-id="84acb-109">Remarks</span></span>

<span data-ttu-id="84acb-110">Cet attribut s’applique aux types de média audio.</span><span class="sxs-lookup"><span data-stu-id="84acb-110">This attribute applies to audio media types.</span></span>

<span data-ttu-id="84acb-111">La valeur de cet attribut est une structure de [**\_ matrice MFFOLDDOWN**](/windows/desktop/api/mfapi/ns-mfapi-mffolddown_matrix) .</span><span class="sxs-lookup"><span data-stu-id="84acb-111">The value of this attribute is an [**MFFOLDDOWN\_MATRIX**](/windows/desktop/api/mfapi/ns-mfapi-mffolddown_matrix) structure.</span></span>

<span data-ttu-id="84acb-112">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="84acb-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="84acb-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84acb-113">Requirements</span></span>



| <span data-ttu-id="84acb-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84acb-114">Requirement</span></span> | <span data-ttu-id="84acb-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="84acb-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="84acb-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84acb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="84acb-117">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="84acb-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="84acb-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84acb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="84acb-119">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="84acb-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="84acb-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="84acb-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="84acb-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="84acb-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84acb-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84acb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84acb-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="84acb-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="84acb-124">**IMFAttributes :: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="84acb-124">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="84acb-125">**IMFAttributes :: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="84acb-125">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="84acb-126">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="84acb-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="84acb-127">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="84acb-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




