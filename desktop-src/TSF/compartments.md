---
title: Compartiments
description: Compartiments
ms.assetid: 7bffab6f-be40-4d3a-9342-6f81557a9656
keywords:
- Text Services Framework (TSF), compartiments
- TSF (Text Services Framework), compartiments
- services de texte, compartiments
- Applications compatibles TSF, compartiments
- compartiments
- Text Services Framework (TSF), types de compartiments
- TSF (Text Services Framework), types de compartiments
- services de texte, types de compartiments
- Applications compatibles TSF, types de compartiments
- types de compartiments
- Text Services Framework (TSF), notifications de modification de compartiment
- TSF (Text Services Framework), notifications de modification de compartiment
- services de texte, notifications de modification de compartiments
- Applications compatibles TSF, notifications de modification de compartiments
- notifications de modification de compartiment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76636c684ee74f7e452b5602ebfd59d6d1947b0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196529"
---
# <a name="compartments"></a><span data-ttu-id="12d08-118">Compartiments</span><span class="sxs-lookup"><span data-stu-id="12d08-118">Compartments</span></span>

## <a name="compartment-types"></a><span data-ttu-id="12d08-119">Types de compartiments</span><span class="sxs-lookup"><span data-stu-id="12d08-119">Compartment Types</span></span>

<span data-ttu-id="12d08-120">Il existe différents types de compartiments.</span><span class="sxs-lookup"><span data-stu-id="12d08-120">There are several different types of compartments.</span></span> <span data-ttu-id="12d08-121">Il existe un compartiment global, et chaque gestionnaire de threads, le gestionnaire de documents et le contexte peuvent contenir un compartiment.</span><span class="sxs-lookup"><span data-stu-id="12d08-121">There is a global compartment, and each thread manager, document manager, and context can contain a compartment.</span></span>

<span data-ttu-id="12d08-122">Le compartiment global permet aux clients de partager des données entre les processus.</span><span class="sxs-lookup"><span data-stu-id="12d08-122">The global compartment enables clients to share data across processes.</span></span> <span data-ttu-id="12d08-123">Pour obtenir le gestionnaire de compartiments globaux, appelez [**ITfThreadMgr :: GetGlobalCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment).</span><span class="sxs-lookup"><span data-stu-id="12d08-123">To obtain the global compartment manager, call [**ITfThreadMgr::GetGlobalCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment).</span></span>

<span data-ttu-id="12d08-124">Le gestionnaire de thread contient un gestionnaire de compartiments qui contient des compartiments pour chaque thread.</span><span class="sxs-lookup"><span data-stu-id="12d08-124">The thread manager contains a compartment manager that contains compartments on a per-thread basis.</span></span> <span data-ttu-id="12d08-125">Cela permet de partager des données au sein d’un thread.</span><span class="sxs-lookup"><span data-stu-id="12d08-125">This allows data to be shared within a thread.</span></span> <span data-ttu-id="12d08-126">Pour obtenir un gestionnaire de compartiments du gestionnaire de threads, appelez **ITfThreadMgr :: QueryInterface** avec IID \_ ITfCompartmentMgr.</span><span class="sxs-lookup"><span data-stu-id="12d08-126">To obtain a thread manager compartment manager, call **ITfThreadMgr::QueryInterface** with IID\_ITfCompartmentMgr.</span></span>

<span data-ttu-id="12d08-127">Chaque gestionnaire de documents créé contient également un gestionnaire de compartiments.</span><span class="sxs-lookup"><span data-stu-id="12d08-127">Each document manager created also contains a compartment manager.</span></span> <span data-ttu-id="12d08-128">Cela permet de partager des données dans un gestionnaire de document spécifique.</span><span class="sxs-lookup"><span data-stu-id="12d08-128">This allows data to be shared within a specific document manager.</span></span> <span data-ttu-id="12d08-129">Pour obtenir le gestionnaire de compartiments du gestionnaire de documents, appelez **ITfDocumentMgr :: QueryInterface** avec IID \_ ITfCompartmentMgr.</span><span class="sxs-lookup"><span data-stu-id="12d08-129">To obtain the document manager compartment manager, call **ITfDocumentMgr::QueryInterface** with IID\_ITfCompartmentMgr.</span></span>

<span data-ttu-id="12d08-130">Chaque contexte créé contient également un gestionnaire de compartiments.</span><span class="sxs-lookup"><span data-stu-id="12d08-130">Each context created also contains a compartment manager.</span></span> <span data-ttu-id="12d08-131">Cela permet de partager des données dans un contexte spécifique.</span><span class="sxs-lookup"><span data-stu-id="12d08-131">This allows data to be shared within a specific context.</span></span> <span data-ttu-id="12d08-132">Pour obtenir un gestionnaire de compartiments de contexte, appelez **ITfContext :: QueryInterface** avec IID \_ ITfCompartmentMgr.</span><span class="sxs-lookup"><span data-stu-id="12d08-132">To obtain a context compartment manager, call **ITfContext::QueryInterface** with IID\_ITfCompartmentMgr.</span></span>

## <a name="creating-and-deleting-a-compartment"></a><span data-ttu-id="12d08-133">Création et suppression d’un compartiment</span><span class="sxs-lookup"><span data-stu-id="12d08-133">Creating and Deleting a Compartment</span></span>

<span data-ttu-id="12d08-134">Un compartiment est créé la première fois que [**ITfCompartmentMgr :: GetCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment) est appelé avec le GUID de compartiment.</span><span class="sxs-lookup"><span data-stu-id="12d08-134">A compartment is created the first time [**ITfCompartmentMgr::GetCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment) is called with the compartment GUID.</span></span> <span data-ttu-id="12d08-135">Le client d’installation doit définir la valeur initiale du compartiment à l’aide de [**ITfCompartment :: SetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue).</span><span class="sxs-lookup"><span data-stu-id="12d08-135">The installing client should set the initial value of the compartment using [**ITfCompartment::SetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue).</span></span> <span data-ttu-id="12d08-136">Tant qu’une valeur n’est pas définie, la valeur de compartiment est vide.</span><span class="sxs-lookup"><span data-stu-id="12d08-136">Until a value is set, the compartment value is empty.</span></span> <span data-ttu-id="12d08-137">Pour cette raison, il n’existe aucun moyen de vérifier que le compartiment existait avant l’appel de **GetCompartment** .</span><span class="sxs-lookup"><span data-stu-id="12d08-137">Because of this, there is no way to verify that the compartment existed before **GetCompartment** was called.</span></span> <span data-ttu-id="12d08-138">Pour éviter cette situation, le client d’installation doit définir la valeur sur une valeur initiale afin que d’autres clients puissent déterminer si le compartiment existe déjà.</span><span class="sxs-lookup"><span data-stu-id="12d08-138">To avoid this situation, the installing client should set the value to some initial value so that other clients can determine if the compartment already exists.</span></span>

<span data-ttu-id="12d08-139">La méthode [**ITfCompartmentMgr :: ClearCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment) est utilisée pour supprimer un compartiment.</span><span class="sxs-lookup"><span data-stu-id="12d08-139">The [**ITfCompartmentMgr::ClearCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment) method is used to remove a compartment.</span></span> <span data-ttu-id="12d08-140">Toute référence existante au compartiment est marquée comme non valide.</span><span class="sxs-lookup"><span data-stu-id="12d08-140">Any existing references to the compartment are marked invalid.</span></span>

## <a name="obtaining-compartments"></a><span data-ttu-id="12d08-141">Obtention de compartiments</span><span class="sxs-lookup"><span data-stu-id="12d08-141">Obtaining Compartments</span></span>

<span data-ttu-id="12d08-142">À l’aide de l’interface [**ITfCompartmentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr) , un client peut énumérer des compartiments en appelant [**ITfCompartmentMgr :: EnumCompartments**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments).</span><span class="sxs-lookup"><span data-stu-id="12d08-142">Using the [**ITfCompartmentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr) interface, a client can enumerate compartments by calling [**ITfCompartmentMgr::EnumCompartments**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments).</span></span> <span data-ttu-id="12d08-143">Cette méthode fournit un objet **IEnumGUID** qui contient les GUID de tous les compartiments installés.</span><span class="sxs-lookup"><span data-stu-id="12d08-143">This method provides an **IEnumGUID** object that contains the GUIDs of all of the installed compartments.</span></span>

<span data-ttu-id="12d08-144">À l’aide du GUID de compartiment, **ITfCompartmentMgr :: GetCompartment** est utilisé pour obtenir un compartiment spécifique.</span><span class="sxs-lookup"><span data-stu-id="12d08-144">Using the compartment GUID , **ITfCompartmentMgr::GetCompartment** is used to obtain a specific compartment.</span></span> <span data-ttu-id="12d08-145">Cette méthode fournit à l’appelant un objet [**ITfCompartment**](/windows/desktop/api/Msctf/nn-msctf-itfcompartment) qui peut obtenir et définir les données de compartiment.</span><span class="sxs-lookup"><span data-stu-id="12d08-145">This method provides the caller with an [**ITfCompartment**](/windows/desktop/api/Msctf/nn-msctf-itfcompartment) object that can obtain and set the compartment data.</span></span>

## <a name="receiving-compartment-change-notifications"></a><span data-ttu-id="12d08-146">Notifications de modification des compartiments de réception</span><span class="sxs-lookup"><span data-stu-id="12d08-146">Receiving Compartment Change Notifications</span></span>

<span data-ttu-id="12d08-147">Lorsque la valeur d’un compartiment change, le gestionnaire TSF avertit tous les récepteurs de notification installés que le compartiment a changé.</span><span class="sxs-lookup"><span data-stu-id="12d08-147">When the value of a compartment changes, the TSF manager notifies any installed advise sinks that the compartment has changed.</span></span> <span data-ttu-id="12d08-148">Pour installer un récepteur de notification de changement de compartiment, créez un objet qui implémente [**ITfCompartmentEventSink**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink).</span><span class="sxs-lookup"><span data-stu-id="12d08-148">To install a compartment change advise sink, create an object that implements [**ITfCompartmentEventSink**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink).</span></span> <span data-ttu-id="12d08-149">Appelez ensuite **ITfCompartment :: QueryInterface** avec IID \_ ITfSource sur l’objet compartiment à surveiller pour obtenir une interface [**ITfSource**](/windows/desktop/api/Msctf/nn-msctf-itfsource) .</span><span class="sxs-lookup"><span data-stu-id="12d08-149">Then call **ITfCompartment::QueryInterface** with IID\_ITfSource on the compartment object to be monitored to obtain an [**ITfSource**](/windows/desktop/api/Msctf/nn-msctf-itfsource) interface.</span></span> <span data-ttu-id="12d08-150">À présent, appelez [**ITfSource :: AdviseSink**](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) avec IID \_ ITfCompartmentEventSink et le pointeur vers l’objet **ITfCompartmentEventSink** .</span><span class="sxs-lookup"><span data-stu-id="12d08-150">Now call [**ITfSource::AdviseSink**](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) with IID\_ITfCompartmentEventSink and the pointer to the **ITfCompartmentEventSink** object.</span></span> <span data-ttu-id="12d08-151">Lorsque la valeur du compartiment change, [**ITfCompartmentEventSink :: OnChange**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange) du récepteur de notifications est appelé avec le GUID du compartiment.</span><span class="sxs-lookup"><span data-stu-id="12d08-151">When the value of the compartment changes, the advise sink's [**ITfCompartmentEventSink::OnChange**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange) is called with the GUID of the compartment.</span></span> <span data-ttu-id="12d08-152">Le récepteur de notifications peut appeler [**ITfCompartment :: GetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-getvalue) pour obtenir la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="12d08-152">The advise sink can call [**ITfCompartment::GetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-getvalue) to obtain the new value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="12d08-153">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="12d08-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12d08-154">**ITfCompartmentMgr**</span><span class="sxs-lookup"><span data-stu-id="12d08-154">**ITfCompartmentMgr**</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr)
</dt> <dt>

[<span data-ttu-id="12d08-155">**ITfCompartment**</span><span class="sxs-lookup"><span data-stu-id="12d08-155">**ITfCompartment**</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfcompartment)
</dt> <dt>

[<span data-ttu-id="12d08-156">**ITfCompartmentEventSink**</span><span class="sxs-lookup"><span data-stu-id="12d08-156">**ITfCompartmentEventSink**</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink)
</dt> <dt>

[<span data-ttu-id="12d08-157">**TfClientId**</span><span class="sxs-lookup"><span data-stu-id="12d08-157">**TfClientId**</span></span>](tfclientid.md)
</dt> <dt>

[<span data-ttu-id="12d08-158">**ITfThreadMgr :: GetGlobalCompartment**</span><span class="sxs-lookup"><span data-stu-id="12d08-158">**ITfThreadMgr::GetGlobalCompartment**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment)
</dt> <dt>

[<span data-ttu-id="12d08-159">**ITfCompartmentMgr::GetCompartment**</span><span class="sxs-lookup"><span data-stu-id="12d08-159">**ITfCompartmentMgr::GetCompartment**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment)
</dt> <dt>

[<span data-ttu-id="12d08-160">**ITfCompartment :: SetValue**</span><span class="sxs-lookup"><span data-stu-id="12d08-160">**ITfCompartment::SetValue**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue)
</dt> <dt>

[<span data-ttu-id="12d08-161">**ITfCompartmentMgr::ClearCompartment**</span><span class="sxs-lookup"><span data-stu-id="12d08-161">**ITfCompartmentMgr::ClearCompartment**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment)
</dt> <dt>

[<span data-ttu-id="12d08-162">**ITfCompartmentMgr::EnumCompartments**</span><span class="sxs-lookup"><span data-stu-id="12d08-162">**ITfCompartmentMgr::EnumCompartments**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments)
</dt> <dt>

[<span data-ttu-id="12d08-163">**ITfSource**</span><span class="sxs-lookup"><span data-stu-id="12d08-163">**ITfSource**</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfsource)
</dt> <dt>

[<span data-ttu-id="12d08-164">**ITfSource :: AdviseSink**</span><span class="sxs-lookup"><span data-stu-id="12d08-164">**ITfSource::AdviseSink**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink)
</dt> <dt>

[<span data-ttu-id="12d08-165">**ITfCompartmentEventSink :: OnChange**</span><span class="sxs-lookup"><span data-stu-id="12d08-165">**ITfCompartmentEventSink::OnChange**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange)
</dt> </dl>

 

 




