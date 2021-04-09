---
description: Cette section décrit comment écrire une transformation de Media Foundation personnalisée (MFT).
ms.assetid: a95828d3-afc5-4f6b-aedd-5b6a72621e0e
title: Écriture d’une table MFT personnalisée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15b9d5ae655ba67d4a526aeb8a82eb9d3912da9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865570"
---
# <a name="writing-a-custom-mft"></a><span data-ttu-id="6e797-103">Écriture d’une table MFT personnalisée</span><span class="sxs-lookup"><span data-stu-id="6e797-103">Writing a Custom MFT</span></span>

<span data-ttu-id="6e797-104">Cette section décrit comment écrire une transformation de Media Foundation personnalisée (MFT).</span><span class="sxs-lookup"><span data-stu-id="6e797-104">This section describes how to write a custom Media Foundation Transform (MFT).</span></span>

## <a name="mft-checklist"></a><span data-ttu-id="6e797-105">Liste de contrôle MFT</span><span class="sxs-lookup"><span data-stu-id="6e797-105">MFT Checklist</span></span>

<span data-ttu-id="6e797-106">Lorsque vous implémentez une table MFT personnalisée, utilisez la liste de vérification suivante pour déterminer les conditions requises :</span><span class="sxs-lookup"><span data-stu-id="6e797-106">When you implement a custom MFT, use the following checklist to determine the requirements:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6e797-107">Tous les MFTs</span><span class="sxs-lookup"><span data-stu-id="6e797-107">All MFTs</span></span></td>
<td><span data-ttu-id="6e797-108">Toutes les MFTs doivent implémenter <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform"><strong>IMFTransform</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6e797-108">All MFTs must implement <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform"><strong>IMFTransform</strong></a>.</span></span><br/> <span data-ttu-id="6e797-109">Les rubriques suivantes fournissent plus d’informations sur l’implémentation de cette interface :</span><span class="sxs-lookup"><span data-stu-id="6e797-109">The following topics give more information about implementing this interface:</span></span>
<ul>
<li><span data-ttu-id="6e797-110"><a href="basic-mft-processing-model.md">Modèle de traitement MFT de base</a></span><span class="sxs-lookup"><span data-stu-id="6e797-110"><a href="basic-mft-processing-model.md">Basic MFT Processing Model</a></span></span></li>
<li><span data-ttu-id="6e797-111"><a href="time-stamps-and-durations.md">Horodatages et durées</a></span><span class="sxs-lookup"><span data-stu-id="6e797-111"><a href="time-stamps-and-durations.md">Time Stamps and Durations</a></span></span></li>
<li><span data-ttu-id="6e797-112"><a href="handling-stream-changes.md">Gestion des modifications de flux</a></span><span class="sxs-lookup"><span data-stu-id="6e797-112"><a href="handling-stream-changes.md">Handling Stream Changes</a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e797-113">Encodeurs et décodeurs</span><span class="sxs-lookup"><span data-stu-id="6e797-113">Encoders and decoders</span></span></td>
<td><span data-ttu-id="6e797-114">Configuration requise : consultez <a href="implementing-a-codec-mft.md">implémentation d’une table MFT de codec</a>.</span><span class="sxs-lookup"><span data-stu-id="6e797-114">Requirements: See <a href="implementing-a-codec-mft.md">Implementing a Codec MFT</a>.</span></span><br/> <span data-ttu-id="6e797-115">Recommandé : implémentez <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise"><strong>IMFQualityAdvise</strong></a> ou <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2"><strong>IMFQualityAdvise2</strong></a>pour prendre en charge les notifications de qualité de service (QoS).</span><span class="sxs-lookup"><span data-stu-id="6e797-115">Recommended: Implement <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise"><strong>IMFQualityAdvise</strong></a> or <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2"><strong>IMFQualityAdvise2</strong></a>, to support quality-of-service (QoS) notifications.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6e797-116">Décodeurs vidéo et processeurs vidéo</span><span class="sxs-lookup"><span data-stu-id="6e797-116">Video decoders and video processors</span></span></td>
<td><span data-ttu-id="6e797-117">Facultatif : prendre en charge l’accélération vidéo DirectX.</span><span class="sxs-lookup"><span data-stu-id="6e797-117">Optional: Support DirectX Video Acceleration.</span></span><br/>
<ul>
<li><span data-ttu-id="6e797-118"><a href="direct3d-aware-mfts.md">MFTs compatible Direct3D</a></span><span class="sxs-lookup"><span data-stu-id="6e797-118"><a href="direct3d-aware-mfts.md">Direct3D-Aware MFTs</a></span></span></li>
<li><span data-ttu-id="6e797-119"><a href="supporting-dxva-2-0-in-media-foundation.md">Prise en charge de DXVA 2,0 dans Media Foundation</a></span><span class="sxs-lookup"><span data-stu-id="6e797-119"><a href="supporting-dxva-2-0-in-media-foundation.md">Supporting DXVA 2.0 in Media Foundation</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e797-120">Codecs matériels</span><span class="sxs-lookup"><span data-stu-id="6e797-120">Hardware codecs</span></span></td>
<td><span data-ttu-id="6e797-121">Voir <a href="hardware-mfts.md">matériel MFTS</a>.</span><span class="sxs-lookup"><span data-stu-id="6e797-121">See <a href="hardware-mfts.md">Hardware MFTs</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6e797-122">Pour que votre MFT soit détectable par les applications...</span><span class="sxs-lookup"><span data-stu-id="6e797-122">To make your MFT discoverable by applications...</span></span></td>
<td><span data-ttu-id="6e797-123">Consultez la page <a href="registering-and-enumerating-mfts.md">inscription et énumération de MFTS</a>.</span><span class="sxs-lookup"><span data-stu-id="6e797-123">See <a href="registering-and-enumerating-mfts.md">Registering and Enumerating MFTs</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e797-124">Traitement asynchrone des données</span><span class="sxs-lookup"><span data-stu-id="6e797-124">Asynchronous data processing</span></span></td>
<td><span data-ttu-id="6e797-125">Le modèle MFT par défaut utilise des appels synchrones (bloquant) pour traiter les données.</span><span class="sxs-lookup"><span data-stu-id="6e797-125">The default MFT model uses synchronous (blocking) calls to process data.</span></span> <span data-ttu-id="6e797-126">Pour certains MFTs, le traitement asynchrone peut être plus efficace.</span><span class="sxs-lookup"><span data-stu-id="6e797-126">For some MFTs, asynchronous processing can be more efficient.</span></span> <span data-ttu-id="6e797-127">Toutefois, il est également plus complexe à implémenter.</span><span class="sxs-lookup"><span data-stu-id="6e797-127">However, it is also more complex to implement.</span></span><br/> <span data-ttu-id="6e797-128">Pour plus d’informations, consultez <a href="asynchronous-mfts.md">MFTS asynchrone</a>.</span><span class="sxs-lookup"><span data-stu-id="6e797-128">For more information, see <a href="asynchronous-mfts.md">Asynchronous MFTs</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6e797-129">Contrôle de la fréquence, mode de pli ou lecture inversée</span><span class="sxs-lookup"><span data-stu-id="6e797-129">Rate control, trick mode, or reverse playback</span></span></td>
<td><span data-ttu-id="6e797-130">Consultez <a href="implementing-rate-control.md">Implementing Rate Control</a>.</span><span class="sxs-lookup"><span data-stu-id="6e797-130">See <a href="implementing-rate-control.md">Implementing Rate Control</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e797-131">Si votre MFT crée des threads...</span><span class="sxs-lookup"><span data-stu-id="6e797-131">If your MFT creates threads...</span></span></td>
<td><span data-ttu-id="6e797-132">Implémentez l’interface <a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient"><strong>IMFRealTimeClient</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="6e797-132">Implement the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient"><strong>IMFRealTimeClient</strong></a> interface.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6e797-133">Si votre MFT a des restrictions de licence...</span><span class="sxs-lookup"><span data-stu-id="6e797-133">If your MFT has licensing restrictions...</span></span></td>
<td><span data-ttu-id="6e797-134">Envisagez d’utiliser le mécanisme de champ d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="6e797-134">Consider using the field-of-use mechanism.</span></span> <span data-ttu-id="6e797-135">Consultez <a href="field-of-use-restrictions.md">restrictions relatives au champ d’utilisation</a>.</span><span class="sxs-lookup"><span data-stu-id="6e797-135">See <a href="field-of-use-restrictions.md">Field of Use Restrictions</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e797-136">Si vous effectuez le portage d’un objet multimédia DirectX existant (DMO)...</span><span class="sxs-lookup"><span data-stu-id="6e797-136">If you are porting an existing DirectX Media Object (DMO)...</span></span></td>
<td><span data-ttu-id="6e797-137">Consultez <a href="comparison-of-mfts-and-dmos.md">comparaison entre MFTS et DMOs</a>.</span><span class="sxs-lookup"><span data-stu-id="6e797-137">See <a href="comparison-of-mfts-and-dmos.md">Comparison of MFTs and DMOs</a>.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="6e797-138">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="6e797-138">This section contains the following topics:</span></span>

-   [<span data-ttu-id="6e797-139">Horodatages et durées</span><span class="sxs-lookup"><span data-stu-id="6e797-139">Time Stamps and Durations</span></span>](time-stamps-and-durations.md)
-   [<span data-ttu-id="6e797-140">Gestion des modifications de flux</span><span class="sxs-lookup"><span data-stu-id="6e797-140">Handling Stream Changes</span></span>](handling-stream-changes.md)
-   [<span data-ttu-id="6e797-141">Implémentation d’une table MFT de codec</span><span class="sxs-lookup"><span data-stu-id="6e797-141">Implementing a Codec MFT</span></span>](implementing-a-codec-mft.md)
-   [<span data-ttu-id="6e797-142">MFTs compatible Direct3D</span><span class="sxs-lookup"><span data-stu-id="6e797-142">Direct3D-Aware MFTs</span></span>](direct3d-aware-mfts.md)
-   [<span data-ttu-id="6e797-143">Matériel MFTs</span><span class="sxs-lookup"><span data-stu-id="6e797-143">Hardware MFTs</span></span>](hardware-mfts.md)
-   [<span data-ttu-id="6e797-144">Mérite du codec</span><span class="sxs-lookup"><span data-stu-id="6e797-144">Codec Merit</span></span>](codec-merit.md)

## <a name="related-topics"></a><span data-ttu-id="6e797-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6e797-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e797-146">Transformations de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6e797-146">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> </dl>

 

 




