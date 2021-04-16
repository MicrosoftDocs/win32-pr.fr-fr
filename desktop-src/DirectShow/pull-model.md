---
description: Modèle d’extraction
ms.assetid: b5246dfe-e6ee-4b91-bfe3-2ec8b8723938
title: Modèle d’extraction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd4becd54bffb39acf30b6d29fca45e6a117989
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521343"
---
# <a name="pull-model"></a><span data-ttu-id="785bb-103">Modèle d’extraction</span><span class="sxs-lookup"><span data-stu-id="785bb-103">Pull Model</span></span>

<span data-ttu-id="785bb-104">Dans l’interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) , le filtre amont détermine les données à envoyer et envoie les données vers le filtre en aval.</span><span class="sxs-lookup"><span data-stu-id="785bb-104">In the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface, the upstream filter determines what data to send, and it pushes the data to the downstream filter.</span></span> <span data-ttu-id="785bb-105">Pour certains filtres, un modèle d' *extraction* est plus approprié.</span><span class="sxs-lookup"><span data-stu-id="785bb-105">For some filters, a *pull* model is more appropriate.</span></span> <span data-ttu-id="785bb-106">Ici, le filtre en aval demande des données à partir du filtre en amont.</span><span class="sxs-lookup"><span data-stu-id="785bb-106">Here, the downstream filter requests data from the upstream filter.</span></span> <span data-ttu-id="785bb-107">Les échantillons sont toujours en aval, de la broche de sortie à la broche d’entrée, mais le filtre en aval lance le Workflow.</span><span class="sxs-lookup"><span data-stu-id="785bb-107">Samples still travel downstream, from output pin to input pin, but the downstream filter initiates the data flow.</span></span> <span data-ttu-id="785bb-108">Ce type de connexion utilise l’interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .</span><span class="sxs-lookup"><span data-stu-id="785bb-108">This type of connection uses the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span>

<span data-ttu-id="785bb-109">Le modèle d’extraction est généralement utilisé pour la lecture de fichiers.</span><span class="sxs-lookup"><span data-stu-id="785bb-109">The typical use for the pull model is in file playback.</span></span> <span data-ttu-id="785bb-110">Par exemple, dans un graphique de lecture AVI, le filtre de [source de fichier Async](file-source--async--filter.md) effectue des opérations de lecture de fichier génériques et remet les données sous forme de flux d’octets, sans informations de mise en forme.</span><span class="sxs-lookup"><span data-stu-id="785bb-110">For example, in an AVI playback graph, the [Async File Source](file-source--async--filter.md) filter performs generic file reading operations and delivers the data as a byte stream, with no format information.</span></span> <span data-ttu-id="785bb-111">Le filtre de [séparateur AVI](avi-splitter-filter.md) lit les en-têtes AVI et analyse le flux dans des exemples vidéo et audio.</span><span class="sxs-lookup"><span data-stu-id="785bb-111">The [AVI Splitter](avi-splitter-filter.md) filter reads the AVI headers and parses the stream into video and audio samples.</span></span> <span data-ttu-id="785bb-112">Le séparateur AVI peut déterminer les données dont il a besoin mieux que le filtre de source de fichier Async, et utilise donc **IAsyncReader** au lieu de **IMemInputPin**.</span><span class="sxs-lookup"><span data-stu-id="785bb-112">The AVI Splitter can determine what data it needs better than the Async File Source filter, and therefore it uses **IAsyncReader** instead of **IMemInputPin**.</span></span>

<span data-ttu-id="785bb-113">Pour demander des données à partir de la broche de sortie, la broche d’entrée appelle l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="785bb-113">To request data from the output pin, the input pin calls one of the following methods:</span></span>

-   [<span data-ttu-id="785bb-114">**IAsyncReader :: Request**</span><span class="sxs-lookup"><span data-stu-id="785bb-114">**IAsyncReader::Request**</span></span>](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request)
-   [<span data-ttu-id="785bb-115">**IAsyncReader::SyncRead**</span><span class="sxs-lookup"><span data-stu-id="785bb-115">**IAsyncReader::SyncRead**</span></span>](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncread)
-   <span data-ttu-id="785bb-116">[**IAsyncReader :: SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned).</span><span class="sxs-lookup"><span data-stu-id="785bb-116">[**IAsyncReader::SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned).</span></span>

<span data-ttu-id="785bb-117">La première méthode est asynchrone, pour prendre en charge plusieurs lectures avec chevauchement.</span><span class="sxs-lookup"><span data-stu-id="785bb-117">The first method is asynchronous, to support multiple overlapped reads.</span></span> <span data-ttu-id="785bb-118">Les autres sont synchrones.</span><span class="sxs-lookup"><span data-stu-id="785bb-118">The others are synchronous.</span></span>

<span data-ttu-id="785bb-119">En théorie, tout filtre peut prendre en charge **IAsyncReader**, mais dans la pratique il est conçu pour les filtres sources qui se connectent aux filtres de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="785bb-119">In theory, any filter can support **IAsyncReader**, but in practice it is designed for source filters that connect to parser filters.</span></span> <span data-ttu-id="785bb-120">L’analyseur fonctionne très bien comme un filtre source dans le modèle push.</span><span class="sxs-lookup"><span data-stu-id="785bb-120">The parser acts very much like a source filter in the push model.</span></span> <span data-ttu-id="785bb-121">Lorsqu’il est suspendu, il crée un thread de streaming qui extrait les données de la connexion **IAsyncReader** et les pousse en aval.</span><span class="sxs-lookup"><span data-stu-id="785bb-121">When it pauses, it creates a streaming thread that pulls data from the **IAsyncReader** connection and pushes it downstream.</span></span> <span data-ttu-id="785bb-122">Les broches de sortie utilisent **IMemInputPin** et le reste du graphique utilise le modèle push standard.</span><span class="sxs-lookup"><span data-stu-id="785bb-122">The output pins use **IMemInputPin**, and the rest of the graph uses the standard push model.</span></span>

## <a name="related-topics"></a><span data-ttu-id="785bb-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="785bb-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="785bb-124">Data Flow dans le graphique de filtre</span><span class="sxs-lookup"><span data-stu-id="785bb-124">Data Flow in the Filter Graph</span></span>](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



