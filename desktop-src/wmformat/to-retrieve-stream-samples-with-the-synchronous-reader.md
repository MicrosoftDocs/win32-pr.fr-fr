---
title: Pour récupérer des exemples de flux avec le lecteur synchrone
description: Pour récupérer des exemples de flux avec le lecteur synchrone
ms.assetid: d5cc4bb7-5fcf-4e1e-80dc-f03feed4dc8a
keywords:
- ASF (Advanced Systems Format), récupération d’exemples de flux
- ASF (format des systèmes avancés), récupération des exemples de flux
- ASF (Advanced Systems Format), lecteurs synchrones
- ASF (format des systèmes avancés), lecteurs synchrones
- lecteurs synchrones, récupération des exemples de flux
- flux, récupérer des exemples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7fd641dc08387606d1fdf04602e46cb9e9cbc2b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104101253"
---
# <a name="to-retrieve-stream-samples-with-the-synchronous-reader"></a><span data-ttu-id="b79f3-109">Pour récupérer des exemples de flux avec le lecteur synchrone</span><span class="sxs-lookup"><span data-stu-id="b79f3-109">To Retrieve Stream Samples with the Synchronous Reader</span></span>

<span data-ttu-id="b79f3-110">Comme pour le lecteur asynchrone, le lecteur synchrone peut récupérer des échantillons par numéro de flux.</span><span class="sxs-lookup"><span data-stu-id="b79f3-110">Like the asynchronous reader, the synchronous reader can retrieve samples by stream number.</span></span> <span data-ttu-id="b79f3-111">Contrairement au lecteur asynchrone, le lecteur synchrone peut fournir des exemples de flux, compressés ou décompressés.</span><span class="sxs-lookup"><span data-stu-id="b79f3-111">Unlike the asynchronous reader, the synchronous reader can deliver stream samples either compressed or uncompressed.</span></span>

<span data-ttu-id="b79f3-112">Pour recevoir des exemples de flux, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="b79f3-112">To receive stream samples, perform the following steps.</span></span>

1.  <span data-ttu-id="b79f3-113">À tout moment avant ou pendant la lecture, appelez [**IWMSyncReader :: SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) en passant le numéro de flux souhaité.</span><span class="sxs-lookup"><span data-stu-id="b79f3-113">Any time before or during playback, call [**IWMSyncReader::SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) passing the desired stream number.</span></span>
2.  <span data-ttu-id="b79f3-114">Récupérez des exemples avec des appels continus à [**IWMSyncReader :: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span><span class="sxs-lookup"><span data-stu-id="b79f3-114">Retrieve samples with continued calls to [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span></span>

<span data-ttu-id="b79f3-115">Vous pouvez vérifier si un flux est sélectionné pour l’exemple de remise en appelant [**IWMSyncReader :: GetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getreadstreamsamples).</span><span class="sxs-lookup"><span data-stu-id="b79f3-115">You can check whether a stream is selected for sample delivery by calling [**IWMSyncReader::GetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getreadstreamsamples).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b79f3-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b79f3-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b79f3-117">**Interface IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="b79f3-117">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="b79f3-118">**Lecture des fichiers avec le lecteur synchrone**</span><span class="sxs-lookup"><span data-stu-id="b79f3-118">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




