---
description: La classe CVideoTransformFilter est principalement conçue comme une classe de base pour les filtres de décompresseur AVI.
ms.assetid: 8eb87f9f-24b3-4dbe-a390-54db993d2724
title: CVideoTransformFilter, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter
api_type:
- COM
api_location: ''
ms.openlocfilehash: 360f46eb7242de01d5e734c5efa17399f23adf7d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846814"
---
# <a name="cvideotransformfilter-class"></a><span data-ttu-id="9a383-103">CVideoTransformFilter, classe</span><span class="sxs-lookup"><span data-stu-id="9a383-103">CVideoTransformFilter class</span></span>

![hiérarchie de la classe cvideotransformfilter](images/vtsip01.png)

<span data-ttu-id="9a383-105">La `CVideoTransformFilter` classe est principalement conçue comme une classe de base pour les filtres de décompresseur avi.</span><span class="sxs-lookup"><span data-stu-id="9a383-105">The `CVideoTransformFilter` class is designed primarily as a base class for AVI decompressor filters.</span></span> <span data-ttu-id="9a383-106">Cette classe ajoute la prise en charge du contrôle de qualité à la classe [**CTransformFilter**](ctransformfilter.md) .</span><span class="sxs-lookup"><span data-stu-id="9a383-106">This class adds support for quality control to the [**CTransformFilter**](ctransformfilter.md) class.</span></span> <span data-ttu-id="9a383-107">La méthode **Receive** du filtre peut décider de supprimer des frames, en fonction des messages de qualité du convertisseur et des mesures de performances collectées par le filtre pendant la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="9a383-107">The filter's **Receive** method can decide to drop frames, based on quality messages from the renderer and performance measurements that the filter collects while it is streaming.</span></span>

<span data-ttu-id="9a383-108">Si le filtre supprime un frame, il continue à déposer des frames jusqu’à ce qu’il atteigne l’image clé suivante.</span><span class="sxs-lookup"><span data-stu-id="9a383-108">If the filter drops a frame, it continues to drop frames until it reaches the next key frame.</span></span> <span data-ttu-id="9a383-109">Pour les flux MPEG, le filtre ne fait pas la distinction entre les frames B et les images P.</span><span class="sxs-lookup"><span data-stu-id="9a383-109">For MPEG streams, the filter does not distinguish between B frames and P frames.</span></span>



| <span data-ttu-id="9a383-110">Variables membres protégées</span><span class="sxs-lookup"><span data-stu-id="9a383-110">Protected Member Variables</span></span>                                                      | <span data-ttu-id="9a383-111">Description</span><span class="sxs-lookup"><span data-stu-id="9a383-111">Description</span></span>                                                                                    |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9a383-112">**m \_ bQualityChanged**</span><span class="sxs-lookup"><span data-stu-id="9a383-112">**m\_bQualityChanged**</span></span>](cvideotransformfilter-m-bqualitychanged.md)           | <span data-ttu-id="9a383-113">Indique si le filtre a supprimé des frames.</span><span class="sxs-lookup"><span data-stu-id="9a383-113">Indicates whether the filter has dropped frames.</span></span>                                               |
| [<span data-ttu-id="9a383-114">**m \_ bSkipping**</span><span class="sxs-lookup"><span data-stu-id="9a383-114">**m\_bSkipping**</span></span>](cvideotransformfilter-m-bskipping.md)                       | <span data-ttu-id="9a383-115">Indique si le filtre supprime actuellement des frames.</span><span class="sxs-lookup"><span data-stu-id="9a383-115">Indicates whether the filter is currently dropping frames.</span></span>                                     |
| [<span data-ttu-id="9a383-116">**m \_ itrAvgDecode**</span><span class="sxs-lookup"><span data-stu-id="9a383-116">**m\_itrAvgDecode**</span></span>](cvideotransformfilter-m-itravgdecode.md)                 | <span data-ttu-id="9a383-117">Durée moyenne nécessaire pour décoder une image.</span><span class="sxs-lookup"><span data-stu-id="9a383-117">Average length of time it has taken to decode a frame.</span></span>                                         |
| [<span data-ttu-id="9a383-118">**m \_ itrLate**</span><span class="sxs-lookup"><span data-stu-id="9a383-118">**m\_itrLate**</span></span>](cvideotransformfilter-m-itrlate.md)                           | <span data-ttu-id="9a383-119">Indique la durée pendant laquelle les exemples arrivent au convertisseur.</span><span class="sxs-lookup"><span data-stu-id="9a383-119">Indicates how late the samples are arriving at the renderer.</span></span>                                   |
| [<span data-ttu-id="9a383-120">**m \_ nFramesSinceKeyFrame**</span><span class="sxs-lookup"><span data-stu-id="9a383-120">**m\_nFramesSinceKeyFrame**</span></span>](cvideotransformfilter-m-nframessincekeyframe.md) | <span data-ttu-id="9a383-121">Nombre de trames reçues par le filtre depuis la dernière image clé.</span><span class="sxs-lookup"><span data-stu-id="9a383-121">The number of frames that the filter has received since the last key frame.</span></span>                    |
| [<span data-ttu-id="9a383-122">**m \_ nKeyFramePeriod**</span><span class="sxs-lookup"><span data-stu-id="9a383-122">**m\_nKeyFramePeriod**</span></span>](cvideotransformfilter-m-nkeyframeperiod.md)           | <span data-ttu-id="9a383-123">Intervalle le plus grand observé entre les images clés.</span><span class="sxs-lookup"><span data-stu-id="9a383-123">The largest observed interval between key frames.</span></span>                                              |
| [<span data-ttu-id="9a383-124">**m \_ nWaitForKey**</span><span class="sxs-lookup"><span data-stu-id="9a383-124">**m\_nWaitForKey**</span></span>](cvideotransformfilter-m-nwaitforkey.md)                   | <span data-ttu-id="9a383-125">Nombre maximal actuel d’images Delta à supprimer.</span><span class="sxs-lookup"><span data-stu-id="9a383-125">The current maximum number of delta frames to drop.</span></span>                                            |
| [<span data-ttu-id="9a383-126">**m \_ tDecodeStart**</span><span class="sxs-lookup"><span data-stu-id="9a383-126">**m\_tDecodeStart**</span></span>](cvideotransformfilter-m-tdecodestart.md)                 | <span data-ttu-id="9a383-127">Durée nécessaire pour décoder l’exemple le plus récent.</span><span class="sxs-lookup"><span data-stu-id="9a383-127">Length of time that it took to decode the most recent sample.</span></span>                                  |
| <span data-ttu-id="9a383-128">Méthodes protégées</span><span class="sxs-lookup"><span data-stu-id="9a383-128">Protected Methods</span></span>                                                               | <span data-ttu-id="9a383-129">Description</span><span class="sxs-lookup"><span data-stu-id="9a383-129">Description</span></span>                                                                                    |
| [<span data-ttu-id="9a383-130">**AbortPlayback**</span><span class="sxs-lookup"><span data-stu-id="9a383-130">**AbortPlayback**</span></span>](cvideotransformfilter-abortplayback.md)                    | <span data-ttu-id="9a383-131">Utilisé pour signaler une erreur de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="9a383-131">Used to signal a streaming error.</span></span>                                                              |
| [<span data-ttu-id="9a383-132">**AlterQuality**</span><span class="sxs-lookup"><span data-stu-id="9a383-132">**AlterQuality**</span></span>](cvideotransformfilter-alterquality.md)                      | <span data-ttu-id="9a383-133">Notifie le filtre qu’une modification de qualité est demandée.</span><span class="sxs-lookup"><span data-stu-id="9a383-133">Notifies the filter that a quality change is requested.</span></span>                                        |
| [<span data-ttu-id="9a383-134">**Çoive**</span><span class="sxs-lookup"><span data-stu-id="9a383-134">**Receive**</span></span>](cvideotransformfilter-receive.md)                                | <span data-ttu-id="9a383-135">Reçoit un exemple de support, le traite et remet un échantillon de sortie au filtre en aval.</span><span class="sxs-lookup"><span data-stu-id="9a383-135">Receives a media sample, processes it, and delivers an output sample to the downstream filter.</span></span> |
| [<span data-ttu-id="9a383-136">**ShouldSkipFrame**</span><span class="sxs-lookup"><span data-stu-id="9a383-136">**ShouldSkipFrame**</span></span>](cvideotransformfilter-shouldskipframe.md)                | <span data-ttu-id="9a383-137">Détermine si le filtre doit supprimer un échantillon spécifié.</span><span class="sxs-lookup"><span data-stu-id="9a383-137">Determines whether the filter should drop a specified sample.</span></span>                                  |
| [<span data-ttu-id="9a383-138">**StartStreaming**</span><span class="sxs-lookup"><span data-stu-id="9a383-138">**StartStreaming**</span></span>](cvideotransformfilter-startstreaming.md)                  | <span data-ttu-id="9a383-139">Appelé lorsque le filtre bascule à l’état suspendu.</span><span class="sxs-lookup"><span data-stu-id="9a383-139">Called when the filter switches to the paused state.</span></span>                                           |
| <span data-ttu-id="9a383-140">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="9a383-140">Public Methods</span></span>                                                                  | <span data-ttu-id="9a383-141">Description</span><span class="sxs-lookup"><span data-stu-id="9a383-141">Description</span></span>                                                                                    |
| [<span data-ttu-id="9a383-142">**CVideoTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="9a383-142">**CVideoTransformFilter**</span></span>](cvideotransformfilter-cvideotransformfilter.md)    | <span data-ttu-id="9a383-143">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="9a383-143">Constructor method.</span></span>                                                                            |
| [<span data-ttu-id="9a383-144">**EndFlush**</span><span class="sxs-lookup"><span data-stu-id="9a383-144">**EndFlush**</span></span>](cvideotransformfilter-endflush.md)                              | <span data-ttu-id="9a383-145">Termine une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="9a383-145">Ends a flush operation.</span></span>                                                                        |



 

 

 



