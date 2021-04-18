---
title: À propos de IMFTransform
description: À propos de IMFTransform
ms.assetid: 889f2d82-148a-4a7e-b78c-37ec86b37e0b
keywords:
- Plug-ins du lecteur Windows Media, interfaces
- plug-ins, interfaces
- plug-ins de traitement de signal numérique, interfaces
- Plug-ins DSP, interfaces
- interfaces, plug-ins DSP
- Plug-ins du lecteur Windows Media, interface IMFTransform
- plug-ins, interface IMFTransform
- plug-ins de traitement de signal numérique, interface IMFTransform
- Plug-ins DSP, interface IMFTransform
- Interface IMFTransform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb58ab84070a8cb9390e4525b9b642f15a29f14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509175"
---
# <a name="about-imftransform"></a><span data-ttu-id="8564a-113">À propos de IMFTransform</span><span class="sxs-lookup"><span data-stu-id="8564a-113">About IMFTransform</span></span>

<span data-ttu-id="8564a-114">L’interface **IMFTransform** est l’une des interfaces qui doivent être implémentées par un plug-in DSP à double mode.</span><span class="sxs-lookup"><span data-stu-id="8564a-114">The **IMFTransform** interface is one of the interfaces that must be implemented by a dual-mode DSP plug-in.</span></span> <span data-ttu-id="8564a-115">Le lecteur Windows Media appelle les méthodes de l’interface **IMFTransform** pour fournir des données au plug-in et récupérer les données traitées à partir du plug-in.</span><span class="sxs-lookup"><span data-stu-id="8564a-115">Windows Media Player calls the methods of the **IMFTransform** interface to provide data to the plug-in and to retrieve processed data back from the plug-in.</span></span> <span data-ttu-id="8564a-116">Pour obtenir la documentation complète de l’interface **IMFTransform** , consultez la section Media Foundation de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="8564a-116">For complete documentation of the **IMFTransform** interface, see the Media Foundation section of the Windows SDK.</span></span>

<span data-ttu-id="8564a-117">Les méthodes de **IMFTransform** peuvent être classées comme suit.</span><span class="sxs-lookup"><span data-stu-id="8564a-117">The methods of **IMFTransform** can be categorized as follows.</span></span>

## <a name="methods-that-handle-format-negotiation"></a><span data-ttu-id="8564a-118">Méthodes qui gèrent la négociation de format</span><span class="sxs-lookup"><span data-stu-id="8564a-118">Methods That Handle Format Negotiation</span></span>

<span data-ttu-id="8564a-119">Le lecteur Windows Media appelle les méthodes suivantes pour obtenir des informations sur les formats de données pris en charge par le plug-in.</span><span class="sxs-lookup"><span data-stu-id="8564a-119">Windows Media Player calls the following methods to get information about the data formats supported by the plug-in.</span></span>

-   <span data-ttu-id="8564a-120">**GetStreamCount**</span><span class="sxs-lookup"><span data-stu-id="8564a-120">**GetStreamCount**</span></span>
-   <span data-ttu-id="8564a-121">**GetStreamLimits**</span><span class="sxs-lookup"><span data-stu-id="8564a-121">**GetStreamLimits**</span></span>
-   <span data-ttu-id="8564a-122">**GetInputStreamInfo**</span><span class="sxs-lookup"><span data-stu-id="8564a-122">**GetInputStreamInfo**</span></span>
-   <span data-ttu-id="8564a-123">**GetOutputStreamInfo**</span><span class="sxs-lookup"><span data-stu-id="8564a-123">**GetOutputStreamInfo**</span></span>
-   <span data-ttu-id="8564a-124">**GetInputAvailableType**</span><span class="sxs-lookup"><span data-stu-id="8564a-124">**GetInputAvailableType**</span></span>
-   <span data-ttu-id="8564a-125">**GetOutputAvailableType**</span><span class="sxs-lookup"><span data-stu-id="8564a-125">**GetOutputAvailableType**</span></span>
-   <span data-ttu-id="8564a-126">**SetInputType**</span><span class="sxs-lookup"><span data-stu-id="8564a-126">**SetInputType**</span></span>
-   <span data-ttu-id="8564a-127">**SetOutputType**</span><span class="sxs-lookup"><span data-stu-id="8564a-127">**SetOutputType**</span></span>
-   <span data-ttu-id="8564a-128">**GetAttributes,**</span><span class="sxs-lookup"><span data-stu-id="8564a-128">**GetAttributes**</span></span>
-   <span data-ttu-id="8564a-129">**GetInputStreamAttributes**</span><span class="sxs-lookup"><span data-stu-id="8564a-129">**GetInputStreamAttributes**</span></span>
-   <span data-ttu-id="8564a-130">**GetOutputStreamAttributes**</span><span class="sxs-lookup"><span data-stu-id="8564a-130">**GetOutputStreamAttributes**</span></span>
-   <span data-ttu-id="8564a-131">**GetStreamIDs**</span><span class="sxs-lookup"><span data-stu-id="8564a-131">**GetStreamIDs**</span></span>

## <a name="methods-that-specify-or-retrieve-state-information"></a><span data-ttu-id="8564a-132">Méthodes qui spécifient ou récupèrent les informations d’État</span><span class="sxs-lookup"><span data-stu-id="8564a-132">Methods That Specify or Retrieve State Information</span></span>

<span data-ttu-id="8564a-133">Le lecteur Windows Media appelle les méthodes suivantes pour récupérer ou définir les valeurs relatives à l’état actuel du plug-in.</span><span class="sxs-lookup"><span data-stu-id="8564a-133">Windows Media Player calls the following methods to get or set values related to the current state of the plug-in.</span></span>

-   <span data-ttu-id="8564a-134">**SetInputType**</span><span class="sxs-lookup"><span data-stu-id="8564a-134">**SetInputType**</span></span>
-   <span data-ttu-id="8564a-135">**SetOutputType**</span><span class="sxs-lookup"><span data-stu-id="8564a-135">**SetOutputType**</span></span>
-   <span data-ttu-id="8564a-136">**GetInputCurrentType**</span><span class="sxs-lookup"><span data-stu-id="8564a-136">**GetInputCurrentType**</span></span>
-   <span data-ttu-id="8564a-137">**GetOutputCurrentType**</span><span class="sxs-lookup"><span data-stu-id="8564a-137">**GetOutputCurrentType**</span></span>
-   <span data-ttu-id="8564a-138">**GetInputStatus**</span><span class="sxs-lookup"><span data-stu-id="8564a-138">**GetInputStatus**</span></span>
-   <span data-ttu-id="8564a-139">**AddInputStreams**</span><span class="sxs-lookup"><span data-stu-id="8564a-139">**AddInputStreams**</span></span>
-   <span data-ttu-id="8564a-140">**DeleteInputStreams**</span><span class="sxs-lookup"><span data-stu-id="8564a-140">**DeleteInputStreams**</span></span>
-   <span data-ttu-id="8564a-141">**GetOutputStatus**</span><span class="sxs-lookup"><span data-stu-id="8564a-141">**GetOutputStatus**</span></span>
-   <span data-ttu-id="8564a-142">**SetOutputBounds**</span><span class="sxs-lookup"><span data-stu-id="8564a-142">**SetOutputBounds**</span></span>

> [!Note]  
> <span data-ttu-id="8564a-143">**SetInputType** et **SetOutputType** sont utilisés à la fois pour la négociation de format et pour la spécification et la récupération des informations d’État.</span><span class="sxs-lookup"><span data-stu-id="8564a-143">**SetInputType** and **SetOutputType** are used both for format negotiation and for specifying and retrieving state information.</span></span>

 

## <a name="methods-that-handle-buffering-and-processing-data"></a><span data-ttu-id="8564a-144">Méthodes qui gèrent la mise en mémoire tampon et le traitement des données</span><span class="sxs-lookup"><span data-stu-id="8564a-144">Methods That Handle Buffering and Processing Data</span></span>

<span data-ttu-id="8564a-145">Le lecteur Windows Media appelle les méthodes suivantes pour initier les différents processus que le plug-in effectue pour effectuer le traitement du signal numérique.</span><span class="sxs-lookup"><span data-stu-id="8564a-145">Windows Media Player calls the following methods to initiate the various processes that the plug-in performs to do the digital signal processing.</span></span>

-   <span data-ttu-id="8564a-146">**ProcessInput**</span><span class="sxs-lookup"><span data-stu-id="8564a-146">**ProcessInput**</span></span>
-   <span data-ttu-id="8564a-147">**ProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="8564a-147">**ProcessOutput**</span></span>
-   <span data-ttu-id="8564a-148">**ProcessMessage**</span><span class="sxs-lookup"><span data-stu-id="8564a-148">**ProcessMessage**</span></span>
-   <span data-ttu-id="8564a-149">**ProcessEvent**</span><span class="sxs-lookup"><span data-stu-id="8564a-149">**ProcessEvent**</span></span>

## <a name="related-topics"></a><span data-ttu-id="8564a-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8564a-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8564a-151">**Interfaces requises**</span><span class="sxs-lookup"><span data-stu-id="8564a-151">**Required Interfaces**</span></span>](required-interfaces.md)
</dt> </dl>

 

 




