---
description: Spécifie si une image vidéo est endommagée.
ms.assetid: 0218F6F6-6832-445C-B733-6A99E4EA2A3B
title: Attribut MFSampleExtension_FrameCorruption (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0d3618e5d847833b539cdfa7f6f99ae784e96c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115002"
---
# <a name="mfsampleextension_framecorruption-attribute"></a><span data-ttu-id="f1723-103">\_Attribut MFSampleExtension FrameCorruption</span><span class="sxs-lookup"><span data-stu-id="f1723-103">MFSampleExtension\_FrameCorruption attribute</span></span>

<span data-ttu-id="f1723-104">Spécifie si une image vidéo est endommagée.</span><span class="sxs-lookup"><span data-stu-id="f1723-104">Specifies whether a video frame is corrupted.</span></span>

## <a name="data-type"></a><span data-ttu-id="f1723-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="f1723-105">Data type</span></span>

<span data-ttu-id="f1723-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f1723-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="f1723-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="f1723-107">Get/set</span></span>

<span data-ttu-id="f1723-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="f1723-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="f1723-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="f1723-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="f1723-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="f1723-110">Applies to</span></span>

[<span data-ttu-id="f1723-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="f1723-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="f1723-112">Notes</span><span class="sxs-lookup"><span data-stu-id="f1723-112">Remarks</span></span>

<span data-ttu-id="f1723-113">Un décodeur vidéo peut définir cet attribut sur ses échantillons de sortie.</span><span class="sxs-lookup"><span data-stu-id="f1723-113">A video decoder can set this attribute on its output samples.</span></span> <span data-ttu-id="f1723-114">Si la valeur est 1, le décodeur a détecté une altération des données dans le frame.</span><span class="sxs-lookup"><span data-stu-id="f1723-114">If the value is 1, the decoder detected data corruption in the frame.</span></span> <span data-ttu-id="f1723-115">Si la valeur est 0, il n’y a aucune altération des données, ou aucune n’a été détectée.</span><span class="sxs-lookup"><span data-stu-id="f1723-115">If the value is 0, there is no data corruption, or none was detected.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1723-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f1723-116">Requirements</span></span>



| <span data-ttu-id="f1723-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f1723-117">Requirement</span></span> | <span data-ttu-id="f1723-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1723-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f1723-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1723-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f1723-120">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f1723-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="f1723-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1723-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f1723-122">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="f1723-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="f1723-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="f1723-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1723-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1723-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1723-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1723-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1723-126">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f1723-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f1723-127">Exemples d’attributs</span><span class="sxs-lookup"><span data-stu-id="f1723-127">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="f1723-128">Exemples de supports</span><span class="sxs-lookup"><span data-stu-id="f1723-128">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




