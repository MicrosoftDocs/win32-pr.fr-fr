---
description: Cherche
ms.assetid: ceccb657-f1e1-4d59-920a-477a95b8a1a4
title: Cherche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ef7e82009198a790d5c0f7818599aa13905ce82
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104570043"
---
# <a name="seeking"></a><span data-ttu-id="41f28-103">Cherche</span><span class="sxs-lookup"><span data-stu-id="41f28-103">Seeking</span></span>

<span data-ttu-id="41f28-104">Les filtres prennent en charge la recherche par le biais de l’interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) .</span><span class="sxs-lookup"><span data-stu-id="41f28-104">Filters support seeking through the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface.</span></span> <span data-ttu-id="41f28-105">L’application interroge le gestionnaire du graphique de filtre pour **IMediaSeeking** et l’utilise pour émettre des commandes de recherche.</span><span class="sxs-lookup"><span data-stu-id="41f28-105">The application queries the Filter Graph Manager for **IMediaSeeking** and uses it to issue seek commands.</span></span> <span data-ttu-id="41f28-106">Le gestionnaire de graphes de filtre distribue chaque commande de recherche à tous les filtres de convertisseur du graphique.</span><span class="sxs-lookup"><span data-stu-id="41f28-106">The Filter Graph Manager distributes each seek command to all of the renderer filters in the graph.</span></span> <span data-ttu-id="41f28-107">Chaque convertisseur transmet la commande en amont, via les broches de sortie des filtres en amont, jusqu’à ce qu’elle atteigne un filtre qui peut exécuter la recherche.</span><span class="sxs-lookup"><span data-stu-id="41f28-107">Each renderer passes the command upstream, through the output pins of the upstream filters, until it reaches a filter that can execute the seek.</span></span> <span data-ttu-id="41f28-108">En général, un filtre source ou un filtre d’analyseur, tel que le [séparateur AVI](avi-splitter-filter.md), effectue l’opération de recherche.</span><span class="sxs-lookup"><span data-stu-id="41f28-108">Typically a source filter or parser filter, such as the [AVI Splitter](avi-splitter-filter.md), carries out the seek operation.</span></span>

<span data-ttu-id="41f28-109">Lorsqu’un filtre effectue une opération de recherche, il vide toutes les données en attente.</span><span class="sxs-lookup"><span data-stu-id="41f28-109">When a filter performs a seek operation, it flushes any pending data.</span></span> <span data-ttu-id="41f28-110">Le résultat est de réduire la latence des commandes de recherche, car les données existantes sont vidées du graphique.</span><span class="sxs-lookup"><span data-stu-id="41f28-110">The result is to minimize the latency of seek commands, because existing data is flushed from the graph.</span></span> <span data-ttu-id="41f28-111">Après une commande Seek, le temps de flux se réinitialise à zéro.</span><span class="sxs-lookup"><span data-stu-id="41f28-111">After a seek command, stream time resets to zero.</span></span>

<span data-ttu-id="41f28-112">Le diagramme suivant illustre la séquence d’événements.</span><span class="sxs-lookup"><span data-stu-id="41f28-112">The following diagram illustrates the sequence of events.</span></span>

![séquence d’événements](images/seeking.png)

<span data-ttu-id="41f28-114">Si un filtre de l’analyseur a plusieurs broches de sortie, il les désigne généralement pour accepter les commandes Seek.</span><span class="sxs-lookup"><span data-stu-id="41f28-114">If a parser filter has more than one output pin, it typically designates one of them to accept seek commands.</span></span> <span data-ttu-id="41f28-115">Les autres codes confidentiels rejettent ou ignorent les commandes de recherche qu’ils reçoivent.</span><span class="sxs-lookup"><span data-stu-id="41f28-115">The other pins reject or ignore any seek commands they receive.</span></span> <span data-ttu-id="41f28-116">De cette façon, l’analyseur conserve tous ses flux synchronisés.</span><span class="sxs-lookup"><span data-stu-id="41f28-116">In this way, the parser keeps all of its streams synchronized.</span></span> <span data-ttu-id="41f28-117">Toutefois, toutes les broches de sortie doivent implémenter [**IMediaSeeking :: GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) et [**IMediaSeeking :: CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) pour retourner les fonctionnalités de recherche du filtre.</span><span class="sxs-lookup"><span data-stu-id="41f28-117">However, all output pins should implement [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) and [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) to return the filter's seeking capabilities.</span></span> <span data-ttu-id="41f28-118">Cela permet de s’assurer que le gestionnaire de graphes de filtres retourne la valeur correcte à l’application.</span><span class="sxs-lookup"><span data-stu-id="41f28-118">This ensures that the Filter Graph Manager returns the correct value to the application.</span></span>

<span data-ttu-id="41f28-119">L’interface [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) est dépréciée pour les filtres.</span><span class="sxs-lookup"><span data-stu-id="41f28-119">The [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) interface has been deprecated for filters.</span></span> <span data-ttu-id="41f28-120">Les clients Automation doivent toujours utiliser cette interface sur le gestionnaire de graphique de filtre, car **IMediaSeeking** n’est pas compatible avec Automation, mais le gestionnaire de graphique de filtre traduit tous les appels **IMediaPosition** en appels **IMediaSeeking** .</span><span class="sxs-lookup"><span data-stu-id="41f28-120">Automation clients still need to use this interface on the Filter Graph Manager, because **IMediaSeeking** is not Automation-compatible, but the Filter Graph Manager translates all **IMediaPosition** calls into **IMediaSeeking** calls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="41f28-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="41f28-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41f28-122">Vidage</span><span class="sxs-lookup"><span data-stu-id="41f28-122">Flushing</span></span>](flushing.md)
</dt> <dt>

[<span data-ttu-id="41f28-123">Temps et horloges dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="41f28-123">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



