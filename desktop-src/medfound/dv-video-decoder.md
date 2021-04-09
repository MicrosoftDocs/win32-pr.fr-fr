---
description: Le décodeur vidéo Media Foundation DV est une Media Foundation transformation qui décode la vidéo DV.
ms.assetid: 97e5ba52-92fc-49e4-9c22-6f61bfda2003
title: Décodeur vidéo DV
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed277c3e4dd1aaa031d4dcf4694c7c3051fe37ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749260"
---
# <a name="dv-video-decoder"></a><span data-ttu-id="4b2b0-103">Décodeur vidéo DV</span><span class="sxs-lookup"><span data-stu-id="4b2b0-103">DV Video Decoder</span></span>

<span data-ttu-id="4b2b0-104">Le décodeur vidéo Media Foundation DV est une [Media Foundation transformation](media-foundation-transforms.md) qui décode la vidéo DV.</span><span class="sxs-lookup"><span data-stu-id="4b2b0-104">The Media Foundation DV video decoder is a [Media Foundation Transform](media-foundation-transforms.md) that decodes DV video.</span></span>

<span data-ttu-id="4b2b0-105">Le décodeur vidéo DV prend en charge les types d’entrée suivants :</span><span class="sxs-lookup"><span data-stu-id="4b2b0-105">The DV video decoder supports the following input types:</span></span>



| <span data-ttu-id="4b2b0-106">Subtype</span><span class="sxs-lookup"><span data-stu-id="4b2b0-106">Subtype</span></span>                 | <span data-ttu-id="4b2b0-107">Description</span><span class="sxs-lookup"><span data-stu-id="4b2b0-107">Description</span></span>                  |
|-------------------------|------------------------------|
| <span data-ttu-id="4b2b0-108">**\_DVC MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="4b2b0-108">**MFVideoFormat\_DVC**</span></span>  | <span data-ttu-id="4b2b0-109">Vidéo DVC/DV</span><span class="sxs-lookup"><span data-stu-id="4b2b0-109">DVC/DV Video</span></span>                 |
| <span data-ttu-id="4b2b0-110">**MFVideoFormat \_ DVHD**</span><span class="sxs-lookup"><span data-stu-id="4b2b0-110">**MFVideoFormat\_DVHD**</span></span> | <span data-ttu-id="4b2b0-111">HD-magnétoscope numérique (1125-60 ou 1250-50)</span><span class="sxs-lookup"><span data-stu-id="4b2b0-111">HD-DVCR (1125-60 or 1250-50)</span></span> |
| <span data-ttu-id="4b2b0-112">**MFVideoFormat \_ DVSD**</span><span class="sxs-lookup"><span data-stu-id="4b2b0-112">**MFVideoFormat\_DVSD**</span></span> | <span data-ttu-id="4b2b0-113">SDL-magnétoscope numérique (525-60 ou 625-50)</span><span class="sxs-lookup"><span data-stu-id="4b2b0-113">SDL-DVCR (525-60 or 625-50)</span></span>  |
| <span data-ttu-id="4b2b0-114">**MFVideoFormat \_ DVSL**</span><span class="sxs-lookup"><span data-stu-id="4b2b0-114">**MFVideoFormat\_DVSL**</span></span> | <span data-ttu-id="4b2b0-115">SD-magnétoscope numérique (525-60 ou 625-50)</span><span class="sxs-lookup"><span data-stu-id="4b2b0-115">SD-DVCR (525-60 or 625-50)</span></span>   |



 

<span data-ttu-id="4b2b0-116">Il prend en charge un seul type de sortie :</span><span class="sxs-lookup"><span data-stu-id="4b2b0-116">It supports a single output type:</span></span>



| <span data-ttu-id="4b2b0-117">Subtype</span><span class="sxs-lookup"><span data-stu-id="4b2b0-117">Subtype</span></span>             | <span data-ttu-id="4b2b0-118">Description</span><span class="sxs-lookup"><span data-stu-id="4b2b0-118">Description</span></span> |
|---------------------|-------------|
| <span data-ttu-id="4b2b0-119">MFVideoFormat \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="4b2b0-119">MFVideoFormat\_YUY2</span></span> | <span data-ttu-id="4b2b0-120">Vidéo YUY2</span><span class="sxs-lookup"><span data-stu-id="4b2b0-120">YUY2 video</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="4b2b0-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4b2b0-121">Requirements</span></span>



| <span data-ttu-id="4b2b0-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4b2b0-122">Requirement</span></span> | <span data-ttu-id="4b2b0-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b2b0-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b2b0-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b2b0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4b2b0-125">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4b2b0-125">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4b2b0-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b2b0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4b2b0-127">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4b2b0-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4b2b0-128">DLL</span><span class="sxs-lookup"><span data-stu-id="4b2b0-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b2b0-129"><dt>Mfdvdec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b2b0-129"><dt>Mfdvdec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b2b0-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b2b0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b2b0-131">Objets codec</span><span class="sxs-lookup"><span data-stu-id="4b2b0-131">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="4b2b0-132">Formats multimédias pris en charge dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4b2b0-132">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="4b2b0-133">Types de média vidéo</span><span class="sxs-lookup"><span data-stu-id="4b2b0-133">Video Media Types</span></span>](video-media-types.md)
</dt> </dl>

 

 




