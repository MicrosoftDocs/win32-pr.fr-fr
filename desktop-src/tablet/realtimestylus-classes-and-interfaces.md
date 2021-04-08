---
description: Cette section contient des informations sur les interfaces et les classes utilisées dans le stylet en temps réel.
ms.assetid: fc0900b4-f08b-4a93-bbc0-d3db067d7917
title: Classes et interfaces RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34769b2c268bcdfe2becf9e759344d972092fe28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866133"
---
# <a name="realtimestylus-classes-and-interfaces"></a><span data-ttu-id="cff20-103">Classes et interfaces RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="cff20-103">RealTimeStylus Classes and Interfaces</span></span>

<span data-ttu-id="cff20-104">Cette section contient des informations sur les interfaces et les classes utilisées dans le stylet en temps réel.</span><span class="sxs-lookup"><span data-stu-id="cff20-104">This section contains information about the interfaces and classes used in the real time stylus.</span></span>

> [!Note]  
> <span data-ttu-id="cff20-105">Les interfaces et les classes de stylet en temps réel ne sont pas conformes à Automation.</span><span class="sxs-lookup"><span data-stu-id="cff20-105">The real time stylus classes and interfaces are not Automation compliant.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="cff20-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="cff20-106">In This Section</span></span>



| <span data-ttu-id="cff20-107">Classe</span><span class="sxs-lookup"><span data-stu-id="cff20-107">Class</span></span>                                                      | <span data-ttu-id="cff20-108">Description</span><span class="sxs-lookup"><span data-stu-id="cff20-108">Description</span></span>                                                                                     |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cff20-109">**RealTimeStylus, classe**</span><span class="sxs-lookup"><span data-stu-id="cff20-109">**RealTimeStylus Class**</span></span>](realtimestylus-class.md)       | <span data-ttu-id="cff20-110">Implémente l’interface [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) .</span><span class="sxs-lookup"><span data-stu-id="cff20-110">Implements the [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) interface.</span></span><br/>                 |
| <span data-ttu-id="cff20-111">[**DynamicRenderer (classe)**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cff20-111">[**DynamicRenderer Class**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))</span></span>     | <span data-ttu-id="cff20-112">Implémente l’interface d' [**interface IDynamicRenderer**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer) .</span><span class="sxs-lookup"><span data-stu-id="cff20-112">Implements the [**IDynamicRenderer Interface**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer) interface.</span></span><br/>     |
| [<span data-ttu-id="cff20-113">**GestureRecognizer, classe**</span><span class="sxs-lookup"><span data-stu-id="cff20-113">**GestureRecognizer Class**</span></span>](gesturerecognizer-class.md) | <span data-ttu-id="cff20-114">Implémente l’interface d' [**interface IGestureRecognizer**](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer) .</span><span class="sxs-lookup"><span data-stu-id="cff20-114">Implements the [**IGestureRecognizer Interface**](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer) interface.</span></span><br/> |
| [<span data-ttu-id="cff20-115">**StrokeBuilder, classe**</span><span class="sxs-lookup"><span data-stu-id="cff20-115">**StrokeBuilder Class**</span></span>](strokebuilder-class.md)         | <span data-ttu-id="cff20-116">Implémente l’interface d' [**interface IStrokeBuilder**](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder) .</span><span class="sxs-lookup"><span data-stu-id="cff20-116">Implements the [**IStrokeBuilder Interface**](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder) interface.</span></span><br/>         |



 

## <a name="interfaces"></a><span data-ttu-id="cff20-117">Interfaces</span><span class="sxs-lookup"><span data-stu-id="cff20-117">Interfaces</span></span>



| <span data-ttu-id="cff20-118">Interface</span><span class="sxs-lookup"><span data-stu-id="cff20-118">Interface</span></span>                                                                          | <span data-ttu-id="cff20-119">Description</span><span class="sxs-lookup"><span data-stu-id="cff20-119">Description</span></span>                                                                                                                                                                                 |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cff20-120">**Interface IDynamicRenderer**</span><span class="sxs-lookup"><span data-stu-id="cff20-120">**IDynamicRenderer Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer)                             | <span data-ttu-id="cff20-121">Expose des méthodes qui vous permettent de contrôler l’affichage des données de stylet en temps réel, car les données sont gérées par l’objet de [**classe RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="cff20-121">Exposes methods enabling you to control the display of stylus data in real time as the data is being handled by the [**RealTimeStylus Class**](realtimestylus-class.md) object.</span></span><br/> |
| [<span data-ttu-id="cff20-122">**Interface IGestureRecognizer**</span><span class="sxs-lookup"><span data-stu-id="cff20-122">**IGestureRecognizer Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer)                         | <span data-ttu-id="cff20-123">Expose des méthodes qui vous permettent de réagir aux événements en reconnaissant des gestes de stylet et en vous permettant d’ajouter des données à la file d’attente d’entrée.</span><span class="sxs-lookup"><span data-stu-id="cff20-123">Exposes methods enabling you to react to events by recognizing stylus gestures and enabling you to add data to the input queue.</span></span><br/>                                                  |
| [<span data-ttu-id="cff20-124">**IRealTimeStylus**</span><span class="sxs-lookup"><span data-stu-id="cff20-124">**IRealTimeStylus**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)                                         | <span data-ttu-id="cff20-125">Gère les données de paquet du stylet à partir d’un digitaliseur en temps réel.</span><span class="sxs-lookup"><span data-stu-id="cff20-125">Handles the stylus packet data from a digitizer in real time.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="cff20-126">**IRealTimeStylus2**</span><span class="sxs-lookup"><span data-stu-id="cff20-126">**IRealTimeStylus2**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus2)                                       | <span data-ttu-id="cff20-127">Étend l’interface IRealTimeStylus.</span><span class="sxs-lookup"><span data-stu-id="cff20-127">Extends the IRealTimeStylus interface.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="cff20-128">**IRealTimeStylus3**</span><span class="sxs-lookup"><span data-stu-id="cff20-128">**IRealTimeStylus3**</span></span>](/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus3)                                       | <span data-ttu-id="cff20-129">Étend l’interface IRealTimeStylus.</span><span class="sxs-lookup"><span data-stu-id="cff20-129">Extends the IRealTimeStylus interface.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="cff20-130">**Interface IRealTimeStylusSynchronization**</span><span class="sxs-lookup"><span data-stu-id="cff20-130">**IRealTimeStylusSynchronization Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylussynchronization) | <span data-ttu-id="cff20-131">Synchronise l’accès à l’objet de [**classe RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="cff20-131">Synchronizes access to the [**RealTimeStylus Class**](realtimestylus-class.md) object.</span></span><br/>                                                                                          |
| [<span data-ttu-id="cff20-132">**Interface IStrokeBuilder**</span><span class="sxs-lookup"><span data-stu-id="cff20-132">**IStrokeBuilder Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder)                                 | <span data-ttu-id="cff20-133">Expose des méthodes qui vous permettent de créer par programmation des traits.</span><span class="sxs-lookup"><span data-stu-id="cff20-133">Exposes methods that enable you to programmatically create strokes.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="cff20-134">**Interface IStylusPlugin**</span><span class="sxs-lookup"><span data-stu-id="cff20-134">**IStylusPlugin Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-istylusplugin)                                   | <span data-ttu-id="cff20-135">Expose des méthodes vous permettant de recevoir des notifications d’événements et d’effectuer un traitement personnalisé en fonction de ces événements.</span><span class="sxs-lookup"><span data-stu-id="cff20-135">Exposes methods enabling you to receive notifications of events and to perform custom processing based on those events.</span></span><br/>                                                          |
| [<span data-ttu-id="cff20-136">**IStylusAsyncPlugin**</span><span class="sxs-lookup"><span data-stu-id="cff20-136">**IStylusAsyncPlugin**</span></span>](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)                                   | <span data-ttu-id="cff20-137">Représente un plug-in asynchrone qui peut être ajouté à la collection de plug-ins asynchrones de la [**classe RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="cff20-137">Represents an asynchronous plug-in that can be added to the [**RealTimeStylus Class**](realtimestylus-class.md) asynchronous plug-in collection.</span></span><br/>                                |
| [<span data-ttu-id="cff20-138">**IStylusSyncPlugin**</span><span class="sxs-lookup"><span data-stu-id="cff20-138">**IStylusSyncPlugin**</span></span>](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)                                     | <span data-ttu-id="cff20-139">Représente un plug-in synchrone qui peut être ajouté à la collection de plug-ins synchrones de la [**classe RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="cff20-139">Represents a synchronous plug-in that can be added to the [**RealTimeStylus Class**](realtimestylus-class.md) synchronous plug-in collection.</span></span><br/>                                   |



 

## <a name="return-values"></a><span data-ttu-id="cff20-140">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="cff20-140">Return Values</span></span>

<span data-ttu-id="cff20-141">Les méthodes de la bibliothèque COM retournent des valeurs de **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="cff20-141">Methods in the COM Library return values of **HRESULT**.</span></span> <span data-ttu-id="cff20-142">Sauf indication contraire, les significations des valeurs **HRESULT** sont décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="cff20-142">Unless otherwise noted, the meanings of the **HRESULT** values are described in the following table.</span></span>



| <span data-ttu-id="cff20-143">Valeur HRESULT</span><span class="sxs-lookup"><span data-stu-id="cff20-143">HRESULT value</span></span>                                   | <span data-ttu-id="cff20-144">Description</span><span class="sxs-lookup"><span data-stu-id="cff20-144">Description</span></span>                                                                              |
|-------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cff20-145">\_OK</span><span class="sxs-lookup"><span data-stu-id="cff20-145">S\_OK</span></span><br/>                                | <span data-ttu-id="cff20-146">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="cff20-146">Success.</span></span><br/>                                                                      |
| <span data-ttu-id="cff20-147">\_pointeur E</span><span class="sxs-lookup"><span data-stu-id="cff20-147">E\_POINTER</span></span><br/>                           | <span data-ttu-id="cff20-148">Au moins un pointeur (pour un paramètre d’entrée ou de sortie) n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="cff20-148">At least one pointer (for either an input or an output parameter) is invalid.</span></span><br/> |
| <span data-ttu-id="cff20-149">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="cff20-149">E\_INVALIDARG</span></span><br/>                        | <span data-ttu-id="cff20-150">Le membre a tenté de passer un argument non valide.</span><span class="sxs-lookup"><span data-stu-id="cff20-150">Member attempted to pass in an invalid argument.</span></span><br/>                              |
| <span data-ttu-id="cff20-151">\_exception encre \_ E</span><span class="sxs-lookup"><span data-stu-id="cff20-151">E\_INK\_EXCEPTION</span></span><br/>                    | <span data-ttu-id="cff20-152">Une exception s’est produite.</span><span class="sxs-lookup"><span data-stu-id="cff20-152">Exception occurred.</span></span><br/>                                                           |
| <span data-ttu-id="cff20-153">\_OUTOFMEMORY E</span><span class="sxs-lookup"><span data-stu-id="cff20-153">E\_OUTOFMEMORY</span></span><br/>                       | <span data-ttu-id="cff20-154">Le système ne peut pas allouer de mémoire pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="cff20-154">System cannot allocate memory to complete the operation.</span></span><br/>                      |
| <span data-ttu-id="cff20-155">E \_ échec</span><span class="sxs-lookup"><span data-stu-id="cff20-155">E\_FAIL</span></span><br/>                              | <span data-ttu-id="cff20-156">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="cff20-156">Unspecified failure occurred.</span></span><br/>                                                 |
| <span data-ttu-id="cff20-157">E \_ INVALIDOPERATION</span><span class="sxs-lookup"><span data-stu-id="cff20-157">E\_INVALIDOPERATION</span></span><br/>                  | <span data-ttu-id="cff20-158">Le membre a tenté d’utiliser une opération non valide.</span><span class="sxs-lookup"><span data-stu-id="cff20-158">Member attempted to use an invalid operation.</span></span><br/>                                 |
| <span data-ttu-id="cff20-159">TPC \_ E \_ mode non valide \_</span><span class="sxs-lookup"><span data-stu-id="cff20-159">TPC\_E\_INVALID\_MODE</span></span><br/>                | <span data-ttu-id="cff20-160">Le membre a tenté d’utiliser un mode non valide.</span><span class="sxs-lookup"><span data-stu-id="cff20-160">Member attempted to use an invalid mode.</span></span><br/>                                      |
| <span data-ttu-id="cff20-161">\_configuration TPC E \_ non valide \_</span><span class="sxs-lookup"><span data-stu-id="cff20-161">TPC\_E\_INVALID\_CONFIGURATION</span></span><br/>       | <span data-ttu-id="cff20-162">Le membre a tenté d’utiliser une configuration non valide.</span><span class="sxs-lookup"><span data-stu-id="cff20-162">Member attempted to use an invalid configuration.</span></span><br/>                             |
| <span data-ttu-id="cff20-163">\_Description du paquet TPC E \_ non valide \_ \_</span><span class="sxs-lookup"><span data-stu-id="cff20-163">TPC\_E\_INVALID\_PACKET\_DESCRIPTION</span></span><br/> | <span data-ttu-id="cff20-164">Le membre a tenté d’utiliser une description de paquet non valide.</span><span class="sxs-lookup"><span data-stu-id="cff20-164">Member attempted to use an invalid packet description.</span></span><br/>                        |



 

## <a name="related-topics"></a><span data-ttu-id="cff20-165">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cff20-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cff20-166">Référence RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="cff20-166">RealTimeStylus Reference</span></span>](realtimestylus-reference.md)
</dt> </dl>

 

 
