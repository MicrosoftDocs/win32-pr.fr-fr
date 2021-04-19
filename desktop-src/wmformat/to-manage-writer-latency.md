---
title: Pour gérer la latence de l’enregistreur
description: Pour gérer la latence de l’enregistreur
ms.assetid: 62ec3f25-5cd9-499e-9579-00e00086df7f
keywords:
- ASF (Advanced Systems Format), gestion de la latence de l’enregistreur
- ASF (format de systèmes avancés), gestion de la latence de l’enregistreur
- ASF (Advanced Systems Format), latence de l’enregistreur
- ASF (format de systèmes avancés), latence de l’enregistreur
- latence de l’enregistreur
- latency
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3260be03344f1bf13252007b10614746ceda3e96
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106509833"
---
# <a name="to-manage-writer-latency"></a><span data-ttu-id="4a75a-109">Pour gérer la latence de l’enregistreur</span><span class="sxs-lookup"><span data-stu-id="4a75a-109">To Manage Writer Latency</span></span>

<span data-ttu-id="4a75a-110">Il faut du temps pour que l’enregistreur traite les exemples.</span><span class="sxs-lookup"><span data-stu-id="4a75a-110">It takes time for the writer to process samples.</span></span> <span data-ttu-id="4a75a-111">La durée entre le passage d’un exemple d’entrée et l’écriture d’un échantillon de sortie est appelée la latence du writer.</span><span class="sxs-lookup"><span data-stu-id="4a75a-111">The amount of time between passing an input sample and the writing of an output sample is called the latency of the writer.</span></span> <span data-ttu-id="4a75a-112">Un certain nombre de facteurs contribuent à la latence de l’enregistreur et vous pouvez le réduire de plusieurs façons.</span><span class="sxs-lookup"><span data-stu-id="4a75a-112">A number of factors contribute to writer latency, and you can reduce it in several ways.</span></span>

<span data-ttu-id="4a75a-113">Le facteur le plus évident impliqué dans la latence du writer est le temps nécessaire pour compresser un exemple.</span><span class="sxs-lookup"><span data-stu-id="4a75a-113">The most obvious factor involved in writer latency is the time it takes to compress a sample.</span></span> <span data-ttu-id="4a75a-114">Dans la plupart des cas, vous n’aurez que peu ou pas de contrôle sur cela.</span><span class="sxs-lookup"><span data-stu-id="4a75a-114">Under most circumstances, you will have little or no control over this.</span></span> <span data-ttu-id="4a75a-115">Si la bande passante n’est pas une préoccupation majeure, vous pouvez réduire la latence en utilisant moins de compression.</span><span class="sxs-lookup"><span data-stu-id="4a75a-115">If bandwidth is not a big concern, you can reduce latency by using less compression.</span></span> <span data-ttu-id="4a75a-116">Bien sûr, vous pouvez obtenir la latence la plus faible en passant des exemples qui sont déjà compressés.</span><span class="sxs-lookup"><span data-stu-id="4a75a-116">Of course, you can achieve the least latency by passing samples that are already compressed.</span></span>

<span data-ttu-id="4a75a-117">Le facteur suivant, et celui sur lequel vous avez généralement le contrôle, est l’ordre dans lequel les exemples sont passés au lecteur.</span><span class="sxs-lookup"><span data-stu-id="4a75a-117">The next factor, and one over which you usually do have control, is the order in which samples are passed to the reader.</span></span> <span data-ttu-id="4a75a-118">Vous pouvez obtenir une meilleure latence en passant des échantillons dans l’ordre de l’heure de présentation et en vous assurant que les échantillons d’entrée sont bien synchronisés entre tous les flux d’entrée.</span><span class="sxs-lookup"><span data-stu-id="4a75a-118">You can achieve better latency by passing samples in order of presentation time, and by ensuring that the input samples are well synchronized between all input streams.</span></span> <span data-ttu-id="4a75a-119">Plus la différence de temps de présentation entre les exemples de flux différents est importante, plus la latence sera élevée.</span><span class="sxs-lookup"><span data-stu-id="4a75a-119">The greater the discrepancy in presentation times between the samples for different streams, the more latency will result.</span></span> <span data-ttu-id="4a75a-120">Vous pouvez définir un maximum pour l’écart entre les exemples d’entrée en appelant [**IWMWriterAdvanced :: SetSyncTolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance).</span><span class="sxs-lookup"><span data-stu-id="4a75a-120">You can set a maximum for the discrepancy between input samples by calling [**IWMWriterAdvanced::SetSyncTolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a75a-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4a75a-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a75a-122">**Écriture de fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="4a75a-122">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




