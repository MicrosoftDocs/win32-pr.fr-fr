---
description: Spécifie si un décodeur est optimisé pour le transcodage plutôt que pour la lecture.
ms.assetid: 0e05cb05-87a8-4174-a3c6-a0a0c7765024
title: Attribut MFT_ENUM_TRANSCODE_ONLY_ATTRIBUTE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fa3349da254534605178995d493f63525a81489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393583"
---
# <a name="mft_enum_transcode_only_attribute-attribute"></a><span data-ttu-id="832b7-103">\_Attribut d' \_ attribut de transcodage d’énumération MFT \_ uniquement \_</span><span class="sxs-lookup"><span data-stu-id="832b7-103">MFT\_ENUM\_TRANSCODE\_ONLY\_ATTRIBUTE attribute</span></span>

<span data-ttu-id="832b7-104">Spécifie si un décodeur est optimisé pour le transcodage plutôt que pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="832b7-104">Specifies whether a decoder is optimized for transcoding rather than for playback.</span></span>

<span data-ttu-id="832b7-105">Actuellement, cet attribut s’applique uniquement aux décodeurs basés sur le matériel qui utilisent le mini-pilote AVStream.</span><span class="sxs-lookup"><span data-stu-id="832b7-105">Currently, this attribute applies only to hardware-based decoders that use the AVStream mini-driver.</span></span> <span data-ttu-id="832b7-106">L’attribut est stocké dans le Registre sous les informations sur les capacités du décodeur.</span><span class="sxs-lookup"><span data-stu-id="832b7-106">The attribute is stored in the registry under the decoder's capabilities information.</span></span> <span data-ttu-id="832b7-107">Pour plus d’informations, consultez la documentation de [**IGetCapabilitiesKey**](/windows/win32/api/strmif/nn-strmif-igetcapabilitieskey).</span><span class="sxs-lookup"><span data-stu-id="832b7-107">For more information, see the documentation for [**IGetCapabilitiesKey**](/windows/win32/api/strmif/nn-strmif-igetcapabilitieskey).</span></span>

<span data-ttu-id="832b7-108">En général, les applications n’utilisent pas cet attribut.</span><span class="sxs-lookup"><span data-stu-id="832b7-108">Applications typically do not use this attribute.</span></span>

## <a name="data-type"></a><span data-ttu-id="832b7-109">Type de données</span><span class="sxs-lookup"><span data-stu-id="832b7-109">Data type</span></span>

<span data-ttu-id="832b7-110">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="832b7-110">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="832b7-111">Notes</span><span class="sxs-lookup"><span data-stu-id="832b7-111">Remarks</span></span>

<span data-ttu-id="832b7-112">Si cette entrée de Registre est présente et égale à 1, la fonction [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) ignore le décodeur, à moins que l’appelant ne spécifie l’indicateur de **\_ \_ \_ décodage \_ d’indicateur d’enum MFT only** dans MFTEnumEx.</span><span class="sxs-lookup"><span data-stu-id="832b7-112">If this registry entry is present and equal to 1, the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function skips the decoder unless the caller specified the **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY** flag in **MFTEnumEx**.</span></span>

<span data-ttu-id="832b7-113">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="832b7-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="832b7-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="832b7-114">Requirements</span></span>



| <span data-ttu-id="832b7-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="832b7-115">Requirement</span></span> | <span data-ttu-id="832b7-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="832b7-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="832b7-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="832b7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="832b7-118">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="832b7-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="832b7-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="832b7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="832b7-120">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="832b7-120">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="832b7-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="832b7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="832b7-122"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="832b7-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="832b7-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="832b7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="832b7-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="832b7-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="832b7-125">**MFTEnumEx**</span><span class="sxs-lookup"><span data-stu-id="832b7-125">**MFTEnumEx**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
</dt> </dl>

 

 
