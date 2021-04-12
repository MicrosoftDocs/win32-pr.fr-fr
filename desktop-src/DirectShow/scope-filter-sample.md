---
description: Exemple de filtre d’étendue
ms.assetid: f967d4c7-94d2-440b-9e52-423feefec66d
title: Exemple de filtre d’étendue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f74ba823e68da1cd1faadd3e1e3acc4e613e2f42
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481520"
---
# <a name="scope-filter-sample"></a><span data-ttu-id="c71a1-103">Exemple de filtre d’étendue</span><span class="sxs-lookup"><span data-stu-id="c71a1-103">Scope Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="c71a1-104">Description</span><span class="sxs-lookup"><span data-stu-id="c71a1-104">Description</span></span>

<span data-ttu-id="c71a1-105">Le filtre d’étendue est un filtre de convertisseur qui affiche des données audio sous forme de formes Wave.</span><span class="sxs-lookup"><span data-stu-id="c71a1-105">The Scope filter is a renderer filter that displays sound data as wave forms.</span></span>

## <a name="usage"></a><span data-ttu-id="c71a1-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="c71a1-106">Usage</span></span>

<span data-ttu-id="c71a1-107">Pour utiliser ce filtre, ouvrez GraphEdit et affichez un fichier audio (ou un fichier vidéo avec un flux audio).</span><span class="sxs-lookup"><span data-stu-id="c71a1-107">To use this filter, open GraphEdit and render an audio file (or a video file with an audio stream).</span></span> <span data-ttu-id="c71a1-108">Déconnectez le convertisseur audio temporairement et insérez l’exemple de filtre Infinite-Pin tee ([exemple de filtre InfTee](inftee-filter-sample.md)).</span><span class="sxs-lookup"><span data-stu-id="c71a1-108">Disconnect the audio renderer temporarily and insert the Infinite-Pin Tee ([InfTee Filter Sample](inftee-filter-sample.md)) sample filter.</span></span> <span data-ttu-id="c71a1-109">Reconnectez le convertisseur audio.</span><span class="sxs-lookup"><span data-stu-id="c71a1-109">Reconnect the audio renderer.</span></span> <span data-ttu-id="c71a1-110">Connectez ensuite la deuxième broche de sortie du filtre de l' Infinite-Pin tee au filtre d’étendue.</span><span class="sxs-lookup"><span data-stu-id="c71a1-110">Then connect the Infinite-Pin Tee filter's second output pin to the Scope filter.</span></span> <span data-ttu-id="c71a1-111">Exécutez maintenant le graphique.</span><span class="sxs-lookup"><span data-stu-id="c71a1-111">Now run the graph.</span></span>

<span data-ttu-id="c71a1-112">La fenêtre d’étendue est implémentée en tant que boîte de dialogue, et non en tant que fenêtre réelle.</span><span class="sxs-lookup"><span data-stu-id="c71a1-112">The Scope window is implemented as a dialog box, not as an actual window.</span></span> <span data-ttu-id="c71a1-113">Les développeurs qui créent des panneaux de contrôle pour modifier les paramètres de filtre en temps réel peuvent souhaiter utiliser une technique comme celle-ci plutôt que des pages de propriétés.</span><span class="sxs-lookup"><span data-stu-id="c71a1-113">Developers creating control panels to alter filter parameters in real time might want to use a technique like this rather than property pages.</span></span>

<span data-ttu-id="c71a1-114">Le filtre d’étendue illustre la configuration d’un thread distinct pour traiter les données.</span><span class="sxs-lookup"><span data-stu-id="c71a1-114">The Scope filter demonstrates setting up a separate thread to process data.</span></span> <span data-ttu-id="c71a1-115">Dans ce cas, les données sont simplement copiées dans une mémoire tampon distincte sur la méthode [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) , puis sont dessinées dans la fenêtre d’étendue sur le thread distinct.</span><span class="sxs-lookup"><span data-stu-id="c71a1-115">In this case, the data is just copied to a separate buffer on the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method, and is then drawn on the Scope window on the separate thread.</span></span>

<span data-ttu-id="c71a1-116">Le filtre d’étendue vous permet également de surveiller la sortie audio pour déterminer si vous découpez, afin de pouvoir ajuster le gain.</span><span class="sxs-lookup"><span data-stu-id="c71a1-116">The Scope filter also enables you to monitor audio output to determine if you are clipping, so you can adjust the gain.</span></span>

<span data-ttu-id="c71a1-117">Ce filtre apparaît dans GraphEdit sous le titre « oscilloscope ».</span><span class="sxs-lookup"><span data-stu-id="c71a1-117">This filter appears in GraphEdit as "Oscilloscope."</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="c71a1-118">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="c71a1-118">Downloading the Sample</span></span>

<span data-ttu-id="c71a1-119">Pour télécharger les exemples du kit de développement logiciel (SDK) DirectShow, installez la dernière version du [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c71a1-119">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="c71a1-120">Cet exemple est installé sous le chemin d’accès suivant : exemples *\[ racine \] SDK* \\ étendue des \\ \\ \\ filtres DirectShow \\ .</span><span class="sxs-lookup"><span data-stu-id="c71a1-120">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\Scope.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c71a1-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c71a1-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c71a1-122">Exemples DirectShow</span><span class="sxs-lookup"><span data-stu-id="c71a1-122">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



