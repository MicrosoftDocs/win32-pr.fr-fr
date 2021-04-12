---
description: Permet au lecteur source d’utiliser des Media Foundation transformations (MFTs) optimisées pour le transcodage.
ms.assetid: 9463EB8C-2CA3-4F8F-8A2A-B1292879DD1B
title: Attribut MF_SOURCE_READER_ENABLE_TRANSCODE_ONLY_TRANSFORMS (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04a9559254216a102613d97824601c004c71bfd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525990"
---
# <a name="mf_source_reader_enable_transcode_only_transforms-attribute"></a><span data-ttu-id="24b66-103">L' \_ \_ attribut de \_ \_ transformation de transcodage \_ uniquement \_ des lecteurs source MF</span><span class="sxs-lookup"><span data-stu-id="24b66-103">MF\_SOURCE\_READER\_ENABLE\_TRANSCODE\_ONLY\_TRANSFORMS attribute</span></span>

<span data-ttu-id="24b66-104">Permet au [lecteur source](source-reader.md) d’utiliser des Media Foundation transformations (MFTS) optimisées pour le transcodage.</span><span class="sxs-lookup"><span data-stu-id="24b66-104">Enables the [Source Reader](source-reader.md) to use Media Foundation transforms (MFTs) that are optimized for transcoding.</span></span>

## <a name="data-type"></a><span data-ttu-id="24b66-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="24b66-105">Data type</span></span>

<span data-ttu-id="24b66-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="24b66-106">**UINT32**</span></span>

<span data-ttu-id="24b66-107">Traiter en tant que valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="24b66-107">Treat as Boolean.</span></span>

## <a name="remarks"></a><span data-ttu-id="24b66-108">Notes</span><span class="sxs-lookup"><span data-stu-id="24b66-108">Remarks</span></span>

<span data-ttu-id="24b66-109">Certains MFTs, en particulier les décodeurs, sont optimisés pour le transcodage plutôt que pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="24b66-109">Some MFTs, particularly decoders, are optimized for transcoding rather than playback.</span></span> <span data-ttu-id="24b66-110">Par défaut, le lecteur source ne chargera pas ces transformations.</span><span class="sxs-lookup"><span data-stu-id="24b66-110">By default, the Source Reader will not load such transforms.</span></span> <span data-ttu-id="24b66-111">Affectez la **valeur true** à cet attribut si vous souhaitez utiliser le transcodage MFTS avec le lecteur source.</span><span class="sxs-lookup"><span data-stu-id="24b66-111">Set this attribute to **TRUE** if you want to use transcoding MFTs with the Source Reader.</span></span>

<span data-ttu-id="24b66-112">Une application peut définir cet attribut s’il ne traite pas les données en temps réel (pour le transcodage ou des scénarios similaires).</span><span class="sxs-lookup"><span data-stu-id="24b66-112">An application might set this attribute if it does not process the data in real time (for transcoding or similar scenarios).</span></span> <span data-ttu-id="24b66-113">Dans le cas contraire, pour la lecture en temps réel, utilisez le comportement par défaut.</span><span class="sxs-lookup"><span data-stu-id="24b66-113">Otherwise, for real-time playback, use the default behavior.</span></span>

<span data-ttu-id="24b66-114">En interne, cet attribut oblige le lecteur source à inclure l’indicateur de **\_ \_ \_ transcodage \_ d’indicateur d’énumération MFT uniquement** lorsqu’il appelle [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span><span class="sxs-lookup"><span data-stu-id="24b66-114">Internally, this attribute causes the Source Reader to include the **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY** flag when it calls [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span></span>

## <a name="requirements"></a><span data-ttu-id="24b66-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="24b66-115">Requirements</span></span>



| <span data-ttu-id="24b66-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="24b66-116">Requirement</span></span> | <span data-ttu-id="24b66-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="24b66-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="24b66-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24b66-118">Minimum supported client</span></span><br/> | <span data-ttu-id="24b66-119">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="24b66-119">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="24b66-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24b66-120">Minimum supported server</span></span><br/> | <span data-ttu-id="24b66-121">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="24b66-121">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="24b66-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="24b66-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="24b66-123"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="24b66-123"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24b66-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24b66-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24b66-125">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="24b66-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="24b66-126">Lecteur source</span><span class="sxs-lookup"><span data-stu-id="24b66-126">Source Reader</span></span>](source-reader.md)
</dt> </dl>

 

 




