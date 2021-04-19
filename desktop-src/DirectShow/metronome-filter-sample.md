---
description: Exemple de filtre métronome
ms.assetid: bb279898-875a-4ce4-ac69-6c58f640fbbd
title: Exemple de filtre métronome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 361b46aafa84590243cfcc05445d91a56ce56e83
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514718"
---
# <a name="metronome-filter-sample"></a><span data-ttu-id="c6daa-103">Exemple de filtre métronome</span><span class="sxs-lookup"><span data-stu-id="c6daa-103">Metronome Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="c6daa-104">Description</span><span class="sxs-lookup"><span data-stu-id="c6daa-104">Description</span></span>

<span data-ttu-id="c6daa-105">Cet exemple de filtre montre comment implémenter une horloge de référence.</span><span class="sxs-lookup"><span data-stu-id="c6daa-105">This sample filter shows how to implement a reference clock.</span></span> <span data-ttu-id="c6daa-106">Le filtre utilise votre entrée de microphone par défaut pour écouter les pics audio (tels que les clics, les clapss de main ou les toux) qu’il utilise pour déterminer une fréquence d’horloge.</span><span class="sxs-lookup"><span data-stu-id="c6daa-106">The filter uses your default microphone input to listen for audio spikes (such as clicks, hand claps, or coughs), which it uses to determine a clock rate.</span></span>

## <a name="usage"></a><span data-ttu-id="c6daa-107">Utilisation</span><span class="sxs-lookup"><span data-stu-id="c6daa-107">Usage</span></span>

<span data-ttu-id="c6daa-108">Générez l’exemple de projet et copiez la DLL de filtre (Metronom.ax) dans le répertoire système de Windows.</span><span class="sxs-lookup"><span data-stu-id="c6daa-108">Build the sample project and copy the filter DLL (Metronom.ax) to your Windows system directory.</span></span> <span data-ttu-id="c6daa-109">Exécutez le fichier métronome. reg pour inscrire la DLL.</span><span class="sxs-lookup"><span data-stu-id="c6daa-109">Run the Metronom.reg file to register the DLL.</span></span>

<span data-ttu-id="c6daa-110">Pour utiliser le filtre :</span><span class="sxs-lookup"><span data-stu-id="c6daa-110">To use the filter:</span></span>

1.  <span data-ttu-id="c6daa-111">Générez un graphique de filtre dans GraphEdit qui restitue un flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="c6daa-111">Build a filter graph in GraphEdit that renders a video stream.</span></span>
2.  <span data-ttu-id="c6daa-112">Supprimez tous les flux audio rendus.</span><span class="sxs-lookup"><span data-stu-id="c6daa-112">Delete any rendered audio streams.</span></span>
3.  <span data-ttu-id="c6daa-113">Ajoutez le filtre métronome au graphique.</span><span class="sxs-lookup"><span data-stu-id="c6daa-113">Add the Metronome filter to the graph.</span></span> <span data-ttu-id="c6daa-114">Il apparaît dans la catégorie filtres DirectShow.</span><span class="sxs-lookup"><span data-stu-id="c6daa-114">It appears in the DirectShow Filters category.</span></span>
4.  <span data-ttu-id="c6daa-115">Exécutez le graphique.</span><span class="sxs-lookup"><span data-stu-id="c6daa-115">Run the graph.</span></span> <span data-ttu-id="c6daa-116">La vidéo commence à s’exécuter à la vitesse normale.</span><span class="sxs-lookup"><span data-stu-id="c6daa-116">The video will begin playing at normal speed.</span></span>
5.  <span data-ttu-id="c6daa-117">Clap vos mains ou utilisez un métronome pour définir une nouvelle vitesse.</span><span class="sxs-lookup"><span data-stu-id="c6daa-117">Clap your hands or use a metronome to set a new speed.</span></span>

## <a name="programming-notes"></a><span data-ttu-id="c6daa-118">Notes de programmation</span><span class="sxs-lookup"><span data-stu-id="c6daa-118">Programming Notes</span></span>

<span data-ttu-id="c6daa-119">Ce filtre fonctionne uniquement pour la vidéo.</span><span class="sxs-lookup"><span data-stu-id="c6daa-119">This filter works only for video.</span></span> <span data-ttu-id="c6daa-120">Le convertisseur audio ne peut pas se synchroniser à des fréquences d’horloge radicalement différentes.</span><span class="sxs-lookup"><span data-stu-id="c6daa-120">The audio renderer is not capable of synchronizing to radically different clock rates.</span></span>

<span data-ttu-id="c6daa-121">Si vous Clap 92 fois par minute (une fois toutes les ~ 652 ms), la vidéo est lue au taux normal.</span><span class="sxs-lookup"><span data-stu-id="c6daa-121">If you clap 92 times per minute (once every ~652 ms), the video will play at the normal rate.</span></span> <span data-ttu-id="c6daa-122">Vous pouvez modifier ce paramètre par défaut en modifiant la valeur de la constante `BPM` dans métronome. cpp.</span><span class="sxs-lookup"><span data-stu-id="c6daa-122">You can change this default by changing the value of the constant `BPM` in Metronom.cpp.</span></span>

<span data-ttu-id="c6daa-123">Si vous arrêtez applaudissements pendant un certain temps, puis redémarrez applaudissements, vous devez redémarrer à peu près la même vitesse ou le filtre l’ignore.</span><span class="sxs-lookup"><span data-stu-id="c6daa-123">If you stop clapping for a period of time and then start clapping again, you must start again at approximately the same speed, or the filter will ignore it.</span></span> <span data-ttu-id="c6daa-124">En outre, la vitesse de lecture de la vidéo est limitée par la vitesse du processeur.</span><span class="sxs-lookup"><span data-stu-id="c6daa-124">Also, the video playback rate is limited by the CPU speed.</span></span> <span data-ttu-id="c6daa-125">Si vous dépassez la limite pour une durée quelconque, le filtre ne répondra plus aux changements de taux.</span><span class="sxs-lookup"><span data-stu-id="c6daa-125">If you exceed the limit for any length of time, the filter will stop responding to rate changes.</span></span> <span data-ttu-id="c6daa-126">Dans ce cas, arrêtez le graphique et redémarrez.</span><span class="sxs-lookup"><span data-stu-id="c6daa-126">If this happens, stop the graph and restart.</span></span>

<span data-ttu-id="c6daa-127">Si vous implémentez votre propre horloge, les règles les plus importantes sont que les horloges de référence ne doivent pas revenir en arrière.</span><span class="sxs-lookup"><span data-stu-id="c6daa-127">If you implement your own clock, the most important rules is that reference clocks must not go backward.</span></span> <span data-ttu-id="c6daa-128">Autrement dit, ils ne doivent jamais signaler une valeur d’heure inférieure à la valeur d’heure précédente.</span><span class="sxs-lookup"><span data-stu-id="c6daa-128">That is, they must never report a time value less than the previous time value.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="c6daa-129">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="c6daa-129">Downloading the Sample</span></span>

<span data-ttu-id="c6daa-130">Pour télécharger les exemples du kit de développement logiciel (SDK) DirectShow, installez la dernière version du [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c6daa-130">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="c6daa-131">Cet exemple est installé sous le chemin d’accès suivant : exemples *\[ racine \] SDK* \\ exemples de \\ \\ filtres DirectShow multimédias \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="c6daa-131">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\Metronome.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6daa-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c6daa-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6daa-133">**CBaseReferenceClock, classe**</span><span class="sxs-lookup"><span data-stu-id="c6daa-133">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> <dt>

[<span data-ttu-id="c6daa-134">Exemples DirectShow</span><span class="sxs-lookup"><span data-stu-id="c6daa-134">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



