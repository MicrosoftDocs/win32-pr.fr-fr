---
description: Exemple de filtre balle
ms.assetid: 80a6db64-ef13-46a2-8f2a-e39095e874b2
title: Exemple de filtre balle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b80301b233f0c1e74933c93fe86a0e1878458e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846730"
---
# <a name="ball-filter-sample"></a><span data-ttu-id="c9994-103">Exemple de filtre balle</span><span class="sxs-lookup"><span data-stu-id="c9994-103">Ball Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="c9994-104">Description</span><span class="sxs-lookup"><span data-stu-id="c9994-104">Description</span></span>

<span data-ttu-id="c9994-105">Le filtre boule est un filtre de source vidéo qui produit une image d’une balle rebondissante.</span><span class="sxs-lookup"><span data-stu-id="c9994-105">The Ball Filter is a video source filter that produces an image of a bouncing ball.</span></span> <span data-ttu-id="c9994-106">Cet exemple illustre la négociation de format et l’utilisation des classes de base de filtre source [**CSource**](csource.md) et [**CSourceStream**](csourcestream.md).</span><span class="sxs-lookup"><span data-stu-id="c9994-106">This sample illustrates format negotiation and the use of the source filter base classes [**CSource**](csource.md) and [**CSourceStream**](csourcestream.md).</span></span>

<span data-ttu-id="c9994-107">Le code dans Fball. h et Fball. cpp gère les interfaces de filtre.</span><span class="sxs-lookup"><span data-stu-id="c9994-107">The code in Fball.h and Fball.cpp manages the filter interfaces.</span></span> <span data-ttu-id="c9994-108">Ces deux fichiers contiennent approximativement le code minimum requis pour un filtre source.</span><span class="sxs-lookup"><span data-stu-id="c9994-108">Those two files contain approximately the minimum code required for a source filter.</span></span> <span data-ttu-id="c9994-109">Les fichiers ball. h et ball. cpp contiennent le code qui rebondit la balle.</span><span class="sxs-lookup"><span data-stu-id="c9994-109">The Ball.h and Ball.cpp files contain the code that bounces the ball.</span></span>

<span data-ttu-id="c9994-110">Ce filtre a une seule broche de sortie, qui fournit un flux vidéo qui montre une balle dans le cadre.</span><span class="sxs-lookup"><span data-stu-id="c9994-110">This filter has a single output pin, which provides a video stream that shows a ball bouncing around in the frame.</span></span> <span data-ttu-id="c9994-111">Le filtre boule accepte également les demandes de gestion de la qualité du filtre en aval, qui illustre une stratégie de gestion de la qualité simple.</span><span class="sxs-lookup"><span data-stu-id="c9994-111">The Ball filter also accepts quality management requests from the downstream filter, which illustrates a simple quality management strategy.</span></span> <span data-ttu-id="c9994-112">Ce filtre implémente l’interface [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) à cet effet.</span><span class="sxs-lookup"><span data-stu-id="c9994-112">This filter implements the [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) interface for that purpose.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="c9994-113">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="c9994-113">Downloading the Sample</span></span>

<span data-ttu-id="c9994-114">Pour télécharger les exemples du kit de développement logiciel (SDK) DirectShow, installez la dernière version du [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c9994-114">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="c9994-115">Cet exemple est installé sous le chemin d’accès suivant : \[ exemples *racine SDK* \] \\ \\ \\ filtres DirectShow multimédias \\ \\ balle.</span><span class="sxs-lookup"><span data-stu-id="c9994-115">This sample is installed under the following path: \[*SDK Root*\]\\Samples\\Multimedia\\DirectShow\\Filters\\Ball.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9994-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c9994-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9994-117">Exemples DirectShow</span><span class="sxs-lookup"><span data-stu-id="c9994-117">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



