---
description: Exemple de filtre dump
ms.assetid: 2ce52e6c-a02f-4737-822a-87b2cf2d933d
title: Exemple de filtre dump
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd64d1f16b0b504743890543b617a24df6bbaab8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522415"
---
# <a name="dump-filter-sample"></a><span data-ttu-id="91a72-103">Exemple de filtre dump</span><span class="sxs-lookup"><span data-stu-id="91a72-103">Dump Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="91a72-104">Description</span><span class="sxs-lookup"><span data-stu-id="91a72-104">Description</span></span>

<span data-ttu-id="91a72-105">Le filtre de vidage est un filtre de convertisseur qui écrit les exemples de supports qu’il reçoit dans un fichier texte.</span><span class="sxs-lookup"><span data-stu-id="91a72-105">The Dump Filter is a renderer filter that writes the media samples it receives to a text file.</span></span>

<span data-ttu-id="91a72-106">Cet exemple illustre l’utilisation de la classe de filtre de base [**CBaseFilter**](cbasefilter.md) et de la classe de code confidentiel d’entrée rendue [**CRenderedInputPin**](crenderedinputpin.md).</span><span class="sxs-lookup"><span data-stu-id="91a72-106">This sample illustrates how to use the base filter class [**CBaseFilter**](cbasefilter.md) and the rendered input pin class [**CRenderedInputPin**](crenderedinputpin.md).</span></span> <span data-ttu-id="91a72-107">Il montre également comment implémenter l’interface [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) .</span><span class="sxs-lookup"><span data-stu-id="91a72-107">It also demonstrates how to implement the [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) interface.</span></span> <span data-ttu-id="91a72-108">Le filtre de vidage a une seule broche d’entrée, qui écrit chaque exemple qu’il reçoit directement dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="91a72-108">The Dump filter has a single input pin, which writes every sample that it receives directly to a file.</span></span>

## <a name="usage"></a><span data-ttu-id="91a72-109">Utilisation</span><span class="sxs-lookup"><span data-stu-id="91a72-109">Usage</span></span>

<span data-ttu-id="91a72-110">Ce filtre est un outil de débogage utile.</span><span class="sxs-lookup"><span data-stu-id="91a72-110">This filter is a useful debugging tool.</span></span> <span data-ttu-id="91a72-111">Par exemple, vous pouvez vérifier, bit par bit, les résultats d’un filtre de transformation.</span><span class="sxs-lookup"><span data-stu-id="91a72-111">For example, you can verify, bit by bit, the results of a transform filter.</span></span> <span data-ttu-id="91a72-112">Vous pouvez créer un graphique manuellement à l’aide de GraphEdit et connecter le filtre de vidage à la sortie d’un filtre de transformation ou de toute autre broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="91a72-112">You can build a graph manually by using GraphEdit, and connect the Dump filter to the output of a transform filter or any other output pin.</span></span> <span data-ttu-id="91a72-113">Vous pouvez également connecter un filtre tee et placer le filtre de vidage sur une des jambes du filtre tee et la sortie standard sur une autre jambe pour analyser les résultats dans un scénario en temps réel.</span><span class="sxs-lookup"><span data-stu-id="91a72-113">You can also connect a tee filter and put the Dump filter on one leg of the tee filter and the typical output on another leg to monitor the results in a real-time scenario.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="91a72-114">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="91a72-114">Downloading the Sample</span></span>

<span data-ttu-id="91a72-115">Pour télécharger les exemples du kit de développement logiciel (SDK) DirectShow, installez la dernière version du [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="91a72-115">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="91a72-116">Cet exemple est installé sous le chemin d’accès suivant : exemples *\[ racine \] du kit de développement logiciel (SDK)* \\ \\ fichiers multimédias \\ \\ filtres DirectShow \\ dump.</span><span class="sxs-lookup"><span data-stu-id="91a72-116">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\Dump.</span></span>

## <a name="related-topics"></a><span data-ttu-id="91a72-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="91a72-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91a72-118">Exemples DirectShow</span><span class="sxs-lookup"><span data-stu-id="91a72-118">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



