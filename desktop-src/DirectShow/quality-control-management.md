---
description: Gestion des Quality-Control
ms.assetid: b1def588-6c9c-4853-a69b-1ba5df8b5ba2
title: Gestion des Quality-Control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c68aff4f8c054f9f649801e1b9829ccd7daaff35
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106516330"
---
# <a name="quality-control-management"></a><span data-ttu-id="f7cd2-103">Gestion des Quality-Control</span><span class="sxs-lookup"><span data-stu-id="f7cd2-103">Quality-Control Management</span></span>

<span data-ttu-id="f7cd2-104">Le contrôle de la qualité est un mécanisme permettant d’ajuster le taux de transmission de données via le graphique de filtre en réponse aux performances d’exécution.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-104">Quality control is a mechanism for adjusting the rate of data flow through the filter graph in response to run-time performance.</span></span> <span data-ttu-id="f7cd2-105">Si un filtre de convertisseur reçoit trop de données ou trop peu de données, il peut envoyer un *message de qualité*.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-105">If a renderer filter is receiving too much data or too little data, it can send a *quality message*.</span></span> <span data-ttu-id="f7cd2-106">Le message de qualité demande un ajustement dans le débit des données.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-106">The quality message requests an adjustment in the data rate.</span></span> <span data-ttu-id="f7cd2-107">Par défaut, les messages de qualité voyagent en amont du convertisseur jusqu’à ce qu’ils atteignent un filtre qui peut répondre (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="f7cd2-107">By default, quality messages travel upstream from the renderer until they reach a filter that can respond (if any).</span></span> <span data-ttu-id="f7cd2-108">Une application peut également implémenter un gestionnaire de qualité personnalisé.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-108">An application can also implement a custom quality manager.</span></span> <span data-ttu-id="f7cd2-109">Dans ce cas, le convertisseur transmet les messages de qualité directement au gestionnaire de qualité de l’application.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-109">In that case, the renderer passes quality messages directly to the application's quality manager.</span></span>

<span data-ttu-id="f7cd2-110">Cet article contient les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-110">This article contains the following topics.</span></span>

-   [<span data-ttu-id="f7cd2-111">Messages de qualité</span><span class="sxs-lookup"><span data-stu-id="f7cd2-111">Quality Messages</span></span>](quality-messages.md)
-   [<span data-ttu-id="f7cd2-112">Contrôle qualité par défaut</span><span class="sxs-lookup"><span data-stu-id="f7cd2-112">Default Quality Control</span></span>](default-quality-control.md)

## <a name="related-topics"></a><span data-ttu-id="f7cd2-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f7cd2-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7cd2-114">Transmission de données pour les développeurs de filtres</span><span class="sxs-lookup"><span data-stu-id="f7cd2-114">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
</dt> <dt>

[<span data-ttu-id="f7cd2-115">Écriture de filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="f7cd2-115">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



