---
title: Configuration de flux Web
description: Configuration de flux Web
ms.assetid: 1eeb6243-5095-4dba-994c-2083beda7b78
keywords:
- flux, configuration de flux Web
- codecs, configuration de flux Web
- Flux Web, configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27c91c36788b858b2378ebf46b553f076c5ec490
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311013"
---
# <a name="configuring-web-streams"></a><span data-ttu-id="5f74f-106">Configuration de flux Web</span><span class="sxs-lookup"><span data-stu-id="5f74f-106">Configuring Web Streams</span></span>

<span data-ttu-id="5f74f-107">Les flux Web sont un type spécialisé de flux de transfert de fichiers utilisé pour distribuer les fichiers associés à un site Web dans un flux unique.</span><span class="sxs-lookup"><span data-stu-id="5f74f-107">Web streams are a specialized type of file transfer stream used to deliver the files associated with a Web site in a single stream.</span></span> <span data-ttu-id="5f74f-108">La configuration du flux Web est résumée dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="5f74f-108">Web stream configuration is summarized in the following table.</span></span>



| <span data-ttu-id="5f74f-109">Paramètre</span><span class="sxs-lookup"><span data-stu-id="5f74f-109">Setting</span></span>                                            | <span data-ttu-id="5f74f-110">Description</span><span class="sxs-lookup"><span data-stu-id="5f74f-110">Description</span></span>                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5f74f-111">**\_Type de média WM \_ . MajorType**</span><span class="sxs-lookup"><span data-stu-id="5f74f-111">**WM\_MEDIA\_TYPE.majortype**</span></span>                      | <span data-ttu-id="5f74f-112">Définissez sur WMMEDIATYPE \_ filetransfer.</span><span class="sxs-lookup"><span data-stu-id="5f74f-112">Set to WMMEDIATYPE\_FileTransfer.</span></span>                                                 |
| <span data-ttu-id="5f74f-113">**\_Type de média WM \_ . SubType**</span><span class="sxs-lookup"><span data-stu-id="5f74f-113">**WM\_MEDIA\_TYPE.subtype**</span></span>                        | <span data-ttu-id="5f74f-114">Définissez sur WMMEDIASUBTYPE \_ webstream.</span><span class="sxs-lookup"><span data-stu-id="5f74f-114">Set to WMMEDIASUBTYPE\_WebStream.</span></span>                                                 |
| <span data-ttu-id="5f74f-115">**\_Type de média WM \_ . bFixedSizeSamples**</span><span class="sxs-lookup"><span data-stu-id="5f74f-115">**WM\_MEDIA\_TYPE.bFixedSizeSamples**</span></span>              | <span data-ttu-id="5f74f-116">Affectez la valeur false.</span><span class="sxs-lookup"><span data-stu-id="5f74f-116">Set to False.</span></span>                                                                     |
| <span data-ttu-id="5f74f-117">**\_Type de média WM \_ . bTemporalCompression**</span><span class="sxs-lookup"><span data-stu-id="5f74f-117">**WM\_MEDIA\_TYPE.bTemporalCompression**</span></span>           | <span data-ttu-id="5f74f-118">Définissez sur True.</span><span class="sxs-lookup"><span data-stu-id="5f74f-118">Set to True.</span></span>                                                                      |
| <span data-ttu-id="5f74f-119">**\_Type de média WM \_ . lSampleSize**</span><span class="sxs-lookup"><span data-stu-id="5f74f-119">**WM\_MEDIA\_TYPE.lSampleSize**</span></span>                    | <span data-ttu-id="5f74f-120">Définit la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="5f74f-120">Set to 0.</span></span>                                                                         |
| <span data-ttu-id="5f74f-121">**\_Type de média WM \_ . formatType**</span><span class="sxs-lookup"><span data-stu-id="5f74f-121">**WM\_MEDIA\_TYPE.formattype**</span></span>                     | <span data-ttu-id="5f74f-122">Définissez sur WMFORMAT \_ webstream.</span><span class="sxs-lookup"><span data-stu-id="5f74f-122">Set to WMFORMAT\_WebStream.</span></span>                                                       |
| <span data-ttu-id="5f74f-123">**\_Type de média WM \_ . punk**</span><span class="sxs-lookup"><span data-stu-id="5f74f-123">**WM\_MEDIA\_TYPE.pUnk**</span></span>                           | <span data-ttu-id="5f74f-124">Affectez la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="5f74f-124">Set to **NULL**.</span></span>                                                                  |
| <span data-ttu-id="5f74f-125">**\_Type de média WM \_ . cbFormat**</span><span class="sxs-lookup"><span data-stu-id="5f74f-125">**WM\_MEDIA\_TYPE.cbFormat**</span></span>                       | <span data-ttu-id="5f74f-126">Défini sur `sizeof(WMT_WEBSTREAM_FORMAT)`.</span><span class="sxs-lookup"><span data-stu-id="5f74f-126">Set to `sizeof(WMT_WEBSTREAM_FORMAT)`.</span></span>                                            |
| <span data-ttu-id="5f74f-127">**\_Type de média WM \_ . pbFormat**</span><span class="sxs-lookup"><span data-stu-id="5f74f-127">**WM\_MEDIA\_TYPE.pbFormat**</span></span>                       | <span data-ttu-id="5f74f-128">Défini sur l’adresse d’une structure de **\_ \_ format de flux de diffusion en continu WMT** correctement configurée.</span><span class="sxs-lookup"><span data-stu-id="5f74f-128">Set to the address of a properly configured **WMT\_WEBSTREAM\_FORMAT** structure.</span></span> |
| <span data-ttu-id="5f74f-129">**\_Format WEBSTREAM WMT \_ . cbSampleHeaderFixedData**</span><span class="sxs-lookup"><span data-stu-id="5f74f-129">**WMT\_WEBSTREAM\_FORMAT.cbSampleHeaderFixedData**</span></span> | <span data-ttu-id="5f74f-130">Défini sur `sizeof(WMT_WEBSTREAM_SAMPLE_HEADER)`.</span><span class="sxs-lookup"><span data-stu-id="5f74f-130">Set to `sizeof(WMT_WEBSTREAM_SAMPLE_HEADER)`.</span></span>                                     |
| <span data-ttu-id="5f74f-131">**\_Format WEBSTREAM WMT \_ . wVersion**</span><span class="sxs-lookup"><span data-stu-id="5f74f-131">**WMT\_WEBSTREAM\_FORMAT.wVersion**</span></span>                | <span data-ttu-id="5f74f-132">défini sur 1.</span><span class="sxs-lookup"><span data-stu-id="5f74f-132">Set to 1.</span></span>                                                                         |
| <span data-ttu-id="5f74f-133">**\_Format WEBSTREAM WMT \_ . wReserved**</span><span class="sxs-lookup"><span data-stu-id="5f74f-133">**WMT\_WEBSTREAM\_FORMAT.wreserved**</span></span>               | <span data-ttu-id="5f74f-134">Définit la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="5f74f-134">Set to 0.</span></span>                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="5f74f-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5f74f-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f74f-136">**Configuration commune à tous les flux**</span><span class="sxs-lookup"><span data-stu-id="5f74f-136">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="5f74f-137">**Configuration de types de flux arbitraires**</span><span class="sxs-lookup"><span data-stu-id="5f74f-137">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> <dt>

[<span data-ttu-id="5f74f-138">**Flux Web**</span><span class="sxs-lookup"><span data-stu-id="5f74f-138">**Web Streams**</span></span>](web-streams.md)
</dt> </dl>

 

 




