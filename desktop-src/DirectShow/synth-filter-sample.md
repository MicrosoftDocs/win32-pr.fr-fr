---
description: Exemple de filtre Synth
ms.assetid: 2d087967-3734-463f-bc5e-9552290ddc0b
title: Exemple de filtre Synth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd569091df92eca3fbff4d8cb200150d6e6bfdca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868518"
---
# <a name="synth-filter-sample"></a><span data-ttu-id="f77ba-103">Exemple de filtre Synth</span><span class="sxs-lookup"><span data-stu-id="f77ba-103">Synth Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="f77ba-104">Description</span><span class="sxs-lookup"><span data-stu-id="f77ba-104">Description</span></span>

<span data-ttu-id="f77ba-105">Le filtre Synth est un filtre source qui génère des formes d’ondes audio.</span><span class="sxs-lookup"><span data-stu-id="f77ba-105">The Synth filter is a source filter that generates audio waveforms.</span></span>

<span data-ttu-id="f77ba-106">Ce filtre illustre la génération de graphiques dynamiques.</span><span class="sxs-lookup"><span data-stu-id="f77ba-106">This filter illustrates dynamic graph building.</span></span> <span data-ttu-id="f77ba-107">Il peut basculer entre le format audio PCM non compressé et le \_ format MS ADPCM compressé (Microsoft adaptative Delta Pulse Code Modulation).</span><span class="sxs-lookup"><span data-stu-id="f77ba-107">It can switch between uncompressed PCM audio and compressed MS\_ADPCM (Microsoft Adaptive Delta Pulse Code Modulation) format.</span></span>

<span data-ttu-id="f77ba-108">Ce filtre apparaît dans GraphEdit comme « filtre de synthétiseur audio ».</span><span class="sxs-lookup"><span data-stu-id="f77ba-108">This filter appears in GraphEdit as "Audio Synthesizer Filter."</span></span>

<span data-ttu-id="f77ba-109">Pour plus d’informations sur la génération de graphiques dynamiques, consultez [génération de graphiques dynamiques](dynamic-graph-building.md).</span><span class="sxs-lookup"><span data-stu-id="f77ba-109">For more information about dynamic graph building, see [Dynamic Graph Building](dynamic-graph-building.md).</span></span>

## <a name="usage"></a><span data-ttu-id="f77ba-110">Utilisation</span><span class="sxs-lookup"><span data-stu-id="f77ba-110">Usage</span></span>

<span data-ttu-id="f77ba-111">Le filtre Synth permet à l’utilisateur de définir la forme d’onde, la fréquence, le nombre de canaux et d’autres propriétés via la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="f77ba-111">The Synth filter enables the user to set the waveform, frequency, number of channels, and other properties through the property page.</span></span> <span data-ttu-id="f77ba-112">Pour définir le point de terminaison supérieur ou inférieur de la plage de fréquences balayées, maintenez la touche Maj enfoncée tout en réglant le curseur fréquence.</span><span class="sxs-lookup"><span data-stu-id="f77ba-112">To set either the upper or lower endpoint of the swept frequency range, hold down SHIFT while adjusting the frequency slider.</span></span> <span data-ttu-id="f77ba-113">Le filtre prend également en charge une interface personnalisée, ISynth2, pour la définition de ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="f77ba-113">The filter also supports a custom interface, ISynth2, for setting these properties.</span></span>

<span data-ttu-id="f77ba-114">Pour illustrer la fonctionnalité de création de graphique dynamique, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="f77ba-114">To demonstrate the dynamic graph building feature, do the following:</span></span>

1.  <span data-ttu-id="f77ba-115">Générez le filtre et inscrivez-le avec l’utilitaire regsvr32.</span><span class="sxs-lookup"><span data-stu-id="f77ba-115">Build the filter and register it with the Regsvr32 utility.</span></span>
2.  <span data-ttu-id="f77ba-116">Lancez GraphEdit.</span><span class="sxs-lookup"><span data-stu-id="f77ba-116">Launch GraphEdit.</span></span>
3.  <span data-ttu-id="f77ba-117">Insérez le filtre de synthétiseur audio.</span><span class="sxs-lookup"><span data-stu-id="f77ba-117">Insert the Audio Synthesizer filter.</span></span> <span data-ttu-id="f77ba-118">Il apparaît dans la catégorie filtres DirectShow.</span><span class="sxs-lookup"><span data-stu-id="f77ba-118">It appears in the DirectShow Filters category.</span></span>
4.  <span data-ttu-id="f77ba-119">Affichez la broche de sortie du filtre.</span><span class="sxs-lookup"><span data-stu-id="f77ba-119">Render the filter's output pin.</span></span>
5.  <span data-ttu-id="f77ba-120">Cliquez sur le bouton **lecture** .</span><span class="sxs-lookup"><span data-stu-id="f77ba-120">Click the **Play** button.</span></span>
6.  <span data-ttu-id="f77ba-121">Ouvrez la page de propriétés du filtre.</span><span class="sxs-lookup"><span data-stu-id="f77ba-121">Open the filter's property page.</span></span>
7.  <span data-ttu-id="f77ba-122">Dans la zone format de sortie, sélectionnez PCM ou Microsoft ADPCM.</span><span class="sxs-lookup"><span data-stu-id="f77ba-122">In the Output Format area, select PCM or Microsoft ADPCM.</span></span>

## <a name="programming-notes"></a><span data-ttu-id="f77ba-123">Notes de programmation</span><span class="sxs-lookup"><span data-stu-id="f77ba-123">Programming Notes</span></span>

<span data-ttu-id="f77ba-124">Cet exemple contient les fichiers suivants :</span><span class="sxs-lookup"><span data-stu-id="f77ba-124">This sample contains the following files:</span></span>

-   <span data-ttu-id="f77ba-125">Dynsrc. h, dynsrc. cpp : contient deux classes de base pour les filtres sources qui prennent en charge la génération de graphiques dynamiques, CDynamicSource et CDynamicSourceStream.</span><span class="sxs-lookup"><span data-stu-id="f77ba-125">Dynsrc.h, Dynsrc.cpp: Contains two base classes for source filters that support dynamic graph building, CDynamicSource and CDynamicSourceStream.</span></span>
-   <span data-ttu-id="f77ba-126">ISynth. h : déclare l’interface ISynth2 personnalisée pour définir des propriétés sur le filtre.</span><span class="sxs-lookup"><span data-stu-id="f77ba-126">ISynth.h: Declares the custom ISynth2 interface for setting properties on the filter.</span></span>
-   <span data-ttu-id="f77ba-127">Resource. h : contient des constantes de ressource.</span><span class="sxs-lookup"><span data-stu-id="f77ba-127">Resource.h: Contains resource constants.</span></span>
-   <span data-ttu-id="f77ba-128">Synth. def : exporte les fonctions DLL requises par la bibliothèque COM.</span><span class="sxs-lookup"><span data-stu-id="f77ba-128">Synth.def: Exports the DLL functions needed by the COM library.</span></span>
-   <span data-ttu-id="f77ba-129">Synth. h, synth. cpp : contient la classe CAudioSynth, qui génère les données audio et la classe CSynthFilter, qui implémente le filtre.</span><span class="sxs-lookup"><span data-stu-id="f77ba-129">Synth.h, Synth.cpp: Contains the CAudioSynth class, which generates the audio data, and the CSynthFilter class, which implements the filter.</span></span>
-   <span data-ttu-id="f77ba-130">Synth. RC : contient les ressources utilisées par le filtre.</span><span class="sxs-lookup"><span data-stu-id="f77ba-130">Synth.rc: Contains resources used by the filter.</span></span>
-   <span data-ttu-id="f77ba-131">Synthprp. h, Synthprp. cpp : implémente la page de propriétés du filtre.</span><span class="sxs-lookup"><span data-stu-id="f77ba-131">Synthprp.h, Synthprp.cpp: Implements the filter's property page.</span></span>

<span data-ttu-id="f77ba-132">La classe CDynamicSource est adaptée à partir de la classe de base [**CSource**](csource.md) .</span><span class="sxs-lookup"><span data-stu-id="f77ba-132">The CDynamicSource class is adapted from the [**CSource**](csource.md) base class.</span></span> <span data-ttu-id="f77ba-133">Elle utilise une ou plusieurs broches de sortie dérivées de la classe CDynamicSourceStream.</span><span class="sxs-lookup"><span data-stu-id="f77ba-133">It uses one or more output pins derived from the CDynamicSourceStream class.</span></span> <span data-ttu-id="f77ba-134">La classe CDynamicSourceStream est adaptée à partir de la classe [**CSourceStream**](csourcestream.md) , mais dérive de la classe [**CDynamicOutputPin**](cdynamicoutputpin.md) plutôt que de la classe [**CBaseOutputPin**](cbaseoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="f77ba-134">The CDynamicSourceStream class is adapted from the [**CSourceStream**](csourcestream.md) class, but derives from the [**CDynamicOutputPin**](cdynamicoutputpin.md) class rather than the [**CBaseOutputPin**](cbaseoutputpin.md) class.</span></span>

<span data-ttu-id="f77ba-135">Les méthodes suivantes de la classe CDynamicSource sont introuvables dans [**CSource**](csource.md):</span><span class="sxs-lookup"><span data-stu-id="f77ba-135">The CDynamicSource class has the following methods not found in [**CSource**](csource.md):</span></span>

-   <span data-ttu-id="f77ba-136">Stop : signale l’événement Stop ([**CDynamicOutputPin :: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md)) et arrête le thread de travail pour tous les codes confidentiels non connectés.</span><span class="sxs-lookup"><span data-stu-id="f77ba-136">Stop: Signals the stop event ([**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md)), and shuts down the worker thread for all unconnected pins.</span></span> <span data-ttu-id="f77ba-137">Sur un code confidentiel connecté, la méthode inactive du pin arrête le thread de travail.</span><span class="sxs-lookup"><span data-stu-id="f77ba-137">On a connected pin, the pin's Inactive method will shut down the worker thread.</span></span>
-   <span data-ttu-id="f77ba-138">Pause : réinitialise l’événement d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="f77ba-138">Pause: Resets the stop event.</span></span>
-   <span data-ttu-id="f77ba-139">JoinFilterGraph : appelle la méthode [**CDynamicOutputPin :: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) sur chaque pin.</span><span class="sxs-lookup"><span data-stu-id="f77ba-139">JoinFilterGraph: Calls the [**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) method on each pin.</span></span>

<span data-ttu-id="f77ba-140">Les méthodes suivantes de la classe CDynamicSourceStream sont introuvables dans [**CSourceStream**](csourcestream.md):</span><span class="sxs-lookup"><span data-stu-id="f77ba-140">The CDynamicSourceStream class has the following methods not found in [**CSourceStream**](csourcestream.md):</span></span>

-   <span data-ttu-id="f77ba-141">DestroySourceThread : arrête le thread de travail.</span><span class="sxs-lookup"><span data-stu-id="f77ba-141">DestroySourceThread: Shuts down the worker thread.</span></span>
-   <span data-ttu-id="f77ba-142">FatalError : signale une erreur au gestionnaire de graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="f77ba-142">FatalError: Signals an error to the filter graph manager.</span></span>
-   <span data-ttu-id="f77ba-143">OutputPinNeedsToBeReconnected : signale que la broche de sortie doit être reconnectée.</span><span class="sxs-lookup"><span data-stu-id="f77ba-143">OutputPinNeedsToBeReconnected: Signals that the output pin should be reconnected.</span></span> <span data-ttu-id="f77ba-144">Lorsque cette méthode est appelée, le thread de travail appelle la méthode [**CDynamicOutputPin ::D ynamicreconnect**](cdynamicoutputpin-dynamicreconnect.md) pour reconnecter le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="f77ba-144">When this method is called, the worker thread calls the [**CDynamicOutputPin::DynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md) method to reconnect the pin.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="f77ba-145">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="f77ba-145">Downloading the Sample</span></span>

<span data-ttu-id="f77ba-146">Pour télécharger les exemples du kit de développement logiciel (SDK) DirectShow, installez la dernière version du [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f77ba-146">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="f77ba-147">Cet exemple est installé sous le chemin d’accès suivant : exemples *\[ racine \] du kit de développement logiciel (SDK)* \\ \\ fichiers multimédias de \\ \\ filtres DirectShow \\ .</span><span class="sxs-lookup"><span data-stu-id="f77ba-147">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\Synth.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f77ba-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f77ba-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f77ba-149">Exemples DirectShow</span><span class="sxs-lookup"><span data-stu-id="f77ba-149">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



