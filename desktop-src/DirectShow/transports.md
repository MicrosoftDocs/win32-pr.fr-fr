---
description: Transports
ms.assetid: 63c5ff5b-293d-4a80-92e8-3ece41321095
title: Transports
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3d87ffacc871fc45ef1e8e645849afc956fb1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519943"
---
# <a name="transports"></a><span data-ttu-id="a306e-103">Transports</span><span class="sxs-lookup"><span data-stu-id="a306e-103">Transports</span></span>

<span data-ttu-id="a306e-104">Pour déplacer des données multimédias via le graphique de filtre, un filtre DirectShow doit prendre en charge l’un des différents protocoles possibles.</span><span class="sxs-lookup"><span data-stu-id="a306e-104">In order to move media data through the filter graph, a DirectShow filter must support one of several possible protocols.</span></span> <span data-ttu-id="a306e-105">Ces protocoles sont appelés transports.</span><span class="sxs-lookup"><span data-stu-id="a306e-105">These protocols are called transports.</span></span> <span data-ttu-id="a306e-106">Lorsque deux filtres se connectent, ils doivent prendre en charge le même transport. dans le cas contraire, ils ne peuvent pas échanger de données multimédias.</span><span class="sxs-lookup"><span data-stu-id="a306e-106">When two filters connect, they must support the same transport; otherwise they cannot exchange media data.</span></span> <span data-ttu-id="a306e-107">En règle générale, un transport requiert que l’un des codes confidentiels prenne en charge une interface particulière.</span><span class="sxs-lookup"><span data-stu-id="a306e-107">Typically, a transport requires that one of the pins support a particular interface.</span></span> <span data-ttu-id="a306e-108">Lorsque les filtres se connectent, un code confidentiel interroge l’autre pour l’interface.</span><span class="sxs-lookup"><span data-stu-id="a306e-108">When the filters connect, one pin queries the other for the interface.</span></span>

<span data-ttu-id="a306e-109">La plupart des filtres DirectShow contiennent les données multimédias dans la mémoire principale et les transmettent à d’autres filtres sur les connexions de code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="a306e-109">Most DirectShow filters hold media data in main memory, and deliver it to other filters across pin connections.</span></span> <span data-ttu-id="a306e-110">Ce type de transport est appelé transport de mémoire locale.</span><span class="sxs-lookup"><span data-stu-id="a306e-110">This type of transport is called local memory transport.</span></span> <span data-ttu-id="a306e-111">Bien que le transport de mémoire locale soit le transport le plus courant dans DirectShow, tous les filtres ne l’utilisent pas.</span><span class="sxs-lookup"><span data-stu-id="a306e-111">Although local memory transport is the most common transport in DirectShow, not all filters use it.</span></span> <span data-ttu-id="a306e-112">Par exemple, certains filtres envoient des données multimédias le long d’un chemin d’accès matériel et utilisent des broches uniquement pour fournir des informations de contrôle.</span><span class="sxs-lookup"><span data-stu-id="a306e-112">For example, some filters send media data along a hardware path, and use pins only to deliver control information.</span></span> <span data-ttu-id="a306e-113">Par exemple, consultez l’interface [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) .</span><span class="sxs-lookup"><span data-stu-id="a306e-113">For example, see the [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) interface.</span></span>

<span data-ttu-id="a306e-114">DirectShow définit deux mécanismes pour le transport de mémoire locale, le modèle push et le modèle pull.</span><span class="sxs-lookup"><span data-stu-id="a306e-114">DirectShow defines two mechanisms for local memory transport, the push model and the pull model.</span></span> <span data-ttu-id="a306e-115">Dans le modèle push, un filtre source génère des données et les remet au filtre suivant en aval.</span><span class="sxs-lookup"><span data-stu-id="a306e-115">In the push model, a source filter generates data and delivers it to the next filter downstream.</span></span> <span data-ttu-id="a306e-116">Ce filtre reçoit passivement les données, les traite, puis les envoie en aval.</span><span class="sxs-lookup"><span data-stu-id="a306e-116">That filter passively receives the data, processes it, and sends it further downstream.</span></span> <span data-ttu-id="a306e-117">Dans le modèle d’extraction, le filtre source est connecté à un filtre d’analyseur.</span><span class="sxs-lookup"><span data-stu-id="a306e-117">In the pull model, the source filter is connected to a parser filter.</span></span> <span data-ttu-id="a306e-118">Le filtre de l’analyseur demande des données à partir du filtre source.</span><span class="sxs-lookup"><span data-stu-id="a306e-118">The parser filter requests data from the source filter.</span></span> <span data-ttu-id="a306e-119">Le filtre source répond aux demandes en livrant des données.</span><span class="sxs-lookup"><span data-stu-id="a306e-119">The source filter responds to the requests by delivering data.</span></span> <span data-ttu-id="a306e-120">Le modèle d’émission utilise l’interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) , et le modèle d’extraction utilise l’interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .</span><span class="sxs-lookup"><span data-stu-id="a306e-120">The push model uses the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface, and the pull model uses the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span>

<span data-ttu-id="a306e-121">Le modèle push est plus courant que le modèle d’extraction.</span><span class="sxs-lookup"><span data-stu-id="a306e-121">The push model is more common than the pull model.</span></span> <span data-ttu-id="a306e-122">Par conséquent, les articles qui suivent supposent un modèle push.</span><span class="sxs-lookup"><span data-stu-id="a306e-122">Therefore, the articles that follow assume a push model.</span></span> <span data-ttu-id="a306e-123">Le dernier article de cette section, [pull Model](pull-model.md), décrit comment l’interface **IAsyncReader** diffère de **IMemInputPin**.</span><span class="sxs-lookup"><span data-stu-id="a306e-123">The last article in this section, [Pull Model](pull-model.md), describes how the **IAsyncReader** interface differs from **IMemInputPin**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a306e-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a306e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a306e-125">Data Flow dans le graphique de filtre</span><span class="sxs-lookup"><span data-stu-id="a306e-125">Data Flow in the Filter Graph</span></span>](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



